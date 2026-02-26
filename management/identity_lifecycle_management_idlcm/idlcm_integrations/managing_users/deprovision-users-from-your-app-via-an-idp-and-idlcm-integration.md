---
description: "This article describes how to remove users from your external apps via an IdP and IdLCM integration."
intercom_id: 11645058
hidden: true
noIndex: true
---

# Deprovision users from your app via an IdP and IdLCM integration

{% hint style="info" %}


**Who can use this feature?**

* IT admins with a tenant in an identity provider
* Workspace **Owners** , **Super** **Admins** , and **Admins**


{% endhint %}

As an IT admin collaborating with a workspace **Owner** , **Super** **Admin** , or **Admin** , you can deprovision users from your external apps via your identity provider (IdP) and an IdLCM integration.

After connecting an integration to your IdP, such as Okta or Entra ID, you can centralize user deprovisioning in your IdP. By establishing a SCIM connection, Cerby automatically detects when users are removed from an IdP app integration, either individually or through a group, triggering the automation jobs to propagate these changes to the external app.

* * *

## Requirements

The following are the requirements to deprovision a user from your external apps via an IdP and IdLCM integration:

  * A user account in your IdP with privileges to manage an app integration.
  * An IdLCM integration connected to your IdP, to which you have management access. For more information, read the article [Create an IdLCM integration for your app](https://help.cerby.com/en/articles/11643479-create-an-idlcm-integration-for-your-app).
* * *

## Deprovision users from your app via an IdP and IdLCM integration

To deprovision users from your external app via an IdP and IdLCM integration, you must complete the following steps:

  1. Log in to the IdP admin console or center of your organization.
  2. Remove users from the app integration. For instructions, read the official documentation of your IdP:

     * **Okta:**
       * [Deprovision a user](https://help.okta.com/en-us/content/topics/provisioning/lcm/lcm-deprovision-user.htm)
       * [Unassign users from applications](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-unassign-apps.htm)

An automation job to deprovision users is triggered by Cerby.
​**TIP:** You can view the progress of the provisioning request in the integration **Activity** tab.

Now you are done.
