---
description: This article describes how to troubleshoot the most common issues with accessing and managing your Instagram account through Cerby.
---

# Troubleshooting: Common issues with Instagram

This article helps you fix the most common issues with accessing and managing your Instagram account through Cerby.

The following are the most common issues:

  * Suspicious login attempt
  * Unable to access settings when turning on MFA
  * Manual MFA enrollment
  * Cerby mobile app behavior
  * Cerby-managed phone number support
  * Email swap
  * Invalid MFA verification code

The following sections describe common scenarios that can cause confusion and, if applicable, a proposed solution.

* * *

# Suspicious login attempt

When you log in automatically to an Instagram account from Cerby using a new device (computer or mobile phone) from a new location, Instagram displays the **Suspicious Login Attempt** dialog box or screen asking you to verify your identity, as shown in **Figure 1**.

<figure><img src="../.gitbook/assets/5ktSl6CtPZ98mhoHP3oXeQ7Qwe-KMcZ2oVUa58itSyDkz6t7d50nKlvm6Abc7_2I2fqTzXkC62fpv_4H1bFtaudiWhM7g7OMzu9o36JJ4iplKtwHKLO3gVe77osClA4dGyv40fW1orOG2kRRs4Zh5CbAe11QVR0E7urkythO9h8KtNzS3DTKUqRmEV7o.jpg" alt="Suspicious Login Attempt Dialog Box or Screen"><figcaption></figcaption></figure>

**Figure 1. Suspicious Login Attempt Dialog Box or Screen**

{% hint style="info" %}


**NOTE:** This behavior occurs whether you have multi-factor authentication (MFA) turned on or not. It may also happen when Cerby performs automated tasks, such as turning on MFA and rotating passwords.


{% endhint %}

In the dialog box or screen, Instagram asks you to verify your identity by sending a six-digit security code to the email address registered in the account.

## Solution

To solve the login attempt prompt, click the **Send Security Code** button from the **Suspicious Login Attempt** dialog box or screen. You will receive a security code at the registered email address.

