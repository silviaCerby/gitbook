---
description: "This article describes how Cerby provides a comprehensive solution for protecting your saved passwords."
intercom_id: 13115952
---

# How Cerby protects your passwords

Cerby helps organizations secure access to applications that are traditionally difficult to manage through standard identity systems. Because passwords are often the most sensitive piece of access data in these applications, Cerby provides a multi-layered protection model designed to safeguard them throughout their lifecycle.

Cerby’s password protection strategy is built on three core principles:

* **Strong encryption** : All sensitive information stored in Cerby is protected by industry-standard encryption.
* **Granular access controls** : Organizations can define who can access or use password data.
* **Operational security features** : Automated and user-initiated capabilities help maintain healthy password hygiene.

These principles work together to help secure access to applications where federated identity is not available.

* * *

## Encryption and data protection

Cerby uses modern encryption practices to protect the sensitive information stored in your workspace. Passwords and secrets are encrypted before they are stored, and only authorized users and devices can access them based on your organization’s configuration and policies.

Cerby supports multiple encryption schemes, ensuring that all sensitive data is encrypted both at rest and in transit. Only authorized, authenticated users can access decrypted information.

This encryption strategy enables secure storage across the Cerby platform, including:

  * Saved account passwords
  * Time-based one-time passwords (TOTPs)
  * Backup codes
  * Secrets
  * Optional secret attachments

Users maintain access to their sensitive information based on the devices and security configurations approved by their workspace administrators.

* * *

## Access control with roles

Cerby uses a role-based access control (RBAC) system to define user permissions for shared accounts. Each role determines what a user can do, ranging from managing account access to viewing sensitive information, such as passwords.

Users who add accounts to Cerby are automatically granted the account Owner role. When they share their accounts with other users for collaboration purposes, they can grant them one of the following roles:

  * **Owner:** Users with this role can share accounts, manage access and account configuration, and view passwords through the user interface (UI) and API responses.
  * **Collaborator:** Users with this role can only view passwords through API responses for account login with Cerby; viewing passwords through the UI is restricted.

For more information about roles and permissions, read the article[ How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

* * *

## Automated password management

With Cerby, organizations can update their passwords as part of their regular access hygiene policies, enabling the following:

  * Reduce the risk of unauthorized access.
  * Ensure access stays aligned with company policy.
  * Maintain consistency across multiple shared accounts.

Administrators and users with appropriate permissions can also perform updates as needed from the Cerby interface.

The following are different ways in which you can leverage automated password rotations:

  * **One-click on-demand experience in the Cerby web app:** For more information, read the article [Rotate an account password automatically](https://help.cerby.com/en/articles/13512602-rotate-an-account-password-automatically).
  * **Password rotation policies on a set schedule or after user login events:** For more information, read the article: [Create a password policy](https://help.cerby.com/en/articles/11466694-create-a-password-policy).
  * **Universal Logout triggered from your IdP and extended to Cerby, or triggered only from Cerby:** For more information, read the articles [Trigger Okta Universal Logout and extend it to Cerby](https://help.cerby.com/en/articles/10495624-trigger-okta-universal-logout-and-extend-it-to-cerby) and [Trigger Cerby Universal Logout](https://help.cerby.com/en/articles/10496392-trigger-cerby-universal-logout).
  * User deprovisioning via SCIM events from your IdP.
  * **Accounts stored in local vaults:** For more information, read the article [Run automated tasks for accounts in local vaults](https://help.cerby.com/en/articles/11682782-run-automated-tasks-for-accounts-in-local-vaults).
* * *

## Secure password generation

Cerby provides tools to help generate new, strong passwords based on customizable strength requirements. The [password generator](https://help.cerby.com/en/articles/8487177-explore-the-password-generator), available in the Cerby web app and browser extension, helps users set passwords that meet internal or external standards, supporting a more secure posture across unmanaged apps.

In automated password rotations, Cerby always provides passwords as robust as possible, in line with your app's recommendations.

* * *

## Configurable viewing restrictions

Cerby enables organizations to customize whether password values can be displayed in the user interface (UI) to specific users. This characteristic ensures that sensitive data is protected in accordance with your internal policies.

The following are some examples of configurable restrictions:

  * Whether **Collaborators** may view a password directly.
  * Whether users can copy a password from the Cerby client apps.
  * Whether password values can be shown in specific interfaces.
* * *

## Trusted devices and secure access

Cerby supports device-level verification to ensure that password access is tied to trusted devices and authenticated user sessions. This support adds a layer of protection and helps keep sensitive information secure across Cerby’s client surfaces.
