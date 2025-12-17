---
description: This article describes how Cerby provides a comprehensive solution for protecting your saved passwords.
intercom_id: 10008672
---

# How Cerby protects your passwords

As an identity, access, and password management platform for disconnected applications, data protection is vital for Cerby. We know passwords are essential assets of your organization, so we have built a multi-layered and comprehensive solution to protect them.

This article describes Cerby’s approach to protecting the passwords of the accounts you and your colleagues share and use daily to log in to their applications.

* * *

## System and architectural protection

As in any password management platform, data encryption is at the core of Cerby and is part of the system and architectural protection for passwords. With this security method, only authorized users with access to the corresponding decryption keys can decrypt a password.

Whenever an organization creates a new Cerby workspace, the Cerby platform automatically generates a default cloud vault and its corresponding encryption keys, which are stored in the database and encrypted with the workspace KMS (AWS Key Management Service) key.

This vault is where users save their sensitive data (accounts and secrets), and Cerby offers the following vault encryption schemes, inclusive of the option referenced above:

  * **Cloud encryption:** Cerby's servers store the decryption keys and the encrypted data, and the unique encryption keys are generated in the server and secured by AWS KMS.
  * **Local encryption:** Cerby's servers store the encrypted data, and the vault data encryption keys are stored exclusively on registered trusted devices. Decryption happens decentralized on such devices. This encryption scheme leverages a Zero Knowledge architecture.

The choice between cloud and local encryption schemes depends on customer security requirements and preferences. For more information, read the article [How Cerby protects your data with cloud and local encryption](https://cerby-test.gitbook.io/cerby-test/management/credential-management/vaults/how-cerby-protects-your-data-with-cloud-and-local-encryption).

* * *

## Role-based protection

Cerby uses a role-based access control (RBAC) system to define user permissions for shared accounts. Each role determines what a user can do, from managing account access to viewing sensitive information like passwords.

Users who add accounts to Cerby are automatically granted the account **Owner** role. When they share their accounts with other users for collaboration purposes, they can grant them one of the following roles:

  * **Owner:** Users with this role can share accounts, manage access and account configuration, and view passwords through the user interface (UI) and API responses.
  * **Collaborator:** Users with this role can only view passwords through API responses for account login with Cerby; viewing passwords through the UI is restricted.

For more information about roles and permissions, read the article [How Cerby manages roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles).

* * *

## Feature-based protection

On top of the system, architectural, and role-based protections, Cerby has the following features to enable organizations and end users to protect their passwords proactively:

  * [Automated password rotations](how-cerby-protects-your-passwords.md#id-automated-password-rotations)
  * [Generation of secure passwords](how-cerby-protects-your-passwords.md#id-generation-of-secure-passwords)
  * [Restrictions on password view capabilities](how-cerby-protects-your-passwords.md#id-restrictions-on-password-view-capabilities)
  * [[Coming soon] Audit analytics for password update attempts](#id-coming-soon-audit-analytics-for-password-update-attempts)

The following sections describe each feature.

### Automated password rotations

Cerby’s key differentiator is automation, and this approach to security is present in our strategy to protect your passwords: automated password rotations are available for multiple [managed accounts](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-accounts),

IT admins can set workspace policies to rotate passwords periodically via automation. Also, Cerby can trigger this automated task based on user deprovisioning or user account deactivation events from an identity provider (IdP), such as Okta or Entra ID.

With automated and regular password rotations by policy, organizations achieve the following:

  * Minimize the risk of unauthorized access.
  * Ensure users have to use Cerby as the front door to access their accounts.
  * Alert if the password status has changed to not being managed by Cerby.

End users can also trigger automated password rotations manually with a single click in the Cerby web app.

It’s worth mentioning that, during automated password rotation, Cerby generates and sets secure passwords following the app’s strength rules.

### Generation of secure passwords

As mentioned, Cerby generates and sets secure passwords when performing automated password rotations. However, you can also use the password generator in the Cerby browser extension to generate a secure password with the following customizable strength rules:

  * Length
  * Uppercase letters
  * Lowercase letters
  * Digits
  * Symbols

For more information about this feature, read the article [Explore the Password Generator](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-the-password-generator).

### Restrictions on password view capabilities

Complementary to the role-based protection for your passwords, you can customize the restrictions to view passwords for users with the account **Collaborator** role.

According to Cerby’s RBAC system, account **Collaborators** are restricted to view passwords through the UI using any of the three Cerby client apps (web app, browser extension, and mobile app). They only have access to passwords through API responses to enable account login through Cerby.

However, based on your needs and security policies, your organization can request Cerby to grant account **Collaborators** access to view passwords through the UI. The following are the features our Technical Support team can enable or disable for a workspace:

  * Display the **Collaborators can view the password for this account** switch in the account details page of the Cerby web app. By activating or deactivating this switch, account **Owners** decide whether to hide or show passwords to account **Collaborators** who have shared access to an account. This decision impacts all client apps.
  * View and copy an account password using the Cerby browser extension inline menu. This feature is enabled only if an account **Owner** activates the **Collaborators can view the password for this account** switch on the account details page.
  * Display the **Copy** icon in the account details screen using the Cerby mobile app. This feature prevents users from copying passwords; therefore, they must use the autofill service of their mobile phone’s operating system.
  * View and copy an account password in the account details screen using the Cerby browser extension popup and inline menu. This feature prevents users from viewing and copying passwords; therefore, they have to click the **Fill** button to enter the password in the corresponding input field.

You can contact the Cerby Technical Support team via email at [support@cerby.com](mailto:support@cerby.com) or through the help chat to request any of the features to be enabled or disabled.

### [Coming soon] Audit analytics for password update attempts

Cerby is building a feature to suggest users not update their account passwords. Cerby will collect analytics data about password update attempts or if the user did change the password.