To retrieve the security code when you have a Cerby-managed email address, you must forward the email because the message in the **Shared Inbox** does not display the code. Follow the instructions in the article [Forward a message from your Cerby inbox](https://help.cerby.com/en/articles/6119548-how-to-forward-a-message-from-your-cerby-inbox), and then open your email to copy the code.

To prevent the **Suspicious Login Attempt** dialog box or screen from being displayed in the future, Cerby recommends you turn on MFA with Cerby as an authenticator app and disable the login requests settings on Instagram. Complete the following steps:

  1. Turn on MFA manually. Follow the instructions in the [How to turn on MFA in Instagram manually](https://help.cerby.com/en/articles/6422083-video-how-to-turn-on-2fa-in-instagram-manually) video.

**NOTE:** If you have already turned on MFA with Cerby as an authenticator app, continue to step 2.

  2. Tap the **Profile** button with your picture or avatar, located on the right in the bottom navigation drawer of the Instagram mobile app. The **Edit profile** screen is displayed.
  3. Tap the **Menu** icon at the top right of the screen. A drop-down list is displayed.
  4. Tap the **Settings** button from the drop-down list. The **Settings** screen is displayed.
  5. Tap the **Security** button. The **Security** screen is displayed.
  6. Tap the **Multi-factor authentication** button located in the **Login security** section. The **Multi-factor authentication** screen is displayed with the **Multi-factor authentication is on** section.
  7. Tap the **Additional methods** button in the How you get login codes section. The **Additional methods** screen is displayed.
  8. Deactivate the switch of the **Login requests** option.

Now you are done.

* * *

# Unable to access settings when turning on MFA

When you attempt to turn on MFA manually or automatically from Cerby using a new device (mobile phone or computer), Instagram may display the **You can’t access certain settings for a few days** dialog box, as shown in **Figure 2**.

<figure><img src="../.gitbook/assets/_q2tILisZ1Sv_AJf7fdMSDJmKnqPfeD1jnbzbLkTaXGc2aq93O2kz944mwAzllnBEpSFeMvY2oLVnTRByvOF_I0wlkpsmBf_e85GPY3GQSuBWAhUkSWnYDw3jg_p43WNPxQH6cPFdoUnNb28ca-9e4TpJzzQ7gAZ8xXx3IfJogex7RnF--NAHW05a7rn5Q.png" alt="You can’t access certain settings for a few days Dialog Box"><figcaption></figcaption></figure>

**Figure 2. You can’t access certain settings for a few days** dialog box

This behavior happens because Instagram verifies and keeps track of your devices. Therefore, if the attempt to turn on MFA comes from a new device, Instagram will not let you change any security settings for one or two days.

## Solution

To solve the MFA enrollment attempt prompt, you have two options:

  * Try again to turn on MFA in a day or two.
  * Use a device with an active session to turn on MFA manually by performing the following actions:

    1. Identify the device with an active session by following the instructions in the [View your account’s recent login activity](https://help.instagram.com/2761108904184084) official documentation from Instagram. The device must have an **Active now** status, as shown in **Figure 3**.

<figure><img src="../.gitbook/assets/InstagramDialogBox_1_70.png" alt=""><figcaption></figcaption></figure>

**Figure 3. Instagram Login Activity** screen

    2. Use the device with the active session to turn on MFA manually. Follow the instructions in the [How to turn on MFA in Instagram manually](https://help.cerby.com/en/articles/6422083-video-how-to-turn-on-2fa-in-instagram-manually) video.

Now you are done.

* * *

# Manual MFA enrollment

Instagram is one of the apps supported by Cerby, and it has an automation workflow that turns on multi-factor authentication (MFA) by simply activating a switch in the **Settings** tab of your account. This automation configures the Cerby mobile app as an authenticator app.

To execute the workflow successfully, you must create and configure a Cerby-managed email address in your Instagram account to receive verification codes. If your business needs prevent you from using a Cerby-managed email address, you can enroll MFA manually.

You can only go through this manual configuration with your Instagram mobile app to retrieve the secret key to configure Cerby as an authenticator app. To enroll MFA manually, follow the instructions in the [How to turn on MFA in Instagram manually](https://help.cerby.com/en/articles/6422083-video-how-to-turn-on-2fa-in-instagram-manually) video.

**IMPORTANT:** Make sure to securely save the recovery or backup codes in Cerby after turning on MFA to help you get back into your account if, for any reason, you lose access. To save the codes, you must complete the following steps:

  1. Copy the recovery codes from Instagram. Follow the instructions in the [How you can use a recovery code on Instagram](https://help.instagram.com/1006568999411025) official documentation.
  2. Click the **Settings** icon of the corresponding Instagram account card in the Cerby web app. The **Settings** tab is displayed in the account details page.
  3. Click the **Add Codes** button located in the **Emergency Controls** section. The **Add MFA Backup Codes** dialog box is displayed.
  4. Paste the recovery codes in the **MFA Backup Codes** field.
  5. Click the **Save Codes** button. The dialog box closes, and a success message box is displayed.

After turning on MFA and configuring Cerby as an authenticator app, your login experience improves. Verification codes are automatically distributed to all account members and auto-filled when they log into Instagram from Cerby as follows:

  * When logging in through the Cerby web app, the verification code is entered automatically as part of the workflow.
  * When logging in through the Instagram mobile app, the verification code is copied to the clipboard using the autofill feature. For more information, see the Cerby mobile app behavior section.

You can turn off MFA on a computer or the Instagram mobile app through your web browser.

* * *

# Cerby mobile app behavior

The Cerby mobile app helps you easily log in to your apps by auto-filling the credentials of the Instagram account you added to Cerby. Open the Instagram app's login screen on your mobile phone and use autofill on every input field according to your operating system (iOS or Android).

When MFA is on, you may have to enter a verification code on an additional screen after auto-filling your credentials. Perform the following actions to retrieve the code according to your verification method:

  * **Cerby app as an authenticator app:** When autofill is enabled on your mobile phone, the verification code is automatically copied to the clipboard. Tap the **Paste** button to fill in the verification code field. For more information, read the article [Turn on MFA with Cerby as an authenticator app for your account](https://help.cerby.com/en/articles/8429534-turn-on-mfa-with-cerby-as-an-authenticator-app-for-your-account).

**NOTE:** If autofill is not enabled or the code is not automatically copied to the clipboard, copy the verification code from the **MFA Code** section. This section is located in the account details using the Cerby mobile app.

  * **Cerby-managed email address:** The verification code is sent to the **Shared Inbox** , and you can retrieve it through the Cerby web app. For more information on the **Shared Inbox** , refer to the articles:
    * [Set up and associate a Cerby-managed email address for your account](https://help.cerby.com/en/articles/11888658-set-up-and-associate-a-cerby-managed-email-address-for-your-account)
    * [View the messages sent to a Cerby-managed email address or phone number](https://help.cerby.com/en/articles/11889348-view-the-messages-sent-to-a-cerby-managed-email-address-or-phone-number)
* * *

# Cerby-managed phone number support

Cerby provides and manages securely generated phone numbers you can use for your Instagram account and across your organization.

By managing this service, Cerby can improve the Instagram login process by automatically filling out your verification codes when MFA is turned on with your phone number as a verification method. These codes are retrieved from your **Shared Inbox** in Cerby. For more information, refer to the article [Set up and associate a Cerby-managed phone number for your account](https://help.cerby.com/en/articles/11889035-set-up-and-associate-a-cerby-managed-phone-number-for-your-account).

{% hint style="danger" %}


**IMPORTANT:** You can’t configure a Cerby-managed phone number when signing up for an Instagram account. When you have it, configure it in Instagram after validating your account.


{% endhint %}

* * *

# Email swap

When you automatically swap the email address of your Instagram account for a Cerby-managed email address, verify it by clicking the link in the confirmation email you receive from Instagram.

This email is sent to your **Shared Inbox** in Cerby, and to be able to click the link, you must forward the message. Follow the instructions in the [How to forward a message from your Cerby inbox](https://help.cerby.com/en/articles/6119548-how-to-forward-a-message-from-your-cerby-inbox) article, and then open your email to confirm your email address for Instagram.

After confirming the email, you can log in to your Instagram account automatically from Cerby.

* * *

# Invalid MFA verification code

Occasionally, when you log in automatically to your Instagram account from Cerby and have MFA on, Instagram shows an error indicating that the verification code is incorrect, even when it is correct.

## Solution

If you encounter this error, Cerby recommends manually entering the verification code. Depending on the verification method you have configured in Cerby, retrieve the code from the Cerby extension, the Cerby mobile app, or the **Shared Inbox** in the Cerby web app.

If you still encounter the error, use one of the recovery or backup codes you saved previously in Cerby. To retrieve a code, you must complete the following steps:

  1. Click the **Settings** icon of the corresponding Instagram account card in the Cerby web app. The **Settings** tab is displayed on the account details page.
  2. Click the **View Codes** button located in the **Emergency Controls** section. The **Confirm your identity to continue** dialog box is displayed.
  3. Click the **It’s me!** button in the **Confirmation Request** screen of the Cerby mobile app to confirm your identity. The dialog box in the Cerby web app closes, and the **View MFA Backup Codes** dialog box is displayed with the codes.

**IMPORTANT:** Remember to use only a recovery or backup code once. If you need to generate a new set of codes, follow the instructions in the [How you can use a recovery code on Instagram](https://help.instagram.com/1006568999411025) official documentation, and save the new codes in Cerby, as described in the Manual MFA enrollment section.
