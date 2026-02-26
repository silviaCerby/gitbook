---
description: "This article describes how to automatically turn off MFA for an account where Cerby is set as an authenticator app."
intercom_id: 13748473
---

# Turn off MFA automatically for an account using the web app

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* **Account Owners**
* Supported using the Cerby web app


{% endhint %}

As the **Owner** of an account for a supported [managed app](https://help.cerby.com/en/articles/8708338-explore-accounts#h_f0a859b407), you can turn off multi-factor authentication (MFA) automatically for your account.

This is a one-click experience in the Cerby web app, where Cerby runs an automated task to turn off MFA server-side. When complete, your account will lack a second layer of protection.

{% hint style="danger" %}


**IMPORTANT:** This automated task is only available when Cerby is set as an authenticator app. Cerby recommends keeping MFA on at all times and only turning it off temporarily for specific operational tasks.


{% endhint %}

To turn off MFA for an account automatically using the Cerby web app, you must complete the following steps:

1. Log in to your [Cerby](https://app.cerby.com/) workspace.
2. Click the corresponding account card. The account details page is displayed with the **Settings** tab activated.
3. Expand the **Multi-factor authentication (MFA) settings** section.
4. Click the **Turn off** button in the **Turn on MFA automatically** section. The **Confirm your identity to continue** dialog box is displayed.
5. Confirm your identity by using one of [Cerby's multi-factor authentication methods](https://help.cerby.com/en/articles/9462605-set-up-your-identity-with-cerby-s-mfa-methods). The **Turn off MFA?** dialog box is displayed.
6. Click the **Turn off MFA Automatically** button. The dialog box closes, a status message box is displayed, and Cerby runs the automated task. When the automation is complete, a success message box is displayed.

{% hint style="info" %}


**NOTE:** If your account is stored in a local vault, the **Transfer to a Cloud Vault** dialog box is displayed after step 6. Complete the following steps to continue:

1. Click the **Confirm** button. A success message indicates that the account has been temporarily assigned to a cloud vault.
2. Click the **Turn off** button in the **Turn on MFA automatically** section again


{% endhint %}{% hint style="success" %}


**TIP:** You can review the progress of this task in the **[Automation Log](https://help.cerby.com/en/articles/11642287-explore-the-automation-log)** by selecting the **Automation Log** option from the left menu in the Cerby web app dashboard and looking for the corresponding automation job.


{% endhint %}

Now you are done.
