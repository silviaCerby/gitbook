---
description: "This article describes how to add a vault backup for your workspace."
intercom_id: 12431284
---

# Add a vault backup

{% hint style="info" %}


**Who can use this capability?**

* Workspace**Owners** , **Super Admins** , and **Admins**
* Only supported using the Cerby web app.


{% endhint %}

As a workspace **Owner** , **Super** **Admin** , or **Admin** , you can create and set up the **Vault Backup** capability to back up the login credentials saved in your Cerby workspace to CyberArk.

This capability provides a reliable recovery system, ensuring that your data remains backed up in the event of an incident. For more information, read the article [Explore Vault Backup](https://cerby-test.gitbook.io/cerby-test/management/credential-management/vaults/vault-backup/back-up-your-cerby-vault-to-an-external-provider).

{% hint style="danger" %}


**IMPORTANT:** After setting up the workspace vault backup, any account added to Cerby or updated is automatically backed up to CyberArk.


{% endhint %}

* * *

## Requirements

The following are the requirements for configuring Vault Backup with CyberArk:

  * A Cerby workspace
  * A Cerby user account with the workspace **Owner** , **Super** **Admin** , or **Admin** role
  * A CyberArk account with the permissions to perform the following:
    * Add an account
    * Update an account
  * The following information from CyberArk:

  **IMPORTANT:** The values in this section must be exclusive to the CyberArk–Cerby connection. To ensure proper isolation, you must create a new platform and a new safe in CyberArk for this purpose

    * **Client ID:** The identifier of the service account created in CyberArk for Cerby. Read CyberArk’s official documentation to learn more about service account creation in step 1 of the article [API token authentication for CyberArk Identity Security Platform Shared Services](https://api-docs.cyberark.com/docs/ispss-api-auth/2c297daca8a97-api-token-authentication-for-cyber-ark-identity-security-platform-shared-services#step-1-create-an-ispss-service-account)

    **IMPORTANT:** The service account must have the proper role to create and update accounts and passwords in CyberArk

    * **Client secret:** The secret generated together with the Client ID. Used by Cerby for secure authentication
    * **CyberArk Base URL:** The base URL of your CyberArk environment in the following format: `https://<identity-tenant-id>.id.cyberark.cloud`
​**IMPORTANT:** If you want to use a domain other than <cyberark.cloud>, contact [support@cerby.com](mailto:support@cerby.com)

    * **CyberArk Auth URL:** The Privilege Cloud Portal API URL for your CyberArk tenant in the following format: `https://<subdomain>.privilegecloud.cyberark.cloud`

    **IMPORTANT:** If you want to use a domain other than <`cyberark.cloud`>, contact [support@cerby.com](mailto:support@cerby.com)

    * **Safe name:** The name of the CyberArk safe dedicated to Cerby, where account data from Cerby will be backed up. Read CyberArk’s official documentation [Create and manage Safes for access control](https://docs.cyberark.com/privilege-cloud-standard/latest/en/content/privilege%20cloud/privcloud-manage-safes.htm?Highlight=Safe) to learn more about safe creation
    * **Platform ID:** The identifier of the CyberArk platform associated with the new safe. Read CyberArk’s official documentation [Set up platforms](https://docs.cyberark.com/privilege-cloud-standard/latest/en/content/privilege%20cloud/privcloud-platforms-setup.htm) to learn more about platform setup

This platform must have the following properties set up as optional:

      * `accountId`
      * `provider`
      * `label`
      * `url`
      * `phone`
      * `email`
      * `originalPhone`
      * `originalEmail`
      * `totpSecret`
      * `backupCodes`
* * *

## Add a vault backup

To add a vault backup in CyberArk for your workspace, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed with the **General** tab activated.
  3. Activate the **Privacy and security** tab.
  4. Activate the **Vault backup** left tab.
  5. Click the **Add vault backup** button. The **Add vault backup** page is displayed.
  6. Configure the connection with CyberArk by completing the following steps:
     1. Select the **CyberArk** option in the **Select a provider** section.
     2. Click the **Done** button. The **Connect to CyberArk** section is displayed.
     3. Enter the information in the following fields:

        * **CyberArk auth URL**
        * **CyberArk base URL**
        * **Client ID**
        * **Client secret**

     4. Click the **Connect** button. Cerby tests the connection with CyberArk, and the **Specify the safe and platform** section is displayed after a successful connection.
     5. Enter the information in the following fields:

        * **Safe name**
        * **Platform ID**

     6. Click the **Validate targets** button. Cerby validates the safe, and after a successful validation, the **Done** button is enabled at the top right of the page.
  7. Click the **Done** button in the top right of the page. The **Vault backup** section is displayed with the information about the vault backup setup.
Any account added or updated after configuring vault backup is automatically backed up to CyberArk.

Now you are done.
