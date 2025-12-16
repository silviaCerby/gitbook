---
description: This article describes how to run automated tasks for accounts assigned to local vaults.
intercom_id: 11682782
---

# Run automated tasks for accounts in local vaults

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super** **Admins** , **Admins,** and **Users**
* Account **Owners**
* Only supported using the Cerby web app


{% endhint %}

As an account Owner with accounts assigned to local vaults, you might have some limitations executing automated tasks, as explained in the article [Explore automation for accounts in local vaults](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-automation-for-accounts-in-local-vaults). Even with these limitations, you can perform the following tasks for accounts assigned to a local vault:

* Rotate your account password
* Turn on multi-factor authentication (MFA)

This article describes how to perform these automated tasks.

* * *

## Rotate your account password

To rotate the password for an account in a local vault, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Select the **All accounts** option from the left navigation drawer. The **All accounts** view is displayed.
  3. Click the **Settings** icon of the corresponding account card. The account details page is displayed with the **Settings** tab activated.
  4. Hover the**Current password** field. The **Rotate password** button and other icons are displayed.
  5. Click the **Rotate password** button. The **Rotate Password** dialog box is displayed.
  6. Click the **Rotate Password** button. The **Transfer to a Cloud Vault** dialog box is displayed. This dialog box indicates that the following occurs:
     1. Your password is temporarily transferred to a cloud vault, where the password is rotated and returned.
     2. After the password is rotated, the cloud vault is deleted.
  7. Click the **Confirm** button. Two messages appear: one a success message and the other indicating that the password is being rotated. You’ll receive an email indicating the result of the password rotation.

Now you are done.

* * *

## Turn on multi-factor authentication (MFA)

To turn on MFA in your account, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Select the **All accounts** option from the left navigation drawer. The **All accounts** view is displayed.
  3. Click the **Settings** icon of the corresponding account card. The account details page is displayed with the **Settings** tab activated.
  4. Expand the **Multi-factor authentication (MFA) settings** section.
  5. Click the **Turn on** button in the **Turn on MFA automatically** section. The **Turn on MFA** dialog box is displayed.
  6. Perform the following steps:
     1. Select the **I've verified that MFA is off for this account** checkbox.
     2. Click the **Turn on MFA** button. The **Transfer to a Cloud Vault** dialog box is displayed. This dialog box indicates that the following occurs:

        * Gain access to the encryption key and can potentially access account secrets.
        * Enable Cerby to MFA on your behalf for the account. A success message and the other indicating that the MFA is turned on.

     3. Click the **Confirm** button.
  7. Follow the steps to [turn on MFA in your app](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/turn-on-mfa-with-cerby-as-an-authenticator-app-for-your-account-using-the-web-app).

Now you are done.
