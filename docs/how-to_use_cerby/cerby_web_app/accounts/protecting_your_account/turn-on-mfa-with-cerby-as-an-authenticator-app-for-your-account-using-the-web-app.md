---
description: This article describes how to turn on MFA with Cerby as an authenticator app for your account to distribute TOTPs.
intercom_id: 8429534
---

# Turn on MFA with Cerby as an authenticator app for your account using the web app

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* **Account Owners**
* Supported using the Cerby web app and mobile app. For the mobile app instructions, read the article [Turn on MFA with Cerby as an authenticator app for your account using the mobile app](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-mobile-app/accounts/protecting-your-account/turn-on-mfa-with-cerby-as-an-authenticator-app-for-your-account-using-the-mobile-app)


{% endhint %}

As an account **Owner** , you can turn on and manage multi-factor authentication (MFA) for your accounts using the Cerby web app. This process involves using a secret key or scanning a QR code.

Unlike traditional authenticator apps tied to a single device or user, Cerby generates and securely distributes time-based one-time passwords (TOTPs) to all users with shared access to the account.

When MFA is turned on with this verification method, Cerby fills in the six-digit security codes required during login. Therefore, you can reduce manual overhead, eliminate the need to share physical devices, and ensure consistent access for all users with account permissions, while maintaining a secure authentication process.

* * *

## Requirements

The following are the requirements to set up and associate Cerby as your authenticator app for your account:

  * A Cerby workspace
  * A Cerby user account with the workspace **Owner** , **Super** **Admin** , **Admin** , or **User** role
  * An account in an app or service provider
  * An account added to Cerby to which you have the **Owner** role
* * *

## Turn on MFA with Cerby as an authenticator app for your account

You can turn on MFA with Cerby as your authenticator app using the following methods:

  * **[Automatic setup](turn-on-mfa-with-cerby-as-an-authenticator-app-for-your-account-using-the-web-app.md#id-automatic-setup):** For supported managed apps, Cerby can automatically turn on MFA without requiring manual input. With one click, Cerby handles the entire setup process for you in the background, including saving the account backup or recovery codes when supported.
  * **[Manual setup](turn-on-mfa-with-cerby-as-an-authenticator-app-for-your-account-using-the-web-app.md#id-manual-setup):** For apps that don’t support automation to turn on MFA, you can manually turn it on by retrieving a secret key from the app’s settings page and entering it in Cerby to complete the setup. Cerby recommends saving the account backup or recovery codes when supported.

The following sections describe the instructions for each option.

### Automatic setup

For supported apps, you can turn on MFA automatically with a single click by completing the following steps in the Cerby web app:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Click the corresponding account card. The account details page is displayed.
  3. Expand the **Multi-factor authentication (MFA) settings** section.
  4. Click the **Turn on** button in the**Cerby authenticator app** section. The **Turn on MFA** dialog box is displayed.
  5. Select the **I’ve verified that MFA is off for this account** option.
  6. Click the **Turn on MFA** button. A message indicating that Cerby is turning on MFA is displayed; when the automation is complete, a success message is displayed.

{% hint style="info" %}


**NOTE:** You can see the status of the automation job to turn on MFA in the [Automation Log](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-the-automation-log). When completed and supported, the account backup or recovery codes are saved in Cerby, and you can see them in the **Emergency controls** section of the account details page.


{% endhint %}

Now you are done.

### Manual setup

For self-managed apps and managed apps that don’t support automation to turn on MFA, you can turn it on manually by completing the following steps using the Cerby web app:

  1. Log in to your app in a web browser.
  2. Navigate to the MFA page in your app settings.
  3. Select the option to turn on MFA with an authenticator app. Commonly, a QR code is displayed.
  4. Complete the steps that corresponds to the setup method you want to use:

     * **Secret key**

       1. Select the **Can’t scan code?** or **Show secret key** option. An alphanumerical secret key is displayed.
       2. Copy the secret key.
       3. Open a separate browser tab.
       4. Log in to your [Cerby](https://app.cerby.com/) workspace.
       5. Click the corresponding account card. The account details page is displayed.
       6. Expand the **Multi-factor authentication (MFA) settings** section.
       7. Click the **Set as MFA** button. The **Save Code** dialog box is displayed.
       8. Paste the secret key in the **Secret Key** field of the **Save Code** dialog box.
       9. Click the **Save Code** button. A six-digit code is displayed.
       10. Copy the code.

     * **QR code**

       1. Log in to your Cerby workspace using your Cerby mobile app.
       2. Tap the corresponding account card to open the account details screen.
       3. Tap the **Activate MFA** button. The mobile phone's camera is displayed.
       4. Scan the QR code with your mobile phone. A six-digit code is displayed on a new screen.
  5. Finish the MFA setup in your app by completing the following steps:
     1. Switch to the browser tab with your app settings.
     2. Paste or enter the six-digit code.
     3. Save the configuration.
     4. Switch to the browser tab with the Cerby web app or take your mobile phone.
     5. Click the **Done** button. The dialog box or the screen closes, and a success message box is displayed.
  6. Save the account backup or recovery codes in Cerby, if supported by the app, by following the instructions in the article [Save the backup or recovery codes of your account](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/save-the-backup-or-recovery-codes-of-your-account).

Now you are done.
