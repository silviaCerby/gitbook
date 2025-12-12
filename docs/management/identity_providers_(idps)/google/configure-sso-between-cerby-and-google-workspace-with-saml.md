---
description: This article describes how to configure Google Workspace as your IdP to enable SSO for Cerby using a custom SAML app.
---

# Configure SSO between Cerby and Google Workspace with SAML

When you create a Cerby workspace, you can configure Google as your identity provider (IdP) to provide single sign-on (SSO) authentication for the users of your corporate directory. This integration enables seamless authentication, as users securely log in to Cerby with one set of credentials.

This article describes how to configure your Google Workspace as the primary IdP to enable SSO using a custom security assertion markup language (SAML) app for Cerby.

* * *

# Supported features

The following are the supported features of configuring SSO between Cerby and Google Workspace:

  * Control who has access to Cerby from Google Workspace.
  * **Service provider-initiated authentication flow:** This authentication flow occurs when users attempt to log in to the app from Cerby.
* * *

# Requirements

The following are the requirements to configure SSO between Cerby and Google:

  * A Google Workspace tenant
  * A user account in Google Workspace with the **Super Administrator** role in your tenant
  * A user account in Cerby with the workspace**Owner** role
  * An invitation sent from Cerby Support via email to create a workspace
​**IMPORTANT:** If you have not received an invitation, send an email to [support@cerby.com](mailto:support@cerby.com) with your request.

* * *

# Configure SSO between Cerby and Google Workspace with SAML

To configure SSO between Cerby and Google Workspace with a custom SAML app, you must complete the following main steps:

  1. Set up a workspace in Cerby
  2. Add a custom SAML app in Google Workspace
  3. Retrieve metadata information from Google Workspace and enter it in Cerby

{% hint style="info" %}


**NOTE:** Depending on the use case, you may be redirected to the Google authentication portal if a session has not been established.


{% endhint %}

The following sections describe each main step.

## 1\. Set up a new workspace in Cerby

To set up a new workspace in Cerby, complete the following steps:

  1. Click the **Create my workspace** button from the invitation email you received from Cerby. The **Welcome to Cerby** page is displayed, as shown in **Figure 1**.
​

<figure><img src="../.gitbook/assets/54d331fd-730c-4fcd-9129-e6ad2ac9ad6a.png" alt=""><figcaption></figcaption></figure>

**Figure 1. Welcome to Cerby** page

  2. Click the **Continue with Google Workspace** button. The **Create your workspace** page is displayed, as shown in **Figure 2**.

<figure><img src="../.gitbook/assets/a783891d-ff6f-4660-beb2-cd521bf3b6db.png" alt=""><figcaption></figcaption></figure>

**Figure 2. Create your workspace** page

  3. Enter the name of your workspace in the **Workspace name** field.
  4. Click the **Create workspace** button. The **Configure SSO through Google Workspace App** page is displayed with instructions to configure the Cerby app in your Google Workspace tenant, as shown in **Figure 3**.

<figure><img src="../.gitbook/assets/9f72aa71-5146-4957-9999-5926db79b71d.png" alt=""><figcaption></figcaption></figure>

**Figure 3.** **Configure SSO through Google Workspace App** page

{% hint style="danger" %}


**IMPORTANT:** Keep the **Configure SSO through Google Workspace App** page open because it contains the required values that you must provide to Google and Cerby to complete the configuration.


{% endhint %}

The next step is 2\. Add a custom SAML app in Google Workspace.

## 2\. Add a custom SAML app in Google Workspace

