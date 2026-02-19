---
intercom_id: 10755356
description: >-
  This document describes how to log in to the Cerby browser extension to access
  your workspace and manage your items.
---

# Log in to the Cerby browser extension

{% hint style="info" %}
**Who can use this feature?**

* Workspace **Owners** , **Super Admins** , **Admins** , **Users** , **Guest Users** , and **Login-Only** users
{% endhint %}

As a user with any workspace role, you can log in to the Cerby browser extension to access your workspace and manage your items.

The extension is an add-on for web browsers that complements your user experience. For example, you can log in automatically to your accounts or autosave your accounts in Cerby. For more information about how the extension works and the supported features, read the article [Explore the Cerby browser extension](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-the-cerby-browser-extension).

The login process is different for workspaces integrated or federated with an identity provider (IdP) such as Okta or Entra ID, with social login or third-party authentication such as Google, and [local user workspaces](https://cerby-test.gitbook.io/cerby-test/management/identity-providers-idps/local-workspace/create-and-configure-a-local-user-workspace):

* **IdP-based or federated workspaces:** All users, except Guest Users, authenticate via single sign-on (SSO) through their corporate login portal. Guest Users authenticate with login credentials managed by Cerby.
* **Social login or third-party authentication:** All users authenticate via single sign-on (SSO) through their external identity portal.
* **Local user workspaces:** All users authenticate with login credentials managed by Cerby.

This article describes how to log in to the Cerby browser extension; it also includes a section on how to [log out of the extension](log-in-to-the-cerby-browser-extension.md#log-out-of-the-cerby-browser-extension).

***

## Requirements

The following are the requirements to log in to the Cerby browser extension:

* The Cerby browser extension must be installed in your web browser:
  * If your organization uses a Mobile Device Management (MDM) solution, the extension may already be installed on your computer
  * If you need to install it manually, complete the instructions in the article Install the Cerby browser extension
* A Cerby workspace
* A Cerby user account with the workspace **Owner** , **Super** **Admin** , **Admin** , **User** , **Guest User** , or **Login-Only** role

***

## Log in to the Cerby browser extension

The process to add a secret manually is different depending on the Cerby client app you use:

* [IdP-based or federated workspaces](log-in-to-the-cerby-browser-extension.md#idp-based-or-federated-workspaces)
* [Social login or third-party authentication](log-in-to-the-cerby-browser-extension.md#social-login-or-third-party-authentication)
* [Local user workspaces](log-in-to-the-cerby-browser-extension.md#local-user-workspaces)

{% hint style="info" %}
**NOTE:** If you have logged in to the Cerby web app and your session in this client app is active, the Cerby browser extension detects your session and logs you in automatically. You only need to complete step 1 and its corresponding substeps.
{% endhint %}

The following sections describe each process.

### IdP-based or federated workspaces

To log in to the Cerby browser extension in IdP-based or federated workspaces, you must complete the following steps:

1. Open the Cerby browser extension popup from the extensions or add-ons section. Based on previous logins or organization prefill, one of the following pages is displayed:
   * **Welcome to Cerby** page
     1. Click the **Log in** button. The **Let's find your workspace** page is displayed on the popup.
     2. Enter the name of your workspace.
     3. Click the **Next** button. An authentication waiting page is displayed on a new browser tab, as shown in **Figure 1**.

![](.gitbook/assets/AD_4nXdAFUFC-9FWY_OHGR7UOEkJJtttFumCFSWTqcCn-7rZA2jMeXe7rv0m6verYqFWs6mpkN35loFzPmvkKwqh0qnIPXqDyNiRVOYQP8XUiLKTzqtQImgPSbEqY35ypim2ES2L2kfpow.png)

**Figure 1.** Authentication waiting page

```
 * **Hi there!** page

   1. Click the **Log in** button of your workspace. An authentication waiting page is displayed on a new browser tab, as shown in **Figure 1**.

   **IMPORTANT:** If you have a **Guest User** role, proceed to the next step right away. After a few seconds, you will be redirected to the corporate login portal, and you must start from step 1.
```

2\. Click the button of your authentication method based on your workspace role:

```
 * **Owner** , **Super** **Admin** , **Admin** , **User** , and **Login-Only**

   1. Click the **SSO Login** button. Your corporate login portal is displayed.

 * **Guest User**

   1. Click the **Log in as a guest user** button. The Cerby login portal is displayed.
```

3\. Authenticate with your login credentials. 4. Provide your multi-factor authentication (MFA) verification code, if applicable. The browser tab closes.

Now you are done.

### Social login or third-party authentication

To log in to the Cerby browser extension in workspaces with social login or third-party authentication, you must complete the following steps:

1. Open the Cerby browser extension popup from the extensions or add-ons section. Based on previous logins or organization prefill, one of the following pages is displayed:
   * **Welcome to Cerby** page
     1. Click the **Log in** button. The **Let's find your workspace** page is displayed on the popup.
     2. Enter the name of your workspace.
     3. Click the **Next** button. The external identity portal is displayed on a new browser tab, as shown in **Figure 2** for Google.

![](.gitbook/assets/AD_4nXfNwPT4bYvvArlBwbeeZg7qjxMawLeiPBNRCuV6zs-ksWx1zrXftqy--HBPsssdGU-MDj0klgrznSh58hMRbDqvUVR-B0yHZRcBwcMnD60IAWezQJ87aYqM400a7qRUAyUu2QNSPA.png)

**Figure 2.** Google identity portal

```
 * **Hi there!** page

   1. Click the **Log in** button of your workspace. The external identity portal is displayed, as shown in **Figure 2** for Google.
```

2\. Select an account to authenticate from the list of accounts with an active session.

**NOTE:** If you don’t have active sessions, you must log in to the third-party authentication platform.

3. Confirm the permissions and access to grant to Cerby on your account. The browser tab closes.

Now you are done.

### Local user workspaces

To log in to the Cerby browser extension in local user workspaces, you must complete the following steps:

1. Open the Cerby browser extension popup from the extensions or add-ons section. Based on previous logins or organization prefill, one of the following pages is displayed:
   * **Welcome to Cerby** page
     1. Click the **Log in** button. The **Let's find your workspace** page is displayed on the popup.
     2. Enter the name of your workspace.
     3. Click the **Next** button. The Cerby login portal is displayed, as shown in **Figure 3**.
   * **Hi there!** page
     1. Click the **Log in** button of your workspace. The Cerby login portal is displayed, as shown in **Figure 3**.

![](.gitbook/assets/AD_4nXf28iFxH19Xv5kvltU4jYP6dJQaBTNn9KyJ0HUdW6GeFgod8R5eRD-APxYArfL0jvllmWJWHORxhT34XRPrcSKavXgDTf9PBSeV6kgbIZw3tMKIxcFD9rfjetOEoCz7pUAaq-pBmQ.png)

**Figure 3.** Cerby login portal

2. Authenticate with your login credentials.
3. Provide your multi-factor authentication (MFA) verification code, if applicable. The browser tab closes.

Now you are done.

***

## Log out of the Cerby browser extension

To log out of the Cerby browser extension, you must complete the following steps:

1. Open the Cerby browser extension popup from the extensions or add-ons section.
2. Click the user profile menu located at the top right. The**My profile** page is displayed.
3. Click the **Log Out** button.

Now you are done.
