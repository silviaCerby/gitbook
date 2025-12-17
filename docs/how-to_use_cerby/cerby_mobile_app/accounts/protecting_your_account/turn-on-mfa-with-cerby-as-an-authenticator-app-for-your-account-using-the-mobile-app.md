---
description: "This article describes how to turn on MFA with Cerby as an authenticator app for your account using the Cerby mobile app."
intercom_id: 12002648
---

# Turn on MFA with Cerby as an authenticator app for your account using the mobile app

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* **Account Owners**
* Supported using the Cerby mobile app and web app. For the web app instructions, read the article [Turn on MFA with Cerby as an authenticator app for your account using the web app](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/turn-on-mfa-with-cerby-as-an-authenticator-app-for-your-account-using-the-web-app)


{% endhint %}

As an account **Owner** , you can turn on and manage multi-factor authentication (MFA) for your accounts using the Cerby mobile app. This process involves using a secret key.

Unlike traditional authenticator apps tied to a single device or user, Cerby generates and securely distributes time-based one-time passwords (TOTPs) to all users with shared access to the account.

When MFA is turned on with this verification method, Cerby fills in the six-digit security codes required during login. Therefore, you can reduce manual overhead, eliminate the need to share physical devices, and ensure consistent access for all users with account permissions, while maintaining a secure authentication process.

* * *

## Requirements

The following are the requirements to turn on MFA with Cerby as an authenticator app for your account:

  * A Cerby workspace
  * A Cerby user account with the workspace **Owner** , **Super Admin** , **Admin** , or **User** role
  * An account in an app or service provider
  * An account added to Cerby to which you have the **Owner** role
* * *

## Turn on MFA with Cerby as an authenticator app for your account

To turn on MFA with Cerby as an authenticator app for your account, you must complete the following steps using the Cerby mobile app:

  1. Log in to your app on your mobile phone.
  2. Navigate to the MFA or two-factor authentication (2FA) screen in the app settings.
  3. Select the option to turn on MFA with an authenticator app. A screen with a QR code is displayed.
​**NOTE:** Commonly, apps display a QR code, but if a secret key is displayed instead, proceed to step 5.

  4. Look for the option to use a secret key; sometimes, you must tap a **Can’t scan code?** button. An alphanumerical secret key is displayed.
  5. Copy the secret key.
  6. Enter the secret key in the Cerby mobile app to set up MFA by completing the following steps:
     1. Open the Cerby mobile app.
     2. Log in to your Cerby workspace.
     3. Tap the corresponding account card. The account details screen is displayed.
     4. Tap the **Activate MFA** button. The mobile phone's camera is displayed.
     5. Tap the **Can’t scan the QR code?** button. The **Enter key manually** screen is displayed.
     6. Paste the secret key in the **Secret key** field.
     7. Tap the **Save secret key** button. A six-digit code is displayed on a new screen.
     8. Tap the **Copy** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1813660361/d758bdeba38f6b9a5e58c75ab354/542154e7-3599-4cbe-93dd-31607f7bce6c?expires=1762304850&signature=1987f52e7b3bd39e6bc384683661e41ea8686bb1cdf3f979220044f7497c59c1&req=dSgmFc94nYJZWPMU3HP0gMVMAMxtxCmViNMVjexTMZsJv9E%2FPIc%3D%0A" alt="">) icon.
  7. Finish the MFA setup in your app by completing the following steps:
     1. Switch to the app where you retrieved the secret key.
     2. Continue with the MFA setup flow.
     3. Paste or enter the six-digit code.
     4. Save the configuration.
     5. Switch to the Cerby mobile app.
     6. Tap the **Done** button. The screen closes.
  8. Save the account backup or recovery codes in Cerby, if supported by the app, by following the instructions in the article [Save the backup or recovery codes of your account](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/save-the-backup-or-recovery-codes-of-your-account).

{% hint style="danger" %}


**IMPORTANT:** You can only save the backup or recovery codes of your account using the Cerby web app. When supported, Cerby recommends that you do it right after completing the MFA setup.


{% endhint %}

Now you are done.
