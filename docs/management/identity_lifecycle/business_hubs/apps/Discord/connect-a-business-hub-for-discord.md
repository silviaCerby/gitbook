---
description: This article describes how to connect a business hub to manage Discord users’ roles from Cerby.
intercom_id: 9823646
---

# Connect a business hub for Discord

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* Only supported using the Cerby web app


{% endhint %}

As a user with any workspace role in Cerby, except **Guest User** and **Login-Only** , you can connect a business hub for Discord to centrally manage users’ roles from Cerby and become the **Owner** of this integration.

The following are the main characteristics of this integration:

* Cerby syncs the Discord users and roles within a server by its ID
* You must manually match users with their corresponding Discord roles and Cerby user accounts after connecting the integration
* You can kick users from a Discord server directly through Cerby
* You can centrally manage the users’ roles on your Discord server using Cerby
* In this release, the ability to invite users to Discord through Cerby is not supported

This article contains instructions on how to connect a Cerby business hub for Discord. For app-specific articles and videos, visit the [Connecting your business hubs](https://help.cerby.com/en/collections/10289415-connecting-your-apps) collection in the Cerby Help Center.

* * *

## Requirements

The following are the requirements to connect a business hub for Discord:

* A Cerby workspace
* A Cerby user account with the **Owner** , **Super Admin** , **Admin** , or **User** role\
  **NOTE:** This user can have any role in the Discord server

* A Discord account profile in Cerby can be set up using a placeholder account without requiring real credentials. Unlike other integrations, Discord doesn't need an automation account, so you don't have to add a service account
* An active Discord server with the following characteristics:
    * To install the **Cerby Integration - Production** application on your Discord server, complete the following steps:

      1. Click the [Cerby Integration - Production](https://discord.com/oauth2/authorize?client_id=1277761866340499552) authorization link. A Discord page opens in your web browser, informing you that an external application wants to access your Discord account.
      2. Select the server where you want to install the application in the **ADD TO SERVER** field.
      3. Click the **Continue** button. The next page displays the permission the Cerby application requires for the integration: **Manage Roles** and**Kick Members**.
      4. Click the **Authorize** button. The **Wait! Are you human?** dialog box is displayed.
      5. Complete the challenge in the dialog box. The **Success!** page is displayed. The Cerby application is installed on the server. It displays the **APP** tag next to its name. You can also see it in the **Integrations** window of the server settings.
​**TIP:** By default, an announcement in the **General** channel informs that the **Cerby Integration - Production** application has been installed. You can turn off this announcement or change the display name by following the next steps:

         1. Right-click the **Cerby Integration - Production** application link in the message. A menu is displayed.
         2. Select the **Change Nickname** option from the menu. The **Change Nickname** window opens.
         3. Enter the new name for the application in the **NICKNAME** field.
         4. Click the **Save** button. The message on the **General** channel displays the updated name for the Cerby application.

* Your [Discord server roles](https://support.discord.com/hc/en-us/articles/214836687-Role-Management-101) must be configured and ordered in the hierarchy you want to manage from Cerby
* You must place the Cerby application at the top of the Discord role hierarchy you want to manage from Cerby. The order in which the Cerby application is placed in the hierarchy list of roles determines what permissions Cerby can change. Anything below the Cerby application enables **Account Owners** in Cerby of the Discord integration to update the user's permissions in Cerby. However, anything that's above the Cerby application cannot be changed by Cerby.
To reorder the role hierarchy in Discord, you must follow the next steps:

    1. Open the Discord server on the desktop or web app.
    2. Right-click your server’s icon on the left. A menu is displayed.
    3. Hover over the **Server Settings** option. Another menu is displayed.
    4. Select the **Roles** option. The **Roles** window opens.
    5. Drag and drop the Cerby application to the highest position in the list. **NOTE:** To learn more about Discord roles and role hierarchy, visit the Discord [Role Management 101](https://support.discord.com/hc/en-us/articles/214836687-Role-Management-101) official website.

* Your Discord server ID (a 19-digit numerical code). You must complete the following steps to get it:

    1. Open the Discord server on the desktop or web app.
    2. Click the **User Settings** (<figure><img src="../../../../../../.gitbook/assets/unnamed_2.png" alt=""><figcaption></figcaption></figure>) icon next to your user name at the bottom left pane. The **My Account** detail window opens.
    3. Select the **Advanced** option in the **APP SETTINGS** section of the left pane. The **Advanced** window opens.
    4. Activate the **Developer Mode** toggle to enable it.
    5. Click the **ESC** (<figure><img src="../../../../../../.gitbook/assets/unnamed_3.png" alt=""><figcaption></figcaption></figure>) button.
    6. Right-click your server’s icon on the left. A menu is displayed.
    7. Select the **Copy Server ID** option. The server ID is copied to the clipboard.

* * *

## Connect a business hub for Discord

To connect a business hub for Discord, you must complete the following main steps from the Cerby web app dashboard:

  1. Add a business hub and connect it to Discord
  2. Check for updates to import users and roles to Cerby
  3. Manage synced users
  4. Connect your app’s user account to the business hub

The following sections describe each main step.

### 1\. Add a business hub and connect it to Discord

To add a business hub and connect it to Discord, you must complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
  3. Click the **Connect Business Hub** button located at the top-right corner of the page. The **Connect your Business Hubs to Cerby** dialog box is displayed.
**TIP:** You can select the **Don’t show this again** option to skip this step the next time you connect a new business hub.

  4. Click the **Get started** button. A wizard is displayed on the **Select app** page.
  5. Select the **Discord** app from the catalog. The **Enter app details** page is displayed on the wizard.
  6. Enter and select your app information in the corresponding fields:

     * **Label in Cerby:** It is the name assigned to your business hub in Cerby, and it will be displayed on the business hub card.

     1. **Business ID:** It is the 19-digit numerical Discord server identifier you obtained in the Requirements section.
     2. **User management and login method:** It is the way your users log in to the app and determines if they must save their credentials in Cerby. You must select **Username and password** method.
  7. Click the **Next** button. The **Select automation account** page is displayed.
  8. Select the Discord account you previously created.
**NOTE:** This account must have been previously created. (See the Requirements section.) It doesn't need to have a real Discord user profile.

  9. Click the **Connect app** button. The wizard closes, and a success message box is displayed. The corresponding business hub is also displayed on the **Business Hubs** view.

The next step is 2\. Check for updates to import users and roles to Cerby.

### 2\. Check for updates to import users and roles to Cerby

To check for updates in your app to identify and import users and roles to Cerby, you must complete the following steps:

  1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
  2. Click the **Settings** (<figure><img src="../../../../../../.gitbook/assets/unnamed_4.png" alt=""><figcaption></figcaption></figure>) icon of the corresponding business hub card. The business hub details page is displayed with the **Settings** tab activated.
  3. Click the **Check for updates** button located at the top right of the page. A message box is displayed with information about the process.
**NOTE:** Depending on the number of users and roles, the check and import process may take a few minutes.

  4. Confirm that the **Check for updates** automated task has the “Completed” status by performing any of the following actions:
     1. Click the **More details** button from the message box.
     2. Select the **Automation** option from the left navigation drawer to open the **Automation** view.

{% hint style="info" %}


**NOTE:** Cerby automatically performs daily checks for updates for all business hubs, but you can trigger them manually, as described above in steps 1 to 3. For more instructions, read the article [Check for updates in your app and apply report](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/sync-your-business-hub-with-your-external-app).


{% endhint %}

The next step is 3\. Manage the synced users, which you must complete from your Cerby dashboard.

### 3\. Manage synced users

To assign a Discord role to the synced users, you must complete the following steps:

**IMPORTANT:** After you check for updates, the following occurs:

* You must ensure you assign yourself a Discord role from Cerby before managing other synced users’ roles.
* The only user who appears as an **Onboarded user** is you, the **Owner** , who onboarded the Discord business hub.
* The rest of the Discord users synced in Cerby appear as **Unmatched users**. You must manually match these users with their corresponding Discord roles, and their Cerby users.

---

  1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
  2. Click the **More options** (<figure><img src="../../../../../../.gitbook/assets/unnamed_5.png" alt=""><figcaption></figcaption></figure>) icon on the corresponding business hub card. A drop-down list is displayed.
  3. Select the **View Members** option from the list. The business hub details page is displayed with the **Members** tab activated.
The app members are displayed in the following tabs of the **User Overview** section:

     * **Unmatched users:** This tab displays the users who were not automatically matched because they use an email address that couldn’t be identified or they are not in the corporate directory.
     * **Onboarded users:** This tab displays the users matched to their Cerby user account.

  4. Activate the **Onboarded users** tab.
  5. Click the drop-down field under the **App access** column next to the user’s name. The list of roles in your Discord server is displayed.
  6. Select the Discord role you want to assign to the user. The update is applied immediately in Discord.

For unmatched users, you can perform one of the following actions:

* Match users
* Remove unmatched users
* Exempt unmatched users

The following sections describe each action.

### Match users

To match users to their corresponding Cerby user accounts, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

  1. Hover the mouse over the External enrollee button under the status column. The **Match user** button appears.
  2. Click the **Match user** button of the corresponding user. The **Match user** dialog box is displayed.
  3. Enter the Cerby username or email address of the user you want to match and invite in the **Match with** field. The user is displayed on a list.
  4. Select the user from the list.
  5. Click the **Next** button. The **Select Cerby role** dialog box is displayed.
  6. Select the corresponding role of the user on the app from the **Cerby role** drop-down list:

     * **Owner:** This role enables sharing access and managing the app settings in Cerby.
     * **Collaborator:** This role enables only logging in to the app.

  7. Click the **Match user** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Onboarded** **users** tab.

### Remove unmatched users

To remove unmatched users from Discord, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

**IMPORTANT:** When you remove users from the **Unmatched users** tab, you are also removing (deprovisioning) those users from the Discord server.
---

  1. Click the **More options** (<figure><img src="../../../../../../.gitbook/assets/unnamed_6.png" alt=""><figcaption></figcaption></figure>) icon of the corresponding user. A drop-down list is displayed.
  2. Select the **Remove user** option from the list. The **Remove user?** dialog box is displayed.
  3. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from the app.

### Exempt unmatched users

Exempted users keep their user accounts active for the seat-based or paid social app, but you cannot manage them through Cerby.

To exempt unmatched users, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

  1. Click the **More options** (<figure><img src="../../../../../../.gitbook/assets/unnamed_7.png" alt=""><figcaption></figcaption></figure>) icon of the corresponding user. A drop-down list is displayed.
  2. Select the **Exempt user** option from the list. The exempt user dialog box is displayed.
  3. Enter a reason for exempting the user in the **Provide a reason** field.
  4. Click the **Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

The next step is 4\. Connect your app’s user account to the business hub.

### 4\. Connect your app’s user account to the business hub

To connect your Discord’s user account to the business hub so Cerby can manage and protect it, you must complete the following steps:

  1. Select the **Accounts** option from the left navigation drawer. The **Accounts** view is displayed.
  2. Click the **Log in** button of the corresponding Make Tenant account card. The **Connect your Make Tenant Account** dialog box is displayed.
  3. Enter the login credentials of your Make user account.
  4. Click the **Connect account** button. The dialog box closes, and a success message box and a new account card for your user account are displayed.

* * *

## Use your business hub

The following are the supported features of Business hubs you can use:

* [Join the app and connect it to Cerby](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/join-your-external-app-and-set-up-your-business-hub-access)
* [Update the app members’ roles](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/update-user-roles-in-your-app-via-a-business-hub)
* [Check for updates in your app and apply report](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/sync-your-business-hub-with-your-external-app)
* [Re-assign the app members’ user accounts](https://help.cerby.com/en/articles/9046211-re-assign-the-app-members-user-accounts)
* [Manage the security of app members’ user accounts](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/protect-your-app-user-accounts-via-a-business-hub)
* [Log in to your app](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/log-in-to-your-app)
* [Track activity on app members’ user accounts](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-users/track-activity-on-app-members-user-accounts)
* [Remove an App](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/remove-a-business-hub)
* [Troubleshooting Apps](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/troubleshooting/troubleshooting-business-hubs)
