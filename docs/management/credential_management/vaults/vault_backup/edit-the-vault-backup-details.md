---
description: This article describes how to edit the vault backup details.
intercom_id: 12431376
---

# Edit the vault backup details

{% hint style="info" %}


**Who can use this capability?**

* Workspace**Owners** , **Super Admins** , and **Admins**
* Only supported using the Cerby web app.


{% endhint %}

As a workspace **Owner** , **Super** **Admin** , or **Admin** , you can edit the configuration credentials to update the connection between Cerby and CyberArk.

To edit the vault backup details, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed with the **General** tab active.
  3. Activate the **Privacy and security** tab.
  4. Activate the **Vault backup** left tab.
  5. Click the **More options** () button of the vault backup. A drop-down menu is displayed.
  6. Select the **Edit** () option. The **Connect to CyberArk** section is displayed with the current values.
  7. Update the CyberArk–Cerby connection values as needed.
**IMPORTANT:** The **CyberArk auth URL** or **CyberArk base URL** values cannot be edited in the **Connect to CyberArk** section.

  8. Click the **Validate targets** button. Cerby validates the safe, and the Connect button is enabled after a successful validation.
  9. Click the **Done** button. The **Vault backup** section is displayed with the updated vault backup.

**IMPORTANT:** A known issue occurs when incorrect **Client ID** or **Client Secret** values are entered, which disables the CyberArk–Cerby connection. If this happens, you must re-establish the connection with the correct values.
---

Now you are done.
