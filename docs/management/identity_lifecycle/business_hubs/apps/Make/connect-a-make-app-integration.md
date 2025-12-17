---
description: This article describes how to add a Make app integration to centrally manage access to it and its assets from Cerby.
intercom_id: 9660535
---

# Connect a Make app integration

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* Only supported using the Cerby web app


{% endhint %}

Cerby leverages an automation-based integration to connect Make to your Cerby workspace. With this connection, you can import your user data, such as roles, permissions, and team members, to centrally and securely manage access from Cerby.

For the connection to happen, you must add to Cerby an automation account with the **Team Admin** role on Make and connect it to the corresponding [app integration](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-business-hubs). Cerby uses this account as a service account to access Make, import the user data, and perform access management actions through automated tasks.

Cerby recommends creating a user account dedicated to this purpose, not intended for human use, with the following characteristics depending on the user management and login method for Make:

* **Single sign-on (SSO) managed by your identity provider (IdP):** If you have configured Make as an enterprise application with SSO in your IdP, such as Okta or Entra ID (formerly Azure AD), Cerby recommends provisioning a Make user account through your IdP to be used as the automation account.
Users will not be asked to save their credentials in Cerby; they will continue logging in as usual via SSO authentication. Cerby will be used only to manage user access to Make.

* **Security and access managed by Cerby:** If Make is not configured in your IdP, Cerby recommends creating an account in Make with an associated Cerby-managed email address and phone number.
Users will be asked to save their credentials in Cerby for logging-in purposes. Make admins will be able to manage security and access to Make through Cerby.

{% hint style="info" %}


**NOTE:** For both scenarios, Cerby recommends turning on multi-factor authentication (MFA) with Cerby as an authenticator app.


{% endhint %}

After importing your users, you gain visibility on who accesses your app. Users with a Cerby account are automatically matched to their corresponding identity in your corporate directory, which may be managed by an IdP, such as Okta or Entra ID (formerly Azure AD).

Matched users are prompted in the Cerby dashboard to connect their Make user accounts to Cerby. After connecting their account, by following the instructions in the article [Join the App and connect it to Cerby](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/join-your-external-app-and-set-up-your-business-hub-access), you can manage and secure their access to Make and update their role, all from one single interface.

External collaborators without a Cerby account are displayed as unmatched users. For them, you can perform the following actions:

* Match and invite users to join the app through Cerby
* Invite users to your workspace as [guest users](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-guest-users) or [local partners](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-partners), with secure credentials provided and managed by Cerby
* Remove unmatched users
* Exempt unmatched users to keep their user account active in Make; however, you cannot manage them through Cerby

