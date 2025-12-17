---
description: This article describes how to set up an AWS KMS integration to create vaults using the keys of your existing environment.
intercom_id: 10085037
---

# Set up an AWS KMS vault integration

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Admins** , **Super** **Admins** , and **Owners**
* If you are interested in this feature but don't see it available in your workspace, email our Sales team at [sales@cerby.com](mailto:sales@cerby.com).


{% endhint %}

With Cerby, you can use the encryption keys within your AWS Key Management Service (KMS) environment for data encryption and decryption, ensuring you maintain full ownership and control over your keys.

Cerby already uses AWS KMS for vault key encryption; however, you can leverage your existing environment for your workspace. Users with the workspace **Admin** , **Super Admin** , or **Owner** role can configure a custom AWS KMS vault integration, manage your vaults, and set a default vault for accounts and secrets. Additionally, as an owner of the AWS KMS environment, you can log the creation, access, and management of your keys and encrypted credentials in your AWS account.

In Cerby’s standard cloud setup, encryption keys are stored and managed by Cerby. For data protection, Cerby implements Zero Knowledge architecture principles and rigorous security protocols. For more information, read the article [How Cerby protects your data with cloud and local encryption](https://cerby-test.gitbook.io/cerby-test/management/credential-management/vaults/how-cerby-protects-your-data-with-cloud-and-local-encryption).

{% hint style="danger" %}


**IMPORTANT:** Consider the following about the AWS KMS vault integration:

* You must _not_ delete or disable your AWS KMS key after the integration; otherwise, you will permanently lose access to all data encrypted with the key unless you have manually backed up the secret and account data beforehand. Cerby does not automatically detect deleted or disabled keys, as this action is outside our control.
* You must _not_ edit the AWS KMS key after the integration; otherwise, you will permanently lose access to all data encrypted with the key unless you have manually backed up the secret and account data beforehand. Editing an AWS KMS key is complex due to encryption dependencies, and it is not supported within Cerby, as changes to the key prevent data decryption.


{% endhint %}

The following is the main process for integrating your AWS KMS environment with Cerby:

1. Create an AWS KMS key in your AWS account.
2. Add an Identity and Access Management (IAM) role with the required policies to enable Cerby to access your AWS KMS key for data encryption and decryption. This cross-account access is a feature supported by AWS, enabling secure sharing of resources with external accounts.
3. Cerby configures the corresponding policies to use your AWS KMS key without having direct access to your data or control over the key.

The following sections detail how to set up your AWS KMS vault integration.

* * *

## Requirements

The following are the requirements to set up an AWS KMS vault integration:

  * A Cerby workspace.
  * A Cerby account with the workspace **Admin** , **Super Admin** , or **Owner** role.
  * The browser you'll use for the AWS KMS vault integration must be a trusted device in Cerby. For more information, read the article [Set up trusted sessions on your devices](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/trusted-devices/set-up-trusted-sessions-on-your-devices).
  * Your Cerby workspace ID. You can find it by completing the following steps:

    1. Log in to your Cerby [workspace](https://app.cerby.com/) using the Cerby web app.
    2. Select the **Settings** option from the left navigation drawer. The **Workspace** **Configuration** page is displayed with the **General** tab activated.
    3. Copy the Cerby workspace ID from the **Workspace ID** field and save it in a safe location.

  * An AWS account with Administrator permissions to create and manage KMS.
  * Your AWS account ID. You can find it by completing the following steps:

    1. Log in to the [AWS console](https://aws.amazon.com/console/) on your web browser.
    2. Click your account name information located at the top right of the page.
    3. Locate the **Account ID** field that contains a 12-digit ID.
    4. Copy the account ID and save it in a safe location.

  * An AWS KMS key with the following characteristics:
    * It must be an asymmetric key.
    * It must be configured with the encryption and decryption usage.
    * It must have multi-region support for replica creation in the following regions supported by Cerby:
      * **Main:** `us-east-2`
      * **Replica:**`us-west-2`

      **IMPORTANT:** This requirement is needed to comply with Cerby’s Disaster Recovery process.

To create a compliant key, you must complete the instructions in step [1. Create your AWS KMS key](set-up-an-aws-kms-vault-integration.md#id-1.-create-your-aws-kms-key).

  * The AWS KMS key ID and the ARNs of the main and replica keys. You can find them by completing the following steps:

    1. Log in to your [AWS console](https://aws.amazon.com/console/) on your web browser.
    2. Access the **Key Management Service (KMS)** console.
    3. Open the KMS key you created after completing the instructions in step [1. Create your AWS KMS key](set-up-an-aws-kms-vault-integration.md#id-1.-create-your-aws-kms-key). The key details page is displayed.
    4. Copy the key ID located at the top of the key details page and save it in a safe location.
    5. Click the **Copy** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1239891766/0e42f7b7884afc9e966f9101dd75/AD_4nXfr-Hj1353b1jTkYtxoZVUzuIr_EzOotrPKegRPTZgRw8x_exWo7CtVkhpdpbGrbMkemEdUoRGWaYUpDmmfmOBZ4TOtooTN6VcGYNHI30gCbubrB5JbseQxe6zcZY-03YAQPXpndr4TE5PwRvlWKw9GIATI?expires=1765422000&signature=75fa31288e9a9ecba96cdcf62cefe3932eadd8dc7a52a58c63a8d1894e72f654&req=dSIkH8F3nIZZX%2FMW3Hu4gXCjGZX1m2LT2jnw5X%2FHot8IE40lfgQW03FsnQYG%0Atw%3D%3D%0A" alt="">) icon of the **ARN** field in the **General configuration** section and save it in a safe location. This is the ARN of the main key.
    6. Activate the **Regionality** tab below the **General configuration** section.
    7. Click the **Copy** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1239891766/0e42f7b7884afc9e966f9101dd75/AD_4nXfr-Hj1353b1jTkYtxoZVUzuIr_EzOotrPKegRPTZgRw8x_exWo7CtVkhpdpbGrbMkemEdUoRGWaYUpDmmfmOBZ4TOtooTN6VcGYNHI30gCbubrB5JbseQxe6zcZY-03YAQPXpndr4TE5PwRvlWKw9GIATI?expires=1765422000&signature=75fa31288e9a9ecba96cdcf62cefe3932eadd8dc7a52a58c63a8d1894e72f654&req=dSIkH8F3nIZZX%2FMW3Hu4gXCjGZX1m2LT2jnw5X%2FHot8IE40lfgQW03FsnQYG%0Atw%3D%3D%0A" alt="">) icon of the **Key ARN** column in the **Related multi-Region keys** section and save it in a safe location. This is the ARN of the replica key.

  * The AWS role ARN. You can find it by completing the following steps:

    1. Log in to your [AWS console](https://aws.amazon.com/console/) on your web browser.
    2. Access the **IAM** dashboard.
    3. Click the **Roles** option from the **Access management** list located at the left
side navigation drawer. The **Roles** page is displayed.

    4. Open the role you created after following the instructions in step [2. Create a new AWS IAM role](set-up-an-aws-kms-vault-integration.md#id-2.-create-a-new-aws-iam-role). The role details page is displayed.
    5. Copy the role ARN from the **ARN** field in the **Summary** section and save it in a safe location.

  * The Cerby account and workspace ID that can use the role created in section [2.1. Create a new role](set-up-an-aws-kms-vault-integration.md#id-2.1.-create-a-new-role). Request this ID at support@cerby.com.
* * *

## Set up an AWS KMS vault integration

To set up an AWS KMS vault integration, you must complete the following main steps:

  1. [Create your AWS KMS key](set-up-an-aws-kms-vault-integration.md#id-1.-create-your-aws-kms-key)
  2. [Create a new AWS IAM role](set-up-an-aws-kms-vault-integration.md#id-2.-create-a-new-aws-iam-role)
  3. [Set up the AWS KMS vault integration in Cerby](set-up-an-aws-kms-vault-integration.md#id-3.-set-up-the-aws-kms-vault-integration-in-cerby)
  4. [Configure logs in AWS for your KMS key](set-up-an-aws-kms-vault-integration.md#id-4.-configure-logs-in-aws-for-your-kms-key)

The following sections describe each main step.

### 1\. Create your AWS KMS key

To create your AWS KMS key, complying with the requirements to integrate with Cerby, you must complete the following steps:

  1. Log in to your [AWS console](https://aws.amazon.com/console/) in your web browser.

  **IMPORTANT:** Make sure you are in the **us-east-2** (**US East Ohio**) region by selecting it from the top navigation bar.

  2. Access the **Key Management Service (KMS)** console.
  3. Select the**Customer managed keys** option from the left menu.
  4. Click the **Create key** button. The **Configure key** page is displayed.
  5. Select the following options:
     1. **Asymmetric** in the **Key type** section.
     2. **Encrypt and decrypt** in the **Key usage** section. The **Key spec** section is displayed.
        1. Select the key material you want your key to have in the **Key spec** section.

        **TIP:** For your security, Cerby recommends using the**RSA_4096** key material.

  6. Expand the **Advanced options** section.
  7. Select the following options:

     * **KMS -_recommended_** in the **Key material** **origin** section.
     * **Multi-Region** **key** in the **Regionality** section.

  8. Click the **Next** button. The **Add labels** page is displayed.
     1. Enter the alias of the key in the **Alias** field.
  9. Click the **Next** button. The **Define key administrative** **permissions** page is displayed.
     1. Configure the key administrators for your KMS key, if needed, on this page.
  10. Click the **Next** button. The **Define key usage permissions** page is displayed.
     1. Configure the key users for your KMS key, if needed, on this page.
  11. Click the **Next** button. The **Review** page is displayed.

     * Review that the information about the KMS key is correct.
     * Keep the policy settings at their default configuration.

  12. Click the **Finish** button. Your key is created and listed on the **Customer managed keys** page.
  13. Create a key replica in the **`us-west-2`** region by completing the following steps:
     1. Click the key you have created on the **Customer managed keys** page. The key details page is displayed.
     2. Activate the **Regionality** tab located below the **General configuration** section. The **Primary key** and **Related multi-Region keys** sections are displayed.
     3. Click the **Create new replica keys** button. The **Create new replica keys** page is displayed.
     4. Select the **US West (Oregon)`us-west-2`** option from the **Choose Regions** drop-down list.
     5. Click the **Next** button. The **Add labels** page is displayed.
     6. Enter the alias of the replica key in the **Alias** field.
     7. Complete steps 9 to 11 to configure the key administrators and key users of your replica key.
     8. Select the **I understand that the values I choose here are not synchronized with any other multi-Region key** option in the **Confirmation** section.
     9. Click the **Create new replica keys** button. The replica key is created and displayed in the **Related multi-Region keys** section.
     10. Copy the key ID located at the top of the key details page and save it in a safe location. You need it in step [3. Set up the AWS KMS vault integration in Cerby](set-up-an-aws-kms-vault-integration.md#id-3.-set-up-the-aws-kms-vault-integration-in-cerby).
     11. Click the **Copy** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1239891766/0e42f7b7884afc9e966f9101dd75/AD_4nXfr-Hj1353b1jTkYtxoZVUzuIr_EzOotrPKegRPTZgRw8x_exWo7CtVkhpdpbGrbMkemEdUoRGWaYUpDmmfmOBZ4TOtooTN6VcGYNHI30gCbubrB5JbseQxe6zcZY-03YAQPXpndr4TE5PwRvlWKw9GIATI?expires=1765422000&signature=75fa31288e9a9ecba96cdcf62cefe3932eadd8dc7a52a58c63a8d1894e72f654&req=dSIkH8F3nIZZX%2FMW3Hu4gXCjGZX1m2LT2jnw5X%2FHot8IE40lfgQW03FsnQYG%0Atw%3D%3D%0A" alt="">) icon of the **ARN** field in the **General configuration** section and save it in a safe location. This is the ARN of the main key, and you need it in step [2.2. Attach a new inline policy to the role](set-up-an-aws-kms-vault-integration.md#id-2.2.-attach-a-new-inline-policy-to-the-role).
     12. Click the **Copy** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1239891766/0e42f7b7884afc9e966f9101dd75/AD_4nXfr-Hj1353b1jTkYtxoZVUzuIr_EzOotrPKegRPTZgRw8x_exWo7CtVkhpdpbGrbMkemEdUoRGWaYUpDmmfmOBZ4TOtooTN6VcGYNHI30gCbubrB5JbseQxe6zcZY-03YAQPXpndr4TE5PwRvlWKw9GIATI?expires=1765422000&signature=75fa31288e9a9ecba96cdcf62cefe3932eadd8dc7a52a58c63a8d1894e72f654&req=dSIkH8F3nIZZX%2FMW3Hu4gXCjGZX1m2LT2jnw5X%2FHot8IE40lfgQW03FsnQYG%0Atw%3D%3D%0A" alt="">) icon of the **Key ARN** column in the **Related multi-Region keys** section and save it in a safe location. This is the ARN of the replica key, and you need it in step [2.2. Attach a new inline policy to the role](set-up-an-aws-kms-vault-integration.md#id-2.2.-attach-a-new-inline-policy-to-the-role).

The next step is [2. Create a new AWS IAM role](set-up-an-aws-kms-vault-integration.md#id-2.-create-a-new-aws-iam-role).

### 2\. Create a new AWS IAM role

To create a new AWS IAM role specific to the AWS KMS integration with Cerby, you must complete the following steps:

  1. [Create a new role](set-up-an-aws-kms-vault-integration.md#id-2.1.-create-a-new-role)
  2. [Attach a new inline policy to the role](set-up-an-aws-kms-vault-integration.md#h_83a97c8c17)
  3. [Edit the trust relationship](set-up-an-aws-kms-vault-integration.md#id-2.3.-edit-the-trust-relationship)

The following subsections describe each step.

#### 2.1. Create a new role

To create a new role in AWS, complete the following steps:

  1. Log in to the [AWS Console](https://console.aws.amazon.com/console/home?nc2=h_ct&src=header-signin).
  2. Access the **IAM** dashboard.
  3. Select the **Roles** option from the **Access management** list in the left navigation drawer. The **Roles** page is displayed.
  4. Click the **Create role** button located at the top right of the page. The **Select trusted entity** page is displayed.
  5. Specify the configuration of the new role by completing the next steps:
     1. Select the **AWS account** option in the **Trusted entity type** section. The **An AWS account** section is displayed below.
     2. Select the **Another AWS account** option in the **An AWS account** section.
     3. Specify the Cerby account and workspace that can use this role by completing the following steps:
        1. Enter the ID provided by the Cerby support team in the **Account ID** field.
        2. Select the **Require external ID** option. The **External ID** field is displayed below.
        3. Enter your Cerby workspace ID in the **External ID** field. You can find it by completing the steps described in the [Requirements](set-up-an-aws-kms-vault-integration.md#id-requirements) section.
  6. Click the **Next** button. The **Add permissions** page is displayed.
  7. Click the **Next** button. The **Name, review, and create** page is displayed.
  8. Enter the name of the new role in the **Role name** field.
  9. Click the **Create role** button. The new role is created and listed on the **Roles** page.

The next step is [2.2. Attach a new inline policy to the role](set-up-an-aws-kms-vault-integration.md#h_83a97c8c17).

#### 2.2. Attach a new inline policy to the role

To attach a new inline policy to the role, you must complete the next steps:

  1. Open the role you created in step [2.1. Create a new role](set-up-an-aws-kms-vault-integration.md#id-2.1.-create-a-new-role) from the **Roles** page. The role details page is displayed.
  2. Click the **Add permissions** button of the **Permissions policies** section. A drop-down list is displayed.
  3. Select the **Create inline policy** option. The **Specify permissions** page is displayed.
  4. Click the **JSON** button in the **Policy editor** section. The policy JSON editor field is displayed.
  5. Copy and paste the following policy configuration in the editor field:

         {
            "Version": "2012-10-17",
            "Statement": [
               {
                  "Sid": "AllowCerbyToUseKMSKey", // You can modify this name, following AWS standards
                  "Effect": "Allow", // Do not modify
                  "Action": [ // Do not modify
                     "kms:Encrypt",
                     "kms:Decrypt",
                     "kms:GetPublicKey",
                     "kms:DescribeKey"
                  ],
                  "Resource": [
                     "{ARN for the main region KMS key}",
                     "{ARN for the replica region KMS key}"
                  ]
               }
            ]
         }

**IMPORTANT:** You must replace the **`{ARN for the main region KMS key}`** and **`{ARN for the replica region KMS key}`** values with the corresponding ARNs for the main and replica keys that you copied in step [1. Create your AWS KMS key](set-up-an-aws-kms-vault-integration.md#id-1.-create-your-aws-kms-key).

  6. Click the **Next** button. The **Review and create** page is displayed.
  7. Enter the name of the policy in the **Policy name** field.
  8. Click the **Create policy** button. A success message is displayed and the policy is attached to your role.
  9. (Optional) Expand the policy details in the **Permissions policies** section to verify that the configuration is correct.

The next step is [2.3. Edit the trust relationship](set-up-an-aws-kms-vault-integration.md#id-2.3.-edit-the-trust-relationship).

#### 2.3. Edit the trust relationship

To edit the trust relationship in the role, you must complete the next steps:

  1. Open the role you created in step [2.1. Create a new role](set-up-an-aws-kms-vault-integration.md#id-2.1.-create-a-new-role) from the **Roles** page. The role details page is displayed.
  2. Activate the **Trust relationships** tab located below the **Summary** section.
  3. Click the **Edit trust policy** button in the **Trusted entities** section. The **Edit trust policy** page is displayed with the following pre filled information:

         {
             "Version": "2012-10-17",
             "Statement": [
                 {
                     "Effect": "Allow",
                     "Principal": {
                         "AWS": "arn:aws:iam::749452252575:root"
                     },
                     "Action": "sts:AssumeRole",
                     "Condition": {
                         "StringEquals": {
                             "sts:ExternalId": "<workspace_id>"
                         }
                     }
                 }
             ]
         }

  4. Replace the information with the following policy:

         {
             "Version": "2012-10-17",
             "Statement": [
                 {
                     "Effect": "Allow",
                     "Principal": {
                         "AWS": "arn:aws:iam::749452252575:role/production-kms-byo-key-access-role"
                     },
                     "Action": "sts:AssumeRole",
                     "Condition": {
                         "StringEquals": {
                             "sts:ExternalId": "<workspace_id>"
                         }
                     }
                 }
             ]
         }

**IMPORTANT:** This policy must include the role allowed to perform actions within AWS, created by Cerby for the production environment: **`production-kms-byo-key-access-role`**. Also, you must replace **`<workspace ID>`** with the ID of your Cerby workspace.

  5. Click the **Update policy** button. The role **Summary** page is displayed again.

The next step is [3. Set up the AWS KMS vault integration in Cerby](set-up-an-aws-kms-vault-integration.md#id-3.-set-up-the-aws-kms-vault-integration-in-cerby).

### 3\. Set up the AWS KMS vault integration in Cerby

To set up the AWS KMS vault integration in Cerby, you must complete the following steps:

  1. Log in to your Cerby [workspace](https://app.cerby.com/) using the Cerby web app.
  2. Select the **Settings** option from the left navigation drawer. The **Workspace** **Configuration** page is displayed.
  3. Activate the **Privacy and Security** tab. A table with a list of vaults is displayed in the **Vault management** section.
  4. Click the **Create new vault** button. The **Create new vault** dialog box is displayed.
  5. Enter the vault name in the **Vault name** field.
  6. Select the **AWS KMS** option from the **Strategy** drop-down list.

  **NOTE:** Select the **Set as default vault** option if you want to set the new vault as the default when adding an item to Cerby.

  7. Click the **Next** button. The **Configure your AWS KMS vault** dialog box is displayed.
  8. Enter the following values in the corresponding fields:

     * **AWS Account ID**
     * **KMS Key ID**
     * **AWS Role ARN**

     **NOTE:** You can find the values by completing the corresponding steps in the [Requirements](set-up-an-aws-kms-vault-integration.md#id-requirements) section.

  9. Click the **Create vault** button. The **Vault created!** message appears, and the **Page reload required** dialog box is displayed.
  10. Click the **Reload page** button. The page is reloaded and the new vault is listed.

Now you are done. The next optional step is [4. Configure logs in AWS for your KMS key](set-up-an-aws-kms-vault-integration.md#id-4.-configure-logs-in-aws-for-your-kms-key).

### 4\. Configure logs in AWS for your KMS key

As an optional step in the AWS KMS integration with Cerby, you can configure logs in AWS to track the events for your key. For example, you can use the [AWS CloudTrail](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html) logging service, which can track all usage and management actions taken on your AWS KMS keys.

* * *

## Save accounts and secrets in your AWS KMS vault

After integrating your AWS KMS vault with Cerby, you can start saving accounts and secrets. Read the following articles to learn more about account and secret creation and vault assignation:

  * [Add an account](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/add-an-account)
  * [Add a secret](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/secrets/add-a-secret)
  * [Assign additional vaults to an account](https://cerby-test.gitbook.io/cerby-test/management/credential-management/vaults/assign-additional-vaults-to-an-account)
* * *

## Manage your AWS KMS vault

Read the article [Create and manage a vault](https://cerby-test.gitbook.io/cerby-test/management/credential-management/vaults/create-a-vault) to learn how to manage your AWS KMS vault.

* * *

## Plan any AWS KMS key modification

As stated at the beginning of this article, you must take into account the following before modifying your AWS KMS key:

  * You must _not_ delete or disable your AWS KMS key; otherwise, you will permanently lose access to all data encrypted with the key unless you have manually backed up the secret and account data beforehand. Cerby does not automatically detect deleted or disabled keys, as this action is outside our control.
  * You must _not_ edit the AWS KMS key; otherwise, you will permanently lose access to all data encrypted with the key unless you have manually backed up the secret and account data beforehand. Editing an AWS KMS key is complex due to encryption dependencies, and it is not supported within Cerby, as changes to the key prevent data decryption.

If you need to delete, remove, disable, or modify your KMS key, plan ahead and consider the following alternative actions for the accounts and secrets assigned to the vault:

  1. Create a new vault with a new key in AWS KMS.
  2. Manually assign the accounts and secrets to a different vault.
  3. Disable the AWS KMS vault within Cerby to avoid unintended data decryption issues.
