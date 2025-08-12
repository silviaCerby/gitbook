# Data definitions

**Description:** This article details the account and member data structures and formats used within the API endpoints.

When making a request to the supported endpoints, the Cerby Read API returns a
response object with key-value pairs containing information about accounts and
users in a Cerby workspace.

This article details the data structures and formats used within the API
endpoints for the following types of information:

  * Account

  * Member

The following sections describe each data structure.

* * *

# Account

In Cerby, accounts are digital records that contain user login information for
a particular application or service provider. An `account` object contains
information about your login credentials on a specific website, such as your
username, password, and other relevant attributes within the context of your
workspace.

## **JSON representation**

The following is a JSON representation of an account response object:

    
    
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
     }

## **Account details**

The following are the details of an account response object:

  * `id` (String): The ID of the account

  * `name` (String): The name or label of the account

  * `username` (String): The username used to log in to the account

  * `provider` (String): The application or service provider to which the account belongs 

  * `vaultId` (String): The ID of the vault where the account is stored in Cerby

  * `idekID` (String): The ID associated with a specific data encryption key

  * `permissions` (Array): The permissions on the account 

  * `workspace` (String): The name of the Cerby workspace to which the account belongs 

  * `mfaEnabled` (Boolean): true if MFA is activated for the account; else, false

  * `autofillMfa` (Boolean): true if MFA is activated for auto-filling with the Cerby browser extension when logging in to the account; else, false

  * `passwordSet` (Boolean): true if a password is set for the account; else, false

  * `passwordVisible` (Boolean): true if the option for collaborators to view the account password is activated; else, false

  * `createdBy` (String): The ID or an object with information about the workspace member who created the account

    * `id`: The ID of the workspace member who created the account

    * `firstName`: The first name of the workspace member who created the account

    * `lastName`: The last name of the workspace member who created the account

    * `email`: The email of the workspace member who created the account

    * `idpUid`: The identifier associated with the workspace member by the identity provider

    * `lastUsed`: The date when the account was last used

    * `createdAt`: The date when the account was created

    * `workspace`: The name of the Cerby workspace to which the account belongs to

  * `createdAt` (String): The date when the account was created

  * `updatedAt` (String): The date when the account was last updated

  * `role` (String): The role you have on the account (**Owner** or **Collaborator**)

  * `avatar_url` (String): The URL of the workspace member’s avatar image

  * `email` (String): The email address of the account **Owner**

  * `type` (String): The type of item. For example, identity, resource, secret, or integration

  * `url` (String): The login URL of the account

  * `domain` (String): The domain of the application or service provider 

  * `meta` (Object): The additional metadata to include in the data request

  * `status` (String): The status of the account in the Cerby workspace. For example, enabled or disabled (removed)

  * `phone` (String): The phone number associated with the account

  * `rotatedBy` (String): The type of password rotation performed on the account. For example, automated_rotation or manual_rotation

  * `rotatedAt` (String): The date when the last rotation of the account password happened

  * `syncedAt` (String): The date when the latest check for updates was performed for an app integration

  * `hasBackupCode` (Boolean): true if Cerby has the MFA backup code stored; else, false 

  * `rotatedById` (String): The ID of the workspace member who performed a password rotation 

  * `domains` (String): The domains related to the account

  * `lastLoginDate` (String): The date when the last login to the account happened

  * `lastLoginUserName` (String): The full name of the last workspace member who logged in to the account through Cerby

  * `isEmailManaged` (Boolean): true if the account has an associated Cerby-managed email address; else, false

  * `isPhoneManaged` (Boolean): true if the account has an associated Cerby-managed phone number; else, false

  * `originalEmail` (String): The original email address associated with the account before setting up a Cerby-managed email address

  * `originalPhone` (String): The original phone number associated with the account before setting up a Cerby-managed phone number

  * `businessId` (String): The ID of the seat-based SaaS application, business hub, or paid social app needed to connect it to a Cerby app integration

  * `mfaTypes` (array): The types of MFA verification methods set up for the account. For example, otp, voip and email 

  * `rotatedByUser` (String): The full name of the workspace member who performed the latest password rotation

  * `hasTotpVirtualDevice` (Boolean): true if MFA authentication with TOTP is enabled with Cerby as an authenticator app; else, false

  * `workspacePolicyResult` (Object): The information about the security policies set for the account

    * `mfa_validation` (Boolean): true if the MFA authentication is enabled for the account; else, false

    * `password_rotation` (Boolean): true if the password was rotated within the policy timeframe; else, false

  * `workspacePolicyCheckDate` (String): The date when the workspace security policies were last verified

* * *

# Member

In Cerby, members are users who have access to a workspace and can create and
save items. A `member` object contains information about the user's name,
email, roles, and other relevant attributes within the context of your
workspace.

## **JSON representation**

The following is a JSON representation of a member response object:

    
    
    {  
        "id": "b6731083-d8f0-47ab-ad09-f2dd191363ba",  
        "firstName": "John",  
        "lastName": "Doe",  
        "email": "johndoe@example.com",  
        "status": "live",  
        "role": "workspace_guest_admin",  
        "isGuest": true,  
        "createdAt": "2024-02-07T11:18:09",  
        "updatedAt": "2024-02-07T11:20:14",  
        "lastActivity": null,  
        "meta": {}  
    }

## **Member details**

The following are the details of a member response object:

  * `id` (String): The ID of the workspace member in Cerby 

  * `firstName` (String): The workspace member’s first name

  * `lastName` (String): The workspace member’s last name 

  * `email` (String): The workspace member’s email address

  * `status` (String): The status of the workspace member. For example, live or disabled

  * `role` (String): The workspace member’s role in Cerby

  * `isGuest` (Boolean): true if the member is a guest user, meaning they are not part of your organization and have external access to your Cerby workspace; else, false

  * `createdAt` (String): The date and time when the workspace member was created in Cerby

  * `updatedAt` (String): The date and time when the workspace member’s information was last updated in Cerby

  * `lastActivity` (String): The date and time when the workspace member was active in the workspace

  * `meta` (Object): The additional metadata to include in the data request

