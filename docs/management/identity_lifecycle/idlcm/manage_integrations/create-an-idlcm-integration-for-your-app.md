---
description: "This article describes how to create an IdLCM integration to connect your disconnected app to your IdP through Cerby."
intercom_id: 11650659
hidden: true
noIndex: true
---

# Create an IdLCM integration for your app

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super** **Admins** , and **Admins**
* Only supported using the Cerby web app


{% endhint %}

As workspace **Owner** , **Super Admin** , or **Admin** , you can create an integration to connect your disconnected apps to your identity provider (IdP) through Cerby’s **Identity Lifecycle Management**(IdLCM) solution.

With IdLCM, you're setting up a SCIM gateway that translates SCIM requests from your IdP into actions for an external app. The IdLCM integration acts as a middle layer that receives, translates, and automates the execution of tasks such as the following:

* User provisioning and deprovisioning
* Asset management
* Groups management
* Sync app

This article provides generic instructions on how to create an IdLCM integration for your app.

* * *

## Requirements

The following are the requirements to create an IdLCM integration:

  * A Cerby workspace
  * A Cerby user account with the workspace **Owner** , **Super Admin** , or **Admin** role
  * A collaboration space (workspace, team, or dashboard) in your app
  * A service account added to Cerby that corresponds to an active user account with a native admin role in your app. For instructions and recommendations on how to create this account, read the article [Create a service account for your IdLCM integration](https://help.cerby.com/en/articles/11641977-create-a-service-account-for-your-idlcm-integration).
  * The user management and login method for your integration must be identified. Depending on your app, the options might be the following:
    * Username and password
    * Single sign-on (SSO) with your IdP
    * Access token
  * A business or organization ID. Commonly, you can find the ID in the following ways:
    * **From the address bar** : After you logged in to your app, sometimes the ID is displayed in the address bar as part of the URL, either in the subdomain, path, or an ID parameter. For example:
      * **123456890** in `https://business.app.com/settings/&business_id=1234567890`
      * **contentzilla** in `https://contentzilla.app.com/`
    * **From the business information or settings** : When you are logged in to your app, navigate to the settings or business information page. The ID is usually displayed in an information section for you to copy.
​**NOTE:** Not all IdLCM integrations require a business or organization ID; Cerby displays an input field when applicable to your app.

* * *

## Create an IdLCM integration for your app

To create an IdLCM integration for your app, you must complete the following main steps:

  1. [Create and set up an IdLCM integration in Cerby](create-an-idlcm-integration-for-your-app.md#id-1.-create-and-set-up-an-idlcm-integration-in-cerby)
  2. [Create and set up an app integration in your IdP connected to IdLCM](create-an-idlcm-integration-for-your-app.md#id-2.-create-and-set-up-an-app-integration-in-your-idp-connected-to-idlcm)
  3. [Sync to import users, roles, and entitlements to Cerby](create-an-idlcm-integration-for-your-app.md#id-3.-sync-users-roles-and-entitlements-from-your-external-app-to-cerby)
  4. [Import users, roles, and entitlements from an IdLCM integration into your IdP](create-an-idlcm-integration-for-your-app.md#id-4.-import-users-roles-and-entitlements-from-an-idlcm-integration-into-your-idp)

The following sections describe each main step.

### 1\. Create and set up an IdLCM integration in Cerby

To create and set up an IdLCM integration in Cerby, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Integrations** option from the left menu. The **Integrations** page is displayed.
  3. Click the **Create integration** button located at the top right of the page. The **New app integration** page is displayed.
  4. Enter the corresponding information in the following fields of the **Select app** section:****

     * **Name:** It is the name to assign to your integration in Cerby.
     * **Select app:** It is the name of the external app. The apps from Cerby’s catalog that match the name are displayed on a list automatically for you to select one.
​**IMPORTANT:** You can only create an IdLCM integration if the app is in Cerby’s catalog.

     * **Business ID or other identifier:** It is the unique identifier of your business or organization within the app. This field is displayed or not depending on the app, and it might have different names, such as Organization ID or Team ID. For generic instructions on how to find the ID, read the [Requirements](create-an-idlcm-integration-for-your-app.md#requirements) section.

  5. Click the **Next** button. The **Service account** section is displayed.
  6. Specify the service account and its login method by completing the following steps:
     1. Select the login method of your service account from the options in the **Select login workflow** section. A list of accounts saved in Cerby for your external app is displayed below.
​**IMPORTANT:** Currently, Cerby only supports username and password as the login method. If no accounts are displayed below, verify that you have created the service account and added it to Cerby, as detailed in the [Requirements](https://docs.google.com/document/d/1gG8wDFl0UfUuC6OdoDEU3zT7UB4HWV0Oqi3rj7xF3UI/edit?pli=1&tab=t.l5l9doui9l70#heading=h.w1btrxgadits) section.

     2. Select the service account from the list below.
     3. Click the **Next** button. The **Settings (Optional)** section is displayed.
  7. Click the **Skip** button. **The Advanced settings (Optional)** is displayed.
​**NOTE:** The **Settings (Optional)** section is currently in development. By skipping it, the integration is created with default settings.

  8. (Optional) Specify the user schema configuration if you have custom roles:
     1. Select the**User schema** option. The **User schema** side drawer is displayed.
     2. Update the user schema to configure any custom roles or fields Cerby must consider.
​**NOTE:** For instructions and recommendations on how to update the user schema, read the article [Configure your user schema](https://help.cerby.com/en/articles/11644390-configure-your-user-schema).

     3. Click the **Save** button. The side drawer closes.
  9. Click the **Test and save** button located at the top right of the page. The **Checking your integration setup…** page is displayed.
Cerby starts an automation job to validate the settings and the provided service account. The page closes, and a success message box is displayed.

The next step is [2. Create and set up an app integration in your IdP connected to IdLCM](create-an-idlcm-integration-for-your-app.md#id-2.-create-and-set-up-an-app-integration-in-your-idp-connected-to-idlcm), which you must complete in your IdP.

### 2\. Create and set up an app integration in your IdP connected to IdLCM

To set up an app integration in your IdP connected to IdLCM, refer to the specific instructions for your IdP. Currently, we only support Okta, so follow the instructions in the article [Create and set up an app integration in Okta connected to IdLCM](https://help.cerby.com/en/articles/11643251-create-and-set-up-an-app-integration-in-okta-connected-to-idlcm).

The next step is [3. Sync users, roles, and entitlements from your external app to Cerby](create-an-idlcm-integration-for-your-app.md#id-3.-sync-users-roles-and-entitlements-from-your-external-app-to-cerby).

### 3\. Sync users, roles, and entitlements from your external app to Cerby

After setting up the app integration in your IdP, you must sync the users, roles, and entitlements from your external app to Cerby. The goal is to import this data to match the current state of the app so you can start managing identities and access through IdLCM.

To sync the users, roles, and entitlements to Cerby, you must complete the following steps from your Cerby web app dashboard:

  1. Select the **Integrations** option from the left menu. The **Integrations** page is displayed.
  2. Click the **More options** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1587026605/e9b15220cb41d0d08e416505e5a7/AD_4nXeeGJZmzwaS-SRUr4CcvXA1PA3rISj09RcmqDq85HoPba8eNIqf_R3tEAQLnllWdWILc1Bqh27pzMZyY8U-YoVbHP4ySRBvsA4AaWgWOVhb9ZQEVfVl1HbwHEUl3rKefAJYLA_HjA?expires=1750950000&signature=d731dd57f65bff0c847fc06ae48d8a834287a8d195c4b39a7e903be1ceec1574&req=dSUvEcl8m4dfXPMW3Hu4gQAyC5km3IJV4Y3MnXKlYzqjwTyY4rqNa4xoxZDY%0AIw%3D%3D%0A" alt="">) icon of the corresponding integrations. A drop-down menu is displayed.
  3. Select the **Settings** option from the menu. The integrations details page is displayed with the **Settings** tab activated.
  4. Click the **Sync** button located at the top right of the page.
​**NOTE:** The check and import may take a few minutes, depending on the number of users. When the process is complete, a success message box is displayed.

The next step is [4. Import users, roles, and entitlements from an IdLCM integration into your IdP](create-an-idlcm-integration-for-your-app.md#id-4.-import-users-roles-and-entitlements-from-an-idlcm-integration-into-your-idp).

### 4\. Import users, roles, and entitlements from an IdLCM integration into your IdP

With the users, roles, and entitlements of your external app synced in Cerby, you must now import this data from the IdLCM integration to your IdP. The goal is to match the current state of the app and the IdLCM integration so you can centralize identity and access management in your IdP.

To import the users, roles, and entitlements to your IdP, refer to the specific instructions for your IdP. Currently, we only support Okta, so follow the instructions in the article[ Import users, roles, and entitlements from an IdLCM integration into Okta](https://help.cerby.com/en/articles/11647808-import-users-roles-and-entitlements-from-an-idlcm-integration-into-okta).
