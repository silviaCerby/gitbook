---
description: "This article describes the basic definitions of terms that are commonly used in Cerby."
intercom_id: 6465559
---

# Glossary

This glossary contains the basic definitions of terms that are commonly used in Cerby:

[A](glossary.md#a) | [B](glossary.md#b) | [C](glossary.md#c) | [D](glossary.md#d) | [E](glossary.md#e) | [F](glossary.md#f) | [G](glossary.md#g) | [H](glossary.md#h) | [I](glossary.md#i) | [J](glossary.md#j) | [K](glossary.md#k) | [L](glossary.md#l) | [M](glossary.md#m) | [N](glossary.md#n) | [O](glossary.md#o) | [P](glossary.md#p) | [Q](glossary.md#q) | [R](glossary.md#r) | [S](glossary.md#s) | [T](glossary.md#t) | [U](glossary.md#u) | [V](glossary.md#v) | [W](glossary.md#w) | [X](glossary.md#x) | [Y](glossary.md#y) | [Z](glossary.md#z)

* * *

## A

### Account

It is a digital record containing the user login information for a particular application or service provider. In the context of identity and access management, accounts are essential for authenticating and granting users access to applications, systems, or service providers such as Mailchimp, Facebook, Twitter, or TikTok.

Accounts usually comprise a username and a password. However, depending on the application default credentials and user needs, additional information could be saved in a Cerby account, such as the following:

  * Email address
  * Phone number
  * Application or service provider name
  * Login URL
  * [Account notes](glossary.md#account-note)
  * [Account custom fields](glossary.md#account-custom-field)

In the context of a Cerby workspace, all users, except the ones with the **Login-only** or **Guest user** role, can add an account to manage and secure access to it through Cerby. When you add an account to Cerby, you automatically become its **Owner** , and when you share it with other workspace members, teams, or guest users, you can assign them one of the following three roles:

  * **[Owner](glossary.md#account-owner):** They can share access, manage the account configuration, and log in to the account.
  * **[Manager](glossary.md#account-manager):** They can request access to account **Owners** for other external users in the context of [local partners](https://help.cerby.com/en/articles/8980877-explore-partners#h_7e4add33a2) and [host-guest partnerships](https://help.cerby.com/en/articles/8980877-explore-partners#h_735a5e4908).
  * **[Collaborator](glossary.md#account-collaborator):** They can only log in to the account.

For more information about roles and the actions users can perform on an account added to Cerby, read the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

### Account autosave

It is a feature in the Cerby web app and browser extension that enables you to save login and signup credentials automatically, streamlining the process of adding accounts.

Workspace **Admins** , **Super Admins** , and **Owners** can set up and turn on this feature for all workspace users and control if specific website domains should be allowed or excluded. For more information, read the article [Explore account autosave](https://help.cerby.com/en/articles/9500455-explore-account-autosave).

### Account card

It is a graphical component in the user interface (UI) of the Cerby web app, mobile app, and browser extension that consists of card-type buttons representing the accounts added to Cerby. These cards redirect users to log in to their applications, perform account management and configuration, and trigger security actions.

### Account Collaborator

It is a role in Cerby with basic permissions to log in to an account added to Cerby and view its details, such as [account notes](glossary.md#account-note) and [account custom fields](glossary.md#account-custom-field). [Account Owners](glossary.md#account-owner) can assign this role to workspace members, teams, or guest users when sharing their accounts with them.

For more information about this role, read the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

### Account custom field

It is an input field users can create as needed to save text-based information related to an account. The following three types of fields are available for customization and categorization of account details:

  * URL link
  * Short text
  * Long text

These fields can only be created and updated by account **Owners** when editing the account details. Both account **Owners** and **Collaborators** can view the information saved in them.

Cerby supports up to 140 custom fields per account. For more information about this feature, read the article [How to add and manage custom fields for your accounts](https://help.cerby.com/en/articles/8076378-how-to-add-and-manage-custom-fields-for-your-accounts).

### Account details page or screen

It is a section in the UI where the details and settings of an account are centralized. You can access the account details page or screen using the Cerby web app, browser extension, and mobile app.

Account **Owners** can edit the details of an account and update its configuration through the account details page or screen. Account **Collaborators** can only view the account details.

### Account Manager

It is a role in Cerby in the context of [local partners](https://help.cerby.com/en/articles/8980877-explore-partners#h_7e4add33a2) and [host-guest partnerships](https://help.cerby.com/en/articles/8980877-explore-partners#h_735a5e4908) with permissions to request access to accounts for other external users.

Account**Managers** send requests to account**Owners** in a host workspace to share their accounts with specific guest workspace members or guest users. However, **Managers** cannot perform user management tasks (remove, edit, or see members' information) and cannot access account security settings.

For more information about this role, read the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

### Account note

It is an input field where users can save additional text-based information related to their accounts. By default, notes are available to all accounts; they are the equivalent of a password note in LastPass or 1Password, and you can import them to Cerby when migrating your items from your password manager.

Account notes can only be updated by account **Owners** when editing the account details. However, both account **Owners** and **Collaborators** can view the information saved in them.

For more information, read the article [How to save and manage account notes](https://help.cerby.com/en/articles/8076365-how-to-save-and-manage-account-notes).

### Account Owner

It is a role in Cerby with permissions to manage the accounts added to Cerby, including their security, configuration, and shared access for other members, teams, or guest users. They can also enter and update account details, such as [account notes](glossary.md#account-note) and [account custom fields](glossary.md#account-custom-field).

Account **Owners** can assign the **Owner** or **Collaborator** role to workspace members, teams, or guest users when sharing their accounts with them. For the detailed permissions of this role, read the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

### All-Access Mode

It is a workspace-level mode with permissions to see all of the existing accounts at a workspace level, except accounts stored in local vaults. They can also see the names of members and teams with shared access to these accounts, and reassign account **Owners** for recovery purposes.

This role is enabled and disabled on demand. For more information, read the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

### Asset

It is a resource, entity, or subproduct associated with and managed by seat-based and paid social apps for specific purposes, like advertising and marketing.

Assets are typically categorized as paid (such as ad accounts) and organic (such as pages, pins, videos, and stories). For example, Pages and Ad Accounts are assets of a Meta Business Manager. Assets can also support organizational use cases, such as managing projects, teams, or other internal structures that exist within a larger business account.

When you connect a [business hub](https://help.cerby.com/en/articles/6831152-explore-business-hubs), you can sync and import the assets of your seat-based and paid social apps to centrally manage access to them from Cerby. After importing them, assets become sub-accounts of a parent business hub in Cerby.

### Asymmetric encryption

It is a cryptographic system also known as public-key encryption that uses a pair of related keys to encrypt and decrypt data: a public and private key. The goal of using this system is to enable the secure exchange of confidential data over insecure channels, such as the Internet.

The public key is used as a data encryption key (DEK) to encrypt the data inside a vault by any agent on the server or the client side. This public key is openly distributed; however, only the intended recipient of the encrypted data, who owns the private key, can access and decrypt the data.

### Authentication

It is a security process that determines users' identities by verifying their login credentials (such as user ID, username, and password) on directories, servers, or databases. The goal is to ensure that only authorized users can access sensitive data, services, or apps.

### Authorization

It is a security process that determines users' roles and access levels based on their identities. Users are granted permission to perform actions and access specific resources with these roles. The goal is to ensure that authenticated users have appropriate and limited access to sensitive data or app functionalities.

### Autofill

It is a feature of the Cerby browser extension and mobile app that automatically fills in login credentials (username, password, and verification codes) into the corresponding fields of a login page or mobile app. Autofill is used for automated and manual logins.

### Auto-login or automated login

It is one of Cerby's automated tasks that enables users to log in to their accounts automatically without manually filling in their credentials. When multi-factor authentication (MFA) is on and managed by Cerby, verification codes are also filled in automatically.

This feature is enabled for all [managed accounts](https://help.cerby.com/en/articles/8708338-explore-accounts#h_f0a859b407); for [self-managed accounts](https://help.cerby.com/en/articles/8708338-explore-accounts#h_079d120056), Cerby performs its best attempt to autofill credentials based on the available account details. The credentials saved in the Cerby workspace must be correct for successful automated logins.

* * *

## B

### Bearer token

It is a security token with a limited lifespan that Cerby requires to authenticate users with its server or API. It comprises a string of characters that is typically passed in the request headers of HTTP requests or in the login command for the [Cerby CLI](glossary.md#cerby-command-line-interface-(cli)).

This token determines the endpoints and data you can access depending on your workspace and item role.

### Business hub

It is an integration that enables users to connect their seat-based and paid social apps to Cerby, aiming to centrally manage users and [assets](glossary.md#asset) from Cerby.

Business hubs (formerly tenants or Apps) are connected to the collaboration spaces of your apps (workspaces, teams, or dashboards) via API- or automation-based integrations. To perform user and asset management tasks, the Cerby bot typically uses a service account with an admin role.

For more information about business hubs and the user and asset management tasks you can perform, read the article [Explore Business hubs](https://help.cerby.com/en/articles/6831152-explore-apps).

### Business ID

It is the unique identifier assigned to the collaboration space (workspace, team, dashboard, business manager, or business center) of a seat-based or paid social app. Depending on the app, this identifier may have different names, such as organization or team ID.

Providing this value is crucial when connecting a [business hub](glossary.md#business-hub) to Cerby.

* * *

## C

### Cerby browser extension

It is a [client app](glossary.md#cerby-client-app) designed to complement the functionalities of the Cerby web app, with features such as automated login, password generation, and account autosave. The extension has a dashboard where users can view the details of their accounts, secrets, business hubs, collections, and subcollections.

### Cerby client app

It is any of the apps with which the users interact for accessing the Cerby platform, their workspace, and the items saved within the workspace. Currently, Cerby has the following client apps available: [web app](glossary.md#cerby-web-app), [browser extension](glossary.md#cerby-browser-extension), [mobile app](glossary.md#cerby-mobile-app), and [CLI](glossary.md#cerby-command-line-interface-(cli)).

### Cerby Command Line Interface (CLI)

It is a [client app](glossary.md#cerby-client-app) that enables users to interact with their accounts and secrets via the command line interface on Linux, Windows, and MacOS. It simplifies command execution, provides enhanced data retrieval from secrets and accounts, and supports the automation of repetitive tasks for efficient data management.

For more information about this client app, read the article [Explore the Cerby CLI](https://help.cerby.com/en/articles/9118683-explore-the-cerby-cli).

### Cerby mobile app

It is a [client app](glossary.md#cerby-client-app) designed to let users manage their accounts, secrets, business hubs, collections, subcollections, and trusted devices directly from their phone. This app supports item management, facilitates MFA setup, and ensures native secure access to sensitive data.

Additionally, the push notifications in the Cerby mobile app serve as an identity confirmation method for multi-factor authentication (MFA). For more information about this client app, read the article [Explore the Cerby mobile app](https://help.cerby.com/en/articles/9715502-explore-the-cerby-mobile-app).

### Cerby platform

It is how Cerby refers to its solution as a whole. The platform comprises the [client apps](glossary.md#cerby-client-app) that work together to provide users with the best experience.

### Cerby user account

It is the digital identity created in Cerby for each user that enables them to access the Cerby platform and their workspace. When an [identity provider (IdP)](glossary.md#identity-provider-(idp)) is configured for a Cerby workspace to leverage single sign-on (SSO) authentication and user provisioning, Cerby user accounts are associated with the users’ identities in their corporate directory.

### Cerby web app

It is a [client app](glossary.md#cerby-client-app) that enables users to securely create, manage, and share their accounts, secrets, collections, subcollections, business hubs, and assets with other workspace members, teams, and external users.

The Cerby web app is the central management interface for workspace **Admins** , **Super Admins** , and **Owners**. They can view all user activity, automation reports, billable accounts, and manage users, among other tasks and actions.

### Cloud encryption

It is one of Cerby's cryptographic strategies to protect user data stored in cloud-based vaults. Encryption keys are generated, stored, and managed in the cloud, and Cerby fully manages the key management system and recovery procedures.

For more information, read the article [How Cerby protects your data with cloud and local encryption](https://help.cerby.com/en/articles/8376548-how-cerby-protects-your-data-with-cloud-and-local-encryption).

### Collection

It is a feature that enables users to group the items they have saved in their workspace: accounts, secrets, business hubs, assets, and subcollections. The goal is to let users organize their items and share them in bulk with other workspace members, teams, and external users.

Only item **Owners** can add their items to a collection, and when they share it, they can assign the following roles to other members, teams, and guest users: [collection Owner](glossary.md#collection-owner) or **[Collaborator](glossary.md#collection-collaborator)**. For more information about this feature, read the article [Explore Collections](https://help.cerby.com/en/articles/8981886-explore-collections).

### Collection card

It is a graphical component in the UI of the Cerby web app, browser extension, and mobile app that consists of card-type buttons representing the collections created in Cerby.

On the Cerby web app, these cards can be expanded, whereas on the browser extension and mobile app, they redirect users to a new screen to view all the items and navigate through its nested subcollections.

### Collection details page or screen

It is a section in the UI where the details and configuration of a collection are centralized. You can access the collection details page or screen using the Cerby web app or mobile app.

Collection **Owners** can edit the details of a collection and update its configuration through the collection details page or screen. Account **Collaborators** can only view the collection details and all the nested items and subcollections.

### Collection Collaborator

It is a role in Cerby with basic permissions to view a collection and the items within. This role is inherited bottom-down on all the nested accounts, secrets, business hubs, assets, and subcollections.

### Collection Owner

It is a role in Cerby with permissions to manage a collection, including its settings and shared access for other members, teams, or guest users. This role is inherited bottom-down on all the nested accounts, secrets, business hubs, assets, and subcollections.

Collection **Owners** can assign the **Owner** or **Collaborator** role to workspace members, teams, or guest users when sharing their collections. For the detailed permissions of this role, read the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

### Context menu

It is the pop-up menu of a web browser that appears when a user right-clicks on a specific element within a web page or application. It provides quick access to actions relevant to the selected element or the current state of the UI.

When right-clicking on an input field of a login or signup page, users can select the **Open Cerby** option to show the Cerby icon of the inline menu if it was not displayed. Also, you can select to enable or disable Cerby for a specific field.

* * *

## D

### Dark mode

It is an appearance preference on the Cerby mobile app that changes the UI from light to dark shades. Dark mode is designed to reduce eye strain in low-light conditions, improve readability, and potentially extend battery life. Cerby inherits this setting from the mobile phone on Android, but users can customize it on iOS independently from their phone settings.

For more information, read the article [Change the theme of the Cerby mobile app](https://help.cerby.com/en/articles/9737399-change-the-theme-of-the-cerby-mobile-app).

### Dashboard

It is the graphical interface of the Cerby web app, browser extension, and mobile app that integrates information about users, accounts, secrets, vaults, business hubs, automated tasks, trusted devices, configuration, and services.

###

## Dev Tools

It is a Cerby module available per request for workspace **Admins** ,**Super Admins** , and **Owners** that enables developers to obtain a bearer token and download the [Cerby CLI](glossary.md#cerby-command-line-interface-(cli)) client app.

### Distribution list

It is a list of email addresses grouped to facilitate forwarding emails from Cerby’s Shared Inbox to multiple recipients simultaneously, streamlining access to verification codes sent to Cerby-managed email addresses or phone numbers.

* * *

## E

### Encryption scheme

It is a method used to encode information, ensuring that it remains confidential and secure from unauthorized access. It involves using algorithms and cryptographic keys to transform plaintext data into ciphertext, which can only be deciphered by trusted devices with the appropriate decryption key.

For more information, read the article [How Cerby protects your data with cloud and local encryption](https://help.cerby.com/en/articles/8376548-how-cerby-protects-your-data-with-cloud-and-local-encryption).

### End-to-end encryption

It is one of Cerby's techniques for guaranteeing data remains encrypted throughout its lifecycle, from origin to destination, preventing unauthorized access even during transit.

* * *

## F

### Flagged account

It is an app’s user account that has been temporarily or permanently restricted due to excessive failed login attempts within a specified timeframe.

* * *

## G

* * *

## H

* * *

## I

### Identity provider (IdP)

It is a system entity that creates, stores, maintains, and manages identity information for users, services, or systems. It provides authentication services to other service providers within a federation or distributed network. Cerby connects with the IDP of an organization to retrieve information from its directory and centralize the user provisioning and deprovisioning processes.

### Import report

It is a detailed summary provided by the Cerby platform after data has been imported from another system. This report is organized into a user-friendly view that includes a progress bar and several sections detailing the status of imported items.

### In-context alerts

It is a notification or warning displayed directly within the user's current workflow or interface. It provides immediate and relevant information without requiring users to navigate away from their current task.

### Inline menu

It is a context-sensitive interface of the Cerby browser extension that appears within input fields in a web page. It enables users to perform immediate actions relative to the field they are interacting with, such as autofilling login credentials, generating secure passwords, or suggesting an email address.

* * *

## J

* * *

## K

* * *

## L

### Local encryption

It is one of Cerby's cryptographic strategies where data encryption and decryption processes are carried out locally on the user's device rather than on a central server or in the cloud.

For more information, read the article [How Cerby protects your data with cloud and local encryption](https://help.cerby.com/en/articles/8376548-how-cerby-protects-your-data-with-cloud-and-local-encryption).

### Local user

It is a user that authenticates directly into Cerby with a username and password managed by Cerby. This process is as opposed to authenticating into a configured [IdP](glossary.md#identity-provider-(idp)) such as Okta.

### Local workspace

It is an environment in which Cerby directly manages users' identities and authentication rather than utilizing an external [IdP](glossary.md#identity-provider-(idp)), such as Okta or Entra ID, for user provisioning. Users are added to a workspace through direct invitations sent to their email addresses from the **All members** page.

For more information, read the article [How to create and configure a local user workspace](https://help.cerby.com/en/articles/8011381-how-to-create-and-configure-a-local-user-workspace).

* * *

## M

### Migration ID

It is the unique identifier in the Import report used to track the status of a migration using the [Password Manager Importer](https://help.cerby.com/en/articles/7217206-what-is-the-password-manager-importer). You can share the Migration ID with the Cerby Customer Support team for troubleshooting. You also receive an email with this ID.

### Multi-factor authentication (MFA)

It is a security process that involves two identification points to authenticate users. The first factor is a password and the second is a verification code sent to different verification methods, such as SMS, email, or mobile application. MFA is configured for the app accounts added on Cerby that support this authentication method.

* * *

## N

* * *

## O

### One-time password (OTP)

It is a password valid for only one login session or transaction on a computer system or other digital device. OTP is also known as a dynamic password or authentication code.

### OpenID Connect (OIDC)

It is an authentication protocol that enables services and applications to verify the identity of a user using an ID token.

* * *

## P

### Permission

It consists of the specific actions that users are enabled to perform in a system, solution, or application. At Cerby, permissions are determined inside the code and work at a workspace and account level.

* * *

## Q

* * *

## R

### Role

It consists of a set of permissions that represent the tasks, activities, or functions that users can perform. Users can have none, one, or multiple (in some cases overlapping) roles.

Cerby manages roles at a workspace and account level, and roles are also inherited from the configuration of your apps.

The following are the different roles in Cerby depending on your access level:

  * Workspace-level roles
    * [Workspace Owner](glossary.md#workspace-owner)
    * [Workspace Admin](glossary.md#workspace-admin)
    * [Workspace User](glossary.md#workspace-user)
  * Account-level roles
    * [Account Owner](glossary.md#h_1a76212f39)
    * [Account Collaborator](glossary.md#h_b88bf91beb)

    **NOTE:** Regardless of their role, all users can add accounts to a workspace and then introduce the account roles, and they can only share the accounts they are owners of. Also, all users can create collections.

For the detailed permissions of each role, read the [Workspace-level roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles#h_e203df23da) and [Item-level roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles#h_50f9a80386) sections in the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

* * *

## S

### Security Assertion Markup Language (SAML)

It is a standard that enables [IdPs](glossary.md#identity-provider-(idp)) and service providers to exchange data to authenticate and authorize users. With this standard, service providers can enable SSO processes for users across applications that support SAML.

### Service provider

It is an entity that provides services, solutions, or applications to end users and organizations. For example, Twitter, Mailchimp, or Instagram.

### Shared Inbox

It is a feature that enables you and your team members to receive and store the messages sent to the phone numbers and email addresses provisioned and managed by Cerby and configured in your app accounts.

Cerby leverages the **Shared Inbox** to provide you with automatic logging-in processes to your accounts, including verification codes for [MFA](glossary.md#multi-factor-authentication-(mfa)).

### Single sign-on (SSO)

It is an authentication method that enables users to log in to multiple applications or services using a single set of credentials.

### System for Cross-Domain Identity Management (SCIM)

It is a standard for automating the interchange of user identity information between IDPs and service providers. At Cerby, this standard enables automation for provisioning and deprovisioning users.

* * *

## T

## U

* * *

## V

### Verification code

It is a security code provided by authenticators when users try to complete tasks (such as recovering a password or turning on MFA) or logging in to a service or application. It ensures that only authorized users gain access or perform the actions. At Cerby, verification codes are sent to the mobile application.

### Voice over Internet Protocol (VoIP)

It is a communication protocol that enables users to access phone services through IP. At Cerby, VoIP is commonly used to deliver verification messages for user authentication.

* * *

## W

### Workspace

It is the environment in which organizations and users can access a set of shared accounts to log in to other apps. For example, an organization can leverage a Cerby workspace to log in to their social media accounts and manage the overall security of these accounts.

Through a Cerby workspace, organizations and users can also manage their accounts and perform the following actions:

  * Manage user permissions.
  * Manage app accounts.
  * Onboard multi-factor authentication (MFA) and rotate passwords for accounts.
  * Manage user provisioning and deprovisioning.
  * Configure authentication with an identity provider (IDP).
  * Retrieve analytics for account usage and user activity.

Organizations may have one or multiple workspaces depending on their needs. Though usually, one organization has one workspace.

Currently, you can only create a workspace from an invitation sent by the Cerby team from our official email address, [help@cerby.com](mailto:help@cerby.com). After creating your workspace, its name is displayed and identified as follows **< workspace name>.cerby.com**.

### Workspace Admin

It is a workspace-level role with permissions to manage accounts and configure their security and also manage users within Cerby, including their permission level. For the detailed permissions of this role, read the [Workspace-level roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles#h_e203df23da) section in the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

### Workspace Owner

It is a workspace-level role with permissions to perform the same actions as **Workspace** **Admins** , as well as configure the IDP settings and create and configure a workspace. For the detailed permissions of this role, read the [Workspace-level roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles#h_e203df23da) section in the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

### Workspace User

It is a workspace-level role with basic permissions to log in to the accounts registered in Cerby, see other users from their organization, and configure the security of accounts. For the detailed permissions of this role, read the [Workspace-level roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles#h_e203df23da) section in the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

* * *

## X

* * *

## Y

* * *

## Z

* * *
