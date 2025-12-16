---
description: This article describes how to update the user roles in your external seat-based and paid social apps via an IdP and business hub.
intercom_id: 11040590
---

# Update user roles in your apps via an IdP and business hub

{% hint style="info" %}


**Who can use this feature?**

* IT admins with a tenant in an identity provider
* Business hub **Owners**
* Only supported using the Cerby web app


{% endhint %}

As an IT admin collaborating with a business hub **Owner** , you can update user roles in your external seat-based and paid social apps via your identity provider (IdP), such as Okta or Entra ID, and a business hub.

For this identity lifecycle management functionality to work, Cerby leverages user and group provisioning from the IdP to update Cerby teams.

* * *

## Requirements

The following are the requirements to update user roles in your apps via your IdP and business hub:

* A user account in your IdP with privileges to manage an app integration
* A Cerby workspace integrated with your IdP for single sign-on (SSO) and automatic user provisioning using the SCIM protocol. Refer to the [Creating and setting up your workspace](https://help.cerby.com/en/collections/5819419-creating-and-setting-up-your-workspace) collection for instructions according to your IdP
* Groups created and configured in your IdP to be used for user provisioning and deprovisioning. For instructions, read the articles according to your IdP:
    * [How to Enable Okta User Provisioning with SCIM](https://cerby-test.gitbook.io/cerby-test/management/identity-providers-idps/okta/how-to-enable-okta-user-provisioning-with-scim)
    * [Configure automatic user and group provisioning with Entra ID via SCIM](https://cerby-test.gitbook.io/cerby-test/management/identity-providers-idps/entra-id/configure-automatic-user-and-group-provisioning-with-entra-id-via-scim)
* A business hub connected to Cerby to which you have the **Owner** role
* The IdP-based teams must have shared access to the business hub integration. For instructions on how to do it, read the article [Add users and teams to your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/add-users-and-teams-to-your-apps-via-a-business-hub); you must follow the process to add a team
* * *

## Update user roles in your apps via your IdP and business hub

To update user roles in your external apps via your IdP and business hub, you must complete the following steps depending on how you want the users to keep access to the business hub integration:

* IdP group reassignment

    1. Log in to the IdP admin console or center of your organization.
    2. Add users or members to the groups assigned to the Cerby app integration with the role you want them to have. For instructions, read the official documentation of your IdP:

       * **Okta:** [Manually assign people to a group](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-assign-group-people.htm)
       * **Entra ID:** [Add members or owners of a group](https://docs.azure.cn/en-us/entra/fundamentals/how-to-manage-groups#add-members-or-owners-of-a-group)

    3. Remove the users or members from the old group. For instructions, read the official documentation of your IdP:

       * **Okta:** [Remove people from a group](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-remove-group-people.htm)
       * **Entra ID:** [Remove members or owners of a group](https://docs.azure.cn/en-us/entra/fundamentals/how-to-manage-groups#remove-members-or-owners-of-a-group)
* Individual share
Given that IdP users and groups are automatically provisioned and deprovisioned from your Cerby workspace, Cerby updates user roles according to the new assigned role.

    1. Log in to your [Cerby](https://app.cerby.com/) workspace.
    2. Complete the instructions in the article [Add users and teams to your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/add-users-and-teams-to-your-apps-via-a-business-hub) to share the business hub integration individually with the role you want the user to have.
    3. Log in to the IdP admin console or center of your organization.
    4. Remove the corresponding users or members from the old group. For instructions, read the official documentation of your IdP:

       * **Okta:** [Remove people from a group](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-remove-group-people.htm)
       * **Entra ID:** [Remove members or owners of a group](https://docs.azure.cn/en-us/entra/fundamentals/how-to-manage-groups#remove-members-or-owners-of-a-group)

Now you are done.
