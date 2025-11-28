# Enable Okta Universal Logout for Cerby

**Description:** This article describes how to enable Okta Universal Logout for Cerby.

{% hint style="info" %} **Who can use this feature?** * Workspace**Owners** ,
**Super Admins** , and **Admins** * Okta **Admins** * Only supported using the
Cerby web app and the Okta Admin dashboard {% endhint %}

As an Okta**Admin** , you can leverage Okta’s [Universal
Logout](https://help.okta.com/oie/en-us/content/topics/itp/universal-
logout.htm) feature to trigger the logout action from Okta and extend it to
Cerby. Because Cerby is included in the Okta Integration Network (OIN) app
catalog, you must only enable it through the Okta dashboard.

As a Cerby workspace**Admin** , **Super Admin** , or **Owner** , you can
enable Okta Universal Logout in Cerby to extend this functionality to Cerby
from the Okta dashboard.

{% hint style="danger" %} **IMPORTANT:** Users must be created via SCIM for
the Universal Logout feature to work. {% endhint %}

* * *

# Requirements

The following are the requirements to set up the Universal Logout feature:

  * A Cerby workspace

  * A user account in Cerby with the workspace**Owner** , **Super Admin** , or **Admin** role

  * An Okta tenant

  * A user account in Okta with **Admin** privileges

  * The Okta instance ID for Cerby. To retrieve this ID, you must complete the following steps:

    1. Log in to your organization's[ Okta Admin Console](https://developer.okta.com/login/).

    2. Select the **Applications** option from the **Applications** drop-down list in the left navigation drawer. The **Applications** page is displayed.

    3. Select the **Cerby** app integration.

    4. Verify that the URL displayed in the browser's address bar has the following format: `https://{your-company}-admin.okta.com/admin/app/<APPLICATION_NAME>/instance/<APPLICATION_ID>/`

    5. Copy and save the <APPLICATION_ID> value.

* * *

# Configure Okta Universal Logout for Cerby

To configure Okta Universal Logout for Cerby, you must complete the following
main steps:

  * Enable Okta Universal Logout for Cerby

  * Extend Okta’s Universal Logout to Cerby

The following sections describe each main step.

## Enable Okta Universal Logout for Cerby

To enable Universal Logout in Cerby, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace. 

  2. Select the **Settings** option in the left navigation drawer. The **Workspace Configuration** view is displayed.

  3. Activate the **IDP Settings** tab.

  4. Activate the **Enable Okta Universal Logout** switch in the **Universal Logout** section. The **Universal Logout Config** dialog box is displayed, as shown in **Figure 1**.

![](images/Screenshot+2025-01-31+at+4_12_05%E2%80%AFp_m_.png)

**Figure 1.** **Universal Logout Config** dialog box

  5. Enter the Okta instance ID for Cerby in the **App instance Id** field. You retrieved this value as part of the Requirements section.

  6. Click the **Enable Universal Logout** button. The dialog box closes, and the **IDP** **Settings** tab in the **Workspace Configuration** view is displayed.

Now you are done.

## **Extend Okta Universal Logout to Cerby**

To extend Okta Universal Logout to Cerby, you must complete the following
steps:

  1. Log in to your organization's[ Okta Admin Console](https://developer.okta.com/login/).

  2. Select the **Applications** option from the **Applications** drop-down list in the left navigation drawer. The **Applications** page is displayed.

  3. Select the **Cerby** app. The **Cerby** **Overview** page is displayed.

  4. Activate the **Authentication** tab.

  5. Click the **Edit** option in the **Logout** section. 

  6. Select the **Okta system or admin initiates logout** checkbox.

  7. Click the **Save** button.

Now you are done.

