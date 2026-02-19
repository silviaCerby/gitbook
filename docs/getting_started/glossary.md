---
description: >-
  This article describes the basic definitions of terms that are commonly used
  in Cerby.
---

# Glossary

This glossary contains the basic definitions of terms that are commonly used in Cerby:

[A](./#a) | [B](./#b) | [C](./#c) | [D](./#d) | [E](./#e) | [F](./#f) | [G](./#g) | [H](./#h) | [I](./#i) | [J](./#j) | [K](./#k) | [L](./#l) | [M](./#m) | [N](./#n) | [O](./#o) | [P](./#p) | [Q](./#q) | [R](./#r) | [S](./#s) | [T](./#t) | [U](./#u) | [V](./#v) | [W](./#w) | [X](./#x) | [Y](./#y) | [Z](./#z)

***

## A

### Account

It is an identity created for users that enables them to sign in and access services, solutions, or apps with a service provider such as Facebook, Twitter, or TikTok.

An account usually consists of a username and a password, but in some cases, such as Facebook Business Manager accounts, they don’t have these identity elements, and users are granted access through the individual profile they already have with such service providers.

At Cerby, accounts are how users with**Account Collaborator** and **Account Owner** roles access their apps. The following two types of accounts exist:

* **Master account.** It is the primary account that Cerby leverages to assign a role to a proxy account for an asset.
* **Proxy account.** It is the account that Cerby leverages to grant users access to the assets and resources of services, solutions, or applications.

### Account card

It is a graphical component in the user interface (UI) of the Cerby web app, mobile app, and browser extension that consists of card-type buttons representing the application accounts added to Cerby.

Depending on the user [role](./#role) on such accounts, these cards redirect users to log in to their applications or to perform account management and security actions.

### Account Collaborator

It is an account-level role with basic permissions to log in to the accounts added to Cerby and with the roles assigned to those accounts. For the detailed permissions of this role, read the [Accounts](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles) section in the article [How Cerby manages roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles).

### Account Owner

It is an account-level role with permissions to manage the accounts added to Cerby and their security and also manage the **Account Collaborators**. For the detailed permissions of this role, see the [Accounts](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles) section in the article [How Cerby manages roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles).

### All-Access Mode

It is a workspace-level mode with permission to see all of the existing accounts at a workspace level, with the exception of accounts stored in local vaults. This role is enabled and disabled on demand.

### Asset

It consists of sub-accounts that belong to a parent account. For example, Pages and Ad Accounts may be assets for a Facebook Business Manager account.

### Authentication

It is a security process to determine the identity of users by verifying their credentials (such as user ID, username, and password) on directories, servers, or databases.

### Authorization

It is a security process to determine the role of users based on their identity. Users are granted permission to perform actions and access specific resources with these [roles](./#role).

***

## B

***

## C

### Cerby local user

It is a user that authenticates directly into Cerby with a username and password managed by Cerby. This process is as opposed to authenticating into a configured IDP such as Okta.

### Collection

It consists of groups of accounts displayed in the Cerby dashboard. Only **Account Owners** can add to collections the accounts they are owners of and share collections with other users (**Account Owners** and **Account Collaborators**).

***

## D

### Dashboard

It is the graphical interface of the Cerby web application that integrates information about users, accounts, configuration, services, and applications.

To navigate through the different features of Cerby, the dashboard contains the left navigation drawer and the main section that contains the different views, pages, information, and [account cards](./#account-card).

***

## E

***

## F

***

## G

***

## H

***

## I

### Identity provider (IDP)

It is a system entity that creates, stores, maintains, and manages identity information for users, services, or systems. It provides authentication services to other service providers within a federation or distributed network. Cerby connects with the IDP of an organization to retrieve information from their directory and centralize the user provisioning and deprovisioning processes.

***

## J

***

## K

***

## L

***

## M

***

## N

***

## O

### One-time password (OTP)

It is a password valid for only one login session or transaction on a computer system or other digital device. OTP is also known as a dynamic password or authentication code.

### OpenID Connect (OIDC)

It is an authentication protocol that enables services and applications to verify the identity of a user using an ID token.

***

## P

### Permission

It consists of the specific actions that users are enabled to perform in a system, solution, or application. At Cerby, permissions are determined inside the code and work at a workspace and account level.

***

## Q

***

## R

### Role

It consists of a set of permissions that represent the tasks, activities, or functions that users can perform. Users can have none, one, or multiple (in some cases overlapping) roles.

Cerby manages roles at a workspace and account level, and roles are also inherited from the configuration of your apps.

The following are the different roles in Cerby depending on your access level:

* Workspace-level roles
  * [Workspace Owner](./#workspace-owner)
  * [Workspace Admin](./#workspace-admin)
  * [Workspace User](./#workspace-user)
*   Account-level roles

    * [Account Owner](./#account-owner)
    * [Account Collaborator](./#account-collaborator)

    **NOTE:** Regardless of their role, all users can add accounts to a workspace and then introduce the account roles, and they can only share the accounts they are owners of. Also, all users can create collections.

For the detailed permissions of each role, read the [Workspace-level roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles) and [Item-level roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles) sections in the article [How Cerby manages roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles).

***

## S

### Security Assertion Markup Language (SAML)

It is a standard that enables IDPs and service providers to exchange data to authenticate and authorize users. With this standard, service providers can enable SSO processes for users across applications that support SAML.

### Service provider

It is an entity that provides services, solutions, or applications to end users and organizations. For example, Twitter, Mailchimp, or Instagram.

### Shared Inbox

It is a feature that enables you and your team members to receive and store the messages sent to the phone numbers and email addresses provisioned and managed by Cerby and configured in your app accounts.

Cerby leverages the **Shared Inbox** to provide you with automatic logging-in processes to your accounts, including verification codes for [2FA](./#two-factor-authentication-\(2fa\)).

### Single sign-on (SSO)

It is an authentication method that enables users to log in to multiple applications or services using a single set of credentials.

### System for Cross-Domain Identity Management (SCIM)

It is a standard for automating the interchange of user identity information between IDPs and service providers. At Cerby, this standard enables automation for provisioning and deprovisioning users.

***

## T

### Two-factor authentication (2FA)

It is a security process that involves two identification points to authenticate users. The first factor is a password and the second is a verification code sent to different verification methods, such as SMS, email, or mobile application. 2FA is configured for the app accounts added on Cerby that support this authentication method.

***

## U

***

## V

### Verification code

It is a security code provided by authenticators when users try to complete tasks (such as recovering a password or turning on 2FA) or logging in to a service or application. It ensures that only authorized users gain access or perform the actions. At Cerby, verification codes are sent to the mobile application.

### Voice over Internet Protocol (VoIP)

It is a communication protocol that enables users to access phone services through IP. At Cerby, VoIP is commonly used to deliver verification messages for user authentication.

***

## W

### Workspace

It is the environment in which organizations and users can access a set of shared accounts to log in to other apps. For example, an organization can leverage a Cerby workspace to log in to their social media accounts and manage the overall security of these accounts.

Through a Cerby workspace, organizations and users can also manage their accounts and perform the following actions:

* Manage user permissions.
* Manage app accounts.
* Onboard two-factor authentication (2FA) and rotate passwords for accounts.
* Manage user provisioning and deprovisioning.
* Configure authentication with an identity provider (IDP).
* Retrieve analytics for account usage and user activity.

Organizations may have one or multiple workspaces depending on their needs. Though usually, one organization has one workspace.

Currently, you can only create a workspace from an invitation sent by the Cerby team from our official email address, [help@cerby.com](mailto:help@cerby.com). After creating your workspace, its name is displayed and identified as follows **< workspace name>.cerby.com**.

### Workspace Admin

It is a workspace-level role with permissions to manage accounts and configure their security and also manage users within Cerby, including their permission level. For the detailed permissions of this role, read the [Workspace-level roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles) section in the article [How Cerby manages roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles).

### Workspace Owner

It is a workspace-level role with permissions to perform the same actions as **Workspace** **Admins** , as well as configure the IDP settings and create and configure a workspace. For the detailed permissions of this role, read the [Workspace-level roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles) section in the article [How Cerby manages roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles).

### Workspace User

It is a workspace-level role with basic permissions to log in to the accounts registered in Cerby, see other users from their organization, and configure the security of accounts. For the detailed permissions of this role, read the [Workspace-level roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles) section in the article [How Cerby manages roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles).

***

## X

***

## Y

***

## Z

***
