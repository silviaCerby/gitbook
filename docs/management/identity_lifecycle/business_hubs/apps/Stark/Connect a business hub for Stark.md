# Connect a business hub for Stark

**Description:** This article describes how to connect a business hub to centrally manage the users of Stark from Cerby.

**Who can use this feature?**

  * Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
  * Only supported using the Cerby web app

  
---  
  
As a user with any workspace role in Cerby, except **Guest User** and **Login-
Only** , you can connect a business hub integration to centrally manage the
users of Stark.

When you connect the business hub, you become its **Owner** , and you can
perform the following user and access management tasks through automated tasks
or API calls executed by the Cerby agent:

  * Check for updates

  * Invite app members

  * Update app members’ roles

  * Remove app members

{% hint style="success" %} **TIP:** For more details about the automated tasks
of a business hub, how it works, and the supported apps, read the article
[Explore Apps](https://help.cerby.com/en/articles/6831152-explore-apps). {%
endhint %}

This article provides instructions on how to connect a business hub for Stark.
For other app-specific articles and videos, review the [Connecting your
business hubs](https://help.cerby.com/en/collections/10289415-connecting-your-
apps) collection in the Cerby Help Center.

* * *

# **Requirements**

The following are the requirements to connect a business hub:

  * A Cerby workspace

  * A Cerby user account with the **Owner** , **Super Admin** , **Admin** , or **User** role

  * A team in Stark

  * Groups configured in your identity provider (IdP) if you want to leverage automatic user provisioning and deprovisioning from your apps based on group assignment events. For more information, read the article [Manage app members from your IdP](https://help.cerby.com/en/articles/9046188-manage-app-members-from-your-idp)

  * An automation account, meaning an active user account with an **Admin** role in Stark to be used as a service account. For instructions and recommendations on how to create and configure this account, read the article [Create an automation or service account for your business hub](https://help.cerby.com/en/articles/9830816-create-an-automation-or-service-account-for-your-business-hub)

  * The user management and login method for your business hub identified to select the corresponding option when connecting your app. For more information, read the **User management and login method** section of the article [Explore Apps](https://help.cerby.com/en/articles/6831152-explore-apps)

  * A business ID. You can find the ID in **the address bar** after logging in to Stark and navigating to the **Manage Team** tab. The ID is displayed in the address bar as part of the URL, between the **organization** and **manage-team** subdirectories. For example, **`12a34b56-7890-123c-4d56-7defg89012h3`** in **`https://account.getstark.co/organization/12a34b56-7890-123c-4d56-7defg89012h3/manage-team`**. Just copy the value and paste it when connecting the business hub.

* * *

# **Connect a business hub for Stark**

To connect a business hub for Stark, you must complete the following main
steps from the Cerby web app dashboard:

  1. Add a business hub and connect it to Stark

  2. Check for updates to import users and roles to Cerby

  3. Connect your Stark user account to the business hub

  4. Manage unmatched users

The following sections describe each main step.

## 1\. [Add a business hub and connect it to
Stark](https://docs.google.com/document/d/1hn6CImgHiemi9Wi-
TYORxWkPo5gw8QCdPSfHAmFNHhw/edit?tab=t.0#heading=h.xa04q566kn1o)

To add a business hub and connect it to Stark, you must complete the following
steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.

  3. Click the **Connect Business Hub** button located at the top-right corner of the page. The **Connect your Business Hubs to Cerby** dialog box is displayed.  
​**TIP:** Select the **Don’t show this again** option to skip this step the
next time you connect a new business hub.

  4. Click the **Get started** button. A wizard is displayed on the **Select app** page.

  5. Select **Stark Hub** from the catalog. The **Enter app details** page is displayed on the wizard.

  6. Enter and select your app information in the corresponding fields:

     * **Label in Cerby: It is the name to assign to your business hub in Cerby, and it will be displayed on the business hub card.**

     * **Business ID:** It is the unique identifier of your business or organization in Stark. For instructions on how to find it, read the Requirements section.

     * **User management and login method:** It is the way your users log in to the app and determines whether they must save their login credentials as a Cerby account connected to the business hub. You must select one of the following methods:

       * **Single sign-on (SSO):** Access is managed by your identity provider, and users log in with SSO authentication. They are not asked to save their credentials in Cerby.

       * **Username and password:** Cerby manages account security and access, and users log in with their credentials after saving them in Cerby.

  7. Click the **Next** button. The **Select automation account** page is displayed with a list of existing Stark accounts.

  8. Select the automation account you have previously added to Cerby, as described in the Requirements section.  
​**NOTE:** If you don’t have an automation account, you are prompted to add
it. Make sure you read Cerby’s recommendations on how to configure it in the
article [Create an automation or service account for your business
hub](https://help.cerby.com/en/articles/9830816-create-an-automation-or-
service-account-for-your-business-hub). You may need to add the account first
and then add the business hub.

  9. Click the **Connect app** button. The wizard closes, and a success message box is displayed.   
The corresponding business hub is also displayed on the **Business Hubs**
view.

The next step is 2\. Check for updates to import users and roles to Cerby.

## 2\. Check for updates to import users and roles to Cerby

To check for updates in your app to identify and import users and roles to
Cerby, you must complete the following steps:

  1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.

  2. Click the **Settings** (![](images/AD_4nXeByVHBSTSp-KuNiohUPzRJ81cmUV-g-W-qM7ABEk0mzfVRcsTnC9XD_6mAQBQObGIKbGJWpnxScMGm_cT3R4uzEzVW0ZAsqkGoo-cmatfJC_I2vgLsWIrLnwQAUqoT_5Llg9mz)) icon of the corresponding business hub card. The business hub details page is displayed with the **Settings** tab activated.

  3. Click the **Check for updates** button located at the top right of the page. A message box is displayed with information about the process.  
​**NOTE:** The check and import process may take a few minutes depending on
the number of users, and because Cerby automatically matches users to their
corresponding Cerby user account.

  4. Confirm that the automated task to check for updates has the “Completed” status by performing any of the following actions:

     * Click the **More details** button from the message box.

     * Select the **Automation** option from the left navigation drawer to open the **Automation** view with a list of automated tasks and their status. 

{% hint style="info" %} **NOTE:** Cerby automatically performs daily checks
for updates for all business hubs, but you can trigger them manually, as
described in this section. When a user is deprovisioned from an IdP and a
check for updates is performed, Cerby generates a report and sends business
hub **Owners** an email to confirm their removal from the app. For more
instructions, read the article [Check for updates in your app and apply
report](https://help.cerby.com/en/articles/9046205-check-for-updates-in-your-
app-and-apply-report). {% endhint %}

The next step is 3\. Connect your Stark user account to the business hub.

## 3\. Connect your Stark user account to the business hub

To connect your Stark user account to the business hub so Cerby can manage and
protect it, you must complete the following steps:

  1. Select the **Accounts** option from the left navigation drawer. The **Accounts** view is displayed.

  2. Click the **Log in** button of the corresponding Stark Hub account card. The **Connect your Stark Hub Account** dialog box is displayed.

  3. Enter the login credentials of your Stark user account.

  4. Click the **Connect account** button. The dialog box closes, and a success message box and a new account card are displayed.

The next step is 4\. Manage unmatched users.

## 4\. Manage unmatched users

During a check for updates, Cerby automatically matches app members to the
Cerby user accounts that correspond to their email addresses, including
existing [guest users](https://help.cerby.com/en/articles/8392946-explore-
guest-users) and [local
partners](https://help.cerby.com/en/articles/8980877-explore-
partners#h_7e4add33a2). Manual matching is required when apps don't provide
email addresses and for app members using personal or external accounts that
couldn’t be identified or are not in the corporate directory.

To view the status of the imported app members, you must complete the
following steps:

  1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.

  2. Click the **More options** (![](images/AD_4nXewApJOBZXewpFew1XrkjC6rCssB5Upy2WRCW8fpJjw2Zmj0xzSkEgw3tUBvW6lyQC2RihdmxzJ6KKXG1pvMGfAeaQnjZUGnThkBo5vdisjtu8WvqHXLgT1_7-xOwkkFy5umyicPg)) icon of the corresponding business hub card. A drop-down list is displayed.

  3. Select the **View Members** option from the list. The business hub details page is displayed with the **Members** tab activated.  
App members are displayed in the following tabs of the **User Overview**
section:

     * **Unmatched users:** This tab displays the users who were not automatically matched.

     * **Onboarded users:** This tab displays the users matched to their Cerby user account. 

     * **Guest users:** This tab displays the users who were matched to an existing Cerby user account but it doesn’t exist in the corporate directory, such as external collaborators.

For unmatched users, you can perform one of the following actions:

  * Match users

  * Remove unmatched users

  * Exempt unmatched users

The following sections describe each action.

### **Match users**

To match users, you must complete the following steps from the **Unmatched
users** tab of the business hub details page:

  1. Click the **Match user** button of the corresponding user. The **Match user** dialog box is displayed.

  2. Enter the username or email address of the user you want to match and invite in the **Match with** field. The user is displayed on a list.

  3. Select the user from the list.

  4. Click the **Next** button. The **Select Cerby role** dialog box is displayed.

  5. Select the role to assign to the user on the business hub **Cerby role** drop-down list:

     * **Owner:** This role enables sharing access and managing business hub settings in Cerby.

     * **Collaborator:** This role enables only logging in to the app from Cerby.

  6. Click the **Match user** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Onboarded** **users** tab.

### **Remove unmatched users**

To remove unmatched users, you must complete the following steps from the
**Unmatched users** tab of the business hub details page:

{% hint style="danger" %} **IMPORTANT:** When removing an unmatched user,
Cerby performs an automated task to revoke the user’s seat and permissions in
Stark. {% endhint %}

  1. Click the **More options** (![](images/AD_4nXewApJOBZXewpFew1XrkjC6rCssB5Upy2WRCW8fpJjw2Zmj0xzSkEgw3tUBvW6lyQC2RihdmxzJ6KKXG1pvMGfAeaQnjZUGnThkBo5vdisjtu8WvqHXLgT1_7-xOwkkFy5umyicPg)) icon of the corresponding user. A drop-down list is displayed.

  2. Select the **Remove user** option from the list. The **Remove user?** dialog box is displayed.

  3. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from the app via an automated task.

### **Exempt unmatched users**

Exempted users keep their user accounts or seats active in your app, but you
cannot manage them through Cerby.

To exempt unmatched users, you must complete the following steps from the
**Unmatched users** tab of the business hub details page:

  1. Click the **More options** (![](images/AD_4nXewApJOBZXewpFew1XrkjC6rCssB5Upy2WRCW8fpJjw2Zmj0xzSkEgw3tUBvW6lyQC2RihdmxzJ6KKXG1pvMGfAeaQnjZUGnThkBo5vdisjtu8WvqHXLgT1_7-xOwkkFy5umyicPg)) icon of the corresponding user. A drop-down list is displayed.

  2. Select the **Exempt user** option from the list. The exempt user dialog box is displayed.

  3. Enter a reason for exempting the user in the **Provide a reason** field.

  4. Click the **Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

* * *

# **Use your business hub**

The following are the supported features of business hubs you can use:

  * [Join the App and connect it to Cerby](https://help.cerby.com/en/articles/9046232-join-the-app-and-connect-it-to-cerby)

  * [Invite new app members](https://help.cerby.com/en/articles/9045790-invite-new-app-members)

  * [Remove app members](https://help.cerby.com/en/articles/9046186-remove-app-members)

  * [Manage app members from your IdP](https://help.cerby.com/en/articles/9046188-manage-app-members-from-your-idp)

  * [Update the app members’ roles](https://help.cerby.com/en/articles/9046201-update-the-app-members-roles)

  * [Check for updates in your app and apply report](https://help.cerby.com/en/articles/9046205-check-for-updates-in-your-app-and-apply-report)

  * [Re-assign the app members’ user accounts](https://help.cerby.com/en/articles/9046211-re-assign-the-app-members-user-accounts)

  * [Manage the security of app members’ user accounts](https://help.cerby.com/en/articles/9046212-manage-the-security-of-app-members-user-accounts)

  * [Log in to your app](https://help.cerby.com/en/articles/9046222-log-in-to-your-app)

  * [Track activity on app members’ user accounts](https://help.cerby.com/en/articles/9046226-track-activity-on-app-members-user-accounts)

  * [Remove an App](https://help.cerby.com/en/articles/9046230-remove-an-app)

