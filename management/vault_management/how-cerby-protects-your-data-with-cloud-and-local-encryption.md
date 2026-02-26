---
description: "This article describes how Cerby supports vaults with cloud and local encryption to protect your account data and secrets."
intercom_id: 8376548
hidden: true
noIndex: true
---

# How Cerby protects your data with cloud and local encryption

Securing and managing access to sensitive data are crucial for organizations of all sizes, especially if they use nonfederated applications for their day-to-day activities.

As an identity and access management platform with enterprise password management capabilities, Cerby's top priority is protecting access to your accounts, account data, and sensitive information (secrets).

With this commitment to data security, Cerby offers two encryption schemes for the vaults where customers store their data: cloud and local encryption. These schemes also correspond to two different products: Cerby Automate and Cerby Protect. The goal is that users can select the approach that aligns with their security needs, regulatory compliance, and operational requirements.

When customers create a new Cerby workspace, the Cerby platform automatically generates a default cloud vault and its corresponding encryption keys, which are stored in the database and encrypted with the workspace KMS (AWS Key Management Service) key.

However, Cerby Protect customers can create additional vaults to leverage a Zero Knowledge architecture with the local encryption scheme. For more information about vaults, read the [How to create and manage a vault](https://help.cerby.com/en/articles/8376564-how-to-create-and-manage-a-vault) article.

The encryption scheme determines how encryption and decryption are performed and where decryption keys are stored. This article describes the two schemes and how they ensure the utmost protection for your data.

* * *

## Cloud encryption

In vaults with cloud encryption, Cerby's servers store the decryption keys, and the unique encryption keys are generated in the server and secured by AWS KMS along with the encrypted data (vault secrets).

Cerby uses an asymmetric key pair that comprises a public and private key to perform secure encryption and decryption operations. The private key is encrypted using the workspace KMS key.

When Cerby Automate customers need to access the data stored in their vault (whether to log in to an account or perform an automated task), the Cerby platform sends a request to Cerby's vaults system, which securely retrieves the appropriate encryption key, decrypts the data, and returns the decrypted data to the Cerby platform.

It's worth mentioning that Cerby's encryption system is the only authorized system that can perform data encryption and decryption, and decryption is performed within the AWS KMS environment, offering robust protection against unauthorized access. By using asymmetric encryption, encryption operations can also be performed on the clients.

As an additional layer of security, Cerby has implemented the role-based access control (RBAC) security mechanism to limit access to the encrypted data.

Cerby recommends cloud encryption for customers with limited IT or security expertise and little control or security enforcement on company devices.

This encryption scheme optimizes the recovery of encrypted data in the event of a disaster or device loss, as Cerby fully manages the key management system and recovery procedures. Customers do not perform additional disaster recovery actions.

### Key management

Cerby implements secure key management. AWS KMS enables the rotation of symmetric encryption keys, ensuring that even if a key is compromised, it is regularly replaced with a new key. Cerby takes advantage of this capability to enhance the overall security posture of customer vaults.

* * *

## Local encryption

In vaults with local encryption, the vault data encryption keys (DEKs) are stored exclusively on trusted devices registered by Cerby's servers, and decryption happens decentralized on such devices.

This encryption scheme leverages a Zero Knowledge architecture, where service providers have no knowledge or access to the decryption keys and the data stored within the encrypted vaults. Customer data remains private and confidential because the architecture prevents access from unauthorized parties, including Cerby.

Additionally, to access customer data stored in the cloud vaults, Cerby Protect users must have access to the registered device, authenticate to Cerby, and have a valid session under the OpenID Connect (OIDC) protocol.

Currently, the following items and item details are encrypted using local encryption:

  * Accounts
    * Passwords
    * Time-based one-time passwords (TOTPs)
    * Backup codes
    * Account notes
  * Secrets
    * Text-based information (body of the secret)
    * File attachments

Cerby recommends local encryption for customers with robust IT or Security teams and strict controls on company devices because encryption and decryption are decentralized, without relying on Cerby's infrastructure or resources.

### Trusted devices and vault replication

In the context of vaults with local encryption, a trusted device refers to a specific device that has been securely registered and authorized by Cerby's servers to access and decrypt the encrypted vaults.

Trusted devices comply with a verification and registration process in Cerby to ensure their authenticity and integrity. These devices can be any of the three clients you use to access a workspace: Cerby web app, Cerby browser extension, and Cerby mobile app.

All of the users in a Cerby workspace must set up at least one trusted device. For more information about trusted devices, read the [How to set up and manage your trusted devices](https://help.cerby.com/en/articles/8142370-how-to-set-up-and-manage-your-trusted-devices) article.

When devices are registered as trusted, Cerby grants them privileges to access and decrypt the local encryption vaults with customer data. These devices store the necessary decryption keys securely, ensuring that the sensitive information remains protected and inaccessible to unauthorized parties.

When **Workspace Admins** create a vault with local encryption, the following sets of keys are generated in a trusted device:

  * Public and private device keys, which are unique per device
  * Vault DEKs, which are unique per vault
  * Local encryption key, which is generated on the server and used to authorize decryption

  **NOTE:** The device keys and local encryption keys are used to decrypt and get local access to the vault DEKs. The private part of the key used for decryption never reaches any of Cerby’s servers.

To share access to a vault, a copy of the vault DEKs encrypted with the target public device key is distributed among all the trusted devices to enable them to perform encryption and decryption operations locally.

This vault replication happens automatically following the eventual consistency model, and it’s required that at least one trusted device with the vault DEKs is active for it to share the vault.

With vault replication, you can ensure that if one device becomes unavailable or compromised, other devices with replicated keys can still access and decrypt the vault data, adding an extra layer of availability and resilience to the encryption process.

It’s worth noting that Cerby cannot decrypt the vault DEKs because it does not have the device private keys. Also, the encrypted vault DEKs are stored transiently until fetched by the target device. In this sense, Cerby acts as a broker by only ensuring the secure transfer of encrypted data.

### Recovery key management

Recovery keys refer to physical copies of a mnemonic code that customers can use as backup or recovery methods to regain access to encrypted vaults if all the devices with the private keys are lost or unavailable. Users typically write down on paper these recovery keys (which is why they are known as paper keys) and store them in a safe place.

At Cerby, **Workspace Admins** can generate recovery keys via their trusted device and initiate a vault recovery process through the Cerby web app.

These keys are never stored or accessible to Cerby, and each key is unique. Therefore, if the copy of a recovery key is lost or was not properly written down, access to the vault cannot be recovered.

In the scenario where an attacker gets access to the recovery key, they cannot use it to decrypt the vault DEKs. Additionally, they wouldn’t have access to the user session of the paper key owner.

For more information about recovery keys, read the [How to generate and manage the recovery keys for your vault](https://help.cerby.com/en/articles/8376680-how-to-generate-and-manage-the-recovery-keys-for-your-vault) article.
