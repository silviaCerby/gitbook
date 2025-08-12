# Troubleshooting: Common issues with X (Twitter)

**Description:** This article describes how to troubleshoot the most common issues with accessing and managing your X (Twitter) account through Cerby.

This article helps you fix the most common issues with accessing and managing
your X (Twitter) account through Cerby.

The following are the most common issues:

  * New login location

  * Turning on MFA manually

  * Cerby mobile app behavior

  * Cerby-managed phone number support

  * Email Swap

  * Invalid MFA verification code

The following sections describe each issue and, if applicable, the proposed
solution.

* * *

# **New login location**

When an X account added to Cerby doesn’t have multi-factor authentication
(MFA) turned on, X displays a dialog box that prompts you to enter a
verification code when you try to log in automatically from Cerby, as shown in
**Figure 1**.

![](gitbook/imagesAhBtkj1RD2dUrptliNvjKTFf_gfNCKIg3guLoF_6I7AQCAfGxh7py4ORiAbQOjb6au_ERi-
_UAsaC5iF8mPbspYjyZ8R7RBg7Z9e_YYcezMEguYVo3yMISO_ZTllgvySj8ey_zjMlWZ0M6s8Hg8265S8ISIAVlwJ5j6viDXDArFhbLz4z4KmImPsDg)

**Figure 1. X Verification Dialog Box**

With this dialog box, X validates the login attempt by sending a verification
code to the registered email address and verifying the location of the login
attempt.

When Cerby does not manage the email address, we cannot enter the verification
code automatically, and the automation workflow is interrupted. Therefore, you
cannot log in unless you retrieve the verification code from the registered
email address.

## Solution

To solve the login attempt prompt, Cerby recommends using a Cerby-managed
email address so that we can enter the verification code automatically. This
code is sent to and retrieved from your Shared Inbox in Cerby.

For instructions on configuring a Cerby-managed email address, refer to the
article [Set up and associate a Cerby-managed email address for your
account](https://help.cerby.com/en/articles/11888658-set-up-and-associate-a-
cerby-managed-email-address-for-your-account).

* * *

# **Turning on MFA manually**

X is one of the [apps
supported](https://help.cerby.com/en/articles/6263064-which-apps-and-
automation-workflows-are-supported-by-cerby) by Cerby. It has an automation
workflow that turns on multi-factor authentication (MFA) by simply activating
a switch in the **Settings** tab of your account details page. Through this
automation, Cerby is configured as an authenticator app.

To execute the workflow successfully, you must create and configure a Cerby-
managed email address in your X account to receive verification codes. If your
business needs prevent you from using a Cerby-managed email address, you can
turn on MFA manually.

You can use this manual configuration with your web browser or the X mobile
app. However, Cerby recommends using your web browser on a computer so you can
scan the QR code displayed on the screen with your Cerby mobile app.

{% hint style="info" %} **NOTE:** To turn on MFA manually, follow the
instructions in the video [Turn on MFA manually for your
accounts](https://help.cerby.com/en/articles/6393776-video-how-to-manually-
enable-2fa-for-an-account) or the article [How to use multi-factor
authentication](https://help.twitter.com/en/managing-your-account/two-factor-
authentication) in the X Help Center. {% endhint %}

After turning on MFA and configuring Cerby as an authenticator app, your login
experience improves. Verification codes are automatically distributed to all
account members and auto-filled when they log in to X from Cerby as follows:

  * When logging in from the Cerby web app, the Cerby browser extension enters the verification code as part of the automated task. 

  * When logging in through the X mobile app, the verification code is copied to the clipboard by using the autofill feature. For more information, see the Cerby mobile app behavior section. 

* * *

# **Cerby mobile app behavior**

The Cerby mobile app helps you easily log in to your apps by autofilling the
credentials of the X account you added to Cerby. Just open the login screen of
the X app on your mobile phone and use autofill on every input field according
to your operating system (iOS or Android).

When MFA is on, you may have to enter a verification code on an additional
screen after autofilling your credentials. Perform the following actions to
retrieve the code according to your verification method:

  * **Cerby as an authenticator app:** When autofill is enabled on your mobile phone, the verification code is automatically copied to the clipboard. Tap the **Paste** button to fill in the verification code field. 

**NOTE:** If autofill is not enabled or the code is not automatically copied
to the clipboard, copy the verification code from the **MFA Code** section.
This section is located in the account details screen using the Cerby mobile
app.

  * **Cerby-managed phone number:** The verification code is sent to the **Shared Inbox** , and you can retrieve it through the Cerby web app. For more information on the **Shared Inbox** , see the article [How to forward a message from your Cerby inbox](https://help.cerby.com/en/articles/6119548-how-to-forward-a-message-from-your-cerby-inbox).

* * *

# **Cerby-managed phone number support**

Cerby provides and manages securely generated phone numbers you can use for
your X accounts and across your organization.

By managing this service, Cerby can improve the login process for X by
automatically filling in your verification codes when MFA is on, with the
phone number as a verification method. You can retrieve these codes from your
**Shared Inbox** in Cerby.

However, X changed the way users update the phone number associated with their
accounts by requesting that they send an SMS with a random code generated by
X.

Given this scenario, Cerby stopped supporting phone numbers for X accounts.
Accounts with an existing Cerby-managed phone number associated and configured
in X will continue working as expected.

* * *

# **Email swap**

When you automatically swap the email address of your X account, X can take up
to 24 hours to propagate the change. This situation occurs whether you change
it automatically by creating a Cerby-managed email address or manually from
your account settings on X.

X displays the email address field as empty in your account settings during
this time. Cerby recommends waiting until X updates the information. Then, you
can continue making other configuration changes.

* * *

# **Invalid MFA verification code**

Sometimes, when you log in automatically to your X account from Cerby and have
MFA on, X shows an error indicating that the verification code is incorrect,
even when it is correct.

## Solution

If you encounter the invalid MFA verification code error, Cerby recommends you
to enter the verification code manually. Depending on the verification method
you have configured in Cerby, retrieve the code from the Cerby extension, the
Cerby mobile app, or the **Shared Inbox** in the Cerby web app.

