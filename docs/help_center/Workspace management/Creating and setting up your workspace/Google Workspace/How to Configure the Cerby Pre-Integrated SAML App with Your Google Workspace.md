# How to Configure the Cerby Pre-Integrated SAML App with Your Google Workspace

## How to Configure the Cerby Pre-Integrated SAML App with Your Google Workspace

**Description:** This article describes how you can configure your Google Workspace as an authentication option for your Cerby workspace.

All Cerby users have the ability to configure a default Identity Provider to power Single Sign On (SSO). This article details how to configure your Google Workspace as the primary Identity Provider to facilitate SSO with the Cerby application.

### Supported Features

* Control in Google Workspace who has access to Cerby.
* Service Provider (SP)-Initiated Authentication (SSO) Flow - This authentication flow occurs when the user attempts to log in to the application from Cerby.

### Requirements

In order to proceed with configuring login with SSO through Google Workspace, you must:

* Have access to the Google Workspace Admin Portal.
* Be a Google Workspace administrator to that tenant
* Have received a _Welcome to Cerby_ email invitation

If you have not received a _Welcome to Cerby_ email invitation, please email [support@cerby.com](mailto:support@cerby.com) to request an invite.

## Step-by-Step Configuration Steps

The following documents the configurations for setting up the SAML2 integration between Cerby and a Google Workspace tenant asthe Identity Provider (IDP) and depending on the use case, the user will be redirected to your Google Sign In Portal for authentication if no session has been established.

To configure your provisioning settings for Cerby in Google Workspace, please complete the following steps:

### Step One - Setup Workspace in Cerby

1. Click on **Create your Workspace** from your _Welcome to Cerby_ email.
2. In the first screen that loads, select **Set Up Google Workspace Login** as your Identity Provider to configure.

!\[]\(gitbook/imagesevVwkUmOMDv0sMyj- AvAb-7qlBXNZPZi1WwraikOdwRb4IMq2htLRtmKjf8V1h3\_ToPW4zmeq\_2B8R8LSzlDjs2G\_HYBpzzBD0dppeTxew3Xb\_PZWk5pSAVx4wAnnRcbOCAyosES%3Ds0)

3. In the next screen, provide a _Workspace_ name. Remember the _Workspace_ name which you have provided for step 2.6 below. Then, click **Next**.
4. The next page will have important configuration information. Leave this tab open and open up a separate window or tab to continue.

### Step Two - Add the SAML App in your Google Admin Account

1. In a new tab, sign in to your Google Workspace Admin portal ([https://admin.google.com/](https://admin.google.com/)).
2. Navigate to **Apps** > **Web and Mobile** and then click on **Add App (NOTE: this is not implemented yet, I will continue with the Custom SAML APP)**
3. Then click "**Search for Apps"** , search for Cerby and click on the first search result.
4. On the following screen, add "Cerby" for your **App Name** and choose the**Cerby Logo** and click**Continue (CUSTOM)**

!\[]\(gitbook/images2afJoCQaXc2qC4x6YmM7ChcXgCh-t0Y2o-Nr6yzCjp2WMq62K7JSqQdA1WoYylEnpCklq4mw3FgSsEJZh1HCEV\_95rtHkdHO\_IPilxCNdpiZBz8na582q29ZwdZw1z8YrM- bkrSt%3Ds0)

5. Now, download the Metadata, (_it will be required for the next steps_) and click **Continue**

!\[]\(gitbook/imageshE7QQMMx5cyBdeIh3QmwioM- XVnIyUdtdcdgFUlv\_G5XW9jiunGybWlYZ65uwkGhLNz16c4yX\_6lmyAM- UcVDKpFoUNuDr\_PW581qjrpwPbKJVzOQEchzZXPhDxH3IZpvgsDRtyu%3Ds0)

6. Under **Service Provider Details** , add the **ACS URL** and **Entity ID** (Copy these values from step 1.4 above.
   1. ACS URL: [**https://YOUR-TENANT-ID-cerbyauth.auth.us-east-2.amazoncognito.com**](https://www.google.com/url?q=https://your-tenant-id-cerbyauth.auth.us-east-2.amazoncognito.com\&sa=D\&source=editors\&ust=1631207321412000\&usg=AOvVaw0FbfmQMyZbtvdcZVn3XhDQ)
   2. ENTITY ID: **urn:amazon:cognito:sp:Your\_Provided\_Id**
   3. Start URL: [**https://app.cerby.com**](https://www.google.com/url?q=https://app.cerby.com\&sa=D\&source=editors\&ust=1631207321412000\&usg=AOvVaw237VctIbBhu9070wDhqUOo)

![](../../../Workspace%20management/Creating%20and%20setting%20up%20your%20workspace/Google%20Workspace/gitbook/imagesgt1Yuh4EfjAMv7rL7yjw51m9HvKQh8LfLraPCLmSnuU7Xi8u7L3MSNTCrsqtAmmdf97i3uui8oCE3gpKNlEGCaFYK1QkOStpKJoXv6g82bVYDemLZziTIiZwx8wMFFgWyKPiiJLT=s0)

7. Finally, add the required attributes and Click **Finish**
   1. Name: [http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name](http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name)
   2. Family Name: [http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname](http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname)
   3. Email Address: [http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress](http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress)

!\[]\(gitbook/imagesXQ1e7S8isDP62EPrCGJ4nVyu\_A- LNlGAXMADim39OW6M46uZvaRu7gofhQ2\_IMphcoWHvCKc4oCiSPBqojjXVnHhpUaBtM27TuypVxccD\_\_zoSf7ag1vYXus- afFygHIeU9itGP4%3Ds0)

8. Once the configuration is complete, return to the “Settings for Cerby” view under the App List section. In this section, you can either turn on the Cerby app for all users or enable it for specific organizations.

### Step Three - Populate SSO configuration in Cerby

1. Return to the Cerby Workspace Configuration page from Step 1.4 above and add the **XML file** from step 2.5.
2. Click on “I\*\* _have already assigned users or groups to the application_\*\* ”, per step 2.8 above.

!\[]\(gitbook/imagesdrdeWkAjF4Z-7sc97CIDXZ8NJi4V4fKpM6WwqvG8C4y93TgYPDHj04PpG7WfttyXDFszWSr7EiZRZm8cvOJ0VKLB5910eZbJq61QIEDx3Dtd3KEzRmTgtgrl- xSnN-NQk-er1qOl%3Ds0)

3. Click on **Finish Configuration**.
4. You are done. Proceed to log in to your Cerby workspace.

## Notes

### Permissions

Cerby’s integration with Google Workspaces leverages Google Accounts only for SSO authentication. To assign permissions for Cerby, users must do so directly within Cerby.

### Error: app\_not\_configured\_for\_user

Sometimes a workspace administrator may be unable to access their workspace after it is created and they’ll see a similar error to the one in the screenshot below.

![](../../../Workspace%20management/Creating%20and%20setting%20up%20your%20workspace/Google%20Workspace/gitbook/imagesnPwF2KyzHoCrwozr6AkuPV2tpzILzfVFLHN4_6XI1YhBmcJ4BuLnIuLTJqcJjnw4GH6FjtwII98I_ewYMW7tJ3-fp0uCLnahu2_Y7u5LLAC5eUzaq4BOc7sqA5sT4Vbg-5L2AdP_=s0)

This problem can be easily resolved by refreshing the page or by logging out and then logging in of their Google account.
