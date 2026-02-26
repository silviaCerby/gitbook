---
description: "This article describes how to add a vault to an account manually."
intercom_id: 9370625
---

# Assign additional vaults to an account

To enhance security and usability for **Account Owners** , **Admins** , and **Super** **Admins,** and to minimize the risk associated with a leaked vault key, Cerby has enabled the manual addition of cloud and local vaults to accounts. This capability enhances user flexibility, leveraging the advantages of each vault type. It also allows users to optimize their account management strategies, ensuring security, accessibility, and efficiency tailored to their specific needs and preferences.

By assigning an account to a local vault, the following occurs:

* You get increased account security by keeping data securely encrypted on the local device.
* Your accounts adhere to the zero-knowledge principles because only the user has access to the encryption keys on their devices, ensuring that no one else, including Cerby, can access the data.
* Automation tasks might be limited because of availability and accessibility to the LEKs.

By assigning an account to a cloud vault, the following occurs:

* You get enhanced automation actions through seamless automated actions such as automatic multi-factor authentication (MFA) and password rotation.
* Cerby gets faster access to encryption keys, allowing it to manage and execute automation tasks efficiently.

This article describes how to add a user vault to an account.

* * *

## Requirements

The following are the requirements to create a vault:

  * A Cerby account with the **Workspace Owner** or **Workspace Admin** role.
  * A trusted session previously set up for the device. For instructions, read the article [Set up trusted sessions on your devices](https://help.cerby.com/en/articles/8142370-set-up-trusted-sessions-on-your-devices).
  * At least one vault assigned to the account.
* * *

## Assign an additional vault to an account

To add a user vault to an account, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using the Cerby web app.
  2. Select the **All accounts** option from the left navigation drawer. The **All** **accounts** view is displayed.
  3. Click the corresponding account. The account details page is displayed with the **Settings** tab activated.
  4. Scroll down to the **Vault Settings** section in the account details.
  5. Click the arrow next to the **Vault Settings** title to expand it. The details of the user vault (s) to which the account is currently assigned are displayed.
​**NOTE:** Among the details, you can see whether the vault is managed locally or in the cloud.

  6. Click the **Assign to vault** option. The **Assign a vault** dialog box is displayed.
  7. Click the **Select a vault** drop-down field to see the list of available vaults.
​**NOTE:** Next to a vault's name, you can see whether it is a local or cloud vault.

  8. Select the vault you want to add to the account.
  9. Click the **Next** button. The **Confirm Vault Assignment** dialog box is displayed in which you can see the notice of what happens after you add an extra vault.
  10. Click the **Assign to vault** button. The dialog box closes, and a success message box is displayed.

* * *

## Remove a vault from an account

To remove a user vault from an account, you must complete the following steps:

{% hint style="danger" %}


**IMPORTANT:** All accounts must have at least one vault assigned.


{% endhint %}

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using the Cerby web app.
  2. Select the **All accounts** option from the left navigation drawer. The **All** **accounts** view is displayed.
  3. Click the corresponding account. The account details page is displayed with the **Settings** tab activated.
  4. Scroll down to the **Vault Settings** section in the account details.
  5. Click the arrow next to the **Vault Settings** title to expand it. The details of the user vault (s) to which the account is currently assigned are displayed.
  6. Hover the mouse over the vault you want to remove. The **Remove** icon appears.
  7. Click the **Remove** icon. The **Remove account from vault** dialog is displayed.
  8. Click the **Remove from vault** button. The vault is removed from the account, and a message is displayed.
