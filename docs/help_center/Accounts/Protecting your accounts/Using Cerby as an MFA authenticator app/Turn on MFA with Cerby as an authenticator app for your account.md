# Turn on MFA with Cerby as an authenticator app for your account

**Description:** This article describes how to turn on MFA with Cerby as an authenticator app for your account.

{% hint style="info" %} **Who can use this feature?** * Workspace**Owners** ,
**Super Admins** , **Admins** , and **Users** * **Account Owners** * Supported
using the Cerby web app {% endhint %}

As an account **Owner** , you can configure Cerby as an authenticator app to
centrally manage multi-factor authentication (MFA) for your accounts.

Unlike traditional authenticator apps tied to a single device or user, Cerby
generates and securely distributes time-based one-time passwords (TOTPs) to
all users with shared access to the account.

When MFA is turned on with this verification method, Cerby fills in the six-
digit security codes required during login. Therefore, you can reduce manual
overhead, eliminate the need to share physical devices, and ensure consistent
access for all users with account permissions, while maintaining a secure
authentication process.

* * *

# **Requirements**

The following are the requirements to set up and associate Cerby as your
authenticator app for your account:

  * A Cerby workspace

  * A Cerby user account with the workspace **Owner** , **Super** **Admin** , **Admin** , or **User** role

  * An account in an app or service provider

  * An account added to Cerby to which you have the **Owner** role

* * *

# **Turn on MFA with Cerby as an authenticator app for your account**

Cerby supports turning on MFA with Cerby as your authenticator app using the
following methods:

  * **Automatic setup (for supported apps):** For supported managed apps, Cerby can automatically turn on MFA without requiring manual input. With one click, Cerby handles the entire setup process for you in the background.

  * **Manual setup:** For apps that don’t support automation to turn on MFA, you can manually turn it on by entering a secret key from the app’s settings page and completing the setup in Cerby.

The following sections describe the setup for each option.

## **Automatic setup**

For [supported apps](https://help.cerby.com/en/articles/6263064-which-apps-
and-automation-workflows-are-supported-by-cerby), you can turn on MFA
automatically with a single click by completing the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.

  2. Click the corresponding account card. The account details page is displayed.

  3. Expand the **Multi-factor authentication (MFA) settings** section.

  4. Click the **Turn on** button in the**Cerby authenticator app** section. The **Turn on MFA** dialog box is displayed.

  5. Select the **I’ve verified that MFA is off for this account** checkbox.

  6. Click the **Turn on MFA** button. A message indicating that Cerby is turning on MFA for your account in the app is displayed.   
**NOTE:** You can see the automation status in the [Automation
Log](https://help.cerby.com/en/articles/11642287-explore-the-automation-log).

Now you are done.

## **Manual setup**

For self-managed apps and [managed
apps](https://help.cerby.com/en/articles/6263064-which-apps-and-automation-
workflows-are-supported-by-cerby) that don’t support automation to turn on
MFA, you can turn it on manually by completing the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.

  2. Click the corresponding account card. The account details page is displayed.

  3. Expand the **Multi-factor authentication (MFA) settings** section.

  4. Click the **Set as MFA** button in the **Cerby authenticator app** section. The **Save Code** dialog box is displayed.

  5. Retrieve a secret key from your app by completing the following steps:

     1. Log in to your account in a separate web browser.

     2. Navigate to the MFA page in your app settings.

     3. Select the option to turn on MFA by scanning a QR code. A QR code is displayed.

     4. Click the **Can’t scan code?** option. A secret key is displayed.

     5. Copy the secret key.

     6. Switch to the browser tab using the Cerby web app.

  6. Paste the secret key in the **Secret Key** field of the **Save Code** dialog box. 

  7. Click the **Save Code** button. A six-digit code is displayed.

  8. Copy the code.

  9. Finish the setup in your app by completing the following steps:

     1. Switch to the browser tab with your app settings.

     2. Paste the code. 

     3. Save the configuration.

  10. Click the **Done** button. The dialog box closes, and a success message box is displayed. 

Now you are done.

