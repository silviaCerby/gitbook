---
description: This article describes the key benefits and configurations of the account autosave feature that captures login and signup credentials.
intercom_id: 9500455
---

# Explore Account Autosave

With the **account autosave** feature, all workspace users can control how Cerby detects and saves credentials during login and signup events through the Cerby browser extension and web app. Workspace**Admins** and**Super Admins** can turn this feature on or off for all workspace users and specify the domains they want to include or exclude from the account autosave settings.

The following are the main benefits of the account autosave feature:

* Streamline adding accounts to Cerby by detecting login and signup events.
* Reduce the disruption of the Cerby browser extension screens for all or specific domains to improve the login and signup experience.
* Customize the saving behavior (enforced or prompted) to balance security and user control.
* Ensure a seamless user experience across the workspace at login and signup.
* Capture and automatically associate accounts to business hub integrations so Cerby can manage and secure access to their seat-based and paid social app
* * *

## Account autosave settings

Two account autosave settings determine the user experience during login and signup:

* Prompted autosave
* Enforced autosave

### Prompted autosave

The **Prompted autosave** setting displays the **Add your account to Cerby** dialog box, asking users whether they want to save their credentials to Cerby when they log in or sign up for accounts in domains configured in the workspace. Users can choose to save or skip the account autosave.

### Enforced autosave

The **Enforced autosave** setting automatically saves credentials without displaying a prompt when users log in or sign up for accounts in domains configured in the workspace. The goal is to ensure that credentials are captured and added to Cerby.

* * *

## Account autosave levels

The account autosave feature operates at two levels:

* Individual level
* Workspace level

### Individual level

The individual level is available for the **Prompted autosave** setting only. The following are the actions all workspace users can perform to manage the account autosave settings:

* In the **Add your account to Cerby** dialog box for specific domains, select the Never save for this site option to prevent the Cerby browser extension from displaying the dialog box again.
* Remove domains from your list of denied domains to let the Cerby browser extension display the **Add your account to Cerby** dialog box again.

### Workspace level

The workspace level is available for both settings, **Prompted** and **Enforced autosave**. The following are the actions workspace**Admins** and**Super Admins** can perform to manage the account autosave settings at the workspace level:

* Turn on or off the account autosave settings for all workspace users.
* Manage which domains are allowed or denied for the account autosave settings for all workspace users.
* * *

## Account autosave role assignments

The following are the cases for which role assignments differ in account autosave:

* Accounts
* Business hubs

### Accounts

All users who create accounts through **Prompted** or **Enforced** **autosave** linked to a new account are automatically assigned the **Owner** role.

### Business hubs

For business hubs, when Cerby captures credentials via **Enforced** and **Prompted autosave** and the associated app account is later linked to a business hub through a sync, Cerby assigns user roles based on whether the user was already invited to the business hub before the sync. The following scenarios describe how roles are assigned in different situations:

* The user is already invited to the business hub
* The user is added to the business hub after account creation

#### The user is already invited to the business hub

A business hub integration **Owner** invites a user to the business hub and assigns them a role (**Owner** or **Collaborator**) before running a sync, and that same user logs in to an account that is captured via **Enforced** and **Prompted autosave** , Cerby performs the following:

* The captured account is associated with the business hub when the sync runs.
* Cerby keeps the role previously defined in the business hub (**Owner** or **Collaborator**) for the user on the associated account.

#### The user is added to the business hub after account creation

If a user creates an account for an app via **Enforced autosave** _before_ being added to a business hub for that same app, and is later synced into the business hub without a specific role assignment, Cerby performs the following:

* Detects the email match between the user and the existing account.
* Automatically assigns the **Collaborator** role to the user in the business hub and the **Owner** role on the previously created account.
* * *

## Related articles

Refer to the following articles to learn more about Cerby’s account autosave settings:

* [Manage the domains that Cerby prompts you to autosave](https://cerby-test.gitbook.io/cerby-test/management/credential-management/accounts/account-autosave/turn-on-and-manage-prompted-account-autosave-in-the-workspace)
* [Turn on Prompted account autosave in the workspace](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-browser-extension/manage-the-domains-where-cerby-prompts-you-to-autosave-your-accounts)
* [Turn on Enforced account autosave in the workspace](https://cerby-test.gitbook.io/cerby-test/management/credential-management/accounts/account-autosave/turn-on-and-manage-enforced-account-autosave-in-the-workspace)
* [Autosave an account at login or signup via the Cerby browser extension](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-browser-extension/autosave-an-account-at-login-or-signup-with-the-cerby-browser-extension)
