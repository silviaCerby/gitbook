# Configure SSO between Cerby and JumpCloud with SAML

**Description:** This article describes how to configure JumpCloud to enable SSO with Cerby using a custom SAML application.

All Cerby users are able to configure a default Identity Provider (IdP) such
as JumpCloud to leverage the Single Sign-On (SSO) authentication feature to
securely authenticate using a single set of credentials.

JumpCloud uses a Security Assertion Markup Language (SAML) application to
integrate with other service providers easily. In this case, the integration
is with Amazon Cognito, and the SAML application is customized and points to a
specific Cerby workspace.

This article describes how to configure JumpCloud as the primary IdP to enable
SSO with the Cerby platform using a SAML integration.

# **Supported features**

The following are the supported features of configuring SSO between Cerby and
JumpCloud with SAML:

  * **Service provider-initiated authentication flow:** This authentication flow occurs when users attempt to log in to the application from Cerby.

  * **Automatic user account creation in Cerby:** This provisioning flow in Cerby occurs automatically on the initial SSO.

# **Requirements**

The following are the requirements to configure SSO between Cerby and
JumpCloud:

  * You must have administrator access to a JumpCloud tenant account.

  * You must have an internal JumpCloud user who can get an application assigned via groups.

  * You must have a user group to assign the application to. This group must have users already assigned as members.

  * You must have received an invitation from Cerby Support via email to create a workspace.

**IMPORTANT:** If you have not received an invitation, send an email to
[support@cerby.com](mailto:support@cerby.com) with your request.

# **Configuring SSO between Cerby and JumpCloud with SAML**

To configure SSO between Cerby and JumpCloud with a SAML integration, you must
complete four main steps:

  1. Set up a workspace in Cerby

  2. Create an application in JumpCloud

  3. Configure the connection settings

  4. Finish the workspace creation in Cerby

The following sections describe each step.

## **1\. Set up a workspace in Cerby**

To set up a workspace in Cerby, complete the following steps:

  1. Click the **Create your Workspace** button from the invitation email. The **Welcome to Cerby** page is displayed, as shown in **Figure 1**.

![](images/p7z6AXQWFNnGo6LxUtYXWNLNocZdCMNheAC9h-ed1cd3RQMVOM2kvzHnpkmJKig0C69KdOyYZf1fkOdlHvTHUBf-0pX1Ib0qp6EYAs3nT_1cXymzo8UZWfZIofX6_AaWERA9AdTizMmBge9MyoVrtBEGVXdrHSyKVFnLQzpyXrkITCwUJ69ot02pBQ)

**Figure 1. Welcome to Cerby Page**

  2. Click the **Set up Generic SAML** button. The **Let's create your workspace** page is displayed.

  3. Enter the name of your workspace in the **Workspace name** field, as shown in **Figure 2**. For example, **Contentzilla**.

![](images/w728sfG6x2vzxDIdkWbWGbZH_dwrKg9p4wGJEzYzDDYshvIS4lSHDV3tjQtAsW9bItfb0ughYrGq1DjojeJzDpgDeAcfWt9ozhFivxqwbuzPhe-75SfthxwOLweX-
ZosGUFR9A1KauDSUO1nSmMZBlFWnTU830Pet7suzk9Y9WWKzFjGdzvXW3gcZA)

**Figure 2. Let's Create Your Workspace Page**

**NOTE:** Remember the workspace name that you have entered. You need it
later.

  4. Click the **Create Workspace** button. The **Configure SSO through Your Generic SAML App** page is displayed, as shown in **Figure 3**. This page contains information to configure the Cerby application in your JumpCloud tenant.

![](images/nZgGYEtA2Kqlzud5XzNh8H0-qp2vLMDHUgR3v-QAnmlrV95fM-x4R192qlvIHTZcjPkZ3kBXDPItNCbnMVa20iFkpzEuk8FWJ2oDV2PKFaeRABh8zSfKT4LRlGh3J7NfXxcN-
FQc1W5qNPFyi7cGCFYzEto9XRqLlhr7RfjsEDMKStwV1IFD7g9DPg)

