# Connect a Snapchat Business Center app integration

**Description:** This article describes how to add a Snapchat Business Center app integration to centrally manage access to it and its assets from Cerby.

Cerby leverages agent-based integration to connect your Snapchat Business
Manager to your Cerby workspace. With this connection, you can import your
user data, such as assets, roles and permissions, and members, to centrally
and securely manage access from Cerby.

For the connection to happen, you must add to Cerby a user account with the
**Organization Admin** role on your Snapchat Business Manager and connect it
to an [app integration](https://help.cerby.com/en/articles/6831152-how-to-use-
tenants). Cerby will use this account as a service account for automation to
access your Snapchat Business Manager, import the user data, and perform
access management tasks.

{% hint style="info" %} **NOTE:** Cerby recommends creating a dedicated
Snapchat Business user account (not assigned to a specific user) to manage the
business center from Cerby. Preferably, set it up with a Cerby-managed email
address and phone number. {% endhint %}

After importing your users and assets, you gain visibility on who accesses
your business center, including partners, and their role level. Users with a
Cerby account are automatically matched to their corresponding identity in
your corporate directory, which may be managed by an identity provider (IdP),
such as Okta or Entra ID (formerly Azure AD).

Matched users are prompted in the Cerby dashboard to connect their Snapchat
Business user accounts to Cerby. After connecting their account, by following
the instructions in the article [Join Snapchat Business Manager and connect
user account to Cerby](https://help.cerby.com/en/articles/9082757-join-
snapchat-business-and-connect-user-account-to-cerby), you can manage and
secure their access to your Snapchat Business Manager and its assets and
update their role, all from one single interface.

