---
description: This article describes how to log in to an account using the Cerby mobile app.
intercom_id: 11139221
---

# Log in to an account using the Cerby mobile app

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Admins** , and **Users**
* Account **Collaborators** and **Owners**
* Supported using the Cerby web app, mobile app, and browser extension


{% endhint %}

Cerby securely stores your login credentials, including usernames, passwords, and multi-factor authentication (MFA) codes, streamlining the login process on your mobile phone.

When the Cerby mobile app detects a login screen, it automatically suggests the appropriate credentials, enabling you to autofill them directly or copy and paste them into the app’s login fields.

* * *

## Requirements

The following are the requirements to effectively use the Cerby mobile app to log in to your accounts:

  * The Cerby mobile app installed and configured. For more information, read the article corresponding to your operating system:
    * [Install and configure the Cerby mobile app on iOS](https://cerby-test.gitbook.io/cerby-test/getting-started/cerby-mobile-app/install-and-configure-the-cerby-mobile-app-on-ios)
    * [Install and configure the Cerby mobile app on Android](https://cerby-test.gitbook.io/cerby-test/getting-started/cerby-mobile-app/install-and-configure-the-cerby-mobile-app-on-android)
  * The **Allow AutoFill** setting turned on for the Cerby mobile app. For more information, read the article [Turn on the Allow AutoFill feature](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-mobile-app/app-configuration/turn-on-the-allow-autofill-feature).
  * MFA turned on for your account, if applicable, using a method managed by Cerby, such as an authenticator app, email address, or phone number.
  * An active session in the Cerby mobile app, meaning that you have already logged in to your Cerby workspace. For more information, read the article Log in to the Cerby mobile app.
* * *

## Log in to an account using the Cerby mobile app

When you log in to an account using the Cerby mobile app, you might encounter the following cases depending on how your app is configured:

  * [Log in to an account with a username and password only](log-in-to-an-account-using-the-cerby-mobile-app.md#id-log-in-to-an-account-with-a-username-and-password-only)
  * [Log in to an account with Cerby-managed MFA](log-in-to-an-account-using-the-cerby-mobile-app.md#id-log-in-to-an-account-with-cerby-managed-mfa)
  * [Log in to an account without using autofill](log-in-to-an-account-using-the-cerby-mobile-app.md#id-log-in-to-an-account-without-using-autofill)

The following sections explain how to log in to your accounts for each case.

### Log in to an account with a username and password only

To log in to an account that doesn't use MFA and only requires filling in the username and password, you must complete the following steps:

  1. Open the app you want to log in to.
  2. Access the login screen.
  3. Tap the **Username** field.

     * If you have the **Allow Autofill** feature correctly configured, your credentials saved in Cerby are displayed.

       1. Tap the credential of the account you want to access. The **Username** field is filled in with your username.

       **NOTE:** If you don't have an active session in the Cerby mobile app, you must log in to your Cerby workspace.

     * If the login credentials saved in Cerby are not displayed:
       * Review whether the **Allow Autofill** feature is correctly configured for the Cerby mobile on your phone.
       * Follow the steps in the [Log in to an account without using autofill](log-in-to-an-account-using-the-cerby-mobile-app.md#id-log-in-to-an-account-without-using-autofill) section.

  4. Repeat step 3 for the **Password** field.
  5. Tap the **Log in** button.

Now you are done.

### Log in to an account with Cerby-managed MFA

To log in to an account that requires filling in your username, password, and a verification code provided by a Cerby-managed MFA method, you must complete the following steps:

  1. Open the app you want to log in to.
  2. Access the login screen.
  3. Tap the **Username** field.

     * If you have the **Allow Autofill** feature correctly configured, your login credentials saved in Cerby are displayed.

       1. Tap the credentials of the account you want to access.

       **NOTE:** If you don't have an active session in the Cerby mobile app, you must log in to your Cerby workspace.

     * If the login credentials saved in Cerby are not displayed:
       * Review whether the **Allow Autofill** feature is correctly configured for the Cerby mobile app on your phone.
       * Follow the steps in the [Log in to an account without using autofill](log-in-to-an-account-using-the-cerby-mobile-app.md#id-log-in-to-an-account-without-using-autofill) section.

       **IMPORTANT:** If you have more than one account saved for the app, the screen with all available accounts is displayed.

     1. Select the account you want to log in to.

The **Username** field is filled in with your username.

  4. Repeat step 3 for the **Password** field.
  5. Tap the **Log in** button. The screen to enter an MFA code is displayed.
  6. Tap the **verification code for this website - Cerby** option displayed above the numerical keyboard. The corresponding field is filled out with the MFA code.

  **NOTE:** If the autofill MFA option is not displayed, you must copy the MFA code manually from the Cerby mobile app by completing the following steps:

     1. Open the Cerby mobile app.
     2. Tap the card corresponding to the account you want to log in to.
     3. Tap and hold the **App OTP** field to copy the current MFA code. A green check mark is displayed within the field.
     4. Return to the app to which you want to log in.
     5. Paste the MFA code you copied.
  7. Tap the button that verifies the code is correct.

Now you are done.

### Log in to an account without using autofill

In some cases, the login screen’s input fields are not recognized as secure, which prevents the autofill option from appearing. Additionally, depending on your device configuration, you might not have set up the **Allow Autofill** feature in the Cerby mobile app settings.

To log in to an account that requires filling in your username, password, and MFA code when autofill is not available, you must complete the following steps:

  1. Open the app you want to log in to.
  2. Access the login screen.
  3. Copy the information from the Cerby mobile app by following the next steps:
     1. Open the Cerby mobile app.
     2. Tap the card corresponding to the account you want to log in to.
     3. Tap and hold the field with the information you want to copy, such as username, password, or MFA code. A green check mark is displayed within the field.
  4. Paste the information you copied into the corresponding field.
  5. Repeat steps 3 and 4 for all the required fields.
  6. Tap the button to log in.

Now you are done.
