---
description: "This article describes how to provision users to your external seat-based and paid social apps via an IdP and business hub."
intercom_id: 11040540
---

# Provision users to your apps via an IdP and business hub

{% hint style="info" %}


**Who can use this feature?**

* IT admins with a tenant in an identity provider
* Business hub **Owners**
* Only supported using the Cerby web app


{% endhint %}

As an IT admin collaborating with a business hub **Owner** , you can provision users to your external seat-based and paid social apps via your identity provider (IdP), such as Okta or Entra ID, and a business hub.

For this identity lifecycle management functionality to work, Cerby leverages user and group provisioning from the IdP to create and update Cerby teams.

{% hint style="danger" %}


**IMPORTANT:** You must plan ahead for the roles you want to assign to the teams with shared access to the business hub integration. Remember that the team's roles will be assigned to all team members both in Cerby and in the external app, including assets if supported.


{% endhint %}

* * *

## Requirements

The following are the requirements to provision user to your external apps via your IdP and business hub:

  * A user account in your IdP with privileges to manage an app integration
  * A Cerby workspace integrated with your IdP for single sign-on (SSO) and automatic user provisioning using the SCIM protocol. Refer to the [Creating and setting up your workspace](https://help.cerby.com/en/collections/5819419-creating-and-setting-up-your-workspace) collection for instructions according to your IdP
  * Groups created and configured in your IdP to be used for user provisioning. For instructions, read the articles according to your IdP:
    * [How to Enable Okta User Provisioning with SCIM](https://help.cerby.com/en/articles/5457593-how-to-enable-okta-user-provisioning-with-scim)
    * [Configure automatic user and group provisioning with Entra ID via SCIM](https://help.cerby.com/en/articles/5638472-configure-automatic-user-and-group-provisioning-with-entra-id-via-scim)
  * A business hub connected to Cerby to which you have the **Owner** role
  * The IdP-based teams must have shared access to the business hub integration. For instructions on how to do it, read the article [Add users and teams to your app via a business hub](https://help.cerby.com/en/articles/9045790-add-users-and-teams-to-your-apps-via-a-business-hub); you must follow the process to add a team
* * *

## Provision users to your apps via your IdP and business hub

To provision users to your external apps via your IdP and business hub, you must complete the following steps:

  1. Log in to the IdP admin console or center of your organization.
  2. Add users or members to the groups assigned to the Cerby app integration. For instructions, read the official documentation of your IdP:

     * **Okta:** [Manually assign people to a group](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-assign-group-people.htm)
     * **Entra ID:** [Add members or owners of a group](https://docs.azure.cn/en-us/entra/fundamentals/how-to-manage-groups#add-members-or-owners-of-a-group)

Given that IdP users and groups are automatically pushed to your Cerby workspace, the new team members also receive shared access to the business hub integration automatically. Therefore, Cerby adds the users to the external app, including assets if supported.

**TIP:** You can view the progress of the provisioning tasks in the **Automation Log** page.

Now you are done.
