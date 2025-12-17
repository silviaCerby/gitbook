---
description: "This article describes how to set up and associate a Cerby-managed email address for your account."
intercom_id: 11888658
---

# Set up and associate a Cerby-managed email address for your account

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* **Account Owners**
* Only supported using the Cerby web app

**IMPORTANT:** If you use local vaults, you must have already set up at least one [trusted session](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/trusted-devices/set-up-trusted-sessions-on-your-devices) on your devices.


{% endhint %}

As an account **Owner** , you can set up and associate your account with a Cerby-managed email address. This contact detail in your account settings is central to how Cerby secures and streamlines access to your apps.

With a Cerby-managed email address, all email messages are routed to your dedicated in-platform Shared Inbox, providing a centralized and private channel for all digital communications related to your account.

When used as a multi-factor authentication (MFA) verification method, Cerby retrieves the verification codes sent to the Cerby-managed email address and fills in the codes during automated logins. These codes are shared with all users who have access to your account, enabling automated logins for them as well. For more information, read the article [Turn on MFA with a Cerby-managed email address for your account](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/turn-on-mfa-with-a-cerby-managed-email-address-for-your-account).

{% hint style="info" %}


**NOTE:** Depending on the app requirements and settings, some apps may not support Cerby-managed email addresses.


{% endhint %}

* * *

## Requirements

The following are the requirements to set up and associate a Cerby-managed email address for your account:

  * A Cerby workspace
  * A Cerby user account with the workspace **Owner** , **Super** **Admin** , **Admin** , or **User** role
  * An account in an app or service provider
  * An account added to Cerby to which you have the **Owner** role
* * *

## Set up and associate a Cerby-managed email address for your account

To set up and associate a Cerby-managed email address for your account, you must complete the following main steps:

  1. [Create the Cerby-managed email address](set-up-and-associate-a-cerby-managed-email-address-for-your-account.md#id-1.-create-the-cerby-managed-email-address)
  2. [Associate the Cerby-managed email address with your account](set-up-and-associate-a-cerby-managed-email-address-for-your-account.md#id-2.-associate-the-cerby-managed-email-address-with-your-account)

The following sections describe each main step.

### 1\. Create the Cerby-managed email address

To create the Cerby-managed email address, you must complete the following steps using the Cerby web app:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Click the corresponding account card. The account details page is displayed.
  3. Click the **Protect with Cerby** button that appears when hovering over the **Email Linked to Account** field. The **Add a Cerby-managed email** dialog box is displayed.
​**NOTE:** Depending on the app requirements and settings, some apps may not support Cerby-managed email addresses; in these cases, the **Protect with Cerby** button is not displayed.

  4. Click the**Protect my email address** button. A success message is displayed.
  5. Click the **Set up email address** button. The **Auto-forward messages** dialog box is displayed. You can set up auto-forward now for the messages sent to the Cerby-managed email address or skip the setup:

     * Set up auto-forward

       1. Click the **Set up auto-forward** button. The **Select Recipients** dialog box is displayed.
       2. Select the message recipients:

          * **Me**
          * **All account owners**
          * **All account collaborators**
          * **Selected distribution lists**

          **NOTE:** You can create a distribution list of workspace users by clicking the **Create a new distribution list** button and following the instructions.

       3. (Optional) Activate the **Auto-forward verification code mails** switch if you want the messages with verification codes to be auto-forwarded to the selected recipients.
       4. Click the **Next** button. The **Confirm recipients** dialog box is displayed.
       5. Click the **Confirm** button. A dialog box with the Cerby-managed email address is displayed.

     * Skip auto-forward

       1. Click the **Skip** button. A dialog box with the Cerby-managed email address is displayed.
  6. Click the **Copy** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1646112130/943f4e580296b948de75d9141d52/AD_4nXfZMNhbUGkMK9mNshDwbFm6FTlqzLN1O44uJJHpkmqYF9w2UGZ-6-0XB1einzAYQvKvhIFwJk5pmSc46W3UPOLNFsEFHyz1ho97Ei3J87SbDFCGB0bcslVV5mGyLe4TqHWdlKhG?expires=1754028000&signature=486cef0f6dfc8a33c90be5838241dedf8a1966d8628f19ccc47fb25ab8e0de3d&req=dSYjEMh%2Fn4BcWfMW3Hu4gf%2BRt%2Frtah0aIRB9s8IM15K8ApeiRoS1VT9oHJrz%0AiA%3D%3D%0A" alt="">) icon to copy the email address.
  7. Click the **Confirm** button. The dialog box closes, and the Cerby-managed email address is displayed in the **Email Linked to Account** field.

The next step is [2. Associate the Cerby-managed email address with your account](set-up-and-associate-a-cerby-managed-email-address-for-your-account.md#id-2.-associate-the-cerby-managed-email-address-with-your-account).

### 2\. Associate the Cerby-managed email address with your account

To associate the Cerby-managed email address with your account, you must complete the following steps in your app:

  1. Log in to your account in the app or service provider.
  2. Navigate to the account settings.
  3. Associate the Cerby-managed email address with your account by pasting the email you copied previously and saving the changes.
  4. Verify the new email address, if prompted.

  **NOTE:** Usually, you must enter a verification code to complete the association process. If you had previously set up auto-forward, the email with the code will be sent to the selected recipients; if you didn’t set it up, complete the instructions in the article [Forward a message from your Cerby inbox](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/forward-a-message-from-your-cerby-inbox) to forward you the message.

**IMPORTANT:** Ensure you associate the Cerby-managed email address with your account. If you don’t do it, Cerby cannot retrieve verification codes and streamline your login.
---

Now you are done.
