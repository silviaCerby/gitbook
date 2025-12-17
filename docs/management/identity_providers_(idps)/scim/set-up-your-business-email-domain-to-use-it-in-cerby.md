---
description: This article describes how to grant access to Cerby to use your business email domain via an Amazon SES integration.
intercom_id: 5855181
---

# Set up your business email domain to use it in Cerby

Cerby can use your business email domain to create and manage the email accounts your employees need for authentication and security purposes. To enable this feature for your Cerby workspace, you must set up an Amazon Simple Email Service (SES) integration.

This article describes how to set up the Amazon SES integration and your Cerby workspace to enable your users to create Cerby-managed email addresses for their accounts with your business email domain.

* * *

## Supported features

The following are the supported features of setting up your business email domain to use it in Cerby:

  * **Email account creation:** Cerby enables users to create a Cerby-managed email address for an account already saved in their workspace
  * **Message management in Cerby:** All messages sent to the Cerby-managed email address are centralized in the [Shared Inbox](https://cerby-test.gitbook.io/cerby-test/getting-started/glossary). These messages can be forwarded to workspace members, and Cerby can access them for authentication purposes, such as retrieving verification codes
* * *

## Requirements

The following are the requirements to set up your business email domain to use it in Cerby:

  * A Cerby workspace
  * A Cerby user account with the workspace **Owner** role
  * An AWS account and access to a business email domain registered in the Domain Name System (DNS), or an already implemented Amazon SES integration
  * Permission for accessing AWS CloudShell and adding Identity and Access Management (IAM) roles in AWS.

  **NOTE:** Cerby recommends using AWS CloudShell because it contains the tools and libraries needed to configure Amazon SES.

{% hint style="danger" %}


**IMPORTANT:** Currently, the available AWS regions for configuring emails with Cerby are `us-east-1`, `us-west-2`, and `eu-east-1`.


{% endhint %}

* * *

## Set up your business email domain to use it in Cerby

To set up your business email domain to use it in Cerby, you must complete the following main steps:

{% hint style="danger" %}


**IMPORTANT:** Consider the following before completing the main steps:

  * If you already have an Amazon SES integration implemented, meaning you can send and receive emails through your existing configuration, you must complete only steps 2 and 3.
  * If and only if you have an AWS account and access to a business email domain, which might be managed by Amazon Route 53, you must complete all three steps.


{% endhint %}
  1. [Configure Amazon SES to send and receive emails](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-1.-configure-amazon-ses-to-send-and-receive-emails)
  2. [Grant access to Cerby to your Amazon SES integration](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-2.-grant-access-to-cerby-to-your-amazon-ses-integration)
  3. [Configure your Cerby workspace to use your business email domain](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-3.-configure-your-cerby-workspace-to-use-your-business-email-domain)
  4. [Set up a custom bounce domain (optional)](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-4.-set-up-a-custom-bounce-domain-(optional))

The following sections describe each main step.

### 1\. Configure Amazon SES to send and receive emails

To configure Amazon SES to send and receive emails, complete the following steps:

  1. Log in to the [AWS Console](https://console.aws.amazon.com/console/home?nc2=h_ct&src=header-signin).
  2. Open an AWS CloudShell terminal.

  **IMPORTANT:** AWS CloudShell is not supported in all of AWS regions. For a list of the supported regions and associated service endpoints, see [AWS CloudShell endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/cloudshell.html).

  3. Run the following command to clone the repository:

         $ git clone https://github.com/cerbyinc/cerby-aws-ses-integration.git

  4. Navigate to the `cerby-aws-ses-integration` cloned directory.
  5. Run the following command to execute the Cerby AWS SES Configuration tool:

         $ python3 main.py <your_business_email_domain>

**IMPORTANT:** Make sure you replace the `<your_business_email_domain>` value with your business email domain.

One of the following two scenarios occurs:

     * If your domain is managed by Amazon Route 53, the Cerby AWS SES Configuration tool attempts to add DNS records to this service.
     * If your domain is not managed by Amazon Route 53, the tool displays the DNS records you need to configure your DNS server manually. For more information, read the [Troubleshooting: Configure your DNS server manually when not using Amazon Route 53](https://docs.google.com/document/d/1Iz6iKFgZkZLbNWRGfqcDL4CWp_hvhf0u9a3Pr8wpSww/edit?tab=t.0#heading=h.ooqafun1cun5) section.

  6. Verify that the configuration for Amazon SES is successful by completing the following steps:
     1. Access the Amazon SES dashboard.
     2. Click the **Identities** button from the **Configuration** list in the left navigation drawer. The **Identities** page is displayed.
     3. Click the domain identity that you have previously set up as part of the Cerby AWS SES Configuration tool execution; its name is your business email domain. The identity details page is displayed.
     4. Scroll down to the **Custom MAIL FROM domain** section. A “Successful” status must be displayed.

     **IMPORTANT:** AWS may take several minutes to up to 48 hours to verify your domain and the DKIM configuration.

  7. Request AWS for production access to Amazon SES by following the instructions from the [Moving out of the Amazon SES sandbox](https://docs.aws.amazon.com/ses/latest/dg/request-production-access.html) article.

  **IMPORTANT:** Amazon SES is configured by default in the sandbox. If you omit to request production access, you will not be able to send emails to any recipient.

Now you can send and receive emails via Amazon SES with your business email domain. The next step is [2. Grant access to Cerby to your Amazon SES integration](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-2.-grant-access-to-cerby-to-your-amazon-ses-integration).

### 2\. Grant access to Cerby to your Amazon SES integration

To grant access to Cerby to use your Amazon SES integration on your behalf, you have two options:

  * [CloudFormation template](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-cloudformation-template)
  * [Manual configuration](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-manual-configuration)

The following subsections describe the steps of each option.

#### CloudFormation template

To leverage a CloudFormation template for granting access to Cerby to use your Amazon SES integration, complete the following steps:

  1. Log in to the [AWS Console](https://console.aws.amazon.com/console/home?nc2=h_ct&src=header-signin).
  2. Access the following URL in the address bar of your browser:

         https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/quickcreate?stackName=cerby-aws-ses-integration&templateURL=https://cerby-public-assets.s3.us-east-2.amazonaws.com/cerby-aws-ses.yaml&param_RoleName=cerby-aws-ses-integration-role&param_EmailAddress=change@me.com&param_ExternalId=changeme

The **Quick create stack** page is displayed with values prefilled.

  3. Enter the corresponding values in the following fields:

     * **EmailAddress:** This email address is used by Cerby to forward messages. For example, **[hello@cer.dev](mailto:hello@cer.dev)**.
     * **ExternalId:** This ID is used along with the role. For example, **CerbyID**.

     **IMPORTANT:** Make sure to enter the external ID without spaces.

**NOTE:** You can modify the values of the **Stack name** and **RoleName** fields to the stack name and role name of your choice, respectively.

  4. Select the “I acknowledge that AWS CloudFormation might create IAM resources” option in the **Capabilities** section located at the bottom of the page.
  5. Click the **Create stack** button. A page with the details of the new stack is displayed.

Now you have granted access to Cerby to use your Amazon SES integration. The next step is [3. Configure your Cerby workspace to use your business email domain](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-3.-configure-your-cerby-workspace-to-use-your-business-email-domain).

#### Manual configuration

To manually configure granting access to Cerby to use your Amazon SES integration, complete the following steps:

  1. [Create a policy](set-up-your-business-email-domain-to-use-it-in-cerby.md#h_b2258b2beb)
  2. [Create a role](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-2.-create-a-role)
  3. [Edit the trust relationship](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-3.-edit-the-trust-relationship)

The following subsections describe each main step.

##### 1\. Create a policy

To create a policy for the new role, complete the following steps:

  1. Log in to the [AWS Console](https://console.aws.amazon.com/console/home?nc2=h_ct&src=header-signin).
  2. Access the IAM dashboard.
  3. Click the **Policies** option from the **Access management** list in the left navigation drawer. The **Policies** page is displayed.
  4. Click the **Create policy** button located at the top right of the page. A wizard is displayed with the **Specify permissions** page.
  5. Activate the **JSON** tab in the **Policy editor** section to display a code block.
  6. Enter the following information in the code block:

         {
             "Version": "2012-10-17",
             "Statement": [
                 {
                     "Action": [
                         "ses:CreateReceiptRule",
                         "ses:CreateReceiptRuleSet",
                         "ses:DeleteReceiptRule",
                         "ses:DeleteReceiptRuleSet",
                         "ses:DescribeReceiptRule",
                         "ses:DescribeReceiptRuleSet"
                     ],
                     "Resource": "*",
                     "Effect": "Allow"
                 },
                 {
                     "Sid": "VisualEditor0",
                     "Effect": "Allow",
                     "Action": "ses:SendEmail",
                     "Resource": "*",
                     "Condition": {
                         "StringEquals": {
                             "ses:FromAddress": "<your_email_address>"
                         }
                     }
                 }
             ]
         }

**IMPORTANT:** Enter the email address you want Cerby to use to forward messages as the `<your_email_address>` value. For example, **[hello@cer.dev](mailto:hello@cer.dev)**.

  7. Click the **Next** button. The **Review and create** page of the wizard is displayed.
  8. Enter a policy name in the **Policy name** field. For example, **CerbyPolicy**.

  **NOTE:** Adding a policy description and tags is optional, so you can continue to the next step.

  9. Click the **Create policy** button. The **Policies** page is displayed with a successful message.

The next step is [2. Create a role](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-2.-create-a-role), which you must complete from the IAM dashboard.

##### 2\. Create a role

To create a role, complete the following steps from the IAM dashboard:

  1. Click the **Roles** option from the **Access management** list in the left navigation drawer. The **Roles** page is displayed.
  2. Click the **Create role** button located at the top right of the page. A wizard is displayed with the**Select trusted entity** page.
  3. Select the **AWS account** option in the **Select trusted entity** section. The **An AWS account** section is displayed below.
  4. Enter and select the following details to specify the Cerby account in AWS that can use this role:
     1. Select the **Another AWS account** option in the **An AWS account** section.
     2. Enter **749452252575** in the **Account ID** field.
     3. Select the “Require external ID (Best practice when a third party will assume this role)” option.
     4. Enter an identifier in the **External ID** field. For example, **CerbyID**.

     **IMPORTANT:** Make sure to enter the external ID without spaces.

  5. Click the **Next** button located at the bottom right of the page. The **Add permissions** page of the wizard is displayed.
  6. Search for the policy that you have created previously by using the search bar in the **Permissions policies** section. For example, enter **CerbyPolicy.**
  7. Select the policy.
  8. Click the **Next** button. The **Name, review, and create** page of the wizard is displayed.
  9. Enter a role name in the **Role name** field. For example, **cerby-aws-ses-integration**.

  **NOTE:** Adding a role description and tags is optional, so you can continue to the next step.

  10. Click the **Create role** button. The wizard closes, and the new role and a success message are displayed.

The next step is [3. Edit the trust relationship](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-3.-edit-the-trust-relationship), which you must complete from the IAM dashboard.

##### 3\. Edit the trust relationship

To edit the trust relationship of the new role, complete the following steps from the IAM dashboard.

  1. Click the new role from the **Roles** section; in this case, its name is **cerby-aws-ses-integration**. The role details page is displayed.
  2. Activate the **Trust relationships** tab.
  3. Click the **Edit trust relationship** button in the **Trusted entities** section. The **Edit Trust policy** page is displayed with a code block.
  4. Edit the policy document so it looks like the following code block:

         {
           "Version": "2012-10-17",
           "Statement": [
             {
               "Effect": "Allow",
               "Principal": {
                 "AWS": "arn:aws:iam::749452252575:role/customer-assumable-roles"
               },
               "Action": "sts:AssumeRole",
               "Condition": {
                 "StringEquals": {
                   "sts:ExternalId": "<external_ID>"
                 }
               }
             }
           ]
         }

**NOTE:** The `<external ID>` value is prefilled with the external ID you previously assigned. In this case, **CerbyID**.

  5. Click the **Update policy** button. The page closes, and the role details page and a success message are displayed.

{% hint style="success" %}


**TIP:** Keep the role details page open. You need the Amazon Resource Name (ARN) of the role to configure the workspace email in Cerby.


{% endhint %}

Now you have granted access to Cerby to use your Amazon SES integration. The next step is [3. Configure your Cerby workspace to use your business email domain](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-3.-configure-your-cerby-workspace-to-use-your-business-email-domain).

### 3\. Configure your Cerby workspace to use your business email domain

To configure your Cerby workspace to use your business email domain, complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed with the **General** tab activated.
  3. Click the **Configure Email** button in the **Workspace Email Configuration** section. The **Configure workspace email** dialog box is displayed.
  4. Enter and select the following details to configure the workspace email:

     * Select the corresponding AWS region option from the **Region** drop-down list.

     **NOTE:** Currently, the available options for receiving emails are **us-east-1** , **us-west-2** , and **eu-east-1**.

     * Enter your AWS Account ID in the **Account ID** field. For example, **123456789123**.
     * Enter the external ID you assigned for the role in the **External ID** field. In this case, **CerbyID**.
     * Enter the ARN of the role in the **Role’s ARN** field.

     **TIP:** Copy the ARN of the role from the role details page that you left open.

     * Enter the email address in the **Email Address** field. In this case, **[hello@cer.dev](mailto:hello@cer.dev)**.

     **IMPORTANT:** The email address must be the same you assigned when granting access to Cerby to your Amazon SES integration.

     * Enter the business email domain in the **Domain** field. Cerby uses this domain to generate email addresses.

  5. Click the **Save** button. The dialog box closes, and a success message box is displayed.

Now you are done. Now you are done. You can optionally complete step [4. Set up a custom bounce domain](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-4.-set-up-a-custom-bounce-domain-(optional)).

### 4\. Set up a custom bounce domain (optional)

After setting up your business email domain to use in Cerby, you can optionally set up a custom bounce domain for undeliverable email messages. By default, Amazon SES handles bounce messages internally; however, you can improve your organization’s email deliverability score by having a custom bounce domain.

With a good score, you can avoid emails being marked as spam or blocked by email providers. Additionally, a custom bounce domain enables you to track and analyze bounce data more effectively.

To set up a custom bounce domain, you must complete the following steps:

  1. Log in to the [AWS Console](https://console.aws.amazon.com/console/home?nc2=h_ct&src=header-signin).
  2. Navigate to the Amazon SES dashboard.
  3. Click the **Identities** button from the **Configuration** list in the left navigation drawer. The **Identities** page is displayed.
  4. Click the domain identity that you have previously set up for Cerby. The identity details page is displayed.
  5. Click the **Edit** button in the **Custom MAIL FROM domain** section of the **Authentication** tab. The **Edit custom MAIL FROM domain** page is displayed.
  6. Enter and select the following options in the **General details** section:

     * Select the **Use a custom MAIL FROM domain** option
     * Enter your bounce domain in the **MAIL FROM domain** field. For example, **bounce**.
     * Select in the **Behavior on MX failure** section the action Amazon SES should take if the MX record is not set up correctly. The options are the following:
       * **Use default MAIL FROM domain**
       * **Reject message**

  7. Click the **Save changes** button. The page closes.
  8. Publish the MX and TXT records on Amazon Route 53 or in your domain provider. For instructions, read the official documentation [Publishing an MX record for Amazon SES email receiving](https://docs.aws.amazon.com/ses/latest/dg/receiving-email-mx-record.html) or the referred documentation for each DNS service provider in the [Troubleshooting: Configure your DNS server manually when not using Amazon Route 53](https://docs.google.com/document/d/1Iz6iKFgZkZLbNWRGfqcDL4CWp_hvhf0u9a3Pr8wpSww/edit?tab=t.0#heading=h.ooqafun1cun5) section.
A “Successful” status must be displayed in the **Custom MAIL FROM domain** section of the **Authentication** tab.

  9. Verify that the setup is correct by sending a test email message to a nonexistent email within your domain.

Now you are done.

* * *

## Troubleshooting: Configure your DNS server manually when not using Amazon Route 53

When you configure Amazon SES to send and receive emails with your business email domain in Cerby, but you don’t use Amazon Route 53 as your DNS service provider, you must configure your DNS server manually.

The Cerby AWS SES Configuration tool provides you with the corresponding DNS records you need, as described in step [1. Configure Amazon SES to send and receive emails](set-up-your-business-email-domain-to-use-it-in-cerby.md#id-1.-configure-amazon-ses-to-send-and-receive-emails).

The records and rules you must configure are the following:

  1. NS records
     1. Configure the nameserver (NS) records for your domain and subdomain in your DNS domain registrar.
  2. MX record
     1. Configure the MX record of your domain or subdomain in your DNS domain registrar to point to the inbound SMTP domain of AWS. For example, if you use the **us-west-2** region, the inbound SMTP domain must be **`inbound-smtp.us-west-2.amazonaws.com`**. Reference the [Amazon Simple Email Service endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/ses.html) article to identify the `Email Receiving Endpoint` for the region you used for the deployment.
For more information on how to configure an MX record, read the official documentation from your DNS service provider, such as the following:

        * [Add an MX record](https://www.godaddy.com/help/add-an-mx-record-19234), for GoDaddy
        * [How do I change my MX records?](https://help.dreamhost.com/hc/en-us/articles/215035328), for DreamHost
        * [Set up email records](https://developers.cloudflare.com/dns/manage-dns-records/how-to/email-records/), for Cloudflare
        * [Changing MX records - Windows](https://support.hostgator.com/articles/hosting-guide/lets-get-started/dns-name-servers/changing-mx-records-windows), for HostGator
        * [How can I set up MX records required for mail service?](https://www.namecheap.com/support/knowledgebase/article.aspx/322/2237/how-can-i-set-up-mx-records-required-for-mail-service), for Namecheap
        * [Changing your domain's DNS settings](https://www.names.co.uk/support/domains/1156-changing_your_domains_dns_settings.html), for Names.co.uk
        * [Adding or Updating MX Records in Your Wix Account](https://support.wix.com/en/article/adding-or-updating-mx-records-in-your-wix-account), for Wix

  3. DKIM records
     1. Configure the DKIM records for your domain and subdomain in your DNS domain registrar.
For more information on how to configure a DKIM record, read the official documentation from your DNS service provider, such as the following:

        * [Add a CNAME record](https://www.godaddy.com/help/add-a-cname-record-19236), for GoDaddy
        * [How do I add custom DNS records?](https://help.dreamhost.com/hc/en-us/articles/215414867-How-do-I-add-custom-DNS-records-), for DreamHost
        * [Managing DNS records in Cloudflare](https://support.cloudflare.com/hc/en-us/articles/360019093151), for Cloudflare
        * [Manage DNS Records with HostGator/eNom](https://support.hostgator.com/articles/hosting-guide/lets-get-started/dns-name-servers/manage-dns-records-with-hostgatorenom), for HostGator
        * [How do I add TXT/SPF/DKIM/DMARC records for my domain?](https://www.namecheap.com/support/knowledgebase/article.aspx/317/2237/how-do-i-add-txtspfdkimdmarc-records-for-my-domain), for Namecheap
        * [Changing your domains DNS Settings](https://www.names.co.uk/support/1156-changing_your_domains_dns_settings.html), for Names.co.uk
        * [Adding or Updating CNAME Records in Your Wix Account](https://support.wix.com/en/article/adding-or-updating-cname-records-in-your-wix-account), for Wix

     2. Create a domain identity in Amazon SES with the following configuration:

        * **Easy DKIM** as the identity type
        * **RSA_2048_BIT** as the DKIM signing key length
        * **DKIM signatures** enabled

     3. Verify the DKIM domain identity with your DNS provider.

For more information on how to create and verify a domain identity, read the [Creating and verifying identities in Amazon SES](https://docs.aws.amazon.com/ses/latest/dg/creating-identities.html) official documentation from AWS.

  4. Email receipt rule
     1. Configure the **`PROXY-MAIL`** rule in the AWS SES dashboard with an action to deliver the received emails to the **`cerby-store-ses-email-production`** Amazon S3 bucket.

For more information on how to configure an email receipt rule, read the [Creating receipt rules console walkthrough](https://docs.aws.amazon.com/ses/latest/dg/receiving-email-receipt-rules-console-walkthrough.html) official documentation from AWS.

Now you are done.

* * *

## Troubleshooting: I have already created Cerby-managed email addresses

When you have already created email addresses with a default domain provided by Cerby but want to start using your business domain, you must remove all of the existing email addresses from your accounts before the setup.

Cerby doesn’t support using email addresses with different domains simultaneously. If this scenario occurs, messages sent to the existing email addresses will not be routed to your workspace.

If you need assistance in identifying the accounts with Cerby-managed email addresses contact the Customer Support team by sending an email to [support@cerby.com](mailto:support@cerby.com) or a message through the help chat of the Cerby dashboard.
