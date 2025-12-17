---
description: "This article describes how to connect a business hub to centrally manage the users of your seat-based and paid social apps from Cerby."
intercom_id: 9046120
---

# Connect a business hub for your app

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super** **Admins** , **Admins** , and **Users**
* Only supported using the Cerby web app


{% endhint %}

As a user with any workspace role in Cerby, except **Guest User** and **Login-Only** , you can connect a business hub integration to centrally manage the users and assets of your seat-based and paid social apps.

When you connect the business hub, you become its **Owner** , and you can perform the following user and access management tasks from Cerby:

* Check for updates
* Add users
* Update user roles
* Remove users

This article provides generic instructions on how to connect a business hub to Cerby. For app-specific articles and videos, visit the [Connecting business hubs for your apps](https://help.cerby.com/en/collections/10289415-connecting-business-hubs-for-your-apps) and [Connecting business hubs for your paid social apps](https://help.cerby.com/en/collections/12330234-connecting-business-hubs-for-your-paid-social-apps) collections in the Cerby Help Center.

* * *

## Requirements

The following are the requirements to connect a business hub:

  * A Cerby workspace
  * A Cerby user account with the workspace **Owner** , **Super** **Admin** , **Admin** , or **User** role
  * A collaboration space (workspace, team, or dashboard) in your app
  * A group assignment configured in your identity provider (IdP) if you want to leverage automatic user provisioning and deprovisioning for your apps based on IdP events. For more information, read the articles available in the [Managing users via an IdP and business hub](https://help.cerby.com/en/collections/12330182-managing-users-via-an-idp-and-business-hub) collection in the Cerby Help Center
  * An automation account, meaning an active user account with a native admin role in your seat-based or paid social app. For instructions and recommendations on how to create this account, read the article[ Create a service account for your business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/create-an-automation-or-service-account-for-your-business-hub)
  * The user management and login method for your business hub identified. For more information, read the **User management and login method** section of the article [Explore Business Hubs](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-business-hubs)
  * A business or organization ID. Commonly, you can find the ID in the following ways:
    * **From the address bar:** When you are logged in to your app, sometimes the ID is displayed in the address bar as part of the URL. For example, **`https://business.app.com/settings/&business_id=1234567890`**. Just copy the value and paste it when connecting the business hub.
    * **From the business information or settings:** When you are logged in to your app, navigate to the settings or business information page. The ID is usually displayed in an information section for you to copy.

​**NOTE:** Not all business hubs require a business or organization ID; Cerby displays an input field when applicable to your app. For more information, read the article [Retrieve the Business ID to connect your disconnected apps to Cerby](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/retrieve-the-business-id-to-connect-your-disconnected-apps-to-cerby).

* * *

## Connect a business hub for your app

To connect a business hub for your seat-based or paid social app, you must complete the following main steps from the Cerby web app dashboard:

  1. [Add a business hub and connect it to your external app](connect-a-business-hub-for-your-app.md#id-1.-add-a-business-hub-and-connect-it-to-your-external-app)
  2. [Check for updates to import users, roles, and assets to Cerby](connect-a-business-hub-for-your-app.md#id-2.-check-for-updates-to-import-users-roles-and-assets-to-cerby)
  3. [Connect your external app user account to the business hub (optional)](connect-a-business-hub-for-your-app.md#id-3.-connect-your-external-app-user-account-to-the-business-hub-(optional))
  4. [Manage unmatched users](connect-a-business-hub-for-your-app.md#id-4.-manage-unmatched-users)

The following sections describe each main step.

### 1\. Add a business hub and connect it to your external app

To add a business hub and connect it to your seat-based or paid social app, you must complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
  3. Click the **Connect Business Hub** button located at the top right of the page. The **Connect your Business Hubs to Cerby** dialog box is displayed.
​**TIP:** You can select the**Don’t show this again option** to skip this step the next time you connect a new business hub.

  4. Click the **Get started** button. A wizard is displayed on the **Select app** page.
  5. Select the corresponding app from the catalog. The **Enter app details** page is displayed on the wizard.
  6. Enter and select your app information in the corresponding fields:

     * **Label in Cerby:** It is the name to assign to your business hub in Cerby, and it will be displayed on the business hub card.
     * **Business ID:** It is the unique identifier of your business or organization within the seat-based or paid social app. This value may exist or not depending on the app and might have different names, such as **Organization ID** or **Team ID**. For generic instructions on how to find the ID, read the [Requirements](connect-a-business-hub-for-your-app.md#requirements) section.
     * **User management and login method** : It is the way your users log in to the app and determines if they must save their credentials in Cerby. You must select one of the following methods:
       * **Single sign-on (SSO)** : Access is managed by your identity provider, and users log in with SSO authentication.
       * **Username and password:** Account security and access are managed by Cerby, and users log in with their credentials.

       **NOTE:** Other input fields relevant to your app might be required.

  7. Click the **Next** button. The **Select automation account** page is displayed. One of the following scenarios occurs:

     * If you already have an account for the external app, a list of accounts is displayed.

       1. Select the corresponding automation account.
       2. Click the **Connect app** button.

     * If you don’t have an account for the external app, you are prompted to add it:

       1. Enter your account details in the corresponding fields:

          * **Account label in Cerby** : It is the name to assign to your account in Cerby, and it is displayed on the account card.
          * **App** : It is the name of the app or service provider to which the account belongs or the login URL.
​**NOTE:** The app you selected in step 5 is displayed on this field, and you cannot change it.

          * **Username** : It is the username you use to log in to your account. Sometimes, the username is your email address.
          * **Current password** : It is the password you use to log in to your account.
          * **Phone Number Linked to Accou** nt: It is the phone number associated with your account
          * Click the **Add account** button.

The wizard closes, and a success message box is displayed. The corresponding business hub is also displayed on the**Business Hubs** page.

The next step is [2. Check for updates to import users, roles, and assets to Cerby](connect-a-business-hub-for-your-app.md#id-2.-check-for-updates-to-import-users-roles-and-assets-to-cerby).

### 2\. Check for updates to import users, roles, and assets to Cerby

To check for updates in your app to identify and import users, roles, and assets to Cerby, you must complete the following steps:

  1. Select the**Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
  2. Click the More options (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1478157284/42584d350993c178cf8025b7786d/AD_4nXf0Jp5QaBPwRG29PMQLNHBp3Ey60jrtlq4maS2tSNAkdfjCjLZHfTpbQ1T5Uh3iCDHzbQmW4a1nJ1aDuRUvUS7FL5TZpYrBZjJ7gWENuWjGw1_TFHw2Cecb5mmSD4T1I5SEztXX?expires=1765476000&signature=25a949074cbb17205f3ac6427505e5ff95a64633ae98ee99db49696c2c7e2a5a&req=dSQgHsh7moNXXfMW3Hu4gSTTh1dr1GGkEKAu8vFBULU9%2FNUFBUu5R%2FWCg12w%0AEg%3D%3D%0A" alt="">) icon of the corresponding business hub card. A drop-down menu is displayed.
  3. Select the **Settings** option from the menu. The business hub details page is displayed with the **Settings** tab activated.
  4. Click the**Sync** button located at the top right of the page. A message box is displayed with information about the process.
​**NOTE:** The check and import process may take a few minutes depending on the number of users and assets.

  5. Confirm that the check for updates automated task has the “Completed” status by performing any of the following actions:
     1. Click the **More details** button from the message box.
     2. Select the **Automation** option from the left menu to open the **Automation** page.

{% hint style="info" %}


**NOTE:** Cerby runs syncs regularly for all business hubs, but you can trigger them manually, as described above in steps 1 to 4. For more information, read the article [Sync your app users with your business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/sync-your-business-hub-with-your-external-app).


{% endhint %}

The next step is [3\. Connect your external app user account to the business hub (optional)](https://docs.google.com/document/d/13bEDsJOdtkkCru_Wred7pgQRZTlLOM1Xj0g5Tj6K2EY/edit?pli=1#heading=h.ruciuhfek6rd).

### 3\. **Connect your external app user account to the business hub (optional)**

As an integration **Owner** , you can access the external app using the service account associated with the business hub. However, to avoid potential conflicts and ensure smooth access, Cerby recommends connecting your external app user account to the business hub, especially if you actively work in the external app.

To connect your external app user account to the business hub so Cerby can manage and protect it, you must complete the following steps:

  1. Select the **Accounts** option from the left menu. The **Accounts** page is displayed.
  2. Click the **Log in** button of the corresponding business hub card. The **Connect your <app name> Hub Account **dialog box is displayed.
  3. Enter the login credentials of your external app user account.
​**NOTE:** If you have already added user accounts to Cerby, the dialog box displays these accounts on a list, and you must select one of them to connect it to the app.

  4. Click the**Connect account** button. The dialog box closes, and a success message box and a new account card for your user account are displayed.

The next step is [4. Manage unmatched users](connect-a-business-hub-for-your-app.md#id-4.-manage-unmatched-users), which you must complete from your Cerby dashboard.

### 4\. Manage unmatched users

After a check for updates, Cerby matches app members to their Cerby user accounts, including existing guest users and local partners. Manual matching is required for users who cannot be matched automatically.

To view the status of the imported external app users, you must complete the following steps:

  1. Select the **Business Hubs** option from the left menu. The**Business Hubs** page is displayed.
  2. Click the **More options** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1478162142/3035664d71b10eae44d2eff82776/AD_4nXd_dCQ1rKiSZSsEz9e8vWL2tr-x_dVg9-I-iIZHkgYbe6vK_hCpei6OP13w0kI1ZiKxqNn7Z9CNB5XIlVKwzRzK7VXxSfD90MmpVfwnpVOO4BYLbAc_1A83QopO1SLHIjhfX0oZOA?expires=1765476000&signature=7cb79f1310de12007ac1a23dcf80d2d33d3d31574aca92474b7d99f4904883a4&req=dSQgHsh4n4BbW%2FMW3Hu4gYUugLNJI2PKbbnePKXrbb73IMrYdIEiN2Xd%2FkLZ%0AGQ%3D%3D%0A" alt="">) icon of the corresponding business hub card. A drop-down menu is displayed.
  3. Select the **View Members** option from the menu. The business hub details page is displayed with the **Members** tab activated.
The app users are displayed in the following tabs of the **User Overview** section:

     * **Unmatched users:** This tab displays the users who were not automatically matched.
     * **Onboarded users:** This tab displays the users matched to their Cerby user account.
     * **Guest users:** This tab displays the users who were matched to a user account that doesn’t exist in the corporate directory, such as external collaborators.

For unmatched users, you can perform one of the following actions:

  * [Match users](connect-a-business-hub-for-your-app.md#match-users)
  * [Remove unmatched users](connect-a-business-hub-for-your-app.md#remove-unmatched-users)
  * [Exempt unmatched users](connect-a-business-hub-for-your-app.md#exempt-unmatched-users)

The following sections describe each action.

#### Match users

To match users to their corresponding Cerby user account, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

  1. Click the **Match user** button of the corresponding user. The **Match user** dialog box is displayed.
  2. Enter the Cerby username or email address of the user you want to match and invite in the **Match with** field. The user is displayed on a list.
  3. Select the user from the list.
  4. Click the **Next** button. The **Select Cerby role** dialog box is displayed.
  5. Select the corresponding role of the user on the business hub integration from the Cerby role drop-down menu:

     * **Owner** : This role enables sharing access and managing the business hub integration settings in Cerby.
     * **Collaborator** : This role enables only logging in to the app through Cerby.

  6. Click the **Match user** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Onboarded users** tab.

#### Remove unmatched users

To remove unmatched users from the seat-based or paid social app, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

**IMPORTANT:** When removing an unmatched user, Cerby revokes the user’s seat and permissions in the external app.
---

  1. Click the **More options** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1478166080/13fd1653b00844e33fb8e6f769df/AD_4nXd_dCQ1rKiSZSsEz9e8vWL2tr-x_dVg9-I-iIZHkgYbe6vK_hCpei6OP13w0kI1ZiKxqNn7Z9CNB5XIlVKwzRzK7VXxSfD90MmpVfwnpVOO4BYLbAc_1A83QopO1SLHIjhfX0oZOA?expires=1765476000&signature=e5c344269b6dc1eede0d637c809a584c0a2083cde6dd455e83a0b9c72953b8f1&req=dSQgHsh4m4FXWfMW3Hu4gSjOiuInUUgplX5sZiKzVwdqKSN7maZELRXuxzMW%0ACA%3D%3D%0A" alt="">) icon of the corresponding user. A drop-down menu is displayed.
  2. Select the**Remove user** option from the menu. The **Remove user?** dialog box is displayed.
  3. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from the external app.

#### Exempt unmatched users

Exempted users keep their user accounts active for the seat-based or paid social app, but you cannot manage them through Cerby.

To exempt unmatched users, you must complete the following steps from the **Unmatched users** tab of the business hub details page

  1. Click the **More options** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1478166644/0675a9a3bb29da17e9c9c8d8a4bf/AD_4nXd_dCQ1rKiSZSsEz9e8vWL2tr-x_dVg9-I-iIZHkgYbe6vK_hCpei6OP13w0kI1ZiKxqNn7Z9CNB5XIlVKwzRzK7VXxSfD90MmpVfwnpVOO4BYLbAc_1A83QopO1SLHIjhfX0oZOA?expires=1765476000&signature=cfe7dc974fd90a906c3a85d1dd1ac0e30041f8b0a37a7cbbf8c5bc4b54e1ec9e&req=dSQgHsh4m4dbXfMW3Hu4gdioEv8%2FmQNPTqg0sTnBkfYp9pLkmwfS%2Fs7Ty1vn%0ANA%3D%3D%0A" alt="">) icon of the corresponding user. A drop-down menu is displayed.
  2. Select the **Exempt user** option from the menu. The **Exempt user** dialog box is displayed.
  3. Enter a reason for exempting the user in the**Provide a reason** field.
  4. Click the**Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

* * *

### Use your business hub

The following are the supported features of business hubs you can use:

  * [Join your external app and set up your business hub access](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/join-your-external-app-and-set-up-your-business-hub-access)
  * [Add users to your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/add-users-and-teams-to-your-apps-via-a-business-hub)
  * [Provision users to your apps via an IdP and business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/provision-users-to-your-apps-via-an-idp-and-business-hub)
  * [Remove users from your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/remove-users-from-your-app-via-a-business-hub)
  * [Remove teams from your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/remove-teams-from-your-app-via-a-business-hub)
  * [Deprovision users from your apps via an IdP and business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/deprovision-users-from-your-apps-via-an-idp-and-business-hub)
  * [Update user roles in your apps via an IdP and business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/update-user-roles-in-your-apps-via-an-idp-and-business-hub)
  * [Update user roles in your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/update-user-roles-in-your-app-via-a-business-hub)
  * [Sync your app users with your business hub ](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/sync-your-business-hub-with-your-external-app)
  * [Protect your app users via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/protect-your-app-user-accounts-via-a-business-hub)
  * [Log in to your app via a business hub](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/log-in-to-your-app)
  * [Track the activity of business hub users](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/track-activity-on-app-members-user-accounts)
  * [Remove a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/remove-a-business-hub)
  * [Troubleshooting Business Hubs](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/troubleshooting/troubleshooting-business-hubs)
