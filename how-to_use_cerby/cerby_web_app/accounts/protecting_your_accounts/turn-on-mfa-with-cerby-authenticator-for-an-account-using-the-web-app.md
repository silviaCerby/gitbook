---
description: "This article describes how to manually turn on MFA for an account using the Cerby web app, setting Cerby as an authenticator app."
intercom_id: 8429534
---

# Turn on MFA with Cerby authenticator for an account using the web app

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* **Account Owners**
* Supported using the Cerby web app and mobile app. For the mobile app instructions, read the article [Turn on MFA with Cerby authenticator for an account using the mobile app](https://help.cerby.com/en/articles/12002648-turn-on-mfa-with-cerby-as-an-authenticator-app-for-your-account-using-the-mobile-app)


{% endhint %}

As an account **Owner** , you can turn on multi-factor authentication (MFA) manually to add a second layer of protection to your account.

This experience is intended for scenarios where the automated task to turn on MFA cannot be completed or is not supported, either because it involves a [self-managed account](https://help.cerby.com/en/articles/8708338-explore-accounts#h_079d120056) or the app requires manual intervention due to recent user interface (UI) updates.

Cerby is set as an authenticator app to generate and distribute time-based one-time passwords (TOTPs) for your account, and fill them in during automated logins.

To turn on MFA manually with Cerby authenticator for an account using the Cerby web app, you must complete the following steps:

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
6. Save the account backup or recovery codes in Cerby, if supported by the app, by following the instructions in the article [Save the backup or recovery codes of your account](https://help.cerby.com/en/articles/12748253-save-the-backup-or-recovery-codes-of-your-account).

Now you are done.
