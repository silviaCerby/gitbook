# Troubleshooting: Common issues with TikTok

**Description:** This article describes how to troubleshoot the most common issues with accessing and managing your TikTok account through Cerby.

This article helps you fix the most common issues with accessing and managing
your TikTok account through Cerby.

The following are the most common issues:

  * Too many login attempts

  * Not receiving codes in the Shared Inbox

  * Manual MFA enrollment

  * Cerby mobile app behavior

  * Email swap

The following sections describe common scenarios that can confuse and, if
applicable, a proposed solution.

* * *

# **Too many login attempts**

TikTok may display the "Too many attempts. Try again later" message and
temporarily restrict access to your account in the following scenarios:

  * When you log in multiple times to your TikTok account from Cerby using the same web browser on your computer and mobile phone.

  * When you log out of one account and try to log in to another TikTok account using the web browser.

  * When you try to rotate the password automatically from Cerby for an account with an active session but without user activity for multiple weeks.

## Solution

To solve the too many login attempts issue, you can perform the following
actions depending on the device you use:

  * Web browser on your computer

    * Use an alternative browser to log in to the account

**IMPORTANT:** Make sure to have installed the corresponding Cerby browser
extension:

      * [Firefox](https://addons.mozilla.org/en-US/firefox/addon/cerby-s-browser-extension/)

      * [Google Chrome](https://chrome.google.com/webstore/detail/cerbys-browser-extension/clccplmaaeihbagbefjinmclielobnkb)

      * [Microsoft Edge](https://microsoftedge.microsoft.com/addons/detail/cerbys-browser-extension/bbaiiaogfdgpbapebajffliefkfipoif)

      * [Safari](https://apps.apple.com/mx/app/cerby-web-extension/id1581820030?l=en&mt=12)

    * Wait a couple of hours before retrying to log in

  * TikTok mobile app on your mobile phone

    * Wait one or more days before retrying to log in

* * *

# **Not receiving codes in the Shared Inbox**

When you have configured a Cerby-managed email address or phone number in your
TikTok account, whether you have MFA turned on or not, TikTok may take some
time to send a verification code when logging in or rotating the password
automatically. Therefore, no message is sent and stored in your **Shared
Inbox** in Cerby.

## Solution

To solve the issue with not receiving verification codes, Cerby recommends
waiting the 60 seconds suggested by TikTok before retrying to send a code.
Sometimes, TikTok queues multiple messages and sends them all at once.

* * *

# **Manual MFA enrollment**

TikTok is one of the [apps
supported](https://help.cerby.com/en/articles/6263064-which-apps-and-
automation-workflows-are-supported-by-cerby) by Cerby, with an automation
workflow to turn on multi-factor authentication (MFA) by simply activating a
switch in the **Settings** tab of the account details page.

When you have turned on MFA with a verification method managed by Cerby, your
logging-in experience improves. Verification codes are automatically
distributed to all account members and auto-filled when they log in to TikTok
from Cerby as follows:

  * **Logging in through the Cerby web app:** The verification code is entered automatically as part of the workflow. 

  * **Logging in through the TikTok mobile app:** You can copy the verification code from the Cerby mobile app. For more information, see the Cerby mobile app behavior section.

To execute the automation workflow successfully, you must have created and
configured a Cerby-managed email address in your TikTok account to receive
verification codes. If your business needs prevent you from using a Cerby-
managed email address or phone number, you can enroll MFA manually.

To turn on MFA manually, follow the instructions in the How to turn on MFA in
TikTok manually [video](https://help.cerby.com/en/articles/6489438-video-how-
to-turn-on-2fa-in-tiktok-manually) or
[article](https://help.cerby.com/en/articles/5955049-how-to-turn-on-2fa-in-
tiktok-manually).

{% hint style="danger" %} **IMPORTANT:** You can only go through this manual
configuration with your TikTok mobile app. {% endhint %}

* * *

# **Cerby mobile app behavior**

The Cerby mobile app helps you easily log in to your apps by auto-filling the
credentials of the TikTok account you added to Cerby. To log in, complete the
following steps:

  1. Open the login screen of the TikTok app on your mobile phone.

  2. Auto-fill your credentials on every input field using Cerby.

  3. Enter the verification code if TikTok prompts you to do so. Perform one of the following actions to retrieve the code for a Cerby-managed email address or phone number configured as MFA verification method:

     * Open the **Shared Inbox** view in the Cerby web app to access the message sent via email or SMS. For more information on the **Shared Inbox** , see the corresponding section in the article [View the messages sent to a Cerby-managed email address or phone number](https://help.cerby.com/en/articles/11889348-view-the-messages-sent-to-a-cerby-managed-email-address-or-phone-number).

     * Open the TikTok account details in the Cerby mobile app to copy the verification code from the **MFA Code** section.

{% hint style="info" %} **NOTE:** For more information on the logging-in
process, see the [Log in to your accounts using the Cerby mobile
app](https://help.cerby.com/en/collections/10147549-log-in-to-your-accounts-
using-the-cerby-mobile-app) collection. {% endhint %}

* * *

# **Email swap**

When you manually swap the email address of your TikTok account for a Cerby-
managed email address, make sure to first remove the email address configured
in TikTok.

Leaving this account information blank prevents the process from getting
interrupted if you don’t have access to the original email address, as TikTok
sends a verification code to it.

{% hint style="danger" %} **IMPORTANT:** If you have turned on MFA in TikTok,
turn it off before removing the email address. For instructions, see the [Turn
off MFA](https://help.cerby.com/en/articles/5955049-how-to-turn-on-2fa-in-
tiktok- manually#h_3af5a48c5d) section in the article [Turn on MFA in TikTok
manually](https://help.cerby.com/en/articles/5955049-how-to-turn-on-2fa-in-
tiktok-manually). {% endhint %}

To remove the email address configured TikTok, you must complete the following
steps:

  1. Open the TikTok application on your mobile phone with your account.

  2. Tap the **Profile** button located at the right in the bottom navigation drawer. A screen with your profile is displayed.

  3. Tap the **Menu** icon located at the top right of the screen. A drop-down menu is displayed.

  4. Tap the **Settings and privacy** option from the list. The **Settings and privacy** screen is displayed.

  5. Tap the **Account** button located in the **Account** section. The **Account** screen is displayed.

  6. Tap the **Account information** button. The **Account information** screen is displayed with the **Phone number** and **Email** fields.

  7. Tap the **Email** button. A dialog box is displayed.

  8. Tap the **Unlink email** button. The **Unlink email address?** screen is displayed.

  9. Tap the **Continue to unlink** button. The **Enter 6-digit code** screen is displayed.

  10. Enter the verification code. This code is sent by TikTok to the email address you have configured in TikTok. The **Account information** screen is displayed with the “Email unlinked” message and the **Email** field blank.

Now you are done.

