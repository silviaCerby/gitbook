---
description: "This article describes how to configure your identity provider to enable SSO for Cerby using a custom SAML integration."
intercom_id: 13328190
---

# Configure SSO between Cerby and your IdP with SAML

With Cerby, you can configure your identity provider (IdP), such as Okta and Entra ID, to provide single sign-on (SSO) authentication for the users of your corporate directory. This integration facilitates a seamless login experience, enabling users to securely access Cerby with a single set of credentials.

Cerby utilizes the Security Assertion Markup Language (SAML) 2.0 standard for this purpose and leverages Amazon Cognito as its underlying identity service. Therefore, a custom SAML application must be configured to point to a specific Cerby workspace.

This article describes how to configure a primary IdP for your Cerby workspace using a SAML integration, as well as the authentication flow. For configuration guides of specific IdPs, read the following articles:

  * [Configure SSO between Cerby and Okta with SAML](https://help.cerby.com/en/articles/5457568-configure-sso-between-cerby-and-okta-with-saml)
  * [Configure SSO between Cerby and Entra ID with SAML](https://help.cerby.com/en/articles/5457563-configure-sso-between-cerby-and-entra-id-with-saml)
  * [Configure SSO between Cerby and Google Workspace with SAML](https://help.cerby.com/en/articles/5560674-configure-sso-between-cerby-and-google-workspace-with-saml)
  * [Configure SSO between Cerby and OneLogin with SAML](https://help.cerby.com/en/articles/11814820-configure-sso-between-cerby-and-onelogin-with-saml)
  * [Configure SSO between Cerby and JumpCloud with SAML](https://help.cerby.com/en/articles/6550878-configure-sso-between-cerby-and-jumpcloud-with-saml)
* * *

## The SAML authentication flow

With SSO using the SAML standard, you centralize access control, ensuring that only authenticated users in your corporate directory can access the Cerby workspace and the disconnected or nonfederated apps managed through Cerby.

Cerby sits in the middle of the authentication flow, acting as a service provider (SP) to your corporate IdP while functioning as an access controller for your target applications.

The following is the authentication flow:

1. **Request:** A user attempts to log in to Cerby (SP-initiated flow).
2. **Redirect:** Cerby redirects the user to your IdP for authentication.
3. **Assertion:** The IdP authenticates the user and sends a signed SAML assertion back to Cerby’s assertion customer service (ACS) URL.
4. **Access:** Cerby validates the assertion and grants the user access to the Cerby workspace. Within the workspace, Cerby facilitates secure access to the target apps.

**Table 1** describes the responsibilities of the IdP and Cerby in the authentication flow.

**Feature**| **IdP**| **Cerby**
---|---|---
Authentication| Primary source of truth for user identity. Handles user login credentials, multi-factor authentication (MFA), and conditional access.| Validates the SAML assertion received from the IdP; does not store user login credentials for the IdP.
Authorization| Defines _who_ can access a Cerby workspace via group or user assignments.| Defines _what_ those users can do inside Cerby, according to Cerby’s Role-Based Access Control (RBAC) system.
Attributes| Provides user metadata required to identify the user.| Uses attributes to create and sync user accounts.

**Table 1.** Responsibilities in the authentication flow

* * *

## Supported features

The following are the supported features of configuring SSO between Cerby and your IdP with SAML:

  * Control who has access to Cerby from your IdP.
  * **SP-initiated authentication flow:** This authentication flow occurs when users attempt to log in to the application from Cerby.
  * **Automatic user account creation in Cerby:** This provisioning flow in Cerby occurs automatically on the initial SSO.
* * *

## Requirements

The following are the requirements to configure SSO in Cerby with your IdP:

  * A tenant in your IdP that supports SAML 2.0 with the following required user attributes ready for mapping:
    * **Email**
    * **Name**
    * **First name**
    * **Last name**
  * A user account in your IdP tenant with privileges to create and configure a SAML application. Commonly, you need an administrator role
  * An invitation sent from Cerby Support via email to create a workspace
​**IMPORTANT:** If you have not received an invitation, send an email to [support@cerby.com](mailto:support@cerby.com) with your request

  * Users and groups created beforehand in the corporate directory integrated with your IdP. Follow the official instructions of your IdP to manage users and groups
* * *

## Configure SSO between Cerby and your IdP with SAML

To configure SSO in Cerby with your IdP, you must complete the following main steps:

  1. [Set up a workspace in Cerby](configure-sso-between-cerby-and-your-idp-with-saml.md#id-1.-set-up-a-workspace-in-cerby)
  2. [Create a SAML application in your IdP](configure-sso-between-cerby-and-your-idp-with-saml.md#id-2.-create-a-saml-application-in-your-idp)
  3. [Configure SSO and the connection settings in your IdP](configure-sso-between-cerby-and-your-idp-with-saml.md#id-3.-configure-sso-and-the-connection-settings-in-your-idp)
  4. [Assign users and groups to the SAML application in your IdP](configure-sso-between-cerby-and-your-idp-with-saml.md#id-4.-assign-users-and-groups-to-the-saml-application-in-your-idp)
  5. [Finish the workspace creation in Cerby](configure-sso-between-cerby-and-your-idp-with-saml.md#id-5.-finish-the-workspace-creation-in-cerby)

{% hint style="info" %}


**NOTE:** Depending on the use case, you may be redirected to your IdP for authentication if a session has not been established.


{% endhint %}

The following sections describe each main step.

### 1\. Set up a workspace in Cerby

To set up a workspace in Cerby, complete the following steps:

  1. Click the **Create my workspace** button from the invitation email you received from Cerby. The **Welcome to Cerby** page is displayed, as shown in **Figure 1**.

<img src="../.gitbook/assets/0f17eb3a-1685-4ec1-b8dd-40b778b63378.png" alt="">

**Figure 1. Welcome to Cerby** page

  2. Click the **Continue with Generic SAML** button. The **Create your workspace** page is displayed, as shown in **Figure 2**.

<img src="../.gitbook/assets/f84db682-6551-4d9a-a5d5-ef81feab14e7.png" alt="">

**Figure 2. Create your workspace** page

  3. Enter the name of your workspace in the**Workspace name** field.
​**NOTE:** Remember the workspace name that you have entered. You need it later.

  4. Click the **Create workspace** button. The**Configure SSO through Your Generic SAML App** page is displayed, as shown in **Figure 3**.

<img src="../.gitbook/assets/bccd3a07-ddf9-48a6-993b-873883102632.png" alt="">

**Figure 3.** **Configure SSO through Your Generic SAML App** page

{% hint style="danger" %}


**IMPORTANT:** Keep the **Configure SSO through Your Generic SAML App** page open because it contains the required values, **SP Entity ID** and **ACS URL** , that you must provide to your IdP to complete the configuration.


{% endhint %}

The next step is [2. Create a SAML application in your IdP](configure-sso-between-cerby-and-your-idp-with-saml.md#id-2.-create-a-saml-application-in-your-idp), which you must complete from your IdP.

### 2\. Create a SAML application in your IdP

To create a SAML application in your IdP, complete the following steps:

  1. Log in to your IdP admin console with the role that enables you to create and configure a SAML application.
  2. Create a new application and select SAML 2.0.
  3. Enter a name for the SAML application. For example, **Cerby SAML**.
  4. Specify **`https://app.cerby.com`** as the start URL, if required.

The next step is [3. Configure SSO and the connection settings in your IdP](configure-sso-between-cerby-and-your-idp-with-saml.md#id-3.-configure-sso-and-the-connection-settings-in-your-idp), which you must complete from your IdP.

### 3\. Configure SSO and the connection settings in your IdP

To configure SSO and the connection settings of the SAML application with Cerby, complete the following steps:

  1. Go to the SSO settings page in your IdP.
  2. Copy the following values from the **Configure SSO through Your Generic SAML App** page that you left open in step [1. Set up a workspace in Cerby](configure-sso-between-cerby-and-your-idp-with-saml.md#id-1.-set-up-a-workspace-in-cerby):

     * **SP Entity ID**
     * **ACS URL**

  3. Paste the values in the corresponding fields of your SSO settings. These fields vary by IdP, so take the following into consideration:

     * The common equivalents of **SP Entity ID** are the **Audience** , **Identifier** , or **Entity ID** fields
     * The common equivalents of **ACS URL** are **Single Sign-On URL** , **Reply URL** , or **Consumer URL**

  4. Map the required attributes from [Table 2. Attribute mapping reference](configure-sso-between-cerby-and-your-idp-with-saml.md#table-2.-attribute-mapping-reference).
  5. Test the SAML application, if this feature is available, to make sure the provided values and attributes are correct.
  6. Save your configuration.
  7. Go to the SAML metadata page or section. For more instructions, read the official documentation of your IdP.
  8. Download or export an XML file to your computer with the IdP metadata.

{% hint style="danger" %}


**IMPORTANT:** If you enter incorrect values and attributes in your IdP, you and the users in your organization won’t be able to log in to Cerby.


{% endhint %}

The next step is [4. Assign users to the SAML application in your IdP](configure-sso-between-cerby-and-your-idp-with-saml.md#id-4.-assign-users-and-groups-to-the-saml-application-in-your-idp), which you must complete from your IdP.

### 4\. Assign users and groups to the SAML application in your IdP

To assign users and groups to the SAML application in your IdP, complete the following steps:

  1. Go to the user assignment settings page in your IdP.
  2. Assign existing users to the SAML application. For more instructions, read the official documentation of your IdP.
  3. Go to the group assignment settings page in your IdP.
  4. Assign existing groups to the SAML application. For more instructions, read the official documentation of your IdP.

The next step is [5. Finish the workspace creation in Cerby](configure-sso-between-cerby-and-your-idp-with-saml.md#id-5.-finish-the-workspace-creation-in-cerby), which you must complete in Cerby.

### 5\. Finish the workspace creation in Cerby

To finish the workspace creation in Cerby, complete the following steps from the **Configure SSO through Your Generic SAML App** page that you left open:

  1. Upload the XML file that you downloaded recently. The name of the file is displayed below the **Metadata XML file** field when it is uploaded.
​**TIP:** You can drag the file from another window or click the button below the **Metadata XML file** field to look for the file on your computer.

  2. Select the **I have already assigned users or groups to the application** option located in the **4\. Assign People or Groups** section.
  3. Click the **Finish Configuration** button located at the bottom of the page. A success message is displayed.

Now you are done. You can proceed to log in to your [Cerby](https://app.cerby.com/) workspace with the same login credentials of your IdP.

{% hint style="danger" %}


**IMPORTANT:**

  * After configuring SSO in a new workspace, it might take some time to propagate changes across all services. During this window, you might briefly be redirected to the fallback Cerby login page or notice that recently added users and settings haven’t appeared yet. This is the expected behavior. Please wait until the propagation is complete, then log in again.
  * Currently, after creating a workspace, you cannot change its name or update the IdP settings.
  * The first user to log in to Cerby is assigned the workspace **Owner** role. For more information about roles, read the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles#h_e203df23da).


{% endhint %}{% hint style="info" %}


**NOTE:** The SAML-based integration leverages your IdP only for authentication. To assign permissions for Cerby, users must do so directly in Cerby.


{% endhint %}

* * *

## Table 2. Attribute mapping reference

Attribute names are case-sensitive and vary by provider. Some IdPs require a simple string (for example, email), while others require a full URI (for example, a schema URL).

**Table 2** provides a reference for the most common attribute mappings. Use these values to ensure your IdP communicates correctly with Cerby for user provisioning and identification.

**Cerby required attribute**| **Equivalent attribute in your IdP**| **Common URI or claim name**
---|---|---
email| User email or NameID| `http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress`
name| Full name or Display name| `http://schemas.xmlsoap.org/ws/2005/05/identity/claims/fullname`
firstName| Given name| `http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname`
lastName| Surname| `http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname`

**Table 2.** Common attribute mapping

{% hint style="danger" %}


**IMPORTANT:** Refer to the map user attributes section of your IdP’s official documentation to ensure you are using the correct values for your specific environment. If these attributes are missing or misconfigured, users may be able to authenticate but will fail to create a profile within the Cerby workspace.


{% endhint %}

* * *

## Troubleshooting common authentication issues

**Table 3** shows the common authentication issues, the potential cause, and the proposed solution after configuring SSO between Cerby and your IdP with SAML.

**Issue**| **Potential cause**| **Solution**
---|---|---
Invalid SAML response| Certificate mismatch| Contact the Cerby Support team through email ([support@cerby.com](mailto:support@cerby.com)) or the help chat to ensure the metadata XML file uploaded to Cerby matches the current signing certificate in your IdP
User access denied after login| User not assigned in IdP| Verify the user is assigned to the SAML application within your IdP's user assignments
Profile missing first or last name| Attribute mapping failure| Ensure the attributes in your IdP exactly match Cerby's requirements, according to [Table 2. Attribute mapping reference](configure-sso-between-cerby-and-your-idp-with-saml.md#table-2.-attribute-mapping-reference)
Entity ID mismatch| Incorrect audience URI| Contact the Cerby Support team through email ([support@cerby.com](mailto:support@cerby.com)) or the help chat to ensure that the **Entity ID** in your IdP matches the one provided by Cerby during the configuration

**Table 3.** Common authentication issues and their solutions
