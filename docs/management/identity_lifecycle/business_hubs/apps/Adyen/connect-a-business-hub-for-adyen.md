---
intercom_id: 12133105
description: >-
  This article describes how to connect a business hub to centrally manage the
  users of Adyen from Cerby.
---

# Connect a business hub for Adyen

{% hint style="info" %}
**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* Only supported using the Cerby web app
{% endhint %}

As a user with any workspace role in Cerby, except **Guest User** and **Login-Only** , you can connect a business hub integration to centrally manage the users of Adyen.

When you connect the business hub, you become its **Owner** , and you can perform the following user and access management tasks through automated tasks and API calls executed by the Cerby agent:

* Check for updates
* Add users
* Update user roles
* Remove users

{% hint style="success" %}
**TIP:** For more details about the automated tasks of a business hub, how it works, and the supported apps, read the article [Explore Business Hubs](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-business-hubs).
{% endhint %}

This article provides instructions on how to connect a business hub for Adyen. For other app-specific articles and videos, review the [Connecting business hubs for your apps](https://help.cerby.com/en/collections/10289415-connecting-your-apps) and [Connecting business hubs for your paid social apps](https://help.cerby.com/en/collections/12330234-connecting-business-hubs-for-your-paid-social-apps) collections in the Cerby Help Center.

***

## Requirements

The following are the requirements to connect a business hub:

* A Cerby workspace
* A Cerby user account with the workspace **Owner** , **Super Admin** , **Admin** , or **User** role
* Groups configured in your identity provider (IdP) if you want to leverage automatic user provisioning and deprovisioning from your apps based on group assignment events. For more information, read the articles available in the [Managing users via an IdP and business hub](https://help.cerby.com/en/collections/12330182-managing-users-via-an-idp-and-business-hub) collection in the Cerby Help Center
* An automation account, meaning an active user account with a native **Merchant admin** role in Adyen to be used as a service account. For instructions and recommendations on how to create and configure this account, read the article [Create a service account for your business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/create-an-automation-or-service-account-for-your-business-hub)
* The user management and login method for your business hub identified to select the corresponding option when connecting your app. For more information, read the **User management and login method** section of the article [Explore Business Hubs](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-business-hubs)

***

## Connect a business hub for Adyen

To connect a business hub for Adyen, you must complete the following main steps from the Cerby web app dashboard:

1. [Add a business hub and connect it to Adyen](connect-a-business-hub-for-adyen.md#id-1.-add-a-business-hub-and-connect-it-to-adyen)
2. [Check for updates to import users and roles to Cerby](connect-a-business-hub-for-adyen.md#id-2.-check-for-updates-to-import-users-and-roles-to-cerby)
3. [Connect your Adyen user account to the business hub](connect-a-business-hub-for-adyen.md#id-3.-connect-your-adyen-user-account-to-the-business-hub)
4. [Manage unmatched users](connect-a-business-hub-for-adyen.md#id-4.-manage-unmatched-users)

The following sections describe each main step.

### 1. Add a business hub and connect it to Adyen

To add a business hub and connect it to Adyen, you must complete the following steps:

1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
2. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
3. Click the **Connect Business Hub** button located at the top-right corner of the page. The **Connect your Business Hubs to Cerby** dialog box is displayed. ​**TIP:** Select the **Don’t show this again** option to skip this step the next time you connect a new business hub.
4. Click the **Get started** button. A wizard is displayed on the **Select app** page.
5. Select **Adyen Business Hub** from the catalog. The **Enter app details** page is displayed on the wizard.
6. Enter and select your app information in the corresponding fields:
   * **Label in Cerby:** It is the name to assign to your business hub in Cerby, and it will be displayed on the business hub card.
   * **Business Unique Identifier:** It is a unique identifier that differentiates your business hub in Cerby from others for the same app. You must select one of the following options:
     * **Sandbox:** An Adyen sandbox environment, used for development and testing with simulated transactions.
     * **Production:** An Adyen production environment, used for live payments with real transactions.
   * **User management and login method:** It is the way your users log in to the app and determines whether they must save their login credentials as a Cerby account connected to the business hub. You must select one of the following methods:
     * **Single sign-on (SSO):** Access is managed by your IdP, and users log in with SSO authentication. They are not asked to save their credentials in Cerby.
     * **Username and password:** Cerby manages account security and access, and users log in with their credentials after saving them in Cerby.
7. Click the **Next** button. The **Select automation account** page is displayed with a list of existing Adyen accounts.
8. Select the automation account you have previously added to Cerby, as described in the [Requirements](connect-a-business-hub-for-adyen.md#requirements) section. ​**NOTE:** If you don’t have an automation account, you are prompted to add it. Make sure you read Cerby’s recommendations on how to configure it in the article [Create a service account for your business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/create-an-automation-or-service-account-for-your-business-hub). You may need to add the account first and then add the business hub.
9. Click the **Connect app** button. The wizard closes, and a success message box is displayed. The corresponding business hub is also displayed on the **Business Hubs** page.

The next step is [2. Check for updates to import users and roles to Cerby](connect-a-business-hub-for-adyen.md#id-2.-check-for-updates-to-import-users-and-roles-to-cerby).

### 2. Check for updates to import users and roles to Cerby

To check for updates in your app to identify and import users and roles to Cerby, you must complete the following steps:

1. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
2. Click the **More options** (![](../../../../.gitbook/assets/AD_4nXewApJOBZXewpFew1XrkjC6rCssB5Upy2WRCW8fpJjw2Zmj0xzSkEgw3tUBvW6lyQC2RihdmxzJ6KKXG1pvMGfAeaQnjZUGnThkBo5vdisjtu8WvqHXLgT1_7-xOwkkFy5umyicPg_215.png)) icon of the corresponding business hub card. A drop-down menu is displayed.
3. Select the **Settings** option from the menu. The business hub details page is displayed with the **Settings** tab activated.
4. Click the **Check for updates** button located at the top right of the page. A message box is displayed with information about the process. ​**NOTE:** The check and import process may take a few minutes depending on the number of users, and because Cerby automatically matches users to their corresponding Cerby user account.
5. Confirm that the automated task to check for updates has the “Completed” status by performing any of the following actions:
   * Click the **More details** button from the message box.
   * Select the **Automation** option from the left menu to open the **Automation** page with a list of automated tasks and their status.

{% hint style="info" %}
**NOTE:** Cerby automatically performs daily checks for updates for all business hubs, but you can trigger them manually, as described in this section. For more instructions, read the article [Sync your app users with your business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/sync-your-business-hub-with-your-external-app).
{% endhint %}

The next step is [3. Connect your Adyen user account to the business hub](connect-a-business-hub-for-adyen.md#id-3.-connect-your-adyen-user-account-to-the-business-hub).

### 3. Connect your Adyen user account to the business hub

To connect your Adyen user account to the business hub so Cerby can manage and protect it, you must complete the following steps:

1. Select the **Accounts** option from the left menu. The **Accounts** page is displayed.
2. Click the **Log in** button of the corresponding Adyen Business Hub account card. The **Connect your Adyen Business Hub Account** dialog box is displayed.
3. Enter the login credentials of your **Adyen** user account.
4. Click the **Connect account** button. The dialog box closes, and a success message box and a new account card are displayed.

The next step is [4. Manage unmatched users](connect-a-business-hub-for-adyen.md#id-4.-manage-unmatched-users).

### 4. Manage unmatched users

During a check for updates, Cerby automatically matches app members to the Cerby user accounts that correspond to their email addresses, including existing [guest users](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-guest-users) and [local partners](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-partners). Manual matching is required when apps don't provide email addresses and for app members using personal or external accounts that couldn’t be identified or are not in the corporate directory.

To view the status of the imported app members, you must complete the following steps:

1. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
2. Click the **More options** (![](../../../../.gitbook/assets/AD_4nXewApJOBZXewpFew1XrkjC6rCssB5Upy2WRCW8fpJjw2Zmj0xzSkEgw3tUBvW6lyQC2RihdmxzJ6KKXG1pvMGfAeaQnjZUGnThkBo5vdisjtu8WvqHXLgT1_7-xOwkkFy5umyicPg_216.png)) icon of the corresponding business hub card. A drop-down menu is displayed.
3. Select the **View Members** option from the menu. The business hub details page is displayed with the **Members** tab activated. App members are displayed in the following tabs of the **User Overview** section:
   * **Unmatched users:** This tab displays the users who were not automatically matched.
   * **Onboarded users:** This tab displays the users matched to their Cerby user account.
   * **Guest users:** This tab displays the users who were matched to an existing Cerby user account but it doesn’t exist in the corporate directory, such as external collaborators.

For unmatched users, you can perform one of the following actions:

* [Match users](connect-a-business-hub-for-adyen.md#match-users)
* [Remove unmatched users](connect-a-business-hub-for-adyen.md#remove-unmatched-users)
* [Exempt unmatched users](connect-a-business-hub-for-adyen.md#exempt-unmatched-users)

The following sections describe each action.

#### Match users

To match users, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

1. Click the **Match user** button of the corresponding user. The **Match user** dialog box is displayed.
2. Enter the username or email address of the user you want to match and invite in the **Match with** field. The user is displayed on a list.
3. Select the user from the list.
4. Click the **Next** button. The **Select Cerby role** dialog box is displayed.
5. Select the role to assign to the user on the business hub **Cerby role** drop-down menu:
   * **Owner:** This role enables sharing access and managing business hub settings in Cerby.
   * **Collaborator:** This role enables only logging in to the app from Cerby.
6. Click the **Match user** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Onboarded users** tab.

#### Remove unmatched users

To remove unmatched users, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

{% hint style="danger" %}
**IMPORTANT:** When removing an unmatched user, Cerby performs an automated task to revoke the user’s seat and permissions in Adyen.
{% endhint %}

1. Click the **More options** (![](../../../../.gitbook/assets/AD_4nXewApJOBZXewpFew1XrkjC6rCssB5Upy2WRCW8fpJjw2Zmj0xzSkEgw3tUBvW6lyQC2RihdmxzJ6KKXG1pvMGfAeaQnjZUGnThkBo5vdisjtu8WvqHXLgT1_7-xOwkkFy5umyicPg_217.png)) icon of the corresponding user. A drop-down menu is displayed.
2. Select the **Remove user** option from the menu. The **Remove user?** dialog box is displayed.
3. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from the app via an automated task.

#### Exempt unmatched users

Exempted users keep their user accounts or seats active in your app, but you cannot manage them through Cerby.

To exempt unmatched users, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

1. Click the **More options** (![](../../../../.gitbook/assets/AD_4nXewApJOBZXewpFew1XrkjC6rCssB5Upy2WRCW8fpJjw2Zmj0xzSkEgw3tUBvW6lyQC2RihdmxzJ6KKXG1pvMGfAeaQnjZUGnThkBo5vdisjtu8WvqHXLgT1_7-xOwkkFy5umyicPg_218.png)) icon of the corresponding user. A drop-down menu is displayed.
2. Select the **Exempt user** option from the menu. The exempt user dialog box is displayed.
3. Enter a reason for exempting the user in the **Provide a reason** field.
4. Click the **Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

## Use your business hub

The following are the supported features of business hubs you can use:

* [Join the external app and set up your business hub access](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/join-your-external-app-and-set-up-your-business-hub-access)
* [Add users to your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/add-users-and-teams-to-your-apps-via-a-business-hub)
* [Provision users to your apps via an IdP and business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/provision-users-to-your-apps-via-an-idp-and-business-hub)
* [Remove users from your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/remove-users-from-your-app-via-a-business-hub)
* [Remove teams from your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/remove-teams-from-your-app-via-a-business-hub)
* [Deprovision users from your apps via an IdP and business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/deprovision-users-from-your-apps-via-an-idp-and-business-hub)
* [Update user roles in your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/update-user-roles-in-your-app-via-a-business-hub)
* [Update user roles in your apps via an IdP and business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/update-user-roles-in-your-apps-via-an-idp-and-business-hub)
* [Sync your app users with your business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/sync-your-business-hub-with-your-external-app)
* [Protect your app users via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/protect-your-app-user-accounts-via-a-business-hub)
* [Log in to your app via a business hub](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/log-in-to-your-app)
* [Track the activity of business hub users](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/track-activity-on-app-members-user-accounts)
* [Remove a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/remove-a-business-hub)