This article describes how to add a Make app integration and import its users and assets to Cerby. For more information about the management tasks you can perform, read the [Use the Make app integration](connect-a-make-app-integration.md#id-use-the-make-app-integration) section.

* * *

## Requirements

The following are the requirements to connect your Make app integration to Cerby:

  * A Cerby user account with any workspace role
  * An automation account, meaning an active Make user account with the **Team Admin** role
  * The ID of your Make organization. To find it, perform the following actions:

    1. Log in to your Make account.
    2. Select the **Organization** option from the left navigation drawer. The **My Organization** page is displayed.
    3. Copy the ID from the address bar. It’s the number after the `organization` subdirectory. For example, `https://us1.make.com/organization/**1234567** /dashboard`.

* * *

## Connect a Make app integration

To connect a Make app integration and import its users and assets to Cerby, you must complete the following main steps:

  1. [Add an app integration and connect it to Make](connect-a-make-app-integration.md#id-1.-add-an-app-integration-and-connect-it-to-make)
  2. [Check for updates and import users and roles to Cerby](connect-a-make-app-integration.md#id-2.-check-for-updates-and-import-users-and-roles-to-cerby)
  3. [Connect your Make user account to Cerby](connect-a-make-app-integration.md#id-3.-connect-your-make-user-account-to-cerby)
  4. [Manage unmatched users](connect-a-make-app-integration.md#id-4.-manage-unmatched-users)

The following sections describe each main step.

### 1\. Add an app integration and connect it to Make

To add an app integration to Cerby and connect it to Make, you must complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.
  3. Click the **Connect app** button located at the top-right corner of the page. The **Connect your apps to Cerby** dialog box is displayed.

  **TIP:** You can select the **Don’t show this again** option to skip this step the next time you connect a new App.

  4. Click the **Get started** button. A wizard is displayed on the **Select app** page.
  5. Select the **Make Tenant** option. The **Enter app details** page is displayed on the wizard.
  6. Enter and select your app information in the corresponding fields:

     * **Label in Cerby:** It is the name to assign to your app integration in Cerby, and it will be displayed on the app card.
     * **Organization ID:** It is the identifier of your Make organization. For instructions on how to find it, read the [Requirements](connect-a-make-app-integration.md#id-requirements) section.
     * **User management and login method:** It is the way your users log in to the app and determines if they must save their credentials in Cerby. You must select one of the following methods:
       * **Single sign-on (SSO):** Access is managed via your identity provider, and users log in via SSO authentication. They are not asked to save their credentials in Cerby.
       * **Username and password:** Account security and access are managed from Ceby, and users log in with their credentials after saving them in Cerby.

  7. Click the **Next** button. One of the following scenarios occurs depending on whether you have added or not the automation account to Cerby:

     * If you have added the automation account, the **Select automation account** page is displayed on the wizard:

       1. Select the corresponding automation account.
       2. Click the **Connect app** button.

     * If you have not added the automation account, the **Add automation account** page is displayed on the wizard:

       1. Enter the account details in the corresponding fields:

          * **Account label in Cerby**
          * **Email Linked to Account**
          * **Current password**
          * **Phone Number Linked to Account**

       2. Click the **Add account** button.

The corresponding app card is displayed on the **Apps** view and an account card is displayed in the **All accounts** view with the “Connect your account” status.

The next step is [2. Check for updates and import users and roles to Cerby](connect-a-make-app-integration.md#id-2.-check-for-updates-and-import-users-and-roles-to-cerby), which you must complete from the Cerby dashboard.

### 2\. Check for updates and import users and roles to Cerby

To check for updates and import your user data to Cerby, which includes team members and roles in Make, you must complete the following steps:

  1. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.
  2. Click the **More options** (<img src="../../../../../../.gitbook/assets/unnamed_33.png" alt="">) icon of the Make Tenant app card that you added. A drop-down list is displayed.
  3. Select the **Check for updates** option from the list. A message box is displayed with information about the user sync process.

  **NOTE:** The check for updates and import process may take a few minutes depending on the number of assets and users and because Cerby automatically matches them to their corresponding Cerby account.

  4. Confirm that the **Check for updates** automation task has the “Completed” status by performing any of the following actions:

     * Click the **More details** button from the message box.
     * Select the **Automation** option from the left navigation drawer to open the **Automation** view.

The Make Tenant account and app cards are displayed on the **All accounts** and **Apps** views, respectively, of each matched user. To connect their user account to Cerby, matched users must follow the instructions in step [3. Connect your Make user account to Cerby](connect-a-make-app-integration.md#id-3.-connect-your-make-user-account-to-cerby).

**NOTE:** After adding the Make app integration, Cerby automatically performs daily checks for updates, but you can do them manually. When a user is deprovisioned from your IdP and a check for updates is performed, Cerby generates a report and sends you an email to confirm their removal from Cerby. Follow the instructions in the article [Check for updates in your app and apply report](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/sync-your-business-hub-with-your-external-app) to apply the report and remove deprovisioned users.
---

The next step is [3. Connect your Make user account to Cerby](connect-a-make-app-integration.md#id-3.-connect-your-make-user-account-to-cerby), which you must complete from your Cerby dashboard.

### 3\. Connect your Make user account to Cerby

To connect your Make user account to Cerby, you must complete the following steps:

  1. Select the **All accounts** option from the left navigation drawer. The **All accounts** view is displayed.
  2. Click the **Log in** button of the corresponding Make Tenant account card. The **Connect your Make Tenant Account** dialog box is displayed.
  3. Enter the login credentials of your Make user account.
  4. Click the **Connect account** button. The dialog box closes, and a success message box and a new account card for your user account are displayed.

The next step is [4. Manage unmatched users](connect-a-make-app-integration.md#id-4.-manage-unmatched-users), which you must complete from your Cerby dashboard.

### 4\. Manage unmatched users

After a check for updates, Cerby automatically matches users to their corresponding Cerby accounts. Users who couldn’t be identified during the check or who are not in the corporate directory are categorized as unmatched. For these users, you can perform one of the following three actions:

  * [Match and invite users](connect-a-make-app-integration.md#id-match-and-invite-users)
  * [Remove unmatched users](connect-a-make-app-integration.md#id-remove-unmatched-users)
  * [Exempt unmatched users](connect-a-make-app-integration.md#id-exempt-unmatched-users)

All of these actions are performed from the **Unmatched users** tab of the **User Overview** section inside the app details page.

#### Match and invite users

To match and invite users to join Make through Cerby, you must perform the following steps:

  1. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.
  2. Click the **More options** (<img src="../../../../../../.gitbook/assets/unnamed_34.png" alt="">) icon of the Make Tenant app card. A drop-down list is displayed.
  3. Select the **View Members** option from the list. The app details page is displayed with the **Members** tab activated and a table of users in the **User Overview** section.
  4. Activate the **Unmatched users** tab from the **User Overview** section.
  5. Click the **Match user** button of the corresponding user. The **Match user** dialog box is displayed.
  6. Enter the username or email address of the user in the **Match with** search bar. A list of users that match your search is displayed.
  7. Select the corresponding option from the list.
  8. Click the **Next** button. The **Select Cerby role** dialog box is displayed.
  9. Select the corresponding role of the user on the Make app integration from the **Role** drop-down list:

  * **Owner:** This role enables sharing access and managing the app integration configuration.
  * **Collaborator:** This role enables only logging in to Make.

  1. Click the **Match user** button. The dialog box closes, a success message box is displayed, and the user is moved to the **Onboarded** **users** tab.

The Make Tenant account and app cards are displayed in the **All accounts** and **Apps** views, respectively, of each matched user. To connect their user account to Cerby, matched users must follow the instructions in the [3. Connect your Make user account to Cerby](connect-a-make-app-integration.md#id-3.-connect-your-make-user-account-to-cerby) step.

#### Remove unmatched users

To remove unmatched users, you must perform the following steps:

  1. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.
  2. Click the **More options** (<img src="../../../../../../.gitbook/assets/unnamed_35.png" alt="">) icon of the Make Tenant app card. A drop-down list is displayed.
  3. Select the **View Members** option from the list. The app details page is displayed with the **Members** tab activated and a table of users in the **User Overview** section.
  4. Activate the **Unmatched users** tab from the **User Overview** section.
  5. Click the **More options** (<img src="../../../../../../.gitbook/assets/unnamed_36.png" alt="">) icon of the corresponding user. A drop-down list is displayed.
  6. Select the **Remove user** option from the list. The **Remove user?** dialog box is displayed.
  7. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from Make.

#### Exempt unmatched users

Exempted users keep their user accounts active for Make, but you cannot manage them through Cerby. To exempt unmatched users, you must perform the following steps:

  1. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.
  2. Click the **More options** (<img src="../../../../../../.gitbook/assets/unnamed_37.png" alt="">) icon of the Make Tenant app card. A drop-down list is displayed.
  3. Select the **View Members** option from the list. The app details page is displayed with the **Members** tab activated and a table of users in the **User Overview** section.
  4. Activate the **Unmatched users** tab from the **User Overview** section.
  5. Click the **More options** (<img src="../../../../../../.gitbook/assets/unnamed_38.png" alt="">) icon of the corresponding user. A drop-down list is displayed.
  6. Select the **Exempt user** option from the list. The exempt user dialog box is displayed.
  7. Enter a reason for exempting the user in the **Provide a reason** field.
  8. Click the **Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

Now you are done. You can start managing and securing access to Make from Cerby.

##
Use the Make app integration

The following are the supported features of the Make app integration you can use:

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
