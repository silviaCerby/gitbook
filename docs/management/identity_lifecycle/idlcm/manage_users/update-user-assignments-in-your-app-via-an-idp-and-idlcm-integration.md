---
description: "This article describes how to update users assigned to your external apps via an IdP and IdLCM integration"
intercom_id: 11645015
---

# Update user assignments in your app via an IdP and IdLCM integration

{% hint style="info" %}


**Who can use this feature?**

* IT admins with a tenant in an identity provider
* Workspace **Owners** , **Super** **Admins** , and **Admins**


{% endhint %}

As an IT admin collaborating with a workspace **Owner** , **Super Admin** , or **Admin** , you can update users and groups in your external apps from your identity provider (IdP) through an IdLCM integration.

After connecting an integration to your IdP, such as Okta or Entra ID, you can centralize user updates in your IdP. By establishing a SCIM connection, Cerby automatically detects changes to users assigned to an IdP app integration, such as changes on custom attributes, triggering the automation jobs to propagate these changes to the external app.

* * *

## Requirements

The following are the requirements to update users in your external apps via an IdP and IdLCM integration:

  * A user account in your IdP with privileges to manage an app integration.
  * An IdLCM integration connected to your IdP, to which you have management access. For more information, read the article [Create an IdLCM integration for your app](https://help.cerby.com/en/articles/11643479-create-an-idlcm-integration-for-your-app).
* * *

## Update user assignments in your app via an IdP and IdLCM integration

To update user assignments in your external app via an IdP and IdLCM integration, you must complete the following steps:

  1. Log in to the IdP admin console or center of your organization.
  2. Edit the user assignments in your app integration by completing the steps depending on how your user was granted access:

     * **User groups:**

       1. Add users or members to the groups assigned to the integrated app with the role you want them to have. For instructions, read the official documentation of your IdP:

          * **Okta** : [Manually assign people to a group](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-assign-group-people.htm)

       2. Remove the users or members from the old group. For instructions, read the official documentation of your IdP:

          * **Okta** : [Remove people from a group](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-remove-group-people.htm)
     * **Individual users**
       * Update the user assignment within the integrated app.**** For instructions, read the official documentation of your IdP:
         * **Okta:** [Manage app integration assignments](https://help.okta.com/en-us/content/topics/apps/apps-manage-assignments.htm)

An automation job to update user assignments is triggered by Cerby.
​**TIP:** You can view the progress of the provisioning request in the integration **Activity** tab.

Now you are done.
