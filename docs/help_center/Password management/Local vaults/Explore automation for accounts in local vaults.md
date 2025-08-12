# Explore automation for accounts in local vaults

**Description:** This article describes how automation works for your accounts in local vaults while ensuring zero-knowledge principles.

With Cerby, you can now perform automated tasks even for the accounts you have
saved in vaults with local encryption.

Automation was previously exclusive to workspaces with cloud vaults,
leveraging server-side tasks performed by the Cerby bot. Now, this capability
extends to accounts in local vaults, combining robust security with seamless
efficiency to elevate your user experience.

Cerby implements the Zero Knowledge principles for accounts in local vaults
through features such as [trusted sessions on your
devices](https://help.cerby.com/en/articles/8142370-set-up-trusted-sessions-
on-your-devices) and [local encryption for
vaults](https://help.cerby.com/en/articles/8376548-how-cerby-protects-your-
data-with-cloud-and-local-encryption) with workspace and user visibility. The
goal is to minimize the blast radius of potential attacks and safeguard
sensitive information.

[This article](https://help.cerby.com/en/articles/6263064-explore-the-
supported-automated-tasks-for-your-managed-accounts) lists the automated tasks
Cerby can perform for your managed accounts with cloud encryption. The
following are the automated tasks supported for accounts in local vaults:

  * Rotate passwords 

  * Turn on multi-factor authentication (MFA) 

* * *

# Learn how automation works for accounts in local vaults

When you join Cerby and create a new workspace, the Cerby platform
automatically generates a default cloud vault and its corresponding encryption
keys. However, you can create additional local vaults to leverage a Zero
Knowledge architecture.

With the automated tasks supported in local vaults, you enhance security and
ensure that exposure is limited and managed effectively, even during an
attack.

The automated tasks for accounts in local vaults are executed as follows:

  1. Your account is stored securely in a local vault.

  2. When you trigger the automated task to rotate a password or turn on MFA, Cerby prompts you to confirm whether it's okay to temporarily use a cloud vault.

  3. When you confirm this action, your local vault encryption key is _temporarily_ shared with the cloud vault.

  4. The Cerby bot performs the automated task using the account information from the cloud vault.

  5. When the automated task is complete, the Cerby bot sends the final status (success or failure) back to the Cerby platform.

  6. The Cerby platform then triggers the removal of the vault encryption key from the cloud vault, ensuring that your account's secrets are only stored locally again.

With the previous flow, Cerby guarantees the following:

  * Your account information is temporarily shared with the cloud vault only for the duration of the automated task.

  * Your key is not exposed to Cerby because we follow the Zero Knowledge principles at all times. Your information is encrypted, and we can’t access your encryption keys. The Cerby bot handles the entire process automatically and securely.

  * After completing the automated task, the cloud vault is cleaned up, and your information remains safe in your local vault.

* * *

# Related articles

The following articles contain more information about automation for accounts
in local vaults:

  * [Manage local vault assignments for an account](https://help.cerby.com/en/articles/11682768-manage-local-vault-assignments-for-an-account)

  * [Run automated tasks for accounts in local vaults](https://help.cerby.com/en/articles/11682782-run-automated-tasks-for-accounts-in-local-vaults)

