---
intercom_id: 9953372
description: >-
  This article describes how to connect a business hub to centrally manage the
  users of Backslash from Cerby.
---

# Connect a business hub for Backslash

{% hint style="info" %}
**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* Only supported using the Cerby web app
{% endhint %}

As a user with any workspace role in Cerby, except **Guest User** and **Login-Only** , you can connect a business hub integration to centrally manage the users and assets of Backslash.

When you connect the business hub, you become its **Owner** , and you can perform the following user and access management tasks from Cerby through automation:

* Check for updates
* Invite app members
* Update app member’s roles
* Remove app members

{% hint style="success" %}
**TIP:** For more details about the automated tasks of a business hub, how it works, and the supported apps, read the article [Explore Apps](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-business-hubs).
{% endhint %}

This article provides instructions on how to connect a business hub for Backslash. For other app-specific articles and videos, review the [Connecting your apps](https://help.cerby.com/en/collections/10289415-connecting-your-apps) collection in the Cerby Help Center.

***

## Requirements

The following are the requirements to connect a business hub:

* A Cerby workspace
* A Cerby user account with the **Owner** , **Super Admin** , **Admin** , or **User** role
* A tenant in Backslash
* A group assignment configured in your identity provider (IdP) if you want to leverage automatic user provisioning and deprovisioning from your apps based on IdP events. For more information, read the **App user provisioning and deprovisioning** section of the article [Explore Business hubs](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-business-hubs)
* An automation account, meaning an active user account with a native admin role in your seat-based or paid social app. For instructions and recommendations on how to create and configure this account, read the article [Create an automation or service account for your business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/create-an-automation-or-service-account-for-your-business-hub)
* The user management and login method for your business hub identified to select the corresponding option when connecting your app. For more information, read the **User management and login method** section of the article [Explore Business hubs](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-business-hubs)

***

## Connect a business hub for Backslash

To connect a business hub to Backslash, you must complete the following main steps from the Cerby web app dashboard:

1. Add a business hub and connect it to Backslash
2. Check for updates to import users, roles, and assets to Cerby
3. Connect your app’s user account to the business hub
4. Manage unmatched users

The following sections describe each main step.

### 1. Add a business hub and connect it to Backslash

To add a business hub and connect it to Backslash, you must complete the following steps:

1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
2. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
3. Click the **Connect Business Hub** button located at the top-right corner of the page. The **Connect your Business Hubs to Cerby** dialog box is displayed. **TIP:** You can select the **Don’t show this again** option to skip this step the next time you connect a new business hub.
4. Click the **Get started** button. A wizard is displayed on the **Select app** page.
5. Select the **Backslash Tenant** app from the catalog. The **Enter app details** page is displayed on the wizard.
6. Enter and select your app information in the corresponding fields:
   * **Label in Cerby:** It is the name to assign to your business hub in Cerby, and it will be displayed on the business hub card.
   * **User management and login method:** It is the way your users log in to the app and determines if they must save their credentials in Cerby. You must select one of the following methods:
     * **Single sign-on (SSO):** Access is managed by your identity provider, and users log in with SSO authentication. They are not asked to save their credentials in Cerby.
     * **Username and password:** Account security and access are managed by Ceby, and users log in with their credentials after saving them in Cerby.
7. Click the **Next** button. The **Select automation account** page is displayed. One of the following scenarios occurs:
   * If you already have an account for the app, a list of accounts is displayed.
     1. Select the corresponding automation account.
     2. Click the **Connect app** button.
   * If you don’t have an account for the app, you are prompted to add it: The wizard closes, and a success message box is displayed. The corresponding business hub is also displayed on the **Business Hubs** view.
     1. Enter your account details in the corresponding fields:
        * **Account label in Cerby:** It is the name to assign to your account in Cerby, and it is displayed on the account card.
        * **App:** It is the name of the app or service provider to which the account belongs or the login URL.\
          **NOTE:** The app you selected in step 5 is displayed on this field, and you cannot change it.
        * **Username:** It is the username you use to log in to your account. Sometimes, the username is your email address.
        * **Current password:** It is the password you use to log in to your account.
     2. Click the **Add account** button.

The next step is 2. Check for updates to import users, roles, and assets to Cerby.

### 2. Check for updates to import users, roles, and assets to Cerby

To check for updates in your app to identify and import users, roles, and assets to Cerby, you must complete the following steps:

1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
2. Click the **Settings** () icon of the corresponding business hub card. The business hub details page is displayed with the **Settings** tab activated.
3. Click the **Check for updates** button located at the top right of the page. A message box is displayed with information about the process. **NOTE:** The check and import process may take a few minutes depending on the number of users and assets, and because Cerby automatically matches users to their corresponding Cerby account.
4. Confirm that the **Check for updates** automated task has the “Completed” status by performing any of the following actions:
   * Click the **More details** button from the message box.
   * Select the **Automation** option from the left navigation drawer to open the **Automation** view.

{% hint style="info" %}
**NOTE:** Cerby automatically performs daily checks for updates for all business hubs, but you can trigger them manually, as described above in steps 1 to 3. When a user is deprovisioned from an identity provider and a check for updates is performed, Cerby generates a report and sends you an email to confirm their removal from the app. For more instructions, read the article [Check for updates in your app and apply report](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/sync-your-business-hub-with-your-external-app).
{% endhint %}

The next step is 3. Connect your app’s user account to the business hub.

### 3. Connect your app’s user account to the business hub

To connect your app’s user account to the business hub so Cerby can manage and protect it, you must complete the following steps:

1. Select the **Accounts** option from the left navigation drawer. The **Accounts** view is displayed.
2. Click the **Log in** button of the corresponding **Backslash Tenant** account card. The **Connect your Backslash Tenant Account** dialog box is displayed.
3. Enter the login credentials of your Backslash user account.
4. Click the **Connect account** button. The dialog box closes, and a success message box and a new account card for your user account are displayed.

The next step is 4. Manage unmatched users, which you must complete from your Cerby dashboard.

### 4. Manage unmatched users

After a check for updates, make sure you manage all unmatched users. By matching users, Cerby ensures that the app’s user accounts correspond to the users’ corporate identities; therefore, you can perform the following automated user management tasks on them:

* Invite app members
* Update app members’ roles
* Remove app members

Additionally, if you have IdP groups configured, you can benefit from automatic user provisioning and deprovisioning based on IdP events, such as account deactivation or group assignments.

{% hint style="info" %}
**NOTE:** After a check for updates, Cerby automatically matches users to their Cerby user accounts according to their email addresses. Manual matching is required for apps that don't provide email addresses or for which users access through personal accounts.
{% endhint %}

To view the status of the imported app’s users, you must complete the following steps:

1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
2.  Click the **More options** (

    <figure><img src="../../../../.gitbook/assets/AD_4nXf0FP_RKAf9OorxP0uXz5WGjOTnXvYacp0DJo59PwEDGIIRjrw2H7qgZXHR9AXLFzvcsvA0IhTt7Ze09Lfy_Aa7YYHJmnwEm3jOHua3vkL7XBXL41Rj5PpGZV5_p1sbw2hDk64P4K5IH6R3WMgo2r0UPko.png" alt=""><figcaption></figcaption></figure>

    ) icon of the corresponding business hub card. A drop-down list is displayed.
3. Select the **View Members** option from the list. The business hub details page is displayed with the **Members** tab activated. The app members are displayed in the following tabs of the **User Overview** section:
   * **Unmatched users:** This tab displays the users who were not automatically matched because they use an email address that couldn’t be identified or they are not in the corporate directory.
   * **Onboarded users:** This tab displays the users matched to their Cerby user account.\
     **NOTE:** After a check for updates, Cerby automatically matches users to their Cerby user accounts according to their email addresses. Manual matching is required for apps that don't provide email addresses or for which users access through personal accounts.
   * **Guest users:** This tab displays the users who were matched to a user account but it doesn’t exist in the corporate directory, such as external collaborators.

For unmatched users, you can perform one of the following actions:

* Match users
* Remove unmatched users
* Exempt unmatched users

The following sections describe each action.

### Match users

To match users to their corresponding Cerby user account, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

1. Click the **Match user** button of the corresponding user. The **Match user** dialog box is displayed.
2. Enter the Cerby username or email address of the user you want to match and invite in the **Match with** field. The user is displayed on a list.
3. Select the user from the list.
4. Click the **Next** button. The **Select Cerby role** dialog box is displayed.
5. Select the corresponding role of the user on the app from the **Cerby role** drop-down list:
   * **Owner:** This role enables sharing access and managing the app settings in Cerby.
   * **Collaborator:** This role enables only logging in to the app.
6. Click the **Match user** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Onboarded** **users** tab.

### Remove unmatched users

To remove unmatched users from the app, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

1.  Click the **More options** (

    <figure><img src="../../../../.gitbook/assets/AD_4nXf0FP_RKAf9OorxP0uXz5WGjOTnXvYacp0DJo59PwEDGIIRjrw2H7qgZXHR9AXLFzvcsvA0IhTt7Ze09Lfy_Aa7YYHJmnwEm3jOHua3vkL7XBXL41Rj5PpGZV5_p1sbw2hDk64P4K5IH6R3WMgo2r0UPko_1.png" alt=""><figcaption></figcaption></figure>

    ) icon of the corresponding user. A drop-down list is displayed.
2. Select the **Remove user** option from the list. The **Remove user?** dialog box is displayed.
3. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from the app.

### Exempt unmatched users

Exempted users keep their user accounts active for the seat-based or paid social app, but you cannot manage them through Cerby.

To exempt unmatched users, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

1.  Click the **More options** (

    <figure><img src="../../../../.gitbook/assets/AD_4nXf0FP_RKAf9OorxP0uXz5WGjOTnXvYacp0DJo59PwEDGIIRjrw2H7qgZXHR9AXLFzvcsvA0IhTt7Ze09Lfy_Aa7YYHJmnwEm3jOHua3vkL7XBXL41Rj5PpGZV5_p1sbw2hDk64P4K5IH6R3WMgo2r0UPko_2.png" alt=""><figcaption></figcaption></figure>

    ) icon of the corresponding user. A drop-down list is displayed.
2. Select the **Exempt user** option from the list. The exempt user dialog box is displayed.
3. Enter a reason for exempting the user in the **Provide a reason** field.
4. Click the **Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

***

## Use your business hub

The following are the supported features of Business hubs you can use:

* [Join the App and connect it to Cerby](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/join-your-external-app-and-set-up-your-business-hub-access)
* [Invite new app members](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/add-users-and-teams-to-your-apps-via-a-business-hub)
* [Remove app members](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/remove-users-from-your-app-via-a-business-hub)
* [Manage app members from your IdP](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/unpublished-manage-app-members-from-your-idp-deprecated)
* [Update the app members’ roles](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/update-user-roles-in-your-app-via-a-business-hub)
* [Check for updates in your app and apply report](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/sync-your-business-hub-with-your-external-app)
* [Re-assign the app members’ user accounts](https://help.cerby.com/en/articles/9046211-re-assign-the-app-members-user-accounts)
* [Manage the security of app members’ user accounts](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/protect-your-app-user-accounts-via-a-business-hub)
* [Log in to your app](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/log-in-to-your-app)
* [Track activity on app members’ user accounts](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/track-activity-on-app-members-user-accounts)
* [Remove an App](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/remove-a-business-hub)
