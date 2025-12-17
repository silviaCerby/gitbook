---
description: This article describes how to turn on multi-factor authentication (MFA) with a Cerby-managed email address for your account.
intercom_id: 11888742
---

# Turn on MFA with a Cerby-managed email address for your account

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* **Account Owners**
* Only supported using the Cerby web app

**IMPORTANT:** If you use local vaults, you must have already set up at least one [trusted session](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/trusted-devices/set-up-trusted-sessions-on-your-devices) on your devices.


{% endhint %}

As an account **Owner** , you can enhance your account's security and streamline your login by turning on multi-factor authentication (MFA) with a Cerby-managed email address.

When configured as an MFA method, verification codes sent via email are securely routed to your dedicated in-platform Shared Inbox. Cerby retrieves these codes to perform automated logins for you and all users with shared access to your account.

Beyond email-based MFA, Cerby also offers a central feature for [turning on MFA automatically with Cerby as an authenticator app](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/turn-on-mfa-with-cerby-as-an-authenticator-app-for-your-account-using-the-web-app). With one click, Cerby executes an automation to perform the configuration behind the scenes. When MFA is on, Cerby provides time-based one-time passwords (TOTPs) for automated logins.

While Cerby recommends using its authenticator app feature for MFA when supported, some applications may only offer email-based MFA or allow for primary and secondary methods. In such cases, the Cerby-managed email address serves as a reliable and secure secondary MFA method.

* * *

## Requirements

The following are the requirements to turn on MFA with a Cerby-managed email address:

  * A Cerby workspace
  * A Cerby user account with the workspace **Owner** , **Super** **Admin** , **Admin** , or **User** role
  * An account in an app or service provider
  * An account added to Cerby to which you have the **Owner** role
  * A Cerby-managed email address already associated with your account. For instructions, read the article [Set up and associate a Cerby-managed email address for your account](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/set-up-and-associate-a-cerby-managed-email-address-for-your-account)
* * *

## Turn on MFA with a Cerby-managed email address for your account

To turn on MFA with a Cerby-managed email address for your account, you must complete the following steps:

  1. Log in to your account using the app or service provider.
  2. Navigate to the MFA or two-factor authentication (2FA) section in the account security settings.
  3. Activate or select the option to turn on MFA.
  4. Select email address as the MFA verification method.
  5. Enter the Cerby-managed email address.
  6. Verify the email address when prompted.

  **IMPORTANT:** You must enter a verification code to complete the configuration process. If you had previously set up auto-forward, the email with the code will be sent to the selected recipients; if you didn’t set it up, complete the instructions in the article [Forward a message from your Cerby inbox](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/forward-a-message-from-your-cerby-inbox) to forward you the message.

Now you are done.
