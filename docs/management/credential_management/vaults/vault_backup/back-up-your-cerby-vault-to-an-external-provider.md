---
description: "This article describes the benefits of backing up your vault to an external provider of your choice, ensuring it remains safe, redundant, and recoverable."
intercom_id: 12004415
---

# Back up your Cerby vault to an external provider

With Cerby, you can securely back up your account information from Cerby to an external credential management provider, such as CyberArk. This Cerby capability enables you to build redundancy and meet risk management practices without adding complexity to your day-to-day work.

The following are the ways in which Cerby backs up your vault to an external workspace:

* **One-way sync:** Account data flows from Cerby to your backup provider only, preventing accidental overwrites or changes in the main vault.
* **Backup redundancy:** Your organization is protected against data loss or corruption.
* **Event-driven updates:** When accounts are created or updated in Cerby, the backup is done automatically in the backup provider.
* **MFA handling:** Multi-factor authentication (MFA) settings are also backed up to ensure consistent security.

**Secure by design:** Data is encrypted in transit to protect sensitive credentials, ensuring your privacy is maintained.

**Secure by design:** Data is encrypted in transit to protect sensitive credentials, maintaining your privacy.

{% hint style="danger" %}


**IMPORTANT:**

* Cerby only supports vault backup with CyberArk for workspace cloud vaults.
* Vault backup is a one-way sync from Cerby to CyberArk. Changes in CyberArk do not sync back to Cerby, and any updates in Cerby overwrite changes made directly in CyberArk. Cerby remains the primary source of truth for your vault data.


{% endhint %}

* * *

## How backing up your Cerby vault to an external provider works

The following environments comprise the Cerby vault backup scheme with an external provider:

  * **Cerby:** The primary vault, where all accounts and credentials live.
  * **CyberArk:** The backup provider where login credentials are stored.

The following is the complete flow of how both environments interact:

  1. A workspace **Owner** , **Super Admin** , or **Admin** sets up the vault backup capability with CyberArk in their Cerby workspace only once.
  2. An account **Owner** adds or updates an account. The Cerby vault backup capability is triggered for each event.
  3. New and updated login credentials are backed up in CyberArk.

* * *

## What you can do with vault backup

The **Vault Backup** capability supports the following main flows:

  * **Discover vault:** Identify your Cerby cloud vault to include in your backup plan.
  * **Verify accounts:** Check that login credentials in CyberArk match what you have in Cerby.
  * **Handle MFA:** MFA settings stay consistent across both vaults.
* * *

## Keeping your data secure

Security is built into every part of vault backup to keep your credentials secure while providing added redundancy.

  * All data is encrypted at rest and in transit.
  * Backing up MFA settings prevents data loss, preserves strong authentication, and keeps the restored vault secure.
  * A one-way sync ensures the primary vault remains the sole source of truth, protecting against corruption, tampering, and upstream attacks from a compromised replica.
  * Even if the recovery vault is breached, the primary stays isolated and secure, simplifying disaster recovery with a clean, reliable state to restore.
* * *

## Related articles

The following articles contain more information about the Vault Backup capability:

  * [Add a vault backup](https://cerby-test.gitbook.io/cerby-test/management/credential-management/vaults/vault-backup/add-a-vault-backup)
  * [View the details of a vault backup](https://cerby-test.gitbook.io/cerby-test/management/credential-management/vaults/vault-backup/view-the-details-of-a-vault-backup)
  * [Edit the vault backup information](https://cerby-test.gitbook.io/cerby-test/management/credential-management/vaults/vault-backup/edit-the-vault-backup-details)
  * [Disable vault backup in your workspace](https://cerby-test.gitbook.io/cerby-test/management/credential-management/vaults/vault-backup/disable-vault-backup-in-your-workspace)
  * [Manually back up all accounts from Cerby to CyberArk](https://cerby-test.gitbook.io/cerby-test/management/credential-management/vaults/vault-backup/manually-back-up-all-accounts-from-cerby-to-cyberark)
