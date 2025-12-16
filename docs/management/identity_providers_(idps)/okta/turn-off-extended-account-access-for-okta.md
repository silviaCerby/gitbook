---
description: This article describes how to turn off the Extended account access feature to stop syncing your accounts with Okta.
intercom_id: 9758233
---

# Turn off Extended account access for Okta

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , and **Admins**
* Only supported using the Cerby web app


{% endhint %}

As a workspace **Admin** , **Super Admin** , or **Owner** , you can turn off the **[Extended account access](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-extended-account-access)** feature to stop syncing your accounts with Okta.

When this feature is on, you and all workspace members can sync and extend the accounts they own to access them from their Okta dashboard powered by Cerby’s automated login.

{% hint style="danger" %}


**IMPORTANT:** By turning off this feature, the following happens:

* Workspace members cannot sync and extend new accounts to Okta.
* All accounts previously extended remain in Okta, but they are no longer updated with the latest changes in user and team access permissions.
* Users can still log in to their applications from the chiclets in their Okta dashboard as long as they retain access permissions in Cerby. This happens because Cerby always verifies its role-based access control (RBAC) system to ensure users have access to an account through any type of share: account, collection, or team.
* The removal of currently extended accounts from Okta is a manual process for each item. For instructions, read the article [Remove an account extended to Okta](https://cerby-test.gitbook.io/cerby-test/management/identity-providers-idps/okta/extended-accounts/remove-an-account-extended-to-okta).


{% endhint %}

To turn off the Extended account access feature, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using your web browser.
  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed.
  3. Activate the **IDP Settings** tab. The**Identity Provider Settings** section is displayed
  4. Deactivate the switch from the **Extend Cerby accounts to Okta** section. The **Turn off extended account access?** dialog box is displayed.
  5. Click the **Turn off** button. The dialog box closes, and a success message box is displayed.

Now you are done. Cerby will stop syncing accounts already extended to Okta, and all workspace members will be unable to sync and extend new items.
