---
description: "This article describes how to automatically invite or remove members of your seat-based and paid social apps from your IdP."
intercom_id: 9046188
---

# [UNPUBLISHED] Manage app members from your IdP (deprecated)

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super Admins** , and **Admins**
* Available to Cerby Automate
* Only supported using the Cerby web app


{% endhint %}

IT admins can automatically invite or remove members of a seat-based or paid social app by triggering provisioning and deprovisioning events in their identity provider (IdP), such as Okta or Entra ID (formerly Azure AD).

When user provisioning is enabled for your Cerby workspace through the System for Cross-domain Identity Management (SCIM) specification, any change in the corporate directory managed by your IdP propagates to Cerby automatically.

For the Apps feature, provisioning and deprovisioning events propagate from group assignments in the IdP to teams in Cerby. Currently, Cerby only supports group assignments from Okta.

The management tasks you can perform on app members are the following:

* [Invite new app members from Okta](unpublished-manage-app-members-from-your-idp-deprecated.md#invite-new-app-members-from-okta)
* [Remove app members from Okta](unpublished-manage-app-members-from-your-idp-deprecated.md#remove-app-members-from-okta)

The following sections describe each task.

* * *

## Invite new app members from Okta

When you use Okta as your IdP and you have enabled automatic user provisioning with SCIM, you can leverage the Group Push feature to create teams and provision users in Cerby with team access to seat-based and paid social apps.

These teams correspond to group assignments in Okta, and they are automatically synced with Cerby.

### Requirements

The following are the requirements to invite app members via group assignments in Okta:

  * The Group Push feature configured for Cerby. For more information, read the [Configure Group Push between Okta and Cerby](https://cerby-test.gitbook.io/cerby-test/management/identity-providers-idps/okta/how-to-enable-okta-user-provisioning-with-scim) section from the [How to Enable Okta User Provisioning with SCIM](https://cerby-test.gitbook.io/cerby-test/management/identity-providers-idps/okta/how-to-enable-okta-user-provisioning-with-scim) article.
  * A group created in Okta to be used to provision and deprovision users for your app. This group corresponds to a team in Cerby. For more information, read the [How to use Teams](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/teams/how-to-use-teams) article.
  * The Cerby team must have shared access to the App in Cerby via an invitation from the app **Owner**. To do so, you must complete the following steps in Cerby:

    1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
    2. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.
    3. Click the **Settings** icon of the corresponding app card. The app details page is displayed with the **Settings** tab activated.
    4. Activate the **Members** tab.
    5. Click the **Invite users** button in the **User Overview** section. The **Send Invite to Join <app name>** wizard is displayed.
    6. Enter the name of the team in the search bar. The team is displayed on a list below the search bar.
    7. Select the corresponding team from the list. The **Members** section is displayed with the team you selected.
    8. Select the corresponding role of the team on the app from the **Role** drop-down list:

       * **Owner:** This role enables sharing access and managing the app settings in Cerby.
       * **Collaborator:** This role enables only logging in to the app.

    9. Select the corresponding role for the team on the app from the **Grant access role for <app name>** section.

    **NOTE:** Access roles are different depending on the app's native roles and permissions. This access role is granted to all the team members.

    10. Click the **Send invites** button. The wizard closes, and a success message box is displayed.

Users who had individual access to the app through Cerby now have access to it via a team. New users receive an invite to join the app, and they must accept the invite, create their user account in the app, and connect this account to Cerby. For instructions, read the article [Join the app and connect it to Cerby](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/join-your-external-app-and-set-up-your-business-hub-access).

### Invite app members via group assignments

To invite new app members automatically from your IdP via group assignments, you must complete the following steps:

  1. Log in to the [Okta Admin Console](https://developer.okta.com/login/) of your organization.
  2. Select the **Groups** option from the **Directory** drop-down list located in the left navigation drawer. The **Groups** page is displayed with a table of groups.
  3. Select the corresponding group from the table. The group details page is displayed with the **People** tab activated.
  4. Click the **Assign people** button. The **Assign people to <group name>** page is displayed with a table of users.
  5. Click the **Add** icon of the user you want to add to the group. A success message box is displayed.

The users are now automatically added to the corresponding team in Cerby via an automation task, and an invite to join the app is sent. Invited users must accept the invite, create their user account in the app, and connect this account to Cerby. For instructions, read the [Join the app and connect it to Cerby](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/join-your-external-app-and-set-up-your-business-hub-access) section.

* * *

## Remove app members from Okta

To remove app members automatically from Okta via group assignments, you must complete the following steps:

  1. Log in to the [Okta Admin Console](https://developer.okta.com/login/) of your organization.
  2. Select the **Groups** option from the **Directory** drop-down list located in the left navigation drawer. The **Groups** page is displayed with a table of groups.
  3. Select the corresponding group from the table. The group details page is displayed with the **People** tab activated.
  4. Click the **Remove** icon of the user you want to remove from the group. A success message box is displayed.

The user is automatically removed from the corresponding team in Cerby and the app via an automation task.

When removing users individually from the IdP, the corresponding member removal propagates to a Cerby workspace. However, to remove the user completely from the seat-based or paid social app, you must do it manually or perform a check for updates and apply the report. For instructions, read the articles [Troubleshooting Apps: Remove app members manually](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/troubleshooting/troubleshooting-business-hubs) or [Check for updates in your app and apply report](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/sync-your-business-hub-with-your-external-app).
