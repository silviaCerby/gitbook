---
description: This article describes how to set up your IdP to support item imports from LastPass for users who authenticate with SSO.
---

# Set up your IdP to support imports from LastPass with SSO authentication

{% hint style="info" %}


**Who can use this feature?**

  * Workspace **Owners** , **Super Admins** , and **Admins**
  * Only supported using the Cerby web app


{% endhint %}

As a workspace **Owner** , **Super Admin** , or **Admin** , you can enable migrations from LastPass to Cerby for users who authenticate with single sign-on (SSO). You must set up your identity provider (IdP), such as Okta or Entra ID (formerly Azure AD), to support this login method.

{% hint style="danger" %}


**IMPORTANT:** Currently, SSO authentication is only supported using the Cerby browser extension in Chrome and Edge. Therefore, you only perform the setup for these client apps, which must be installed on the end user’s computers.


{% endhint %}

To set up your IdP, you must complete the following steps in your corresponding tenant:

  * Okta

    1. Follow the instructions in the article [Create OIDC app integrations](https://help.okta.com/en-us/content/topics/apps/apps_app_integration_wizard_oidc.htm) to add or edit the **Sign-in redirect URIs** value for the LastPass application.
    2. Enter the following value as the sign-in redirect URI:

       * **`chrome-extension://clccplmaaeihbagbefjinmclielobnkb/lastpass-sso-callback.html`** for Chrome
       * **`chrome-extension://bbaiiaogfdgpbapebajffliefkfipoif/lastpass-sso-callback.html`** for Edge
  * Entra ID

    1. Follow the instructions in the article [Quickstart: Register an application with the Microsoft identity platform](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app?tabs=certificate#configure-platform-settings) to add a**** redirect URI for the LastPass app.
    2. Enter the following value as the redirect URI:

       * **`chrome-extension://clccplmaaeihbagbefjinmclielobnkb/lastpass-sso-callback.html`** for Chrome
       * **`chrome-extension://bbaiiaogfdgpbapebajffliefkfipoif/lastpass-sso-callback.html`** for Edge
  * Google Workspace

    1. Follow the instructions in the article [Setting up OAuth 2.0](https://support.google.com/cloud/answer/6158849?hl=en), topic **Web applications** , to specify an authorized redirect URI for the LastPass entry. The setup is in the [Credentials](https://console.cloud.google.com/project/_/apis/credentials) page of the Google Cloud Console.
    2. Enter the following value as the redirect URI:

       * **`chrome-extension://clccplmaaeihbagbefjinmclielobnkb/lastpass-sso-callback.html`** for Chrome
       * **`chrome-extension://bbaiiaogfdgpbapebajffliefkfipoif/lastpass-sso-callback.html`** for Edge

Now you are done. All workspace users can now import their items from LastPass to Cerby if they log in to LastPass with SSO authentication.
