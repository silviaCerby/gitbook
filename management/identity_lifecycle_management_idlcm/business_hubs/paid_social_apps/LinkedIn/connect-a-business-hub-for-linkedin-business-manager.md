---
description: "This article describes how to connect a business hub to centrally manage the users and assets of LinkedIn Business Manager from Cerby."
intercom_id: 9816555
---

# Connect a business hub for LinkedIn Business Manager

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* Only supported using the Cerby web app


{% endhint %}

As a user with any workspace role in Cerby, except **Guest User** and **Login-Only** , you can connect a business hub integration to centrally manage the users and assets of LinkedIn Business Manager.

When you connect a business hub, you become its **Owner** , and you can perform the following user and access management tasks from Cerby through automation :

* Check for updates
* Invite app members
* Update app member’s roles
* Remove app members

**TIP:** For more details about the automated tasks of a business hub, how it works, and the supported apps, read the article [Explore Business hubs](https://help.cerby.com/en/articles/6831152-explore-apps).
---

Additionally, you can manage the following LinkedIn Business Manager assets from Cerby:

* Partners
* People
* Accounts
* Pages

**IMPORTANT:** Note that the Cerby integration imports all people from your LinkedIn Business Manager, including those who are still in **INVITED** status and have not yet accepted the invitation.
---

This article provides instructions for connecting a business hub for LinkedIn Business Manager. For other app-specific articles and videos, review the [Connecting your business hubs](https://help.cerby.com/en/collections/10289415-connecting-your-apps) collection in the Cerby Help Center.

* * *

## Requirements

The following are the requirements to connect a business hub:

  * A Cerby workspace
  * A Cerby user account with any workspace role
  * A LinkedIn personal account with multi-factor authentication (MFA) turned on and managed by Cerby. The following are the guides you can refer to set up your LinkedIn account properly:
  * To turn on MFA for your LinkedIn account, follow the steps in the official guide [Turn two-step verification on and off](https://www.linkedin.com/help/linkedin/answer/a1381088/turn-two-step-verification-on-and-off)
  * To configure Cerby to manage your LinkedIn account, follow the steps in the article [How to turn on MFA managed by Cerby](https://help.cerby.com/en/articles/8429534-how-to-turn-on-2fa-managed-by-cerby)
  * Your LinkedIn personal account must be part of a [LinkedIn Business Manager](https://business.linkedin.com/marketing-solutions/business-manager) account created to manage your LinkedIn assets
  * An automation account, meaning an active LinkedIn user account with a native **Admin** role in LinkedIn Business Manager.
  * A group assignment configured in your identity provider (IdP) if you want to leverage automatic user provisioning and deprovisioning from your apps based on IdP events. For more information, read the **App user provisioning and deprovisioning** section of the article [Explore Business hubs](https://help.cerby.com/en/articles/6831152-explore-apps)
  * The user management and login method for your business hub identified to select the corresponding option when connecting your app. For more information, read the **User management and login method** section of the article [Explore Business hubs](https://help.cerby.com/en/articles/6831152-explore-apps)
  * The LinkedIn Business Manager ID. You can find the ID as follows:

    1. Log in to [LinkedIn Business Manager](https://business.linkedin.com/marketing-solutions/business-manager) using your LinkedIn account credentials. The LinkedIn Business Manager main page is displayed
    2. Locate the 19-digit numerical ID under the LinkedIn Business Manager name on the left pane, as shown in **Figure 1**

<img src="../../../../../../.gitbook/assets/AD_4nXeLQIjoy60EI-ytezN5yT7uK7_WqLIdBbaYfixkL8o7ESl13q95vRv4f9-oiqBthaE2msO3aKvE1dcOhK2B6cuNalofYayo_puOjtCMlqIPcHtTZbIfZkLYwZ-gb-q31Ple4tbHHXJ_CI6G8sY2Eo0iKwck.png" alt="">

**Figure 1.** Location of the LinkedIn Business Manager ID

* * *

## Connect a business hub for LinkedIn Business Manager

To connect a business hub to LinkedIn Business Manager, you must complete the following main steps from the Cerby web app dashboard:

  1. [Add a business hub and connect it to LinkedIn Business Manager](connect-a-business-hub-for-linkedin-business-manager.md#id-1.-add-a-business-hub-and-connect-it-to-linkedin-business-manager)
  2. [Check for updates to import users, roles, and assets to Cerby](connect-a-business-hub-for-linkedin-business-manager.md#id-2.-check-for-updates-to-import-users-roles-and-assets-to-cerby)
  3. [Connect your app’s user account to the business hub](connect-a-business-hub-for-linkedin-business-manager.md#id-3.-connect-your-apps-user-account-to-the-business-hub)
  4. [Manage unmatched users](connect-a-business-hub-for-linkedin-business-manager.md#id-4.-manage-unmatched-users)

The following sections describe each main step.

### 1\. Add a business hub and connect it to LinkedIn Business Manager

To add a business hub and connect it to LinkedIn Business Manager, you must complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
  3. Click the **Connect Business Hub** button located at the top-right corner of the page. The **Connect your Business Hubs to Cerby** dialog box is displayed. **TIP:** You can select the **Don’t show this again** option to skip this step the next time you connect a new business hub.
  4. Click the **Get started** button. A wizard is displayed on the **Select app** page.
  5. Select the **LinkedIn Business Manager** app from the catalog. The **Enter app details** page is displayed on the wizard.
  6. Enter and select your app information in the corresponding fields:

     * **Label in Cerby:** It is the name you want to assign to your business hub in Cerby, and it will be displayed on the business hub card.
     * **Business ID:** It is the unique identifier of LinkedIn Business Manager. Read the [Requirements](connect-a-business-hub-for-linkedin-business-manager.md#requirements) section to learn how to get it.
     * **User management and login method:** It is the way your users log in to the app and determines if they must save their credentials in Cerby. You must select one of the following methods:
       * **Single sign-on (SSO):** Access is managed by your identity provider, and users log in with SSO authentication. They are not asked to save their credentials in Cerby.
       * **Username and password:** Ceby manages the account security and access, and users log in with their credentials after saving them in Cerby.

  7. Click the **Next** button. The **Select automation account** page is displayed. One of the following scenarios occurs:

     * If you already have an account for the app, a list of accounts is displayed.

       1. Select the corresponding automation account.
       2. Click the **Connect app** button.

     * If you don’t have an account for the app, you are prompted to add it:

       1. Enter your account details in the corresponding fields:
         1. **Account label in Cerby:** It is the name to assign to your account in Cerby, and it is displayed on the account card.
         2. **App:** It is the name of the app or service provider to which the account belongs or the login URL. In this case, LinkedIn **NOTE:** The app you selected in step 5 is displayed on this field, and you cannot change it.
         3. **Username:** It is the username you use to log in to your account. Sometimes, the username is your email address.
         4. **Current password:** It is the password you use to log in to your account.
         5. **Phone Number Linked to Account:** It is the phone number associated with your account
       2. Click the **Add account** button.

The wizard closes, and a success message box is displayed. The corresponding business hub is also displayed on the **Business Hubs** view.

The next step is [2. Check for updates to import users, roles, and assets to Cerby](connect-a-business-hub-for-linkedin-business-manager.md#id-2.-check-for-updates-to-import-users-roles-and-assets-to-cerby).

### 2\. Check for updates to import users, roles, and assets to Cerby

To check for updates in your app to identify and import users, roles, and assets to Cerby, you must complete the following steps:

  1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
  2. Click the **Settings** (<img src="../../../../../../.gitbook/assets/unnamed_27.png" alt="">) icon of the corresponding LinkedIn Business Manager business hub card. The business hub details page is displayed with the **Settings** tab activated.
  3. Click the **Check for updates** button located at the top right of the page. A message box is displayed with information about the process.

  **NOTE:** The check and import process may take a few minutes depending on the number of users and assets, and because Cerby automatically matches users to their corresponding Cerby account.

  4. Confirm that the **Check for updates** automated task has the “Completed” status by performing any of the following actions:

     * Click the **More details** button from the message box.
     * Select the **Automation** option from the left navigation drawer to open the **Automation** view.

{% hint style="info" %}


**NOTE:** Cerby automatically performs daily checks for updates for all business hubs, but you can trigger them manually, as described above in steps 1 to 3. When a user is deprovisioned from an identity provider and a check for updates is performed, Cerby generates a report and sends you an email to confirm their removal from the app. For more instructions, read the article [Check for updates in your app and apply report](https://help.cerby.com/en/articles/9046205-check-for-updates-in-your-app-and-apply-report).


{% endhint %}

The next step is [3. Connect your app’s user account to the business hub](connect-a-business-hub-for-linkedin-business-manager.md#id-3.-connect-your-apps-user-account-to-the-business-hub).

### 3\. Connect your app’s user account to the business hub

To connect your app’s user account to the business hub so Cerby can manage and protect it, you must complete the following steps:

  1. Select the **Accounts** option from the left navigation drawer. The **Accounts** view is displayed.
  2. Click the **Log in** button of the corresponding Make Tenant account card. The **Connect your Make Tenant Account** dialog box is displayed.
  3. Enter the login credentials of your Make user account.
  4. Click the **Connect account** button. The dialog box closes, and a success message box and a new account card for your user account are displayed.

The next step is [4. Manage unmatched users](connect-a-business-hub-for-linkedin-business-manager.md#id-4.-manage-unmatched-users), which you must complete from your Cerby dashboard.

### 4\. Manage unmatched users

After a check for updates, make sure you manage all unmatched users. By matching users, Cerby ensures that the app’s user accounts correspond to the users’ corporate identities; therefore, you can perform the following automated user management tasks on them:

  * Invite app members
  * Update app members’ roles
  * Remove app members

Additionally, if you have IdP groups configured, you can benefit from automatic user provisioning and deprovisioning based on IdP events, such as account deactivation or group assignments.

**IMPORTANT:** After a check for updates, Cerby automatically matches users to their Cerby user accounts according to their email addresses. Manual matching is required for apps that don't provide email addresses or for which users access through personal accounts.
---

To view the status of the imported app’s users, you must complete the following steps:

  1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
  2. Click the **More options** (<img src="../../../../../../.gitbook/assets/unnamed_28.png" alt="">) icon of the corresponding business hub card. A drop-down list is displayed.
  3. Select the **View Members** option from the list. The business hub details page is displayed with the **Members** tab activated.
The app members are displayed in the following tabs of the **User Overview** section:

     * **Unmatched users:** This tab displays the users who were not automatically matched because they use an email address that couldn’t be identified or they are not in the corporate directory.
     * **Onboarded users:** This tab displays the users matched to their Cerby user account.
     * **Guest users:** This tab displays the users who were matched to a user account but it doesn’t exist in the corporate directory, such as external collaborators.

For unmatched users, you can perform one of the following actions:

  * [Match users](connect-a-business-hub-for-linkedin-business-manager.md#match-users)
  * [Remove unmatched users](connect-a-business-hub-for-linkedin-business-manager.md#remove-unmatched-users)
  * [Exempt unmatched users](connect-a-business-hub-for-linkedin-business-manager.md#exempt-unmatched-users)

The following sections describe each action.

### Match users

To match users to their corresponding Cerby user accounts, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

  1. Click the **Match user** button of the corresponding user. The **Match user** dialog box is displayed.
  2. Enter the Cerby username or email address of the user you want to match and invite in the **Match with** field. The user is displayed on a list.
  3. Select the user from the list.
  4. Click the **Next** button. The **Select Cerby role** dialog box is displayed.
  5. Select the corresponding role of the user on the app from the **Cerby role** drop-down list:

  * **Owner:** This role enables sharing access and managing the app settings in Cerby.
  * **Collaborator:** This role enables only logging in to the app.

  1. Click the **Match user** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Onboarded** **users** tab.

### Remove unmatched users

To remove unmatched users from the app, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

  1. Click the **More options** () icon of the corresponding user. A drop-down list is displayed.
  2. Select the **Remove user** option from the list. The **Remove user?** dialog box is displayed.
  3. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from the app.

### Exempt unmatched users

Exempted users keep their user accounts active for the seat-based or paid social app, but you cannot manage them through Cerby.

To exempt unmatched users, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

  1. Click the **More options** () icon of the corresponding user. A drop-down list is displayed.
  2. Select the **Exempt user** option from the list. The exempt user dialog box is displayed.
  3. Enter a reason for exempting the user in the **Provide a reason** field.
  4. Click the **Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

* * *

## Use your business hub

The following are the supported features of Business hubs you can use:

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
