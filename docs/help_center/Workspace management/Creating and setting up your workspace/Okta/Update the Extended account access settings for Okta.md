# Update the Extended account access settings for Okta

**Description:** This article describes how to update the settings of the Extended account access feature for Okta.

{% hint style="info" %} **Who can use this feature?** * Workspace**Owners** ,
**Super Admins** , and **Admins** * Supported using the Cerby web app {%
endhint %}

As a workspace **Admin** , **Super Admin** , or **Owner** , you can update the
settings of the **[Extended account
access](https://help.cerby.com/en/articles/9616265-explore-extended-account-
access)** feature for Okta. With this feature, you and all workspace members
can sync and extend the accounts they own to access them from their Okta
dashboard powered by Cerby’s automated login.

You may want to update these settings if the domain of your Okta instance
changes or the Okta API token expires. Cerby will display the **Update**
status in your workspace settings to indicate when the token is no longer
valid to perform syncs.

# Requirements

The following are the requirements to update the Extended account access
settings:

  * A user account in Okta with the following roles:

    * [Application Administrator](https://support.okta.com/help/s/article/What-are-Application-Administrator-roles-and-permissions?language=en_US) to create and manage app integrations in your Okta tenant

    * [Read-only Administrator](https://help.okta.com/en-us/content/topics/security/administrators-read-only-admin.htm) to read Okta groups

  * A user account in Cerby with the workspace **Admin** , **Super Admin** , or **Owner** role

  * A new API token from Okta created for this purpose. For instructions on how to create or retrieve the token, read the official documentation [Manage Okta API tokens  
](https://help.okta.com/en-us/content/topics/security/api.htm#create-okta-api-
token)Additionally, set the corresponding [rate
limits](https://support.okta.com/help/s/article/API-Token-Rate-Limit-
Violation?language=en_US) for the following API endpoint:

    * `/api/v1/apps*`

# Update the Extended account access settings for Okta

To update the Extended account access settings for Okta, you must complete the
following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using your web browser.

  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed.

  3. Activate the **IDP Settings** tab. The**Identity Provider Settings** section is displayed.  
The fields related to the **Extended account access** feature are **IDP
Domain** and **API Token**.

  4. Click the **More options**(![](gitbook/imagesAD_4nXfunp9b1XgNVYScDAmZkXwouh6DfLa__XsHuXs4ONbO8xud3Oy5ZL77KoSG2ZVsKsU-O77D0w4w5mYjfzJt7OQnI4VlVRlBXRcOIgqtbBg2bmGsCBOm223v-D6b3MVPmax5h7uaJKWX0GojdmYo40rtfAU)) icon of the field you want to update. A drop-down list is displayed.

  5. Select the **Edit** option from the list.

  6. Confirm your identity according to your multi-factor authentication (MFA) method:

     * [Push notification on the Cerby mobile app](https://help.cerby.com/en/articles/9462605-confirm-your-identity-with-cerby-s-mfa-methods#h_f2f6b354f7)

     * [Email magic link](https://help.cerby.com/en/articles/9462605-confirm-your-identity-with-cerby-s-mfa-methods#h_1f5622eac0)

The input field is enabled in editing mode.

  7. Enter the new value in the corresponding input field:

     * **IDP Domain:** It is the domain of the Okta tenant configured for your Cerby workspace.

**IMPORTANT:** You must include the protocol part (**`https://`**) of the URL.
For example, **`https://mycompany.okta.com`**.

     * **API Token:** It is the token that you generated or retrieved previously as part of the Requirements section. For instructions, read the official documentation [Manage Okta API tokens](https://help.okta.com/en-us/content/topics/security/api.htm#create-okta-api-token).

**TIP:** Click the **Test connection** button for the **API Token** field to
verify Cerby can connect with Okta with the new token.

  8. Click the **Done** (![](gitbook/imagesAD_4nXcnuiIgXemRqPygER2Kqx86uB_hdyjsJcIR-UGvESio8w0n5Zpz_l3uHn4P_BOsk_hzheDiN0zovLL86nr_BLgjz7kLkgv5hd-cYqdN9sYkpL0Wv-6G9qi7-2tHEYWO2uI8yBd6M_C-FljCZ_VkkZCxt3s_)) icon. A success message box is displayed.

Now you are done. You and all workspace members can continue syncing their
extended accounts with Okta.

