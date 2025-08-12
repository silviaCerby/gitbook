# Explore Vaults

**Description:** This article describes the benefits of the Vaults feature to ensure the privacy and security of your stored data.

At Cerby, vaults are protected spaces for storing and managing your account
data and sensitive information (secrets). They provide an additional layer of
security by implementing encryption and access controls to ensure that only
authorized users can access the stored data.

When you join Cerby and create a new workspace, the Cerby platform
automatically generates a default cloud vault and its corresponding encryption
keys. However, you can create additional local vaults to leverage a Zero
Knowledge architecture. The following are the characteristics of each vault
strategy:

  * **Cloud vault:** Cerby stores and manages the encryption keys, and all automated tasks are supported.   
**NOTE:** By default, Cerby uses the AWS KMS service, but you can also set up
an [Azure Key vault
integration](https://help.cerby.com/en/articles/9189942-set-up-an-azure-key-
vault-integration).

  * **Local vault:** Users hold the encryption keys in trusted devices, which are not accessible to Cerby. This vault strategy has limited automated tasks.

For more information about the vault strategy or encryption, read the article
[How Cerby protects your data with cloud and local
encryption](https://help.cerby.com/en/articles/8376548-how-cerby-protects-
your-data-with-cloud-and-local-encryption).

* * *

# User visibility

When creating a vault, you can choose its visibility and if you want it to be
the default vault. The visibility options are the following:

  * **User visibility:** The vault is only accessible to specific users via an access share. 

  * **Workspace visibility:** Vault access is automatically shared with all the workspace users.

**IMPORTANT:** Currently, Cerby only supports vaults with workspace
visibility; in a future release, user visibility will be supported.  
---  
  
* * *

# Default vault

Selecting a default vault makes it the predetermined vault when adding
accounts and secrets. It is also where all the items are stored when
transferring them to Cerby via the [Password Manager
Importer](https://help.cerby.com/en/articles/7175132-how-to-use-the-password-
manager-importer).

* * *

# Recovery key

After creating a vault, you can generate a recovery key. With this key, you
can regain access to encrypted vaults if all the devices with the private keys
are lost or unavailable. For more information about recovery keys, read the
article [How to generate and manage the recovery keys for your
vault](https://help.cerby.com/en/articles/8376680-how-to-generate-and-manage-
the-recovery-keys-for-your-vault).

* * *

# Trusted sessions on devices

Setting up a trusted device is a requirement for creating a vault. With this
setup, you ensure that all interactions with the Cerby platform come from
authorized devices that meet corporate security standards.

In local vaults, trusted sessions on any of your devices are vital because
they hold the corresponding encryption and decryption keys to access and
decrypt the data of your accounts and secrets stored in your vaults. Also,
encryption and decryption operations happen decentralized on such devices. For
more information about trusted devices, read the article [Set up trusted
sessions on your devices](https://help.cerby.com/en/articles/8142370-set-up-
trusted-sessions-on-your-devices).

When you no longer need a vault, you can disable it. With this status, users
and teams with shared access to the vault cannot add more items (accounts or
secrets). Still, the existing items remain active and accessible to them.

* * *

# Related articles

The following articles contain more information about how to create and manage
vaults:

  * Create a vault

  * Manage vaults in a workspace

