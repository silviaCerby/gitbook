---
description: "This article describes how to automatically turn on MFA for an account using the Cerby web app, setting Cerby as an authenticator app."
intercom_id: 13748418
---

# Turn on MFA automatically for an account using the Cerby web app

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super Admins** , **Admins** , and **Users**
* Account **Owners**
* Only supported using the Cerby web app


{% endhint %}

As the **Owner** of an account for a supported [managed app](https://help.cerby.com/en/articles/8708338-explore-accounts#h_f0a859b407), you can turn on multi-factor authentication (MFA) automatically to add a second layer of protection to your account.

This is a one-click experience in the Cerby web app, where Cerby runs an automated task to configure MFA server-side. When complete, Cerby is set as an authenticator app to generate and distribute time-based one-time passwords (TOTPs) for your account, and fill them in during automated logins.

To turn on MFA for an account automatically using the Cerby web app, you must complete the following steps:

{% hint style="danger" %}


**IMPORTANT:** Make sure MFA is off for your account in your app settings.


{% endhint %}

1. Log in to your [Cerby](https://app.cerby.com/) workspace.
2. Click the corresponding account card. The account details page is displayed with the **General** tab activated.
3. Expand the **Multi-factor authentication (MFA) settings** section.
4. Click the **Turn on** button in the**Cerby authenticator app** section. The **Turn on MFA** dialog box is displayed.
5. Select the **I’ve verified that MFA is off for this account** option.
6. Click the **Turn on MFA** button. The dialog box closes, a status message box is displayed, and Cerby runs the automated task. When the automation is complete, a success message box is displayed.

{% hint style="success" %}


**TIP:** You can review the progress of this task in the **[Automation Log](https://help.cerby.com/en/articles/11642287-explore-the-automation-log)** by selecting the **Automation Log** option from the left menu in the Cerby web app dashboard and looking for the corresponding automation job.


{% endhint %}{% hint style="info" %}


**NOTE:** When completed and supported, the account backup or recovery codes are also automatically saved in Cerby, and you can see them in the **Emergency controls** section of the account details page. For instructions to do it manually, read the article [Save the backup or recovery codes of your account](https://help.cerby.com/en/articles/12748253-save-the-backup-or-recovery-codes-of-your-account).


{% endhint %}

Now you are done.
