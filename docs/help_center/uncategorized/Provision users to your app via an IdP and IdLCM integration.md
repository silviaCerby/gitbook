# Provision users to your app via an IdP and IdLCM integration

**Description:** This article describes how to provision users your external apps via an IdP and IdLCM integration

{% hint style="info" %} **Who can use this feature?** * IT admins with a
tenant in an identity provider * Integration **Owners** * Only supported using
the Cerby web app {% endhint %}

As an IT admin collaborating with an integration **Owner** , you can provision
users to your external apps from your identity provider (IdP) through an IdLCM
integration.

After connecting an integration to your IdP, such as Okta or Entra ID, you can
centralize user provisioning in your IdP. By establishing a SCIM connection,
Cerby automatically detects when users are assigned to an IdP app integration,
either individually or through a group, triggering the automation jobs to
propagate these changes to the external app.

* * *

# **Requirements**

The following are the requirements to provision users to your external apps
via an IdP and IdLCM integration:

  * A user account in your IdP with privileges to manage an app integration.

  * An IdLCM integration connected to your IdP to which you have the **Owner** role. For more information, read the article [Create an IdLCM integration for your app](https://help.cerby.com/en/articles/11643479-create-an-idlcm-integration-for-your-app).

* * *

# **Provision users to your app via an IdP and IdLCM integration**

To provision users to your external apps via your IdP and IdLCM integration,
you must complete the following steps:

  1. Log in to the IdP admin console or center of your organization.

  2. Assign users or groups to the app integration. For instructions, read the official documentation of your IdP:

     * **Okta:**

       * [Assign an app integration to a user](https://help.okta.com/oie/en-us/content/topics/provisioning/lcm/lcm-assign-app-user.htm)

       * [Assign an app integration to a group](https://help.okta.com/oie/en-us/content/topics/provisioning/lcm/lcm-assign-app-groups.htm)

An automation job to provision users is triggered by Cerby.

**TIP:** You can view the progress of the provisioning request in the
**Activity** tab of the integration details page.

Now you are done.

