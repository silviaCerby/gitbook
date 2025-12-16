---
description: This article describes how to troubleshoot the most common issues with the accounts you sync and extend to Okta.
intercom_id: 9759116
---

# Troubleshooting Extended account access

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super Admins** , **Admins** , and **Users**
* Account **Owners**
* Only supported using the Cerby web app


{% endhint %}

The following sections contain instructions to troubleshoot the most common issues with the **[Extended account access](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-extended-account-access)** feature:

* Sync your extended accounts with Okta manually
* Remove a user with All-Access Mode from an extended account
* * *

## Sync your extended accounts with Okta manually

If one or multiple extended accounts are not automatically updated in Okta after user and team access permission changes in Cerby, you can sync the accounts manually to propagate the latest updates to Okta. To know the status of your extended accounts, read the article [View the status of an extended account](https://cerby-test.gitbook.io/cerby-test/management/identity-providers-idps/okta/extended-accounts/view-the-status-of-an-extended-account).

Two methods are available to sync your extended accounts with Okta manually:

* Sync one extended account
* Sync all your extended accounts

The following sections describe each method.

### Sync one extended account

To sync only one extended account, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using your web browser.
  2. Click the corresponding account card. The account details page is displayed.
  3. Expand the**Connected services and apps** section.
  4. Click the **More options** (<figure><img src="../../../.gitbook/assets/unnamed_14.png" alt=""><figcaption></figcaption></figure>) icon. A drop-down list is displayed.
  5. Select the **Sync account manually** option from the list. The **Sync account manually?** dialog box is displayed.
  6. Click the **Sync account** button. The dialog box closes, and Cerby starts syncing your account.

Now you are done.

### Sync all your extended accounts

To sync all your extended accounts, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using your web browser.
  2. Click the user profile menu at the top right of the Cerby dashboard. A drop-down menu is displayed.
  3. Select the **My Profile** option. The **My Profile** page is displayed with the **General** tab activated.
  4. Expand the**Connected Apps and Services** section.
  5. Click the **Sync with Okta** button. The **Sync your accounts with Okta manually?** dialog box is displayed.
  6. Click the **Sync accounts** button. The dialog box closes, and Cerby starts syncing all your extended accounts.

Now you are done.

* * *

## Remove a user with All-Access Mode from an extended account

If you or another workspace **Super Admin** or **Owner** turns on **All-Access Mode** while the Extended account access feature is on, and you or this user is removed from an account in Cerby, the corresponding chiclet will not be removed from the Okta dashboard automatically.

This behavior is due to Cerby’s role-based access control (RBAC) system, because **All-Access Mode** enables users to view all accounts within the workspace and recover accounts by reassigning **Owners**.

To solve this issue, you must turn off **All-Access Mode** first and then follow the corresponding instructions from the Sync your extended accounts with Okta manually section to sync one or multiple accounts.

* * *

## View the SCIM external ID of a user

As a workspace **Admin** , **Super Admin** , or **Owner** , you can view the SCIM external ID of all users to determine whether they can use the Extended account access feature.

The SCIM external ID is a unique identifier assigned to all users by an identity provider (IdP) like Okta when it creates or updates a record in a SCIM-enabled service provider like Cerby. This ID is crucial for user provisioning, deprovisioning, and matching between Okta and Cerby.

In the context of Extended account access, only users who have a SCIM external ID in Cerby’s directory can use this feature to extend their accounts because they are synced with Okta.

To view the SCIM external ID of a user, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using your web browser.
  2. Select the **All members** option from the left navigation drawer. The **All Members** view is displayed.
  3. Click the **More** button from the **Accounts** column of the corresponding user. The user details page is displayed.
If the user has an identifier, its value is displayed in the **SCIM external ID** field along with the **Active** status.

If the user does not have a SCIM external ID, you must contact your IT admin so that they can configure the ID properly in your Okta instance.
