---
description: "This article describes how to manually turn on MFA for an account using the Cerby mobile app, setting Cerby as an authenticator app."
intercom_id: 12002648
---

# Turn on MFA with Cerby authenticator for an account using the mobile app

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* **Account Owners**
* Supported using the Cerby mobile app and web app. For the web app instructions, read the article [Turn on MFA with Cerby authenticator for an account using the web app](https://help.cerby.com/en/articles/8429534-turn-on-mfa-with-cerby-as-an-authenticator-app-for-your-account-using-the-web-app)


{% endhint %}

As an account **Owner** , you can turn on multi-factor authentication (MFA) manually to add a second layer of protection to your account.

This experience is intended for scenarios where the automated task to turn on MFA cannot be completed or is not supported, either because it involves a [self-managed account](https://help.cerby.com/en/articles/8708338-explore-accounts#h_079d120056) or the app requires manual intervention due to recent user interface (UI) updates.

Cerby is set as an authenticator app to generate and distribute time-based one-time passwords (TOTPs) for your account, and fill them in during automated logins.

To turn on MFA manually with Cerby authenticator for an account using the Cerby mobile app, you must complete the following steps:

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
  8. Tap the **Copy** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1813660361/d758bdeba38f6b9a5e58c75ab354/542154e7-3599-4cbe-93dd-31607f7bce6c?expires=1771416000&signature=fbe289edf27c0d2f757699cf745abc05d60af3955ff925f87c89756321c8858f&req=dSgmFc94nYJZWPMW3Hu4geEAHCJCj%2BlPd6lo4RurUQ0H8k4gAlWGo2MFsQAQ%0AnQ%3D%3D%0A" alt="">) icon.
7. Finish the MFA setup in your app by completing the following steps:
  1. Switch to the app where you retrieved the secret key.
  2. Continue with the MFA setup flow.
  3. Paste or enter the six-digit code.
  4. Save the configuration.
  5. Switch to the Cerby mobile app.
  6. Tap the **Done** button. The screen closes.
8. Save the account backup or recovery codes in Cerby, if supported by the app, by following the instructions in the article [Save the backup or recovery codes of your account](https://help.cerby.com/en/articles/12748253-save-the-backup-or-recovery-codes-of-your-account).

{% hint style="danger" %}


**IMPORTANT:** You can only save the backup or recovery codes of your account using the Cerby web app. When supported, Cerby recommends that you do it right after completing the MFA setup.


{% endhint %}

Now you are done.
