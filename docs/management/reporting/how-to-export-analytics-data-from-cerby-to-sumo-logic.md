---
description: This article describes how to configure the integration to export analytics data from Cerby to Sumo Logic.
intercom_id: 7956602
---

# How to export analytics data from Cerby to Sumo Logic

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , and **Admins**
* This is a beta feature currently available to a limited number of workspaces


{% endhint %}

With Cerby, you can export the analytics data of your workspace to a security information and event management (SIEM) solution like Sumo Logic via an integration. This is a feature that customers can request from the Cerby Customer Support team.

The integration leverages an Amazon S3 bucket, where Cerby exports the logs of analytic events in JSON files every minute as long as Cerby has registered events. The bucket is the data source for Sumo Logic via a hosted collector.

This article describes the instructions to configure the analytics data export to Sumo Logic.

* * *

## Configure the analytics data export to Sumo Logic

To configure the export of the analytics data that Cerby registers and stores for a workspace, you must complete the following main steps:

  1. [Create and configure an Amazon S3 bucket](how-to-export-analytics-data-from-cerby-to-sumo-logic.md#id-1.-create-and-configure-an-amazon-s3-bucket)
  2. [Add and configure a hosted collector in Sumo Logic](how-to-export-analytics-data-from-cerby-to-sumo-logic.md#id-2.-add-and-configure-a-hosted-collector-in-sumo-logic)

The following sections describe each main step.

* * *

### 1\. Create and configure an Amazon S3 bucket

To create and configure an Amazon S3 bucket, complete the following steps:

  1. Create an Amazon S3 bucket for storing objects by following the instructions in the [Create your first S3 bucket](https://docs.aws.amazon.com/AmazonS3/latest/userguide/creating-bucket.html) official documentation.

  **NOTE:** Make sure to select the **ACLs disabled** and **Block all public access** options when creating your bucket.

  2. Add a bucket policy to grant Cerby writing permissions on the bucket by following the instructions in the [Adding a bucket policy by using the Amazon S3 console](https://docs.aws.amazon.com/AmazonS3/latest/userguide/add-bucket-policy.html) official documentation. Use the following policy:

         {
             "Version": "2012-10-17",
             "Statement": [
                 {
                     "Sid": "Statement1",
                     "Effect": "Allow",
                     "Principal": {
                         "AWS": "arn:aws:iam::<cerby_account>:role/<cerby_role>"
                     },
                     "Action": [
                         "s3:GetObject",
                         "s3:GetObjectVersion",
                         "s3:PutObject",
                         "s3:DeleteObject"
                     ],
                     "Resource": "arn:aws:s3:::<your-bucket-name>/*"
                 },
                 {
                     "Sid": "Statement2",
                     "Effect": "Allow",
                     "Principal": {
                         "AWS": "arn:aws:iam::<cerby_account>:role/<cerby_role>"
                     },
                     "Action": [
                         "s3:ListBucket",
                         "s3:ListBucketVersions",
                         "s3:GetBucketLocation"
                     ],
                     "Resource": "arn:aws:s3:::<your-bucket-name>"
                 }
             ]
         }

**IMPORTANT:**

     * Contact the Cerby Customer Support team to ask for the `cerby_account` and `cerby_role` values. Ensure you add the name of your bucket in the `Resource` parameters.
     * The Cerby Customer Support team will share the values through a Cerby secure secret. Refer to the article [View a secret](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/secrets/view-a-secret) to learn how to view the values.

  3. Share the bucket name and its path with the Cerby Customer Support team.

The next step is [2. Add and configure a hosted collector in Sumo Logic](how-to-export-analytics-data-from-cerby-to-sumo-logic.md#id-2.-add-and-configure-a-hosted-collector-in-sumo-logic).

* * *

### 2\. Add and configure a hosted collector in Sumo Logic

To add and configure a hosted collector in Sumo Logic, complete the following steps:

  1. Add a hosted collector in Sumo Logic by following the instructions in the [Configure a Hosted Collector and Source](https://help.sumologic.com/docs/send-data/hosted-collectors/configure-hosted-collector/) official documentation.
  2. Configure the Amazon S3 bucket as a reading source for the hosted collector by following the instructions in the [Grant Access to an AWS Product](https://help.sumologic.com/docs/send-data/hosted-collectors/amazon-aws/grant-access-aws-product/) official documentation.

Now you’re done with the configuration.