**Figure 3. Configure SSO through Your Generic SAML App Page**

**IMPORTANT:** Keep the **Configure SSO through Your Generic SAML App** page
open because it contains the required values that you must provide to
JumpCloud and Cerby to complete the configuration.

The next step is 2\. Create an application in JumpCloud, which you must
complete from JumpCloud.

* * *

## **2\. Create an application in JumpCloud**

To create an application in JumpCloud, complete the following steps:

  1. Log in to the [JumpCloud Console](https://console.jumpcloud.com/login/admin) as an administrator.

  2. Click the **SSO** button from the **USER AUTHENTICATION** drop-down list located in the left navigation drawer. The **SSO** page is displayed, as shown in **Figure 4**.

![](images/u0VgI4PJPpIaApaG_0DG4sZ1_Y1d7dQ20tgza_6o7ECrFI27IPnd2zloadCfyL-B4_Rug_wpdY7UwHplsRnXTbsKoGmlLBaQ8ko7PVifOxe-
oHnGXAHUU5qRbCxPrDnJDjiUJIvcLMSnDVoS1zNu_yixVoujDedPRkZG-
yAGuTjCsi8Jj3LvR5Bj-Q)

**Figure 4. SSO Page**

  3. Click the **Add app** icon located to the left of the **Search** bar. The **Configure New SSO Application** dialog box is displayed, as shown in **Figure 5**.

![](images/orCHKQJk0YQr9pWcUINDbcHGr0vF3mTFc-FOfZIdZD-
mdVmUnbyhoPGVrZOygzxDJ0uzZ0rvCO5UUeDam1JfLyj8eKePcUMv3SGL1Rg-
xqzmym5EsHGITVaVfKRG3cfRI9-P4s7qeNcED7OvwlRe0WqozWoWIPz46LAAXfH-
WFj65MrEcLvf7xT0zA)

**Figure 5. Configure New SSO Application Dialog Box**

  4. Click the **Custom SAML App** button located at the bottom of the dialog box. The **New Application** dialog box is displayed with the **General Info** tab activated, as shown in **Figure 6**.

![](images/uN3Zk741fc-
XWpOy2cjQLdL4Ig8cdw03Juc5dkHI41H_1l1cakyhwMigCyECsvd_pGrGZHFAbKFjyK2z5KFxN5Fey8EBL5IWwoaVe7miLHulcIxPEl3aSywjMFPwfgqRMYRnvyRspdddf4LIXovOK3JZIEsA2EpKriqpRsonP0-R9013SDjd3mzviA)

**Figure 6. General Info Tab in the New Application Dialog Box**

  5. Enter a name for your JumpCloud SAML application in the **Display Label** field. For example, **Cerby SAML Contentzilla**.

The next step is 3\. Configure the connection settings, which you must
complete from the **New Application** dialog box.

* * *

## **3\. Configure the connection settings**

To configure the connection settings of the SAML application with Cerby,
complete the following steps:

  1. Activate the **SSO** tab, as shown in **Figure 7**. 

![](images/WRTKM8LqK_5wyT3whL_1KbgM_6tcjJ1kYUt5IzoiedwOXDJ2qVqQwm31AVHBdZ0zwgS7QE-6dtGqCY05dwmWQ_ENWUObL5LLIXy06n_GvyrnLcdb8NNwEjcF_pJxhRYpy0Be8HQyxgeNJiG3y3M6eQGi5NVnJ9g5acTmyHD_N_d5Wtzq6zLeEmbDLg)

**Figure 7. SSO Tab in the New Application Dialog Box**

  2. Enter the following information in the corresponding fields:

     * Enter **`https://jumpcloud.com`** in the **IdP Entity ID** field.

     * Enter the corresponding values in the **SP Entity ID** and **ACS URL** fields from the **Configure SSO through Your Generic SAML App** page that you left open.

  3. Select the **Declare Redirect Endpoint** option located below on the page.

  4. Enter the attribute metadata required by Amazon Cognito by performing the following actions:

     1. Click three times the **add attribute** button of the **USER ATTRIBUTE MAPPING** field located at the bottom of the dialog box in the **Attributes** section. The **Service Provider Attribute Name** field and **JumpCloud Attribute Name** drop-down list are displayed with three rows, as shown in **Figure 8**.

![](images/N4R16clMFuHUjsPiSjt4PyRRzZ2UpYeTLQmVlpV-
ij4zNLhbcO3cCbHsGbsKRl3UhUbtzd5npP9QT5m2BC6dMSjr4upV6-cY9zk4bWQnL1j8zW6NZDoGay-
wJYg9cORsaI3F06pg-T6ooSiDUugsXdieykNPODkPCE0YCRyyA47z8Xbos9IG9HAUXw)

**Figure 8. Attributes Section**

     2. Select the **email** option from the **JumpCloud Attribute Name** drop-down list in the first row.

     3. Enter **`http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress`** in the **Service Provider Attribute Name** field for the first row.

     4. Select the **lastname** option from the **JumpCloud Attribute Name** drop-down list in the second row.

     5. Enter **`http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname`** in the corresponding **Service Provider Attribute Name** field for the second row.

     6. Select the **firstname** option from the **JumpCloud Attribute Name** drop-down list in the third row.

     7. Enter **`http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name`** in the corresponding **Service Provider Attribute Name** field for the third row.

  5. Activate the **User Groups** tab, as shown in **Figure 9**.

![](images/JT4iTdw6bmQLumcn_-f5uLS-
wGoQpsr415-Z8KZ81oyrTI3whFr_KSOB__1fuBB4ckm16Q02XqY4STYZRDhZPcSM9xkFpxuSnWemgayJo7qg8fwrnMhxejdTfQQz7wAiZHixlU-
ahBkAKQGju148P3cZHw4AgP6HDYyLJbaKZF813jho0JCsA2E1xw)

**Figure 9. User Groups Tab in the New Application Dialog Box**

  6. Select the option of the user group you want to assign the SAML application.

  7. Click the **activate** button located at the bottom of the dialog box. The **Please confirm your new SSO connector instance** dialog box is displayed.

  8. Click the **continue** button. The dialog box closes, and the **SSO** page is displayed with the SAML application you added recently and a success message box.

  9. Open the SAML application you added. The **SAML 2.0** dialog box is displayed.

  10. Activate the **SSO** tab, as shown in **Figure 10**.

![](images/NAXfIHvKXZRwsJs154q8auSkWktXnK7FigcJOlUWKWqEwRXHL67z3UX3wSdbTYRwoiwdnGQZ5SMin2BeGjNNxLTmLaqcAGyWr5vgGdn77G-_g5Qvd6U-aa07wB9FBzmEQTPJwqdZbrsZeVszDYfXUaITI0myp16MSoz06ErNNJfdMi3xokm3rfuNrA)

**Figure 10. SSO Tab in the SAML 2.0 Dialog Box**

  11. Click the **Export Metadata** button below the **JumpCloud Metadata** field. An XML metadata file is automatically downloaded to your computer.

The next step is 4\. Finish the workspace creation in Cerby.

* * *

## **4\. Finish the workspace creation in Cerby**

To finish the workspace creation in Cerby, complete the following steps from
the **Configure SSO through Your Generic SAML App** page that you left open:

  1. Upload the XML that you downloaded recently. The name of the file is displayed below the **Metadata XML file** field when it is uploaded.

**TIP:** You can drag the file from another window or click the button below
the **Metadata XML file** field to look for the file on your computer.

  2. Select the **I have already assigned users or groups to the application** option located in the **4\. Assign People or Groups** section.

  3. Click the **Finish Configuration** button located at the bottom of the page. The **Your Workspace** page is displayed confirming that your workspace has been created successfully.

  4. Click the **Login** button. The login page of JumpCloud is displayed.

  5. Authenticate with the credentials (email address and password) you use for JumpCloud. The Cerby dashboard is displayed.

Now you are done.

{% hint style="danger" %} **IMPORTANT:** Currently, after creating a
workspace, you cannot change its name or update the IdP settings. {% endhint
%}

