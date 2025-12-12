---
description: This article describes how to turn on multi-factor authentication (MFA) with a Cerby-managed phone number for your account.
---

# Turn on MFA with a Cerby-managed phone number for your account

{% hint style="info" %}


**Who can use this feature?**

  * Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
  * **Account Owners**
  * Only supported using the Cerby web app

**IMPORTANT:** If you use local vaults, you must have already set up at least one [trusted session](https://help.cerby.com/en/articles/8142370-set-up-trusted-sessions-on-your-devices) on your devices.


{% endhint %}

As an account **Owner** , you can enhance your account's security and streamline your login by turning on multi-factor authentication (MFA) with a Cerby-managed phone number.

When configured as an MFA method, verification codes sent via SMS are securely routed to your dedicated in-platform Shared Inbox. Cerby retrieves these codes to perform automated logins for you and all users with shared access to your account.

Beyond SMS-based MFA, Cerby also offers a central feature for turning on MFA automatically with Cerby as an authenticator app. With one click, Cerby executes an automation to perform the configuration behind the scenes. When MFA is on, Cerby provides time-based one-time passwords (TOTPs) for automated logins.

While Cerby recommends using its authenticator app feature for MFA when supported, some applications may only offer SMS-based MFA or allow for primary and secondary methods. In such cases, the Cerby-managed phone number is a reliable and secure secondary MFA method.

* * *

# Requirements

The following are the requirements to turn on MFA with a Cerby-managed phone number:

  * A Cerby workspace
  * A Cerby user account with the workspace **Owner** , **Super** **Admin** , **Admin** , or **User** role
  * An account in an app or service provider
  * An account added to Cerby to which you have the **Owner** role
  * A Cerby-managed phone number already associated with your account. For instructions, read the article [Set up and associate a Cerby-managed phone number for your account](https://help.cerby.com/en/articles/11889035-set-up-and-associate-a-cerby-managed-phone-number-for-your-account)
* * *

# Turn on MFA with a Cerby-managed phone number for your account

To turn on MFA with a Cerby-managed phone number for your account, you must complete the following steps:

  1. Log in to your account using the app or service provider.
  2. Navigate to the MFA or two-factor authentication (2FA) section in the account security settings.
  3. Activate or select the option to turn on MFA.
  4. Select phone number or SMS as the MFA verification method.
  5. Enter the Cerby-managed phone number.
  6. Verify the phone number when prompted.

**IMPORTANT:** You must enter a verification code to complete the configuration process. To retrieve the code, look for the SMS received in the Shared Inbox or account inbox. For instructions, read the article [View the messages sent to a Cerby-managed email address or phone number](https://help.cerby.com/en/articles/11889348-view-the-messages-sent-to-a-cerby-managed-email-address-or-phone-number).

Now you are done.
