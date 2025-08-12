# How Cerby protects your passwords

**Description:** This article describes how Cerby provides a comprehensive solution for protecting your saved passwords.

As an identity, access, and password management platform for disconnected
applications, data protection is vital for Cerby. We know passwords are
essential assets of your organization, so we have built a multi-layered and
comprehensive solution to protect them.  
  
This article describes Cerby’s approach to protecting the passwords of the
accounts you and your colleagues use daily to log in to their applications.

* * *

# System and architectural protection

As in any password management platform, data encryption is at the core of
Cerby and is part of the system and architectural protection for passwords.
With this security method, only authorized users with access to the
corresponding decryption keys can decrypt a password.

Whenever an organization creates a new Cerby workspace, the Cerby platform
automatically generates a default cloud vault and its corresponding encryption
keys, which are stored in the database and encrypted with the workspace KMS
(AWS Key Management Service) key.

This vault is where users save their sensitive data (accounts and secrets),
and Cerby offers the following vault encryption schemes, inclusive of the
option referenced above:

  * **Cloud encryption:** Cerby's servers store the decryption keys and the encrypted data, and the unique encryption keys are generated in the server and secured by AWS KMS.

  * **Local encryption:** Cerby's servers store the encrypted data, and the vault data encryption keys are stored exclusively on registered trusted devices. Decryption happens decentralized on such devices. This encryption scheme leverages a Zero Knowledge architecture.

The choice between cloud and local encryption schemes depends on customer
security requirements and preferences. For more information, read the article
[How Cerby protects your data with cloud and local
encryption](https://help.cerby.com/en/articles/8376548-how-cerby-protects-
your-data-with-cloud-and-local-encryption).

* * *

# Feature-based protection

On top of the system and architectural protection, Cerby offers the following
features that enable organizations and end users to protect their passwords
proactively:

  * Automated password rotations

  * Generation of secure passwords

  * Restrictions on view permissions

  * [Coming soon] Audit analytics for password update attempts

The following sections describe each feature.

## **Automated password rotations**

Cerby’s key differentiator is automation, and this approach to security is
present in our strategy to protect your passwords: automated password
rotations are available for multiple [managed
accounts](https://help.cerby.com/en/articles/8708338-explore-
accounts#h_f0a859b407),

IT admins can set workspace policies to rotate passwords periodically via
automation. Also, Cerby can trigger this automated task based on user
deprovisioning or user account deactivation events from an identity provider
(IdP), such as Okta or Entra ID.

With automated and regular password rotations by policy, organizations achieve
the following:

  * Minimize the risk of unauthorized access.

  * Ensure users have to use Cerby as the front door to access their accounts.

  * Alert if the password status has changed to not being managed by Cerby.

End users can also trigger automated password rotations manually with a single
click in the Cerby web app.

It’s worth mentioning that, during automated password rotation, Cerby
generates and sets secure passwords following the app’s strength rules.

For more information about automated tasks on managed accounts, read the
article [Explore the supported automated tasks for managed
accounts](https://help.cerby.com/en/articles/6263064-explore-the-supported-
automated-tasks-for-your-managed-accounts).

## **Generation of secure passwords**

As mentioned, Cerby generates and sets secure passwords when performing
automated password rotations. However, you can also use the password generator
in the Cerby browser extension to generate a secure password with the
following customizable strength rules:

  * Length

  * Uppercase letters

  * Lowercase letters

  * Digits

  * Symbols 

For more information about this feature, read the article [Explore the
Password Generator](https://help.cerby.com/en/articles/8487177-explore-the-
password-generator).

## **Restrictions on view permissions**

To protect access to a password without affecting productivity, you can set
restrictions on view permissions for shared accounts. With this feature, users
with the **Collaborator** role on an account can view or not the password
through any of the Cerby client apps (web app, browser extension, and mobile
app).

The following are the restriction types, depending on how they are enabled:

  * Customized restrictions for all workspace users

  * Manual restrictions on individual accounts

The following sections describe each restriction type.

### Customized restrictions for all workspace users

The Cerby Technical Support team can customize restrictions for all workspace
users. Based on customers’ needs and security policies, Cerby can enable or
disable features for viewing and hiding passwords.

In the most restrictive configuration, Cerby limits a user's ability to view
the password across all interfaces, requiring the user to always use Cerby to
log in to their accounts.

The following are the features Cerby can enable or disable for a workspace:

  * Display the **Collaborators can view the password for this account** switch in the account details page of the Cerby web app. By activating or deactivating this switch, account **Owners** decide whether to hide or show passwords to account **Collaborators** who have shared access to an account. This decision impacts all client apps.

  * View and copy an account password using the Cerby browser extension inline menu. This feature is enabled only if an account **Owner** activates the **Collaborators can view the password for this account** switch on the account details page.

  * Display the **Copy** icon in the account details screen using the Cerby mobile app. This feature prevents users from copying passwords; therefore, they must use the autofill service of their mobile phone’s operating system.

  * View and copy an account password in the account details screen using the Cerby browser extension popup and inline menu. This feature prevents users from viewing and copying passwords; therefore, they have to click the **Fill** button to enter the password in the corresponding input field.

You can contact the Cerby Technical Support team via email at
[support@cerby.com](mailto:support@cerby.com) or through the help chat to
request any of the features to be enabled or disabled.

### Manual restrictions on individual accounts

Account **Owners** can set manual restrictions on individual accounts for
viewing or hiding passwords. The Cerby Technical Support team must enable the
display of the **Collaborators can view the password for this account** switch
on the account details page of the Cerby web app.

As mentioned above, by activating or deactivating this switch, account
**Owners** decide whether to hide or show passwords to account
**Collaborators** who have shared access to an account.

This restriction is displayed in the **Emergency controls** expandable section
of the account details page. When activated, account **Collaborators** can
view the account password across all Cerby client apps.

## **[Coming soon] Audit analytics for password update attempts**

Cerby is building a feature to suggest users not update their account
passwords. Cerby will collect analytics data about password update attempts or
if the user did change the password.

