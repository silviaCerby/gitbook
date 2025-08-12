# Create and set up an app integration in Okta connected to IdLCM

**Description:** This article describes how to create and set up an app integration in Okta connected to IdLCM for user provisioning in your external apps.

Cerby's **Identity Lifecycle Management** (IdLCM) solution enables you to
manage disconnected apps from your identity provider (IdP). When integrated
with Okta and using Cerby as the intermediary, you can automate user lifecycle
management to create, update, and deactivate user accounts in the external app
based on SCIM events, streamlining administration and ensuring consistency
across systems.

As part of the provisioning setup, you can define custom attributes in Okta to
represent your external app roles and map them accordingly. The goal is to
ensure centralized management of user access and permissions via Okta.

This article describes the process of creating and setting up an app
integration in Okta connected to IdLCM for user provisioning in your external
apps

* * *

# Requirements

The following are the requirements to set up an app integration in Okta
connected to IdLCM:

  * An Okta tenant

  * A user account in Okta with privileges to manage an app integration in your Okta tenant

  * A user account in Cerby with the workspace **Owner** , **Super** **Admins** , or **Admins** role

  * A Cerby IdLCM integration successfully created for an app. For instructions on creating the integration, read the article [Create an IdLCM integration for your app](https://help.cerby.com/en/articles/11650659-create-an-idlcm-integration-for-your-app).

  * A SCIM gateway token. For instructions on how to retrieve the SCIM gateway token, read the article [Retrieve the SCIM gateway token and URL for an IdLCM integration](https://help.cerby.com/en/articles/11642821-retrieve-the-scim-gateway-token-and-url-for-an-idlcm-integration).

  * A SCIM gateway URL. For instructions on how to retrieve the SCIM gateway URL, read the article [Retrieve the SCIM gateway token and URL for an IdLCM integration](https://help.cerby.com/en/articles/11642821-retrieve-the-scim-gateway-token-and-url-for-an-idlcm-integration).

  * The app's login page URL. You can find the URL by completing the following steps: 

    1. Log in to your [Cerby](https://app.cerby.com/) workspace.

    2. Select the **Integrations** option from the left menu. The **Integrations** page is displayed.

    3. Select the integration you want to connect to Okta. The integration details page is displayed with the **Settings** tab activated.

    4. Activate the **Connected services** left**** tab. 

    5. Click the **Copy** icon (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1584712034/37654ef6faeee93bdf4ea2f4a413/AD_4nXdC8FzycgYlwfvcVwFQMXImb5XYFdhIo3nGHLM8hi1KBzlSfub9XXSlsDyrfGMiOFjy15n-0sQGFWQbE-X6X-XEVwFM8gClRM1PO1kfbR-FniCu9k2R9HkbegoY3FadqKF9LG6DlQ?expires=1751490000&signature=d6be6a3753adf7d6276ce4c4865a33c3d53b1b3ebadd0f9e43696d2f705fbd46&req=dSUvEs5%2Fn4FcXfMW3Hu4gVIYP3yko6TKEO0B4t0QWujADPnD%2BTDUkH8u97%2F0%0AfA%3D%3D%0A)) in the **Bookmark URL** field located in the **Quick access shortcut** section. 

* * *

# Create and set up an app integration in Okta connected to IdLCM

To create and set up an app integration in Okta connected to IdLCM, you must
complete the following steps:

  1. Create an app integration in Okta

  2. Configure your Okta app integration

  3. Add a custom attribute for your roles

  4. Map the role attribute to your app

The following sections describe each step.

## 1\. Create an app integration in Okta

To create an integration in Okta for your Cerby-integrated app, complete the
following steps:

  1. Log in to the[ Okta Admin Console](https://developer.okta.com/login/) of your organization.

  2. Select the **Applications** option from the **Applications** drop-down list located in the left menu. The **Applications** page is displayed

  3. Click the **Create App Integration** button.**** The**Create a new app integration** wizard is displayed.

  4. Select the **SWA - Secure Web Authentication** option.

  5. Click the **Next** button. The **Create SWA Integration** page is displayed. 

  6. Enter the following information in the**General App Settings** section:

     * **App name:** It is the name of your app integration. Preferably, use the same name as the IdLCM integration you created in Cerby.

     * **App's login page URL:** It is the URL of the sign-in page for your integration. For instructions on how to find the URL, read the Requirements section.

  7. Configure the settings in the**How will your users sign in?** section based on your organization's preferences**.** For instructions, read the official documentation [Create SWA app integrations](https://help.okta.com/oie/en-us/content/topics/apps/apps_app_integration_wizard_swa.htm).

  8. Click the **Finish** button. The app integration settings page is displayed.

The next step is 2\. Configure your Okta app integration.

## Configure your Okta app integration

With your Okta app integration created, you must enable the SCIM option and
configure the settings for your SCIM app integration. These settings enable
Okta to manage user provisioning between your connected SCIM app and Okta user
profiles.

To configure SCIM provisioning for your app integration, you must complete the
following steps from the app integration settings page:

  1. Activate the **General** tab.

  2. Click the **Edit** option located at the top right of the **App Settings** section.

  3. Select the **SCIM** option in the **Provisioning** section. 

  4. Click the **Save** button. 

  5. Configure the SCIM connection by performing the following actions:

     1. Activate the **Provisioning** tab. 

     2. Select the **Integration** option from the **Settings** section of the left menu. The **SCIM Connection** page is displayed.

     3. Click the **Edit** button.

     4. Configure the following SCIM connection details:

        * Enter the SCIM gateway URL you have copied previously from Cerby in the **SCIM connector base URL**. For instructions on how to retrieve it, read the article [Retrieve the SCIM gateway token and URL for an IdLCM integration](https://help.cerby.com/en/articles/11642821-retrieve-the-scim-gateway-token-and-url-for-an-idlcm-integration).

        * Enter **email** in the **Unique identifier field for users** field. 

        * Select the following options in the Supported provisioning actions section:

          * **Import New Users and Profile Updates**

          * **Push New Users**

          * **Push Profile Updates**

        * Select the **HTTP Header** option from the **Authentication Mode** drop-down menu.

        * Enter the SCIM gateway token you have previously generated and copied from Cerby in the **Authorization** field. For instructions on how to retrieve the SCIM gateway token, read the article [Retrieve the SCIM gateway token and URL for an IdLCM integration](https://help.cerby.com/en/articles/11642821-retrieve-the-scim-gateway-token-and-url-for-an-idlcm-integration).

     5. Click the **Test Connector Configuration** button. The **Test Connector Configuration** dialog box is displayed, and you must wait until a success message is displayed.

     6. Click the **Close** button. The dialog box closes. 

     7. Click the **Save** button. The **Test Connector Configuration** dialog box is displayed. After a few seconds, the dialog box closes, and the app integration settings page is displayed. 

  6. Configure the provisioning to app settings by completing the following steps:

     1. Activate the **Provisioning** tab. 

     2. Select the **To App** section from the **Settings** section of the left menu. The **Provisioning to App** section is displayed.

     3. Click the **Edit** button at the top right to activate the options below.

     4. Select the **Enable** checkbox of the following options:

        * **Create Users**

        * **Update User Attributes**

        * **Deactivate Users**

     5. Click the **Save** button. A success message box is displayed.

The next step is 3\. Add a custom attribute for your roles.

## 3\. Add a custom attribute for your roles

To manage roles in your Cerby-integrated app, you must add a custom attribute
in Okta. Default user profiles only include basic fields like name and email,
so creating a new attribute lets you store and send role information during
provisioning.

To add an attribute for your custom roles, you must complete the following
steps from the **Provisioning to App** section:

  1. Scroll down to the **Attribute Mappings** section of your app integration.

  2. Click the **Go to Profile Editor** button. The **Profile Editor** page is displayed.

  3. Add a custom attribute for your roles by performing the following actions:

     1. Click the **Add Attribute** button. The**Add Attribute** dialog box is displayed.

     2. Select the **string array** option from the**Data type** drop-down menu.

     3. Enter a descriptive name to display for the attribute in the **Display name** field.

     4. Enter **roles** in the **Variable name** field.   
​**NOTE:** Make sure the **roles** value appears in the **External name**
field.

     5. Enter **urn:ietf:params:scim:schemas:extension:enterprise:2.0:User** in the**External namespace** field.

     6. Select the **Define enumerated list of values** option. The**Attributes members** section is displayed.

     7. Add an attribute member for each role supported in your Ceby-integrated app by providing the following details:

        1. **Display names:** It is the readable name of the role shown in the Okta interface. For example, **Admin** or **User**

        2. **Values** : It is the actual role identifier sent to the external app. For example, **admin-role** or **user-role**

  4. Click the **Save** button.

The next step is 4\. Map the role attribute to your app.

## 4\. Map the role attribute to your app

After defining a custom attribute for your roles, you must map it to your
Cerby-integrated app. The goal is to ensure that user details, including
roles, are accurately sent during provisioning, so your app can assign the
right roles to each user.

To map your role attribute from Okta to your Cerby-integrated app, you must
complete the following steps from the app integration settings page:

  1. Activate the **Provisioning** tab. 

  2. Select the **To App** option from the **Settings** section of the left menu.

  3. Scroll down to the bottom of the **Attribute Mappings** section.

  4. Click the **Show Unmapped Attributes** button.

  5. Look for the attribute that you want to update and click the corresponding **Edit** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1584796151/4d32faf44af2895739ab24bb87e9/AD_4nXewvbFnLx9Kyz6-K5YeauL08oL2gxsJX2MK65jhyk_ZGjBd74m7tEC8w0V7MeGyzFzLy1JwCud9GeAVn1MlrNsgGUfqwam7aOVWmXPbsVoCYB9uF2C09lUnhNcv7ovgF2t8Hi-BUQ?expires=1751490000&signature=027af6b4ec0da4d9bdf0df94a56aab90fa192a804f49484a8cb83434fa0f2072&req=dSUvEs53m4BaWPMW3Hu4gUPXbyah%2BZ2aJSO7eHfikBOLz%2FWAQs3wyzb%2BQsD3%0AAA%3D%3D%0A)) icon. The **Application roles** dialog box is displayed.

  6. Select the **Expression** option from the**Attribute value** drop-down menu.

  7. Define and enter an expression to map the attribute appropriately. For instructions, read the official documentation [Okta Expression Language](https://developer.okta.com/docs/reference/okta-expression-language/). 

  8. Click the **Save** button.

Now you are done.

