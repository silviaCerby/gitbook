---
description: "This article describes how to manually back up all your accounts from a Cerby vault to CyberArk."
intercom_id: 12597970
---

# Manually back up all accounts from Cerby to CyberArk

**Who can use this capability?**

* Workspace**Owners** , **Super Admins** , and **Admins**
* Only supported using the Cerby web app.

---

As a workspace **Owner** , **Super** **Admin** , or **Admin** , you can manually back up all accounts in your Cerby vault to CyberArk. When you first set up the vault backup, only accounts that are created or updated after setup are automatically backed up, previously existing accounts are not included.

To ensure all accounts are stored in CyberArk, you can use the **Back up accounts** option in the vault backup setup to manually back up every account in your workspace.

**IMPORTANT:** Vault backup is a one-way sync from Cerby to CyberArk. Changes made in CyberArk do not sync back to Cerby. Cerby remains the primary source of truth for your vault data.
---

To manually back up all accounts from a Cerby vault to CyberArk, you must complete the following steps:

1. Log in to your [Cerby](https://app.cerby.com/) workspace.
2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed with the **General** tab active.
3. Activate the **Privacy and security** tab.
4. Activate the **Vault backup** left tab.
5. Click the **More options** () button of the vault backup. A drop-down menu is displayed.
6. Select the **Back up accounts** () option. A success message is displayed.

**IMPORTANT:** Depending on the workspace size, backing up the accounts to CyberArk might take several minutes to complete.
---

Now you are done.
