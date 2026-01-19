---
description: "This article describes how to deprovision users from your external seat-based and paid social apps via an IdP and business hub."
intercom_id: 11040570
---

# Deprovision users from your apps via an IdP and business hub

{% hint style="info" %}


**Who can use this feature?**

* IT admins with a tenant in an identity provider
* Business hub **Owners**
* Only supported using the Cerby web app


{% endhint %}

As an IT admin collaborating with a business hub **Owner** , you can deprovision users from your external seat-based and paid social apps via your identity provider (IdP), such as Okta or Entra ID, and a business hub.

For this identity lifecycle management functionality to work, Cerby leverages user and group deprovisioning from the IdP to update Cerby teams.

* * *

## Requirements

The following are the requirements to deprovision users from your external apps via your IdP and business hub:

  * A user account in your IdP with privileges to manage an app integration
  * A Cerby workspace integrated with your IdP for single sign-on (SSO) and automatic user provisioning using the SCIM protocol. Refer to the [Creating and setting up your workspace](https://help.cerby.com/en/collections/5819419-creating-and-setting-up-your-workspace) collection for instructions according to your IdP
  * Groups created and configured in your IdP to be used for user deprovisioning. For instructions, read the articles according to your IdP:
    * [How to Enable Okta User Provisioning with SCIM](https://cerby-test.gitbook.io/cerby-test/management/identity-providers-idps/okta/how-to-enable-okta-user-provisioning-with-scim)
    * [Configure automatic user and group provisioning with Entra ID via SCIM](https://cerby-test.gitbook.io/cerby-test/management/identity-providers-idps/entra-id/configure-automatic-user-and-group-provisioning-with-entra-id-via-scim)
  * A business hub connected to Cerby to which you have the **Owner** role
  * The IdP-based teams must have shared access to the business hub integration. For instructions on how to do it, read the article [Add users and teams to your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/add-users-and-teams-to-your-apps-via-a-business-hub); you must follow the process to add a team
* * *

## Deprovision users from your apps via your IdP and business hub

To deprovision users from your external apps via your IdP and business hub, you must complete the following steps:

  1. Log in to the IdP admin console or center of your organization.
  2. Perform any of the following actions. For instructions, read the official documentation of your IdP:

     * Remove the users from a group
       * **Okta:** [Remove people from a group](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-remove-group-people.htm)
       * **Entra ID:** [Remove members or owners of a group](https://docs.azure.cn/en-us/entra/fundamentals/how-to-manage-groups#remove-members-or-owners-of-a-group)
     * Deactivate or delete the users
       * **Okta:** [Deactivate and delete user accounts](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-deactivate-user-account.htm)
       * **Entra ID:** [Delete a user](https://docs.azure.cn/en-us/entra/fundamentals/how-to-create-delete-users#delete-a-user)

Given that IdP users and groups are automatically deprovisioned from your Cerby workspace, any the following actions happens depending on whether users have shared access to the business hub integration individually or through another team:

     * Cerby removes the users from the external app.
     * Cerby keeps access for the users with the same role.
     * Cerby updates the user roles in the external app, including assets if supported.

     **TIP:** You can view the progress of the deprovisioning tasks in the **Automation** **Log** page.

Now you are done.
