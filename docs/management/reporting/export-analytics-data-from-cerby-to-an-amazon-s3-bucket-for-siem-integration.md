---
description: This article describes how to set up analytics data export from Cerby to an Amazon S3 bucket for SIEM integration.
intercom_id: 11713898
---

# Export analytics data from Cerby to an Amazon S3 bucket for SIEM integration

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super Admins** , and **Admins**
* This is a beta feature currently available to a limited number of workspaces


{% endhint %}

With Cerby, you can export the analytics data of your workspace to a security information and event management (SIEM) solution via an integration. This is a feature that customers can request to be enabled by our Support team.

The integration leverages an Amazon S3 bucket, where Cerby exports the logs of analytic events in JSON files every minute as long as Cerby has registered events. This S3 bucket serves as the data source for the integration you set up with your preferred SIEM platform.

When your SIEM solution is configured to ingest data from the bucket, it can continuously consume and process these logs as part of the organization’s broader security monitoring strategy. By integrating Cerby’s analytics data into your SIEM, you can enhance visibility into user behavior and access activity, helping to enforce security policies, detect anomalies, and respond more effectively to potential threats.

This article describes the instructions to set up the analytics data export for your SIEM solution.

* * *

## Requirements

The following are the requirements to configure the integration to export analytics data from Cerby via an Amazon S3 bucket:

  * A Cerby account in AWS.
  * A Cerby role in AWS.

{% hint style="danger" %}


**IMPORTANT:** Contact our Support team via email at [support@cerby.com](mailto:support@cerby.com) or through the help chat in the Cerby web app dashboard to request these values


{% endhint %}

* * *

## Set up the analytics data export to a SIEM integration via an Amazon S3 bucket

To set up the analytics data export to a SIEM integration via an Amazon S3 bucket, you must complete the following main steps:

  1. [Create and configure an Amazon S3 bucket](export-analytics-data-from-cerby-to-an-amazon-s3-bucket-for-siem-integration.md#id-1.-create-and-configure-an-amazon-s3-bucket)
  2. [Configure your SIEM solution to ingest data from the S3 bucket](export-analytics-data-from-cerby-to-an-amazon-s3-bucket-for-siem-integration.md#id-2.-configure-your-siem-solution-to-ingest-data-from-the-amazon-s3-bucket)

The following sections describe each main step.

### 1\. Create and configure an Amazon S3 bucket

To create and configure an Amazon S3 bucket, you must complete the following steps:

  1. Create an Amazon S3 bucket for storing objects by following the instructions in the [Create your first S3 bucket](https://docs.aws.amazon.com/AmazonS3/latest/userguide/GetStartedWithS3.html#creating-bucket) official documentation.
  **NOTE:** Make sure to select the **ACLs disabled** and **Block all public access** options when creating your bucket.

  2. Add a bucket policy to grant Cerby writing permissions on the bucket by following the instructions in the [Adding a bucket policy by using the Amazon S3 console](https://docs.aws.amazon.com/AmazonS3/latest/userguide/add-bucket-policy.html) official documentation. Use the following policy:
​

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

**IMPORTANT:** Make sure you add the name of your bucket in the **`Resource`** parameters and replace **`cerby_account`** and**`cerby_role`** with the values provided by our Support team.

  3. Share the **bucket name** and its **path** with our Support team.

The next step is 2. Configure your SIEM solution to ingest data from the S3 bucket
​

### 2\. Configure your SIEM solution to ingest data from the Amazon S3 bucket

To start consuming Cerby analytics data, you must configure your SIEM solution to ingest logs directly from the Amazon S3 bucket. While the exact steps vary depending on the tool, most SIEM solutions offer support for reading from S3, so refer to the official documentation for instructions.

Typically, you must complete the following steps:

  1. Create a data collector or source in your SIEM solution.
  2. Set up access for your SIEM solution to the S3 bucket. Typically, you must provide the following information:

     * S3 bucket name and region
     * Credentials for the SIEM to access the S3 bucket, such as IAM role or access keys

  3. Configure additional settings required by your SIEM solution, such as the following:

     * Path filters
     * Data format
     * Polling interval
     * Timestamp parsing
* * *

## Appendix: Analytic events format

The following is an example of a JSON object with the analytic events that Cerby sends to the S3 bucket:

    {
        "timestamp":1708567151605,
        "eventName":"LOGIN_TO_ACCOUNT_ATTEMPT",
        "accountName":"Vaulted account",
        "accountProvider":"unmanaged",
        "scimExternalId":"01abcdefghijKLmNO2x3",
        "city":"Columbus",
        "region":"Ohio",
        "country":"United States",
        "ip":"189.000.000.000",
        "deviceName":"iPhone",
        "workspace":"cerby",
        "userId":"012345a6-7b89-012c-d345-6ef78dc90d12",
        "userEmail":"user@email.com",
        "messageId":"012A3456-78B9-01C2-3DEF-GHIJ45678K9L"
    }

The following table provides a description of each field included in the JSON object:

**Field**| **Description**
---|---
**`timestamp`**|  Unix timestamp representing when the event occurred
**`eventName`**|  Name of the event that was triggered
**`accountName`**|  Name of the account related to the event
**`accountProvider`**|  Provider of the account related to the event
**`scimExternalId`**|  External SCIM identifier associated with the user
**`city`**|  City from which the event originated
**`region`**|  State or region from which the event originated
**`country`**|  Country from which the event originated
**`ip`**|  IP address from which the event originated
**`deviceName`**|  Type of device used. For example, Mac, PC, and smartphone
**`workspace`**|  Name of the customer workspace where the event occurred
**`userId`**|  Identifier of the user who triggered the event
**`userEmail`**|  Email of the user who triggered the event
**`messageId`**|  Unique identifier for the message

**Table 1**. Descriptions of the fields included in each JSON object
