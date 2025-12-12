---
description: This article describes how to configure Okta to enable SSO with the Cerby application using a SAML integration.
---

# Configure SSO between Cerby and Okta with SAML

All Cerby users are able to configure a default Identity Provider (IDP) such as Okta to leverage the Single Sign-On (SSO) authentication feature to securely authenticate to Cerby using a single set of credentials.

This article describes how to configure Okta as the primary IDP to enable SSO with the Cerby application using a Security Assertion Markup Language (SAML) integration.

# Supported features

The following are the supported features of configuring SSO between Cerby and Okta with SAML:

  * **Service provider-initiated authentication flow.** This authentication flow occurs when users attempt to log in to the application from Cerby.
  * **Automatic user account creation in Cerby.** This provisioning flow in Cerby occurs automatically on the initial SSO.

# Requirements

The following are the requirements to configure SSO between Cerby and Okta:

  * An Okta tenant
  * A user account in Okta with privileges to manage an app integration in your Okta tenant
  * A user account in Cerby with the **Workspace Owner** role
  * An invitation sent from Cerby Support via email to create a workspace

**IMPORTANT:** If you have not received an invitation, send an email to [support@cerby.com](mailto:support@cerby.com) with your request.

  * Users and groups created beforehand in your Okta directory. Follow the corresponding instructions in the Okta Help Center to manage users and groups:
    * [Manage users](https://help.okta.com/en/prod/Content/Topics/users-groups-profiles/usgp-people.htm)
    * [Manage groups](https://help.okta.com/en/prod/Content/Topics/users-groups-profiles/usgp-groups-main.htm)

# Configuring SSO between Cerby and Okta with SAML

To configure SSO between Cerby and Okta with a SAML integration, you must complete four main steps:

  1. Set up a workspace in Cerby
  2. Add the SAML-based app to Okta
  3. Assign users and groups to the Cerby app
  4. Retrieve the metadata information from Okta

**NOTE:** Depending on the use case, you may be redirected to Okta for authentication if a session has not been established.

The following sections describe each step.

## 1\. Set up a workspace in Cerby

To set up a workspace in Cerby, complete the following steps:

  1. Click the **Create your Workspace** button from the invitation email you received from Cerby. The **Welcome to Cerby** page is displayed.
  2. Click the **Set up Okta** button, as shown in **Figure 1.** The **Let's create your workspace** page is displayed.

<figure><img src="../.gitbook/assets/rcotutawmHHshyDoAHNbu7k23KNRUOW0Fl8mYn-UscjcaJhvX47yTQQKJWq_qg3BDdvzBYJw9z8DRQ4szsOHPy1YvVz5sAyrDCfm7dr3b5_RpHRFbH1-8JKWOsa-8jSQj9ck75iAc5YJuubGnGXIoDXOh7C5Y7Xx7Mu1M8FZtfhWTtgAt3ikuIMf.png" alt=""><figcaption></figcaption></figure>

**Figure 1. Welcome to Cerby Page**

  3. Enter the name of your workspace in the **Workspace name** field, as shown in **Figure 2**.

<figure><img src="../.gitbook/assets/COije7X5xO9fpcmxZVuhuReCBxRWGdxgiqZGm4STRCdvSi26_xOvWngQEByTRTLPMeJSX1OV7W5c-ObJGML8x7POgQEbx_Dbg_91Q9IkK4tOSepH0X5Tvj9KlftV8lHWPm89zd3hGPZqzllh4fG-tBSZBXglw3dA6DfCsbte-Z8AvrSXjdXhEFRE.png" alt=""><figcaption></figcaption></figure>

**Figure 2. Let's Create Your Workspace Page**

**NOTE:** Remember the workspace name that you have entered. You need it later.

  4. Click the **Create Workspace** button. The **Configure SSO through Okta SAML App** page is displayed with instructions to configure the Cerby app in your Okta tenant.

**IMPORTANT:** Keep the **Configure SSO through Okta SAML App** page open because it contains the required values that you must provide to Okta and Cerby to complete the configuration.

The next step is 2\. Add the SAML-based app to Okta.

* * *

## 2\. Add the SAML-based app to Okta

To add the SAML-based app to Okta, complete the following steps:

  1. Log in to the [Okta Admin Console](https://developer.okta.com/login/) of your organization.
  2. Select the **Applications** option from the **Applications** drop-down list located in the left navigation drawer. The **Applications** page is displayed, as shown in **Figure 3**.

<figure><img src="../.gitbook/assets/Ih5LuLAsLtErdAjPRbKObOw60GKyYOrOpsjJ9g1SVc1GX_Z5v7hDcXKshssg6__xtc9jUT0hXBMqCPHlzWTTxksSZAVDuC-Y2RYydqTpou1itByUgfsmM3xHRrcL0hPSfMeERbooCUKUfh8rwGnpqBlmxR1VHDrIVsGZHPXWVclpOJxTGCa9qrp2.png" alt=""><figcaption></figcaption></figure>

**Figure 3. Applications Page in the Okta Admin Console**

  3. Search for the Cerby app by performing the following actions:
     1. Click the **Browse App Catalog** button. The **Browse App Integration Catalog** page is displayed.
     2. Enter **Cerby** in the search bar above the **All Integrations** section. A list of apps is displayed below the search bar.
     3. Select the **Cerby** option from the list, as shown in **Figure 4**. The **Cerby Overview** page is displayed.

<figure><img src="../.gitbook/assets/XwVBN_rTtth6uLiYSZk71KWEdvq-RhHFNvS_8jOgTelShMF-d0BNB5yIGvZEKuAaJ_CdvAP6BY4vP8SLLetqaBQR1D9Ds-J2lyam1gtQoSUjUEfvnThlT7QWpTmGM-4R5jedNijYHkXxKZ0UCUWGvRpJYVjZ9iPajR5eRRIvC_bcB7qMYWiLru6TnA.png" alt=""><figcaption></figcaption></figure>

**Figure 4. Apps List in the Browse App Integration Catalog Page**

     4. Click the **Add Integration** button. The **Add Cerby** page is displayed with the **General Settings** tab activated.
  4. Enter the name of the app in the **Application label** field of the **General Settings** tab, as shown in **Figure 5**. For example, you can enter **Cerby**.

<figure><img src="../.gitbook/assets/8Fx6yQ0Qk-yr5oDAdUid4qjx_hXDTwxVucAqCU5gyezPwoy3_PmxfpQnbxibPuBlKzd3AmnO2x2TWvhnNam4BVf1JkXyVE4kDeSb5ie1DjLP-ZpQcFu1c5JdCpn9LjbZGdt8kwck7k3Mdq3QexfTNSDxeXB5tTrqVJqPtDlc5bLoRIoVxA6LVx-fyQ.png" alt=""><figcaption></figcaption></figure>

**Figure 5. General Settings Tab in the Add Cerby Page**

  5. Click the **Next** button. The **Sign-On Options** tab is activated.
  6. Select the **SAML 2.0** option located in the **Sign on methods** section.
  7. Enter the corresponding values in the **SubDomain** and **Pool ID** fields of the **Advanced Sign-on Settings** section, as shown in **Figure 6**. These values are located in the **Configure SSO through Okta SAML App** page that you left open in Cerby.

**TIP:** You can use the **Copy** button in the **Configure SSO through Okta SAML App** page in Cerby to copy the values to the clipboard.

<figure><img src="../.gitbook/assets/Tw-AqL7je9Rr60_pf4LF3kr5aPlxDXfCJEE4P7HBa-7qh9DIMF8qa9QLn_bJ9IBFdnaiqghJX21yWajt2P-nthSU2yfggY4EtVprSJOVZ4yVbZoK_DGATUgm54215Z5Yg78xtE3eYGIN8cygKNKlxsuG7fihdQp_OKmd7MIGD0JjzbSkYSRHtJIe.png" alt=""><figcaption></figcaption></figure>

**Figure 6. Advanced Sign-On Settings Section in the Sign-On Options Tab**

  8. Click the **Done** button located at the bottom of the **Add Cerby** page. The **Cerby** app page is displayed.

The next step is 3\. Assign users and groups to the Cerby app.

* * *

## 3\. Assign users and groups to the Cerby app

To assign the users and groups you already created to the Cerby app integration, complete the following steps:

**IMPORTANT:** Users must have a profile created in Okta and groups must be configured before adding them to the Cerby app.

  1. Activate the **Assignments** tab of the **Cerby** app page, as shown in **Figure 7**. The users of your Okta directory are displayed in a table.

<figure><img src="../.gitbook/assets/hEAEx3cTtrBiVZBVkbx9hVOssjZ3LpVW3pgyvD1abSByrNaM6dCa_bZ7HVUt8K6UScq12jXgZuG__h0PQCZUmva5RrRHx-3VYWkfbbqpgnganF-kKHoaul-bmmyllcS12R9WzP_926QlEFh7X602RXp5PdyPogUHVVX5WLnHbLruly6xrByYhWB8WQ.png" alt=""><figcaption></figcaption></figure>

**Figure 7. Assignments Tab**

  2. Assign individually the users from your directory to the Cerby app by performing the following steps:
     1. Select the **Assign to People** option from the **Assign** drop-down list. The **Assign Cerby to People** dialog box is displayed.
     2. Click the **Assign** button of the user you want to add to the Cerby app, as shown in **Figure 8**. A dialog box is displayed to assign a user name to the user.

<figure><img src="../.gitbook/assets/AAkxIzUFUpQN3SNg11CQ0JuJeWqmC4M1bIl01BLIeskHLqZbkt25EIRJ3VJZxsx6pW1k5oLPh8P-K2_X-eQW7MpZH2dev0q9GQwX8qj1Hi0fho2Jai-q3C1MkjGE07ivNZpwhYCR9W_2rp9FT3wSawBmaCBJFYgoRguxPOtQIDI3Uhh3hpztfYww5A.png" alt=""><figcaption></figcaption></figure>

**Figure 8. Assign Cerby to People Dialog Box**

     3. Enter the user name in the **User Name** field.

**IMPORTANT:** Make sure that the user name is a valid email address.

     4. Click the **Save and Go Back** button. The dialog box closes.
     5. Click the **Done** button. The **Assign Cerby to People** dialog box closes.
  3. Assign the groups you have already created to the Cerby app by performing the following steps:
     1. Select the **Assign to Groups** option from the **Assign** drop-down list. The **Assign Cerby to Groups** dialog box is displayed with a list of groups, as shown in **Figure 9**.

<figure><img src="../.gitbook/assets/Hfogp61_dSACdlhuhm_SZDHV1Q1HtILLkTfmULUnVMsl1xq9_biGbWVSAlT_jonDvY5NuTNsILbYDacdWOmav9uFUSIAK004ADAAARyixYcW2UR3G5nLr5qMw7e1v2crEmLCMpOSZ7ITa5NzsUjfE5ELveh_9kjpnYnSEF2fg-LFsl0wcNDrV80PTA.png" alt=""><figcaption></figcaption></figure>

**Figure 9. Assign Cerby to Groups Dialog Box**

     2. Click the **Assign** button for each group you want to assign the Cerby app integration to. The **Assign** button changes to an **Assigned** status.
     3. Click the **Done** button when you complete assigning groups. The dialog box closes.

**TIP:** To verify the groups are successfully assigned to the Cerby app integration, click the **Groups** button from the **Filters** column of the table. The groups you assigned are displayed in the table.

The next step is 4\. Retrieve the metadata information from Okta.

* * *

## 4\. Retrieve the metadata information from Okta

To retrieve the metadata information from Okta, complete the following steps:

  1. Activate the **Sign On** tab on the **Cerby** app integration page in Okta.
  2. Click the **Actions** drop-down list in the **SAML Signing Certificates** section. A drop-down list is displayed with the **View IdP metadata** and **Download certificate** options.
  3. Right-click the **View IdP metadata** option. A context menu is displayed, as shown in **Figure 10**.

<figure><img src="../.gitbook/assets/14NRudimdc-scoj-8i28pY9t0I6tSvWmTzRdYmqYNVOjCrL0-sgYyhjXkblw_beiERcncywn2PiB26qbKQ4hsdQ94_fPr9zMxjY_icStdDJ9Uncu_Fnt4AIz3xlYeiR2IjrcPb2FmOqKz4JAG7jNfza98h6s_G-SIAK-JpTXjcaUO5638L5wdtlIYA.png" alt=""><figcaption></figcaption></figure>

**Figure 10. Context Menu for the View IdP metadata option**

  4. Select the **Copy Link Address** option from the context menu.
  5. Paste the link address in the **Okta Identity Provider metadata** field of the **Configure SSO through Okta SAML App** page that you left open in Cerby, as shown in **Figure 11**. The link address must look like the following example: `https://**< OKTA_TENANT>**.okta.com/app/**< okta-generated-id>**/sso/saml/metadata`

<figure><img src="../.gitbook/assets/klMvI3Jksb53AS0Me3I_p-A7rk23orDWGEm8RtLdXm7Vt039DlROGMmINEUyVXiFpHrQG9hPNd83RKUyvLY9mmW43hhhLFqXqxCDQ2h393iU-dj8OhT39r-n671lG86Tn_MFKE_cjqXuQYcADVGask9FAmN5sCa4zrt6iu5q5ok020vGhOxc0oDf.png" alt=""><figcaption></figcaption></figure>

**Figure 11. Configure SSO Through Okta SAML App Page in Cerby**

  6. Select the **I have already assigned users or groups to the application** option.
  7. Click the **Finish Configuration** button. A page is displayed with a message telling you that your workspace has been successfully created.
  8. Click the **Login** button. Your new Cerby workspace is displayed.

Now you are done.

{% hint style="danger" %}


**IMPORTANT:** Currently, after creating a workspace, you cannot change its name or update the IdP settings.


{% endhint %}

* * *

{% hint style="info" %}


**NOTE 1:** Assigned users via group or individually can now log in to Cerby via SSO through the Cerby app integration displayed on their Okta dashboard. In Cerby, accounts are automatically created after the initial SSO login.


{% endhint %}{% hint style="info" %}


**NOTE 2:** The SAML-based integration leverages Okta only for authentication. To assign permissions for Cerby, users must do so directly in Cerby.


{% endhint %}{% hint style="info" %}


**NOTE 3** : This integration does not currently support IDP-initiated login from Okta. To log in to Cerby from an Okta dashboard, a bookmark app must be created. The bookmark app must point to your workspace, which would be **`<workspace-name>`**`.cerby.com`. For example, if your workspace name is **`cerby`** , the bookmark app should point to **`cerby.cerby.com`**. For more information on creating a bookmark in Okta, see the [How to Create a Bookmark App](https://support.okta.com/help/s/article/How-do-you-create-a-bookmark-app?language=en_US) article.


{% endhint %}
