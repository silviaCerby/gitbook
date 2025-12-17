---
description: "This article describes the benefits of the Vaults feature to ensure the privacy and security of your stored data."
intercom_id: 10065157
---

# Explore Vaults

At Cerby, vaults are protected spaces for storing and managing your account data and sensitive information (secrets). They provide an additional layer of security by implementing encryption and access controls, ensuring that only authorized users can access the stored data.

You can create additional local vaults to leverage a Zero-Knowledge architecture. The following are the characteristics of Cerby's vault strategy:

  * **Cloud vault:** Cerby stores and manages the encryption keys, and all automated tasks are supported.
  * **Local vault:** Users hold the encryption keys in trusted devices, which are not accessible to Cerby. This vault strategy has limited automated tasks.
* * *

## User visibility

When creating a vault, you can choose its visibility and determine whether it should be the default vault. The visibility options are the following:

* **User visibility:** The vault is only accessible to specific users via an access share.
* **Workspace visibility:** Vault access is automatically shared with all the workspace users.

**IMPORTANT:** Currently, Cerby only supports vaults with workspace visibility; in a future release, user visibility will be supported.
---

* * *

## Default vault

Selecting a default vault makes it the predetermined vault when adding accounts and secrets. It is also where all the items are stored when transferring them to Cerby via the [Password Manager Importer](https://cerby-test.gitbook.io/cerby-test/management/credential-management/item-importer/migrate-from-lastpass-to-cerby).

* * *

## Recovery key

After creating a vault, you can generate a recovery key. With this key, you can regain access to encrypted vaults if all the devices with the private keys are lost or unavailable. For more information about recovery keys, read the article [How to generate and manage the recovery keys for your vault](https://cerby-test.gitbook.io/cerby-test/management/credential-management/vaults/generate-and-manage-the-recovery-keys-for-your-vault).

* * *

## Trusted sessions on devices

Setting up a trusted device is a requirement for creating a vault. With this setup, you ensure that all interactions with the Cerby platform come from authorized devices that meet corporate security standards.

In local vaults, trusted sessions on any of your devices are vital because they hold the corresponding encryption and decryption keys to access and decrypt the data of your accounts and secrets stored in your vaults. Also, encryption and decryption operations happen decentralized on such devices. For more information about trusted devices, read the article [Set up trusted sessions on your devices](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/trusted-devices/set-up-trusted-sessions-on-your-devices).

When you no longer need a vault, you can disable it. With this status, users and teams with shared access to the vault cannot add more items (accounts or secrets). Still, the existing items remain active and accessible to them.
