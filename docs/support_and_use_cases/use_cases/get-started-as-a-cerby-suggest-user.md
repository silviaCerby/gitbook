---
description: This article described the key initial steps you can perform as a Cerby Suggest user.
intercom_id: 8843620
---

# Get started as a Cerby Suggest user

Hi there, welcome to Cerby Suggest!

If you are reading this guide, it means you have started using Cerby Suggest or are interested in knowing more about it. Cerby Suggest is designed to provide recommendations for your organization’s licensed apps when you are signing up for a new account for an app. With Cerby Suggest, you can request IT managers in your organization to grant you access to the suggested app.

The following are the actions you can perform to get started with Cerby Suggest:

* Log in to a workspace
* Install the Cerby browser extension
* Add items to Cerby
* Protect your accounts
* Share your items

The following sections describe each action.

* * *

## Log in to a workspace

The first step to using Cerby is to log in to your workspace.

A workspace is a collaboration environment where organizations manage and secure access to their accounts and collections. After **Workspace Owners** create a workspace, its name is displayed and identified as follows: **< workspace name>.cerby.com**.

The login experience is the same for all the Cerby client apps:

  1. Enter your workspace name when prompted on the login screen or page. The login page of your identity provider (IdP), such as Okta or Entra ID, is displayed.
  2. Enter your credentials and authenticate via single sign-on (SSO).

{% hint style="info" %}


**NOTE:** If your IdP has multi-factor authentication (MFA) enforced, you’ll be prompted to set it up.


{% endhint %}

To see the complete logging process, follow the instructions in the video [How to log in to your Cerby workspace](https://cerby-test.gitbook.io/cerby-test/getting-started/video-how-to-log-in-to-your-cerby-workspace).

{% hint style="danger" %}


**IMPORTANT:** Ensure your IT team has granted you access to Cerby via the SSO integration of your IdP. Also, ask for the workspace name.


{% endhint %}

* * *

## Install the Cerby browser extension

For an optimal user experience, Cerby recommends installing the browser extension.

If your company uses an MDM service, the Cerby browser extension may have already been installed on your computer.

To install it manually, navigate to the website according to your web browser and follow the installation instructions:

* [Firefox](https://addons.mozilla.org/en-US/firefox/addon/cerby-s-browser-extension/)
* [Google Chrome](https://chrome.google.com/webstore/detail/cerbys-browser-extension/clccplmaaeihbagbefjinmclielobnkb)
* [Microsoft Edge](https://microsoftedge.microsoft.com/addons/detail/cerbys-browser-extension/bbaiiaogfdgpbapebajffliefkfipoif)
* [Safari](https://apps.apple.com/mx/app/cerby-web-extension/id1581820030?l=en&mt=12)
* * *

## Add items to Cerby

After you have accessed the Cerby platform, you can start adding items. You can add items in Cerby in the following ways:

* Manually
* At login

The following sections describe each option.

### Manually

The process of adding items to Cerby manually is different depending on the item type:

* Accounts
* Collections

The following sections describe the instructions for each item type.

### Accounts

Accounts are the digital records with the login information (such as username and password) for specific apps or service providers. Each account has its corresponding card in the Cerby dashboard.

When adding an account, you are granted the **Owner** role on it. To add an account manually, follow the instructions in the video [How to add and share an account, and view your account details](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/video-how-to-add-and-share-an-account-and-view-your-account-details).

### Collections

Collections are groups of accounts that you can create to help you keep your items organized, and they help you share items in bulk with other users or teams. Each collection has its corresponding card in the Cerby dashboard.

You can only add to a collection the items to which you have the **Owner** role. When creating a collection, you are granted the **Owner** role on it. To create a collection manually, follow the instructions in the video [How to create and share a collection](https://cerby-test.gitbook.io/cerby-test/management/credential-management/collections/video-how-to-create-and-share-a-collection).

### At login

With Cerby Suggest, you can easily save the credentials you enter to access an app through its login page. By activating the **Save credentials at login** feature, the Cerby browser extension can automatically identify your login attempt and suggest you add the account to Cerby.

To save your credentials at login, follow the instructions in the article [How to save your credentials at login via the Cerby browser extension](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-browser-extension/autosave-an-account-at-login-or-signup-with-the-cerby-browser-extension).

* * *

## Protect your accounts

With Cerby Suggest, you can take the following actions to enhance the security of your accounts:

* Turn on MFA for your accounts
* Generate secure passwords

The following sections describe each action.

### Turn on MFA for your accounts

Cerby recommends always turning on MFA for the accounts that offer such a security method. You can set up Cerby as an authenticator app to provide you with time-based one-time passwords (TOTPs).

By managing this service, Cerby can improve the login process of your apps by automatically filling in the TOTPs you need. You can also copy them using the Cerby browser extension and the Cerby mobile app.

To turn on MFA for your accounts, follow the instructions in the video [How to turn on MFA for your accounts](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/video-how-to-turn-on-mfa-for-an-account-manually). The setup process is performed through the Cerby mobile app.

### Generate secure passwords

With the Password generator feature, available through the browser extension, Cerby Suggest enables you to generate secure passwords anytime by selecting the strength rules applicable to your app or service provider.

After generating the password, you can use it to sign up for a new account and add it to Cerby or to manually rotate the password for your accounts in Cerby and your app.

To generate a password, follow the instructions in the article [How to generate passwords using the Cerby browser extension](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-browser-extension/generate-secure-passwords-using-the-cerby-browser-extension).

* * *

## Share your items

With your items added to Cerby, you can start sharing them. Currently, you have two options to do so:

* Internally with other workspace users
* Externally via a public link

The following sections describe each option.

### Internally with other workspace users

With Cerby Suggest, you can share your items internally with users and teams within your workspace. When sharing any item, you must assign one of the two following roles:

* **Owner:** Your colleagues can view and share the items with other users and edit the item details.
* **Collaborator:** Your colleagues can only view the item details. For accounts, they can only log in to applications.

The process of sharing items is different depending on the item type:

* Accounts
* Collections

The following sections describe the instructions for each item type.

### Accounts

To share an account, follow the instructions in the video [How to add and share an account, and view your account details](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/video-how-to-add-and-share-an-account-and-view-your-account-details).

### Collections

To share a collection, follow the instructions in the video [How to create and share a collection](https://cerby-test.gitbook.io/cerby-test/management/credential-management/collections/video-how-to-create-and-share-a-collection).

### Externally via a public link

With Cerby Suggest, you can share your items with external collaborators via a public link. This account access grant is temporary because you can set an expiration time and one-time access.

To share accounts with external collaborators, follow the instructions in the article [How to share items with external users via a link](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/share-items-with-external-users-via-a-link).
