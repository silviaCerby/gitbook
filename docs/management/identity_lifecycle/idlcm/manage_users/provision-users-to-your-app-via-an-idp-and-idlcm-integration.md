---
description: This article describes how to provision users to your external app via an IdP and IdLCM integration
---

# Provision users to your app via an IdP and IdLCM integration

{% hint style="info" %}


**Who can use this feature?**

  * IT admins with a tenant in an identity provider
  * Workspace**Owners, Super Admins,** and**Admins**


{% endhint %}

As an IT admin collaborating with a workspace **Owner** , **Super** **Admin** , or **Admin** , you can provision users to your external apps from your identity provider (IdP) through an IdLCM integration.

After connecting an integration to your IdP, such as Okta or Entra ID, you can centralize user provisioning in your IdP. By establishing a SCIM connection, Cerby automatically detects when users are assigned to an IdP app integration, either individually or through a group, triggering the automation jobs to propagate these changes to the external app.

* * *

# Requirements

The following are the requirements to provision users to your external apps via an IdP and IdLCM integration:

  * A user account in your IdP with privileges to manage an app integration.
  * An IdLCM integration connected to your IdP, to which you have management access. For more information, read the article [Create an IdLCM integration for your app](https://help.cerby.com/en/articles/11643479-create-an-idlcm-integration-for-your-app).
* * *

# Provision users to your app via an IdP and IdLCM integration

To provision users to your external app via your IdP and IdLCM integration, you must complete the following steps:

  1. Log in to the IdP admin console or center of your organization.
  2. Assign users or groups to the app integration. For instructions, read the official documentation of your IdP:

     * **Okta:**
       * [Assign an app integration to a user](https://help.okta.com/oie/en-us/content/topics/provisioning/lcm/lcm-assign-app-user.htm)
​**NOTE** : For external apps supporting entitlements, you can grant access to an entitlement by completing the following steps:

         1. Retrieve the entitlement string value from your IdLCM integration. For instructions, read the article [Retrieve the entitlement string value from your IdLCM integration](https://help.cerby.com/en/articles/12454992-retrieve-the-entitlement-string-value-from-your-idlcm-integration).
         2. Click the **Add Another** button located next to your **entitlementsAlpha** custom**** attribute. A new field appears.
         3. Enter the entitlement string value in the field.

       * [Assign an app integration to a group](https://help.okta.com/oie/en-us/content/topics/provisioning/lcm/lcm-assign-app-groups.htm)

**NOTE:** For external apps supporting entitlements, you can assign and grant access to entitlements by assigning the corresponding entitlement string value to your group. How you assign attribute values can vary based on your IT admin's policies and preferred Okta approach. For instruction on how to retrieve entitlement string values, read the article [Retrieve the entitlement string value from your IdLCM integration](https://help.cerby.com/en/articles/12454992-retrieve-the-entitlement-string-value-from-your-idlcm-integration).

An automation job to provision users is triggered by Cerby.

**TIP:** You can view the progress of the provisioning request in the **Activity** tab of the integration details page.

Now you are done.
