---
description: This article describes the Cerby CLI commands, explaining their purpose and usage.
intercom_id: 9136331
---

# Use the Cerby CLI

This article is a reference guide for starting to interact with the Cerby CLI features from your command line. Here, you can discover all of Cerby CLI commands available for the following actions:

* Secrets
* Accounts
* Sync your data

​​The following sections describe each action.

* * *

## Secrets

Cerby CLI enables you to perform the following actions with your secrets in Cerby:

* Get all secrets
* Get the value of a secret by ID

### Get all secrets

Execute the following command to get the list of all your secrets in Cerby:

    cerby-{os} secrets list

By default, the result array contains the first 20 secrets in your Cerby workspace. You can add the pagination flags `--page-size` and `--start-index` to get the list of a specific page or to set the starting index of the array. Refer to the [Interpret and customize the Cerby CLI output](https://cerby-test.gitbook.io/cerby-test/extending-cerby/cerby-cli/interpret-and-customize-the-cerby-cli-output-data) article to learn more about the output.

The resulting JSON has the following main keys:

* `itemsPerPage` (Number): The number of secret objects returned in the secureSecrets array
* `secureSecrets` (array): The secret object with information about each shared or owned secret in the Cerby workspace
    * `body` (Object)
    * `category` (String): The secret category, which might be any of the following: text, server, ssh_key, database, wifi_password, software_license, or custom
    * `createdAt` (String): The date when the secret was created
    * `createdBy` (String): The ID of the member who created the secret
    * `createdByDetails` (Object): The information of the member who created the secret
      * `firstName` (String): The first name of the member who created the secret
      * `lastName` (String): The last name of the member who created the secret
    * `id` (String): The secret ID
    * `idekId` (String)
    * `requiresIdentityChallenge` (Boolean): `true` if the secret requires members to complete an identity challenge to access the secret when shared; `false` if the secret is accessible without the challenge
    * `roles` (array): The list of roles on the secret
    * `status` (String): The status of the secret
    * `title` (String): The title of the secret
    * `updatedAt` (String): The date when the secret was last updated
    * `updatedBy` (String): The ID of the member who last updated the secret
    * `updatedByDetails` (Object): The information of the member who last updated the secret
      * `firstName` (String): The first name of the member who last updated the secret
      * `lastName` (String): The last name of the member who last updated the secret
    * `vaultId` (String): The ID of the vault where the secret is stored
    * `version` (Number)
    * `versionId` (String)
    * `workspace` (String): The name of the Cerby workspace to which the secret belongs
* `startIndex` (Number): Indicates the starting index within the response array from which results are displayed
* `totalResults` (Number): Indicates the total number of secrets returned in the results, which must be the same number of secrets you see in your workspace

The following is an example of the result the command returns:

    {
      "itemsPerPage": 6,
      "secureSecrets":[
        {
          "body": null,
          "category": "text",
          "createdAt": "2024-03-11T24:31:39.177000",
          "createdBy": "d3f73961-a0ac-54ba-ade7-d94035413c59",
          "createdByDetails":{
            "firstName": "John",
            "lastName": "Doe"
          },
          "id": "c2a47fce-00cd-3b1a-aaa8-775afc9005a8",
          "idekId": "3df71750-a9ac-43ba-adc7-f94146734a59",
          "requiresIdentityChallenge": false,
          "roles": [
            "secure_secret_collaborator"
          ],
          "status": "active",
          "title": "mktCampaign-Global-secret",
          "updatedAt": "024-03-11T24:31:39.177000",
          "updatedBy": "d3f73961-a0ac-54ba-ade7-d94035413c59",
          "updatedByDetails": {
            "firstName": "John",
            "lastName": "Doe"
          },
          "vaultId": "c9a370a4-9b38-ac98-b04a-a0009498d543",
          "version": 0,
          "versionId": "51d6742a-04c9-44aa-917d-4c0d24fedaf7",
          "workspace": "Acme"
        },
        //This is a sample. More secret objects are returned in this array.
      ],
      "startIndex": 1,
      "totalResults": 20
    }

### Get the value of a secret by ID

Execute the following command to get the information of a particular secret:

    cerby-{os} secrets get --id={secret-id}

You must replace the secret-id parameter with the corresponding secret ID. You can obtain the ID by first using the secrets list command and copying it from the result.

The resulting output is the value of the secret.

## Accounts

The Cerby CLI enables you to perform the following actions with your accounts in Cerby:

* Get all accounts
* Get the information of an account by ID
* Include the password in the information of an account

### Get all accounts

Execute the following command to get the list of all the accounts you created or someone shared with you in Cerby:

    cerby-{os} accounts list

By default, the result array contains the first 20 accounts in your Cerby workspace. You can add the pagination flags `--page-size` and `--start-index` to get the list of a specific page or to set the starting index of the array. Refer to the [Interpret and customize the Cerby CLI output](https://cerby-test.gitbook.io/cerby-test/extending-cerby/cerby-cli/interpret-and-customize-the-cerby-cli-output-data) article to learn more about the output.

The resulting JSON has the following main keys:

* `startIndex` (Number): Indicates the starting index within the response array from which results are displayed.
* `limit` (Number): Indicates the number of account objects returned in the accounts array.
* `totalResults` (Number): Indicates the total number of accounts the CLI found, which must be the same number of secrets you see in your workspace.
* `accounts`
    * `id` (String): The ID of the account
    * `name` (String): The name of the account
    * `username` (String): The username used to log in to the account
    * `provider` (String): The account type
    * `vaultId` (String): The ID of the vault where the account is stored
    * `idekID` (String)
    * `permissions` (array): The permissions you have over the account
    * `workspace` (String): The name of the Cerby workspace to which the account belongs
    * `mfaEnabled` (Boolean): `true` if the MFA is activated for the account; else, `false`
    * `autofillMfa` (Boolean): `true` if the MFA is activated for auto-filling with the Cerby extension when logging in to the account; else, `false`
    * `passwordSet` (Boolean): `true` if a password is set for the account; else, `false`
    * `passwordVisible` (Boolean): `true` if the password is visible for the account; else, `false`
    * `createdBy` (String): The ID of the member who created the account
    * `createdAt` (String): The date when the account was created
    * `updatedAt` (String): The date when the account was last updated
    * `role` (String): The role you have over the account
    * `avatar_url` (String)
    * `email` (String): The Cerby-managed email address of the account owner
    * `type` (String): The account type, for example, “Identity”
    * `url` (String): The URL of the account
    * `domain` (String): The domain of the account
    * `meta` (Object): The account meta information
    * `status` (String): The status of the account in the Cerby workspace
    * `phone` (String): The phone number associated with the account
    * `rotatedBy` (String): The type of rotation for the account when sharing. For example, “manual_rotation”
    * `rotatedAt` (String): The date when the last rotation of the account happened
    * `syncedAt`
    * `hasBackupCode` (Boolean): `true` if the account manages a backup code; else, `false`
    * `rotatedById` (String): The ID of the member who last shared the account.
    * `domains` (Object): The information on the domains related to the account
      * `allowedDomains` (array): The information of a domain related to the account
        * `domain` (String)
        * `subdomain` (String)
        * `hostname` (String)
        * `path` (String)
        * `url` (String)
        * `isMainDomain` (Boolean)
      * id(String)
    * `lastLoginDate` (String): The date when the last login to the account happened
    * `lastLoginUserName` (String): The full name of the last member who logged in to the account through Cerby
    * `isEmailManaged` (Boolean): `true` if the account has the Cerby-managed email enabled; else, `false`
    * `isPhoneManaged` (Boolean): `true` if the account has the Cerby-managed email enabled; else, `false`
    * `originalEmail` (String): The original email address associated with the account before setting a Cerby-managed email address
    * `originalPhone` (String): The original email address associated with the account before setting a Cerby-managed phone number
    * `businessId` (String)
    * `mfaTypes` (array)
    * `rotatedByUser` (String)
    * `hasTotpVirtualDevice` (Boolean)
    * `workspacePolicyResult` (Object): The information about the policies set for the account
      * `mfa_validation` (Boolean): `true` if the MFA authentication is enabled for the account; else, `false`
      * `password_rotation` (Boolean): `true` if the password rotation is enabled for the account; else, `false`
    * `workspacePolicyCheckDate` (String): The date when the account policies were last modified

The following is an example of the result the command returns:

    {
      "limit": 20,
      "startIndex": 1,
      "totalResults": 15
      "accounts": [
        {
          "id": "55d3a51f-9181-46b9-9f43-cbb915155c66",
          "name": "Acme Account",
          "username": "johndoe@gmail.com",
          "provider": "google",
          "vaultId": "f9b480d4-f68e-4afa-b04a-8adb9498d543",
          "idekID": "218095a1-d41f-1234-a278-4541953adac1",
          "permissions": [],
          "workspace": "Acme",
          "mfaEnabled": false,
          "autofillMfa": true,
          "passwordSet": true,
          "passwordVisible": false,
          "createdBy": "b62e592c-4986-1234-978b-8223903a4ece",
          "createdAt": "2024-02-03T13:20:32",
          "updatedAt": "2024-02-03T13:23:04",
          "role": "owner",
          "avatar_url": "",
          "email": "johndoe@gmail.com",
          "type": "secret",
          "url": null,
          "domain": null,
          "meta": {},
          "status": "enabled",
          "phone": "1232395629",
          "rotatedBy": "manual_rotation",
          "rotatedAt": "2024-02-03T13:56:26",
          "syncedAt": null,
          "hasBackupCode": false,
          "rotatedById": "b62e592c-4986-4afa-89d4-8223903a4ece",
          "domains": null,
          "lastLoginDate": "2024-02-18T04:17:05",
          "lastLoginUserName": "John Doe",
          "isEmailManaged": false,
          "isPhoneManaged": true,
          "originalEmail": null,
          "originalPhone": null,
          "businessId": "",
          "mfaTypes": [],
          "rotatedByUser": null,
          "hasTotpVirtualDevice": false,
          "workspacePolicyResult": {
            "mfa_validation": false,
            "password_rotation": true
          },
          "workspacePolicyCheckDate": "2024-02-03T13:56:27"
        },
        //This is a sample. More account objects are returned in this array.
      ],
      …
    }

### Get the information of an account by ID

Execute the following command to get the information of a particular account:

    cerby-{os} accounts get --id={account-id}

You must replace the `account-id` parameter with the corresponding account ID. You can obtain that ID by first using the accounts list command and copying it from the result.

The resulting JSON is an object with information about the account.

### Include the password in the information of an account

Execute the following command to get the information of a particular account, including the account password:

    cerby-{os} accounts get --id={account-id} --with-password

You must replace the `account-id` parameter with the corresponding account ID. You can obtain the ID by first using the accounts list command and copying it from the result.

The resulting JSON is an object with information about the account, which includes the password key.

## Sync your data

Most sensitive data, such as passwords and secrets, are encrypted within designated vaults in Cerby for security considerations. Synchronization within the Cerby platform and the CLI is crucial in maintaining consistency between your local environment and the platform.

When syncing your information locally, the Cerby CLI storage mechanism relies on the operating system. For example, for MacOS, we use Keychain, and for Windows, we use the Credentials Manager.

With this information stored locally, you can use local bots to retrieve the password of an account or the secret value associated with it. However, to access this information, you must complete two crucial steps:

  1. [Set up a trusted device](https://cerby-test.gitbook.io/cerby-test/extending-cerby/cerby-cli/set-up-the-cerby-cli-as-a-trusted-device): To establish a secure connection between your device and Cerby, allowing it to synchronize.
  2. **Sync the data:** To retrieve and store the relevant information by executing the following command:

         cerby-{os} sync

**NOTE:** The sync command does not return any output.
---
