---
description: This article describes how to turn on the Extended account access feature for accessing your apps from Okta with Cerby's automated login.
---

# Turn on Extended account access for Okta

{% hint style="info" %}


**Who can use this feature?**

  * Workspace Owners, Super Admins, and Admins
  * Only supported using the Cerby web app


{% endhint %}

As a workspace **Admin** , **Super Admin** , or **Owner** , you can turn on the **[Extended account access](https://help.cerby.com/en/articles/9616265-explore-extended-account-access)** feature for your Cerby workspace configured with Okta as the identity provider (IdP).

With this feature, you and all workspace members can sync the accounts they own to access them from their Okta dashboard powered by Cerby’s automated login.

* * *

# Requirements

The following are the requirements to turn on the Extended account access feature:

  * Okta
    * A user account in Okta with the following roles:
      * [Application Administrator](https://support.okta.com/help/s/article/What-are-Application-Administrator-roles-and-permissions?language=en_US) to create and manage app integrations in your Okta tenant
      * [Read-only Administrator](https://help.okta.com/en-us/content/topics/security/administrators-read-only-admin.htm) to read Okta groups
    * An Okta API token created for configuring and turning on this feature. For instructions on how to create or retrieve the token, read the official documentation [Manage Okta API tokens
](https://help.okta.com/en-us/content/topics/security/api.htm#create-okta-api-token)Additionally, set the corresponding [rate limits](https://support.okta.com/help/s/article/API-Token-Rate-Limit-Violation?language=en_US) for the following API endpoint:

      * `/api/v1/apps*`

 **IMPORTANT:** Remember to always adhere to the principle of least privilege; therefore, avoid creating the Okta API token as a **Super Admin** or **Org Admin**.

    * Users provisioned from Okta to Cerby. Optionally, you can also provision Okta groups
  * Cerby
    * A user account in Cerby with the workspace **Admin** , **Super Admin** , or **Owner** role
    * A Cerby workspace configured with Okta as the IdP and the following features enabled:
      * Single sign-on (SSO) authentication using a Security Assertion Markup Language (SAML) integration
      * User provisioning using the System for Cross-domain Identity Management (SCIM) specification
    * The Extended account access feature enabled by our Customer Support team. You can contact us via email at [support@cerby.com](mailto:support@cerby.com)
* * *

# Turn on Extended account access for Okta

To turn on the Extended account access feature for Okta, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using your web browser.
  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed.
  3. Activate the **IDP Settings** tab. The**Identity Provider Settings** section is displayed, as shown in **Figure 1**.

<figure><img src="../.gitbook/assets/AD_4nXdCGj_qWhrxpMFC0kzOvshMDbgGP9k6qsnC3PXif7Wj2N98EdruGrmmSzqIJO3jtYzyRmwPiY267Ec1VmpufXMMV0daKS0qbKaqvgwQXWQvrQEKrNyiDoSefUIAucRMjbI3y9oPcBrWk6qefEZDLwYv9496.png" alt="Screenshot of the Workspace Configuration page with the IDP Settings tab activated. In the Extend Cerby accounts to Okta section, you can turn on this feature"><figcaption></figcaption></figure>

**Figure 1.** **Identity Provider Settings** section in the **IDP Settings** tab of the **Workspace Configuration** page

  4. Turn on the switch from the **Extend Cerby accounts to Okta** section.
  5. Confirm your identity according to your multi-factor authentication (MFA) method:

     * [Push notification on the Cerby mobile app](https://help.cerby.com/en/articles/9462605-confirm-your-identity-with-cerby-s-mfa-methods#h_f2f6b354f7)
     * [Email magic link](https://help.cerby.com/en/articles/9462605-confirm-your-identity-with-cerby-s-mfa-methods#h_1f5622eac0)

The **Turn on extended account access?** dialog box is displayed.

  6. Enter the corresponding values in the following input fields:

     * **IDP Domain:** It is the domain of your Okta tenant configured with your Cerby workspace.

**IMPORTANT:** You must include the protocol part (**`https://`**) of the URL. For example, **`https://mycompany.okta.com`**.

     * **API Token:** It is the token that you generated or retrieved previously as part of the Requirements section. For instructions, read the official documentation [Manage Okta API tokens](https://help.okta.com/en-us/content/topics/security/api.htm#create-okta-api-token).

**TIP:** You can click the **Test connection** button to verify that Cerby can connect with Okta.

  7. Click the **Turn on** button. The dialog box closes, and a success message box is displayed.

Now you are done. You and all workspace members can start syncing and extending their accounts to Okta. For instructions, read the article Sync and extend an account to Okta.
