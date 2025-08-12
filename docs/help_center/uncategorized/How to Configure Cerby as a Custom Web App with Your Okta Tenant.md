# How to Configure Cerby as a Custom Web App with Your Okta Tenant

All Cerby users have the ability to configure a default Identity Provider to
power Single Sign On (SSO). This article details how to configure Okta as the
primary Identity Provider to facilitate SSO with the Cerby application.

## Supported Features

  * Service Provider (SP)-Initiated Authentication (SSO) Flow - This authentication flow occurs when the user attempts to log in to the application from Cerby.

  * Identity Provider (IDP)-Initiated Authentication (SSO) Flow - This authentication flow occurs when the user attempts to log in to Cerby from Okta.

  * Automatic account creation in Cerby on initial SSO.

## Requirements

In order to proceed with configuring login with SSO through Okta, you must:

  * Have access to an Okta tenant

  * Be an Okta administrator to that tenant

  * Have received a _Welcome to Cerby_ email invitation

If you have not received a _Welcome to Cerby_ email invitation, please email
[support@cerby.com](mailto:support@cerby.com) to request an invite.

## Configuration Steps

The following documents the configurations for setting up the OIDC integration
between Cerby and Okta. Okta is the Identity Provider (IDP) and depending on
the use case, the user will be redirected to Okta for authentication if no
session has been established.

To configure your provisioning settings for Cerby in Okta, there are three
main steps to follow:

##

## Step One - Setup Cerby Workspace Name

  1. Click on the invite url in your _Welcome to Cerby_ email. This should take you to a page with a URL that looks as follows: [https://app.cerby.com/signup?inviteId=<your_invite_id>&token=<invite_token>](https://app.cerby.com/signup?inviteId=<your_invite_id>&token=<invite_token>).

  2. In the first field, enter your desired workspace name. In the second field, you will see the workspace URL automatically populated. Take note of the workspace domain (underlined in red, below) as it appears in this second field. It will be necessary for step 2.4, below.

     * In the below example, the full URL is <https://contentzilla_corporation.cerby.com>. This makes the workspace domain name "contentzilla_corporation".

     * ![](gitbook/imagesCerby_Workspace_Creation.png)

  3. Click **Next** and keep this page open in a separate tab while you proceed to "Step Two - Add the Cerby App to Okta", below. 

## Step Two - Add the Cerby App to Okta

  1. Log in to your organization’s Okta tenant and click on the **Admin** button.

     1. ![](gitbook/imagesOkta_Click_On_Admin.png)

  2. Navigate to **Applications** > **Applications** > **Add Application**. In the upper right, click on **Create New App**.

     1. ![](gitbook/imagesOkta_Create_New_App.png)

  3. In the resulting pop up modal, select the following items and then click on **Create** :

     * For **Platform** , select "Web".

     * For **Sign On method** , select "OpenID Connect".

       * ![](gitbook/imagesScreen+Shot+2021-02-09+at+5.16.59+PM.png)

  4. On the following screen, populate the following fields in the following way and then click on **Save**.

     * For **Application Name** , populate it with "Cerby".

     * For **Application Logo** , upload the below png.

![](gitbook/imagesCerby_logo_sample.png)

     * For **Login redirect URIs** , populate it with <https://cerby-corporation.cerby.com/auth/callback> where "cerby-corporation" should be replaced by your workspace domain name from step 1.2, above. 

     * For **Logout redirect URIs** , populate it with <https://cerby-corporation.cerby.com/auth/logout> where "cerby-corporation" should be replaced by your workspace domain name from step 1.2, above.

![](gitbook/imagesOkta_Create_Cerby_App.png)

  5. Now review your recently created app under the **General** tab and scroll down to the "General Settings" section. Click on **Edit** and ensure the following is configured:

     * Click on the "Refresh Tokens" checkbox.

     * Click on the "Implicit (Hybrid)" checkbox.

     * Click on the "Allow ID Token with implicit grant type" checkbox.

     * Click on the "Allow Access Token with implicit grant type" checkbox.

     * Ensure "Use Persistent Token" is selected under **Refresh token behavior**.

![](gitbook/imagesRefresh_Tokens.png)

  6. Then, scroll down to the "Login" section under the **General** tab and do the following. Then, click on **Save** at the bottom of this section.

     * Toggle **Login Initiated by** to "Either Okta or App".

     * Click on "Display application icon to users" under **Application visibility**.

     * Click on "Redirect to app to initiate login (OIDC Compliant)" under **Login flow.**

     * Populate **Initiate login URI** with "[https://app.cerby.com/auth/login?workspace=cerby-corporation"](https://app.cerby.com/auth/login?workspace=cerby-corporation%22) where "cerby-corporation" should be replaced by your workspace domain name from step 1.2, above. 

![](gitbook/imagesOkta_Login_Flow.png)

  7. Next, scroll to the top of the **General** section. Copy and save to a temporary and safe location the following three fields under the **General** tab, as shown below.

     1. Okta Client ID

     2. Client Secret

     3. Okta domain

![](gitbook/imagesOkta_App_Items.png)

  8. Then, navigate to **Security** > **API** > **Tokens** and click on **Create Token**.

![](gitbook/imagesOkta_API_Token.png)

  9. In the following modal, name the Token "Cerby" and then click on **Create Token**. In the following modal, copy and save the "Token Value" to the same location as the values from step 2.6, above.

![](gitbook/imagesAPI_Token.png)

  10. You can assign People or Groups to the Cerby app now or after "Step Three - Configure SSO in Cerby", below. Read the section "Assign People or Group" below to see instructions on how to do so.

##

## Step Three - Configure SSO in Cerby

  1. Return to the tab opened during "Step One - Setup Cerby Workspace Name".

  2. Enter your Okta Client ID, Client Secret, Okta domain, and Okta Token from steps 2.7 and 2.9, above:

![](gitbook/imagesScreen+Shot+2020-11-23+at+10.16.44+%281%29.png)

  3. Hit the “Next” button and you should be done!

If you experience any issues or have any questions, please reach out to
[support@cerby.com](mailto:support@cerby.com) to engage our support staff.

## Assign People or Groups

To give people or groups access to the Cerby application, click the
**Assignments** tab under the configured Cerby app, then click **Assign**.
Leveraging **Groups** is recommended to assign access. If assigning access to
**People** , ensure the **User Name** is a valid email.

Assigned users via group or directly will now be able to log into Cerby via
SSO through the Cerby app on their Okta dashboards. Keep in mind, accounts
won't be created in Cerby until the initial SSO login.

## Notes

## Permissions

Cerby’s integration with Okta leverages Okta only for authentication. To
assign permissions for Cerby, users must do so directly within Cerby.

  
  
  
​