External collaborators without a Cerby account are displayed as unmatched
users. For these users, you can perform the following actions:

  * Match and invite users to join the app through Cerby

  * Invite users to your workspace as [guest users](https://help.cerby.com/en/articles/8392946-how-to-invite-a-guest-user-to-your-workspace) or [local partners](https://help.cerby.com/en/articles/8980877-explore-partners#h_7e4add33a2), with secure credentials provided and managed by Cerby

  * Remove unmatched users

  * Exempt unmatched users to keep their user account active in Snapchat for Business; however, you cannot manage them through Cerby

This article describes how to add a Snapchat Business Center app integration
and import its users and assets to Cerby.

For more information about the management tasks you can perform, read the [Use
Apps](https://help.cerby.com/en/articles/9046120-connect-an-app#h_24b4a346b5)
section from the article [Connect an
App](https://help.cerby.com/en/articles/9046120-connect-an-app).

* * *

# **Requirements**

The following are the requirements to connect your Snapchat Business Center
app integration to Cerby:

  * An Cerby account

  * An active Snapchat Business Manager account with the **Organization Admin** role

  * The Business Manager ID of your Snapchat Business Manager. To find it, perform the following actions after logging in to your Snapchat Business account:

    1. Select the **Business Details** option from the left navigation drawer. The **Business Details** page is displayed.

    2. Copy the value from the **Organization ID** field in the **Organization Name** section.

* * *

# **Connect a Snapchat Business Center app integration**

To connect a Snapchat Business Center app integration and import its users and
assets to Cerby, you must complete the following main steps:

  1. Add an app integration and connect it to your Snapchat Business Manager

  2. Check for updates and import users and roles to Cerby

  3. Connect your Snapchat Business account to Cerby

  4. Manage unmatched users

The following sections describe each main step.

## **1\. Add an app integration and connect it to your Snapchat Business
Manager**

To add a Snapchat Business Center app integration to Cerby and connect it to
your Snapchat Business Manager, you must complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.

  3. Click the **Connect app** button located at the top-right corner of the page. The **Connect your apps to Cerby** dialog box is displayed.

**TIP:** You can select the **Don’t show this again** option to skip this step
the next time you connect a new App.

  4. Click the **Get started** button. A wizard is displayed on the **Select app** page.

  5. Select the **Snapchat Business Tenant** option. The **Enter app details** page is displayed on the wizard.

  6. Enter and select your app information in the corresponding fields:

     * **Label in Cerby: It is the name to assign to your app integration in Cerby, and it will be displayed on the app card.**

     * **Team ID:** It is the identifier of your Snapchat Business Manager. To find it, perform the following actions after logging in to your Snapchat Business account:

       1. Select the **Business Details** option from the left navigation drawer. The **Business Details** page is displayed.

       2. Copy the value from the **Organization ID** field in the **Organization Name** section. 

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

The Snapchat Business Tenant app card is displayed on the **Apps** view and an
account card is displayed in the **All accounts** view with the “Connect your
account” status.

The next step is 2\. Check for updates and import users and roles to Cerby,
which you must complete from the Cerby dashboard.

## **2\. Check for updates and import users and roles to Cerby**

To check for updates and import your user data to Cerby, which includes
members, ad accounts, and roles of your Snapchat Business Manager, you must
complete the following steps:

  1. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.

  2. Click the **More options** icon of the Snapchat Business Tenant app card that you added. A drop-down list is displayed.

  3. Select the **Check for updates** option from the list. A message box is displayed with information about the user sync process.

**NOTE:** The check for updates and import process may take a few minutes
depending on the number of assets and users and because Cerby automatically
matches them to their corresponding Cerby account.

  4. Confirm that the **Check for updates** automation task has the “Completed” status by performing any of the following actions:

     * Click the **More details** button from the message box.

     * Select the **Automation** option from the left navigation drawer to open the **Automation** view.

The Snapchat Business Tenant account and app cards are displayed on the **All
accounts** and **Apps** views, respectively, of each matched user. To connect
their user account to Cerby, matched users must follow the instructions in the
3\. Connect your Snapchat Business account to Cerby step.

{% hint style="info" %} **NOTE:** After adding the Snapchat Business Center
app integration, Cerby automatically performs daily checks for updates, but
you can do them manually. When a user is deprovisioned from your IdP and a
check for updates is performed, Cerby generates a report and sends you an
email to confirm their removal from Cerby. Follow the instructions in the
article [Check for updates in your app and apply
report](https://help.cerby.com/en/articles/9046205-check-for-updates-in-your-
app-and-apply-report) to apply the report and remove deprovisioned users. {%
endhint %}

The next step is 3\. Connect your Snapchat Business account to Cerby, which
you must complete from your Cerby dashboard.

## **3\. Connect your Snapchat Business account to Cerby**

To connect your Snapchat Business account to Cerby, you must complete the
following steps:

  1. Select the **All accounts** option from the left navigation drawer. The **All accounts** view is displayed.

  2. Click the **Log in** button of the corresponding Snapchat Business Tenant account card. The **Connect your Snapchat Business Tenant Account** dialog box is displayed.

  3. Enter the login credentials of your Snapchat Business user account.

  4. Click the **Connect account** button. The dialog box closes, and a success message box and a new account card for your user account are displayed.

{% hint style="info" %} **NOTE:** Cerby recommends you grant permissions to
users on your Snapchat Business Manager before sharing ad accounts and access
to them in your Cerby workspace. {% endhint %}

The next step is 4\. Manage unmatched users, which you must complete from your
Cerby dashboard.

## **4\. Manage unmatched users**

After a check for updates, Cerby automatically matches users to their
corresponding Cerby accounts. Users who couldn’t be identified during the
check or who are not in the corporate directory are categorized as unmatched.
For these users, you can perform one of the following three actions:

  * Match and invite users

  * Remove unmatched users

  * Exempt unmatched users

All of these actions are performed from the **Unmatched users** tab of the
**User Overview** section inside the app details page.

{% hint style="danger" %} **IMPORTANT:** The actions you perform for unmatched
users propagate to the corresponding roles and permissions on assets. {%
endhint %}

### Match and invite users

To match and invite users to join your Snapchat Business Manager through
Cerby, you must perform the following steps:

  1. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.

  2. Click the **More options** icon of the Snapchat Business Tenant app card. A drop-down list is displayed.

  3. Select the **View Members** option from the list. The app details page is displayed with the **Members** tab activated and a table of users in the **User Overview** section.

  4. Activate the **Unmatched users** tab from the **User Overview** section.

  5. Click the **Match user** button of the corresponding user. The **Match user** dialog box is displayed.

  6. Enter the username or email address of the user in the **Match with** search bar. A list of users that match your search is displayed.

  7. Select the corresponding option from the list.

  8. Click the **Next** button. The **Select Cerby role** dialog box is displayed.

  9. Select the corresponding role of the user on the Snapchat Business tenant from the **Role** drop-down list:

     * **Owner:** This role enables sharing access and managing the account configuration.

     * **Collaborator:** This role enables only logging in to the account.

  10. Click the **Match user** button. The dialog box closes, a success message box is displayed, and the user is moved to the **Onboarded** **users** tab.

The Snapchat Business Tenant account and app cards are displayed in the **All
accounts** and **Apps** views, respectively, of each matched user. To connect
their user account to Cerby, matched users must follow the instructions in the
3\. Connect your Snapchat Business account to Cerby step.

### Remove unmatched users

To remove unmatched users, you must perform the following steps:

  1. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.

  2. Click the **More options** icon of the Snapchat Business app card. A drop-down list is displayed.

  3. Select the **View Members** option from the list. The app details page is displayed with the **Members** tab activated and a table of users in the **User Overview** section.

  4. Activate the **Unmatched users** tab from the **User Overview** section.

  5. Click the **More options** icon of the corresponding user. A drop-down list is displayed.

  6. Select the **Remove user** option from the list. The **Remove user?** dialog box is displayed.

  7. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from your Snapchat Business Manager.

### Exempt unmatched users

Exempted users keep their user accounts active for your Snapchat Business
Manager, but you cannot manage them through Cerby. To exempt unmatched users,
you must perform the following steps:

  1. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.

  2. Click the **More options** icon of the Snapchat Business app card. A drop-down list is displayed.

  3. Select the **View Members** option from the list. The app details page is displayed with the **Members** tab activated and a table of users in the **User Overview** section.

  4. Activate the **Unmatched users** tab from the **User Overview** section.

  5. Click the **More options** icon of the corresponding user. A drop-down list is displayed.

  6. Select the **Exempt user** option from the list. The exempt user dialog box is displayed.

  7. Enter a reason for exempting the user in the **Provide a reason** field.

  8. Click the **Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

* * *

Now you are done. You can start managing and securing access to your Snapchat
Business Manager and its assets from Cerby.

The following are the supported features of the Snapchat Business Center app
integration you can use:

  * [Join Snapchat Business and connect user account to Cerby](https://help.cerby.com/en/articles/9082757-join-snapchat-business-and-connect-user-account-to-cerby)

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

