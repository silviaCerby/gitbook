---
description: "This article describes how to manually turn off MFA for an account where Cerby is set as an authenticator app."
intercom_id: 11880506
---

# Turn off MFA with Cerby authenticator for an account using the web app

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* **Account Owners**
* Supported using the Cerby web app


{% endhint %}

As an account **Owner** , you can turn off multi-factor authentication (MFA) manually for your account.

This experience is intended for scenarios where the automated task to turn off MFA cannot be completed or is not supported, either because it involves a [self-managed account](https://help.cerby.com/en/articles/8708338-explore-accounts#h_079d120056) or the app requires manual intervention due to recent user interface (UI) updates. When complete, your account will lack a second layer of protection.

{% hint style="danger" %}


**IMPORTANT:** Cerby recommends keeping MFA on at all times and only turning it off temporarily for specific operational tasks


{% endhint %}

To turn off MFA with Cerby authenticator for an account using the web app, you must complete the following main steps:

1. [Turn off MFA manually in your app](turn-off-mfa-with-cerby-authenticator-for-an-account-using-the-web-app.md#id-1.-turn-off-mfa-manually-in-your-app)
2. [Turn off MFA manually in Cerby](turn-off-mfa-with-cerby-authenticator-for-an-account-using-the-web-app.md#id-2.-turn-off-mfa-manually-in-cerby)

The following sections describe each main step.

* * *

## 1\. Turn off MFA manually in your app

To turn off MFA manually in your app, complete the following steps:

{% hint style="danger" %}


**IMPORTANT:** Refer to your app’s official documentation for the accurate steps to turn off MFA for accounts with an authenticator app as the verification method.


{% endhint %}

  1. Log in to your account through the app’s login page.
  2. Navigate to the MFA page in your app settings.
  3. Select the option to turn off or remove the authenticator app as the MFA method.
  **NOTE:** Some platforms may send you a confirmation email or display a final prompt.

  4. Check that no authenticator app is no longer needed to log in to your account.

The next step is [2. Turn off MFA manually in Cerby](turn-off-mfa-with-cerby-authenticator-for-an-account-using-the-web-app.md#id-2.-turn-off-mfa-manually-in-cerby).

* * *

## 2\. Turn off MFA manually in Cerby

To turn off MFA manually in Cerby, complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Click the corresponding account card. The account details page is displayed with the **Settings** tab activated.
  3. Expand the **Multi-factor authentication (MFA) settings** section.
  4. Click the **Turn off** button in the **Cerby authenticator app** section. The **Confirm your identity to continue** dialog box is displayed.
  5. Confirm your identity using one of [Cerby's multi-factor authentication methods](https://help.cerby.com/en/articles/9462605-set-up-your-identity-with-cerby-s-mfa-methods). The **Turn off MFA?** dialog box is displayed.
  6. Select the **I have turned MFA off in your app’s settings** option.
  7. Click the **Turn off MFA** button. The dialog box closes, and a success message is displayed.

Now you are done.
