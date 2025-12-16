---
intercom_id: 11366395
description: >-
  This article describes how to connect a business hub to centrally manage the
  users and assets of Rollbar from Cerby.
---

# Connect a business hub for Rollbar

{% hint style="info" %}
**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* Only supported using the Cerby web app
{% endhint %}

As a user with any workspace role in Cerby, except **Guest User** and **Login-Only** , you can connect a business hub integration to centrally manage the users and assets of Rollbar.

When you connect the business hub, you become its **Owner** , and you can perform the following user and access management tasks through automated tasks executed by the Cerby agent:

* Check for updates
* Add users
* Remove users

{% hint style="success" %}
**TIP:** For more details about the automated tasks of a business hub, how it works, and the supported apps, read the article [Explore Business Hubs](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-business-hubs).
{% endhint %}

{% hint style="info" %}
**NOTE:** The automated task to update user roles is not available for this business hub because Rollbar doesn’t support roles.
{% endhint %}

This article provides instructions on how to connect a business hub for Rollbar. For other app-specific articles and videos, review the [Connecting business hubs for your apps](https://help.cerby.com/en/collections/10289415-connecting-your-apps) and [Connecting business hubs for your paid social apps](https://help.cerby.com/en/collections/12330234-connecting-business-hubs-for-your-paid-social-apps) collections in the Cerby Help Center.

***

## Requirements

The following are the requirements to connect a business hub:

* A Cerby workspace
* A Cerby user account with the workspace **Owner** , **Super Admin** , **Admin** , or **User** role
* Groups configured in your identity provider (IdP) if you want to leverage automatic user provisioning and deprovisioning from your apps based on group assignment events. For more information, read the articles available in the [Managing users via an IdP and business hub](https://help.cerby.com/en/collections/12330182-managing-users-via-an-idp-and-business-hub) collection in the Cerby Help Center
* An automation account, meaning an active user account in Rollbar to be used as a service account. For instructions and recommendations on how to create and configure this account, read the article [Create a service account for your business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/create-an-automation-or-service-account-for-your-business-hub)
* A Business ID. You can find the ID in the following ways:
  * **In the address bar:** When you are logged into your Rollbar account, the ID is displayed in the address bar as part of the URL, after the domain. For example, **`mycompany`** in **`https://rollbar.com/mycompany`**. Just copy the value and paste it when connecting the business hub.
  * **In the business information or settings:** When you are logged in to Rollbar, select the **Settings** option from the left menu, and the **General** page is displayed. The ID is displayed under the **Account Details** section in the **Account Name** field for you to copy.

***

## Connect a business hub for Rollbar

To connect a business hub for Rollbar, you must complete the following main steps from the Cerby web app dashboard:

1. Add a business hub and connect it to Rollbar
2. Check for updates to import users and assets to Cerby
3. Connect your Rollbar user account to the business hub
4. Manage unmatched users

The following sections describe each main step.

### 1. Add a business hub and connect it to Rollbar

To add a business hub and connect it to Rollbar, you must complete the following steps:

1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
2. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
3. Click the **Connect Business Hub** button located at the top-right corner of the page. The **Connect your Business Hubs to Cerby** dialog box is displayed. ​**TIP:** Select the **Don’t show this again** option to skip this step the next time you connect a new business hub.
4. Click the **Get started** button. A wizard is displayed on the **Select app** page.
5. Select **Business unique identifier** from the catalog. The **Enter app details** page is displayed on the wizard.
6. Enter and select your app information in the corresponding fields:
   * **Label in Cerby:** It is the name to assign to your business hub in Cerby, and it will be displayed on the business hub card.
   * **Business ID:** It is the unique identifier of your business or organization in **Business unique identifier**. For instructions on how to find it, read the Requirements section.
   * **User management and login method:** It is the way your users log in to the app and determines whether they must save their login credentials as a Cerby account connected to the business hub.
     1. Select the **Username and password** option because account security and access are managed by Cerby, and users log in with their credentials after saving them in Cerby. **IMPORTANT:** The **Single sign-on (SSO)** option is not currently available for Rollbar.
7. Click the **Next** button. The **Select automation account** page is displayed with a list of existing Rollbar accounts.
8. Select the automation account you have previously added to Cerby, as described in the Requirements section. ​**NOTE:** If you don’t have an automation account, you are prompted to add it. Make sure you read Cerby’s recommendations on how to configure it in the article [Create a service account for your business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/create-an-automation-or-service-account-for-your-business-hub). You may need to add the account first and then add the business hub.
9. Click the **Connect app** button. The wizard closes, and a success message box is displayed. The corresponding business hub is also displayed on the **Business Hubs** page.

The next step is 2. Check for updates to import users and assets to Cerby.

### 2. Check for updates to import users and assets to Cerby

To check for updates in your app to identify and import users and assets to Cerby, you must complete the following steps:

1. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
2.  Click the **More options** (

    ) icon of the corresponding business hub card. A drop-down menu is displayed.
3. Select the **Settings** option from the menu. The business hub details page is displayed with the **Settings** tab activated.
4. Click the **Check for updates** button located at the top right of the page. A message box is displayed with information about the process. ​**NOTE:** The check and import process may take a few minutes depending on the number of users and assets, and because Cerby automatically matches users to their corresponding Cerby user account.
5. Confirm that the automated task to check for updates has the “Completed” status by performing any of the following actions:
   * Click the **More details** button from the message box.
   * Select the **Automation** option from the left menu to open the **Automation** page with a list of automated tasks and their status.

{% hint style="info" %}
**NOTE:** Cerby automatically performs daily checks for updates for all business hubs, but you can trigger them manually, as described in this section. For more instructions, read the article [Sync your app users with your business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/sync-your-business-hub-with-your-external-app).
{% endhint %}

The next step is 3. Connect your Rollbar user account to the business hub.

### 3. Connect your Rollbar user account to the business hub

To connect your Rollbar user account to the business hub so Cerby can manage and protect it, you must complete the following steps:

1. Select the **Accounts** option from the left menu. The **Accounts** page is displayed.
2. Click the **Log in** button of the corresponding Business unique identifier account card. The **Connect your Business unique identifier Account** dialog box is displayed.
3. Enter the login credentials of your **Rollbar** user account.
4. Click the **Connect account** button. The dialog box closes, and a success message box and a new account card are displayed.

The next step is 4. Manage unmatched users.

### 4. Manage unmatched users

During a check for updates, Cerby automatically matches app members to the Cerby user accounts that correspond to their email addresses, including existing [guest users](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-guest-users) and [local partners](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-partners). Manual matching is required when apps don't provide email addresses and for app members using personal or external accounts that couldn’t be identified or are not in the corporate directory.

To view the status of the imported app members, you must complete the following steps:

1. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
2.  Click the **More options** (

    ) icon of the corresponding business hub card. A drop-down menu is displayed.
3. Select the **View Members** option from the menu. The business hub details page is displayed with the **Members** tab activated. App members are displayed in the following tabs of the **User Overview** section:
   * **Unmatched users:** This tab displays the users who were not automatically matched.
   * **Onboarded users:** This tab displays the users matched to their Cerby user account.
   * **Guest users:** This tab displays the users who were matched to an existing Cerby user account but it doesn’t exist in the corporate directory, such as external collaborators.

For unmatched users, you can perform one of the following actions:

* Match users
* Remove unmatched users
* Exempt unmatched users

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
**IMPORTANT:** When removing an unmatched user, Cerby performs an automated task to revoke the user’s seat and permissions in Rollbar.
{% endhint %}

1.  Click the **More options** (

    ) icon of the corresponding user. A drop-down menu is displayed.
2. Select the **Remove user** option from the menu. The **Remove user?** dialog box is displayed.
3. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from the app via an automated task.

#### Exempt unmatched users

Exempted users keep their user accounts or seats active in your app, but you cannot manage them through Cerby.

To exempt unmatched users, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

1.  Click the **More options** (

    ) icon of the corresponding user. A drop-down menu is displayed.
2. Select the **Exempt user** option from the menu. The exempt user dialog box is displayed.
3. Enter a reason for exempting the user in the **Provide a reason** field.
4. Click the **Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

## Use your business hub

The following are the supported features of business hubs you can use:

* [Join the external app and set up your business hub access](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/join-your-external-app-and-set-up-your-business-hub-access)
* [Join the external app and set up your business hub access](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/join-your-external-app-and-set-up-your-business-hub-access)
* [Add users to your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/add-users-and-teams-to-your-apps-via-a-business-hub)
* [Provision users to your apps via an IdP and business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/provision-users-to-your-apps-via-an-idp-and-business-hub)
* [Remove users from your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/remove-users-from-your-app-via-a-business-hub)
* [Remove teams from your app via a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/remove-teams-from-your-app-via-a-business-hub)
* [Deprovision users from your apps via an IdP and business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/deprovision-users-from-your-apps-via-an-idp-and-business-hub)
* [Sync your app users with your business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/sync-your-business-hub-with-your-external-app)
* [Log in to your app via a business hub](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/log-in-to-your-app)
* [Track the activity of business hub users](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/track-activity-on-app-members-user-accounts)
* [Remove a business hub](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/remove-a-business-hub)
