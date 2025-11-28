# Turn off MFA with Cerby as an authenticator app for your account using the web app

**Description:** This article describes how to turn off Cerby as your authenticator app for your account.

{% hint style="info" %} **Who can use this feature?** * Workspace**Owners** ,
**Super Admins** , **Admins** , and **Users** * **Account Owners** * Supported
using the Cerby web app {% endhint %}

As an account **Owner** , you can turn off multi-factor authentication (MFA)
with Cerby as an authenticator app for your account.

To turn off MFA with Cerby as an authenticator app for your account, you have
the following options:

  * Turn off MFA automatically

  * Turn off MFA manually

The following sections describe the setup for each option.

* * *

# **Turn off MFA automatically**

To turn off MFA automatically using Cerby, you must complete the following
steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.

  2. Click the corresponding account card. The account details page is displayed with the **Settings** tab activated.

  3. Expand the **Multi-factor authentication (MFA) settings** section.

  4. Click the **Turn off** button in the **Turn on MFA automatically** section. The **Confirm your identity to continue** dialog box is displayed.

  5. Confirm your identity using one of [Cerby's multi-factor authentication methods](https://help.cerby.com/en/articles/9462605-set-up-your-identity-with-cerby-s-mfa-methods). The **Turn off MFA?** dialog box is displayed.

  6. Click the **Turn off MFA Automatically** button.

     * If you are using a local vault for your account, the **Transfer to a Cloud Vault** dialog box is displayed.

       1. Click the **Confirm** button. A success message indicates that the account has been temporarily assigned to a cloud vault.

       2. Click the **Turn off** button in the **Turn on MFA automatically** section again.

A message is displayed indicating that Cerby is turning off MFA for your
account; when the automation is complete, a success message is displayed.

{% hint style="info" %} **NOTE:** You can see the status of the automation job
to turn off MFA in the [Automation
Log](https://help.cerby.com/en/articles/11642287-explore-the- automation-log).
{% endhint %}

Now you are done.

* * *

# **Turn off MFA manually**

To turn off MFA manually using Cerby, you must complete the following steps:

  1. Turn off MFA manually in your app

  2. Turn off MFA manually in Cerby

Now you are done.

## **1\. Turn off MFA manually in your app**

To turn off MFA manually in your app, you can complete the following steps:

{% hint style="danger" %} **IMPORTANT:** Refer to your app’s official
documentation for the accurate steps to turn off using an authenticator app
for your account. {% endhint %}

  1. Log in to your account using the app or service provider.

  2. Navigate to the MFA page in your app settings.

  3. Select the option to turn on MFA by scanning a QR code. A QR code is displayed.

  4. Select the option to disable or remove the authenticator app.

  5. Verify your identity.

  6. Confirm the removal. 

**NOTE:** Some platforms may send you a confirmation email or display a final
prompt.

  7. Check that no authenticator app is needed to log in to your account.

The next step is 2\. Turn off MFA manually in Cerby.

## **2\. Turn off MFA manually in Cerby**

To turn off MFA manually in Cerby, you can complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.

  2. Click the corresponding account card. The account details page is displayed with the **Settings** tab activated.

  3. Expand the **Multi-factor authentication (MFA) settings** section.

  4. Click the **Turn off** button in the **Cerby authenticator app** section. The **Confirm your identity to continue** dialog box is displayed.

  5. Confirm your identity using one of [Cerby's multi-factor authentication methods](https://help.cerby.com/en/articles/9462605-set-up-your-identity-with-cerby-s-mfa-methods). The **Turn off MFA?** dialog box is displayed.

  6. Select the **I have turned MFA off in your app’s settings** checkbox. 

  7. Click the **Turn off MFA** button. The dialog box closes, and a success message is displayed.

Now you are done.

