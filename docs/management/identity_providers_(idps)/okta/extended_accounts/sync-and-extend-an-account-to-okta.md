---
description: "This article describes how to extend an account to start logging in to it from Okta with Cerby’s automated login."
intercom_id: 9759106
---

# Sync and extend an account to Okta

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* Account**Owners**
* Only supported using the Cerby web app


{% endhint %}

As a user with any workspace role in Cerby, except the **Login-only** role, you can sync and extend your accounts to access them from your Okta dashboard powered by Cerby’s automated login.

{% hint style="danger" %}


**IMPORTANT:** The **[Extended account access](https://help.cerby.com/en/articles/9616265-explore-extended-account-access)** feature must be turned on for your workspace, and you must have the **Owner** role on the account you want to sync and extend.


{% endhint %}

Your accounts become applications in Okta with their corresponding chiclet on the main page of the dashboard under the following naming convention: **`<account name> - <app name>`**. For example, if you have an account for Instagram named Contentzilla, its name in Okta would be **`Contentzilla - Instagram`**. If the account has duplicates, consecutive numbers are included at the end of the name and enclosed in parentheses.

Other users with the **Owner** or **Collaborator** role on your Cerby accounts can also see the corresponding chiclets.

After the first sync, any change in Cerby accounts is automatically updated in Okta. The following are the changes that propagate from Cerby to Okta:

* User and team access permission updates in Cerby accounts, including assigning or unassigning users to Okta groups, which propagates to teams in Cerby with shared access to accounts.
* Account removals.
* Account label updates.
* User deprovisioning or deactivation in Okta, which causes the user to be removed from the Cerby workspace and lose access to Cerby accounts.

{% hint style="info" %}


**NOTE:** The first sync may take from minutes to hours, depending on the number of accounts and users with shared access to them, while subsequent syncs happen faster whenever an update is registered in Cerby.


{% endhint %}

To sync and extend an account to Okta, you must complete the following steps:

1. Log in to your [Cerby](https://app.cerby.com/) workspace using your web browser.
2. Click the corresponding account card. The account details page is displayed.
3. Expand the**Connected services and apps** section.
4. Click the **Sync** button from the **Extended account access for Okta** section. The **Extend your account to Okta?** dialog box is displayed.
5. Click the **Extend account** button. The dialog box closes, and Cerby starts syncing your account.
When the sync is complete, a success message box is displayed. The dates when the account was extended and last synced are also displayed in the **Extended account access for Okta** section.

Now you are done. You and all workspace members and teams with shared access to your account as **Owners** or **Collaborators** will see the corresponding chiclet in the Okta dashboard for logging-in purposes.