To add a custom SAML app in Google Workspace, complete the following steps:

  1. Log in to the [Google Admin Console](https://admin.google.com/) of your organization in a new browser tab.
  2. Select the **Web and mobile apps** option from the**Apps** drop-down list in the left menu. The **Web and mobile apps** page is displayed.
  3. Add a custom SAML app by completing the following steps:
     1. Select the **Add custom SAML app** option from the **Add app** drop-down menu. The **Add custom SAML app** page is displayed with a wizard on the **App details** step, as shown in **Figure 4**.

<figure><img src="../.gitbook/assets/cd6e6615-4fbb-4a41-ba12-81bfa7ef9e4a.png" alt=""><figcaption></figcaption></figure>

**Figure 4.** **Add custom SAML app** page in the Google Admin Console

     2. Enter **Cerby** in the **App name** field.
     3. Upload the Cerby logo in the **App icon** section by completing the following steps:
        1. Download to your computer the logo shown in **Figure 5**.

<figure><img src="../.gitbook/assets/f665e6b4-94a6-4667-a0ba-d8ffaf520b2a.png" alt=""><figcaption></figcaption></figure>

**Figure 5.** Cerby logo

        2. Click the **Camera** (<figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1696413103/e3f1a40e409a672a87d73c44b70c/d1022570-bd48-4284-aaae-7329baacb8e2?expires=1756458000&signature=eee90eeec3c111a0a40fe947d615c5076b363813d86d8e8a884e4276a3346f44&req=dSYuEM1%2FnoBfWvMW3Hu4gUfb7vTn9XkhPe4qnbRgcIlNeLqLdDk4ELzO086X%0AfA%3D%3D%0A" alt=""><figcaption></figcaption></figure>) icon.
        3. Select the Cerby logo file from your computer.
  4. Click the **CONTINUE** button. The **Google Identity Provider details** step of the wizard is displayed.
  5. Click the **DOWNLOAD METADATA** button to download an XML file that contains all the information Cerby needs to configure the SAML connection.
​**IMPORTANT:** Make sure you download the XML file, because you need it later.

  6. Click the **CONTINUE** button. The **Service provider details** step of the wizard is displayed.
  7. Copy the values from the browser tab you left open when completing step 1\. Set up a new workspace in Cerby to paste them into their corresponding fields in the Google Admin Console, as shown in **Figure 6** :

     * **ACS URL**
     * **Entity ID**
​

<figure><img src="../.gitbook/assets/18436bbe-1c86-433b-a3e0-4125fb342350.png" alt=""><figcaption></figcaption></figure>

**Figure 6.** Required values in the **Service provider details** step

  8. Enter **`https://app.cerby.com`** in the **Start URL (optional)** field.
  9. Click the **CONTINUE** button. The **Attribute mapping** step of the wizard is displayed.
  10. Map the required attributes from Table 1. Attribute mappings in Google Directory by completing the following steps:
     1. Click the **ADD MAPPING** button. A new row is displayed with a drop-down menu and an empty field.
     2. Select the corresponding option from the drop-down menu in the **Google Directory attributes** column.
     3. Enter the corresponding value in the empty field of the **App attributes** column. **Figure 7** shows how the page looks with all the mapping attributes.

<figure><img src="../.gitbook/assets/e467b9f6-b0b0-4b72-a57f-885f342b459a.png" alt=""><figcaption></figcaption></figure>

**Figure 7.** Attribute mappings in Google Directory

  11. Click the **FINISH** button. The page closes, and the **Cerby** SAML app details page is displayed.
  12. Turn on the Cerby SAML app for all users or specific organizations by following the instructions in the section [Step 2: Turn on your SAML app](https://support.google.com/a/answer/6087519#zippy=%2Cstep-turn-on-your-saml-app) of the official Google Workspace documentation.

The next step is 3\. Retrieve metadata information from Google Workspace and enter it in Cerby.

## 3\. Retrieve metadata information from Google Workspace and enter it in Cerby

To retrieve metadata information from Google Workspace and enter it in Cerby, complete the following steps from the **Configure SSO through Google Workspace App** page you left open:

  1. Upload the XML file you downloaded previously in the **Metadata XML file** section.
  2. Select the **I have already assigned users or groups to the application** option.
  3. Click the **Finish Configuration** button. A success message is displayed.

Now you are done. You can proceed to log in to your [Cerby](https://app.cerby.com/) workspace.

{% hint style="info" %}


**NOTE:** The SAML-based integration leverages Google only for authentication. To assign permissions for Cerby, users must do so directly in Cerby.


{% endhint %}{% hint style="danger" %}


**IMPORTANT** : This integration does not currently support IdP-initiated login from Google, so the tile in the Google Workspace dashboard created automatically after completing the configuration will not work. You can add a bookmark for all users and enrolled browsers pointing to your Cerby workspace. Just follow the instructions to add a bookmark in the official documentation [Manage bookmarks](https://support.google.com/chrome/a/answer/10265060?hl=en&sjid=9969570391997900493-NC). The bookmark URL is **`https://<workspace-name>.cerby.com`**, where you must include your workspace name; for example, if your workspace name is **Cerby** , the bookmark URL must be **`https://cerby.cerby.com`**.


{% endhint %}

* * *

# Table 1. Attribute mappings in Google Directory

The following table shows the attribute mappings in Google Directory you must configure as part of step 2\. Add a SAML-based custom app to your Google Workspace:

**Google Directory attributes**| **App attributes**
---|---
**Name**| **`http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name`**
**Family Name**| **`http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname`**
**Email Address**| **`http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress`**

**Table 1.** Attribute mappings in Google Directory

* * *

# Troubleshooting: “Error: app_not_configured_for_user” message

When you complete the configuration described in this article and immediately try to access your Cerby workspace, you may encounter the “Error: app_not_configured_for_user” message, as shown in **Figure 7**.

<figure><img src="../.gitbook/assets/492ffb0b-02fd-471a-ba17-85e1f8b123ac.png" alt=""><figcaption></figcaption></figure>

**Figure 7.** “Error: app_not_configured_for_user” message in your web browser

This issue happens because changes in the Google Admin console take time to propagate across services and users. For more information, read the official documentation [How changes propagate to Google services](https://support.google.com/a/answer/7514107?sjid=17262937684630672603-NC).

To solve the issue, refresh the page or log out and then log in to your Google account.
