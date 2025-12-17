---
description: This article describes how to manually turn on MFA for Google using Cerby as an authenticator.
intercom_id: 6992597
---

# How to turn on MFA for Google manually

The Cerby platform has a central feature that enables users to automatically turn on multi-factor authentication (MFA) for their application accounts. This feature adds an extra layer of security to authentication processes.

However, not all applications support automation for turning on MFA from Cerby. In these cases, users must manually configure MFA in the platforms of their service providers.

This article describes the steps to manually configure and turn on MFA for Google using Cerby as an authenticator.

## Requirements

The following are the requirements to configure MFA for Google:

* A Google account added to Cerby
* An active account on Google
* A Cerby-managed phone number configured in your Google account. For detailed instructions, review the [How to add a Cerby-managed email or phone number to your account](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/video-how-to-add-a-cerby-managed-email-or-phone-number-to-your-account) video

**NOTE:** Cerby recommends turning on MFA using a browser on a desktop computer.

## Turn on MFA for Google

To turn on MFA for your Google account, you must complete the following main steps:

1. [Turn on MFA with your Cerby-managed phone number](how-to-turn-on-mfa-for-google-manually.md#id-1.-turn-on-mfa-with-your-cerby-managed-phone-number)
2. [Turn on MFA with Cerby as an authenticator](how-to-turn-on-mfa-for-google-manually.md#id-2.-turn-on-mfa-with-cerby-as-an-authenticator)
3. [Save the secret key in Cerby](how-to-turn-on-mfa-for-google-manually.md#id-3.-save-the-secret-key-in-cerby)

The following sections describe each main step.

### 1\. Turn on MFA with your Cerby-managed phone number

To turn on MFA with your Cerby-managed phone number, you must complete the following steps:

1. Log in to your [Cerby](https://app.cerby.com/) workspace.
2. Log in to your corresponding Google account from Cerby. The Google Account **Home** page is displayed in a new tab.
3. Click the **Security** button in the left navigation drawer. The **Security** page is displayed.
4. Click the **2-Step Verification** button on the **Signing in to Google** section. The **2-Step Verification** page is displayed with the **Protect your account with 2-Step verification** section.
5. Click the **GET STARTED** button. The **Let’s set up your phone** section is displayed.

**IMPORTANT:** Ensure the **Text message** option is selected in the **How do you want to get codes?** section.

6. Click the **NEXT** button. The **Confirm that it works** section is displayed. A verification code is sent to the Cerby-managed phone number via SMS, and you may receive a notification with the code in your phone via the Cerby mobile app.
7. Get the verification code from the account inbox in Cerby or from the notification on your phone.

**NOTE:** To access the account inbox, perform the following actions:

   1. Switch to the tab with the Cerby web app.
   2. Click the **Settings** icon of the corresponding Google account card. The account details page is displayed with the **Settings** tab activated.
   3. Activate the **Inbox** tab. A table of messages sent to the Cerby-managed phone number via SMS is displayed.
   4. Copy the corresponding verification code from the **Message** column.
8. Enter the verification code in the **Enter the code** field.
9. Click the **NEXT** button. The **It worked! Turn on 2-Step Verification?** section is displayed.
10. Click the **TURN ON** button. The **Available second step** section is displayed with the Cerby-managed phone number verified.

The next step is [2. Turn on MFA with Cerby as an authenticator](how-to-turn-on-mfa-for-google-manually.md#id-2.-turn-on-mfa-with-cerby-as-an-authenticator), which you must complete from the **2-Step Verification** page.

* * *

### 2\. Turn on MFA with Cerby as an authenticator

To turn on MFA with Cerby as an authenticator, you must complete the following steps:

  1. Click the **Authenticator app** button in the **Add more second steps to verify it’s you** section of the **2-Step Verification** page. The **Authenticator app** page is displayed.
  2. Click the **Set up authenticator** button. The **Set up authenticator app** dialog box is displayed with a QR code.
  3. Click the **Can’t scan it?** button. A set of instructions is displayed with a secret key.
  4. Copy the secret key.

  **IMPORTANT:** Leave the dialog box open because you need it later.

The next step is [3. Save the secret key in Cerby](how-to-turn-on-mfa-for-google-manually.md#id-3.-save-the-secret-key-in-cerby), which you must complete from the Cerby web app.

* * *

### 3\. Save the secret key in Cerby

To save the secret key in Cerby, you must complete the following steps:

  1. Switch to the tab that was left open with the Cerby web app.
  2. Click the **Settings** icon from the corresponding account card in Cerby. The account details page is displayed with the **Settings** tab activated.
  3. Click the **Set as MFA** button from the **Cerby authentication App** option in the **Multi-factor authentication settings (MFA)** section. The **Save Code** dialog box is displayed.
  4. Paste in the **Secret key** field the secret key you copied previously..
  5. Click the **Save Code** button. A success message box and the **Verify your code** dialog box are displayed with a confirmation code.
  6. Copy the confirmation code.
  7. Switch to the tab with the **Set up authenticator app** dialog box of the Google configuration.
  8. Click the **Next** button. The dialog box prompts you to enter a six-digit confirmation code.
  9. Paste the confirmation code in the **Enter Code** field.
  10. Click the **Verify** button. The dialog box closes, and an authenticator is displayed with the “Added just now” status.
  11. Click the **Back** icon. The **2-Step Verification** page is displayed with an authenticator app as the default MFA verification method.

Now you are done.
