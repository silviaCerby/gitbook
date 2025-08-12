# Connect a TikTok Business Center app integration

**Description:** This article describes how to connect a TikTok Business Center app integration to centrally manage access to it and its assets from Cerby.

Cerby leverages an API and agent-based integration to connect your TikTok
Business Center to your Cerby workspace. With this connection, you can import
your user data, such as assets, roles and permissions, and members, to
centrally and securely manage access from Cerby.

For the connection to happen, you must connect an app integration to Cerby
using the active session of a user account with the **Admin** role on your
TikTok Business Center. Cerby uses this user account to grant permissions to
the Cerby Asset Manager app to sync and import user data and perform user and
asset management tasks on your behalf.

{% hint style="info" %} **NOTE:** Cerby recommends creating a dedicated
account in TikTok for Business (not assigned to a specific user) to manage the
business center from Cerby. Preferably, set it up with a Cerby-managed email
address and phone number. {% endhint %}

After importing your users and assets, you gain visibility on who accesses
your business center, including partners, and their role level. Users with a
Cerby account are automatically matched to their corresponding identity in
your corporate directory, which may be managed by an identity provider (IdP),
such as Okta or Entra ID (formerly Azure AD).

Matched users are prompted in the Cerby dashboard to connect their TikTok for
Business user accounts to Cerby. After connecting their accounts, by following
the instructions in the article [Join the TikTok Business Center and connect
user account to Cerby](https://help.cerby.com/en/articles/9082605-join-tiktok-
tiktok-for-business-and-connect-user-account-to-cerby), you can manage and
secure their access to your TikTok Business Center and its assets and update
their role, all from one single interface.

External collaborators without a Cerby account are displayed as unmatched
users. For these users, you can perform the following actions:

  * Match and invite users to join the app through Cerby

  * Invite users to your workspace as [guest users](https://help.cerby.com/en/articles/8392946-how-to-invite-a-guest-user-to-your-workspace) or [local partners](https://help.cerby.com/en/articles/8980877-explore-partners#h_7e4add33a2), with secure credentials provided and managed by Cerby

  * Remove unmatched users

  * Exempt unmatched users to keep their user account active in TikTok for Business; however, you cannot manage them through Cerby

With [native partners](https://help.cerby.com/en/articles/8980877-explore-
partners#h_e7fa9c355c), you can also gain visibility on the users who access
your assets to run ad campaigns on your partner's side. For more information,
read the article [Connect a TikTok for Business native partner to
Cerby](https://help.cerby.com/en/articles/9082765-connect-a-tiktok-for-
business-native-partner-to-cerby).

This article describes how to connect a TikTok Business Center app integration
and import users and assets to Cerby.

For more information about the management tasks you can perform, read the [Use
Apps](https://help.cerby.com/en/articles/9046120-connect-an-app#h_24b4a346b5)
section from the article [Connect an
App](https://help.cerby.com/en/articles/9046120-connect-an-app).

* * *

# **Requirements**

The following are the requirements to connect your TikTok Business Center app
integration to Cerby:

  * A Cerby account

  * An active TikTok for Business account with the **Admin** role on your TikTok Business Center added to Cerby

  * The Business Manager ID of your TikTok Business Center. To find it, follow the instructions in the [How do I find my Business Center ID?](https://ads.tiktok.com/help/article/tiktok-business-center?lang=en#anchor-8) section of the [About TikTok Business Center](https://ads.tiktok.com/help/article/tiktok-business-center) official documentation

  * Your browser must be configured to allow pop-ups. Follow the corresponding instructions to allow pop-ups:

    * [Google Chrome](https://support.google.com/chrome/answer/95472?hl=en)

    * [Microsoft Edge](https://support.microsoft.com/en-us/search?query=allow%20pop%20ups%20in%20edge)

    * [Mozilla Firefox](https://support.mozilla.org/en-US/kb/pop-blocker-settings-exceptions-troubleshooting)

    * [Safari](https://support.apple.com/guide/safari/block-pop-ups-sfri40696/mac)

* * *

# **Connect a TikTok Business Center app integration**

To add a TikTok Business Center app integration and import its users and
assets to Cerby, you must complete the following main steps:

  1. Add an app integration and connect it to your TikTok Business Center 

  2. Check for updates and import user data to Cerby

  3. Connect your TikTok for Business account to Cerby

  4. Auto-claim the Owner role in Cerby

  5. Manage unmatched users

The following sections describe each main step.

## **1\. Add an app integration and connect it to your TikTok Business
Center**

To add a TikTok Business Center app integration to Cerby and connect it to
your TikTok Business Center, you must complete the following steps:

{% hint style="danger" %} **IMPORTANT:** Make sure you are logged in to your TikTok For Business account in a separate tab of the same web browser window. Cerby identifies this account to connect your TikTok Business Center to the Cerby Asset Manager through the **App Authorization | TikTok For Business** pop-up window in steps 5 and 6. {% endhint %}

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.

  3. Click the **Connect app** button located at the top-right corner of the page. The **Connect your apps to Cerby** dialog box is displayed.

**TIP:** You can select the **Don’t show this again** option to skip this step
the next time you connect a new App.

  4. Click the **Get started** button. A wizard is displayed on the **Select app** page.

  5. Select the **TikTok Business** option from the app catalog. The **Grant access to Cerby** page is displayed on the wizard with the **App Authorization | TikTok for Business** pop-up window on top, as shown in **Figure 1**.

![](gitbook/images0FVFAb1a0_3uSitn-
_o0yP-4wVMpXogHaoKMJikMlwEo7s5OJBaEJhAcSMQs3ymYlRnmeIP_IxGvRFX5KnIH4jlTZ2km52RKBNxAVeji0b8aO620gKlqIwbDw_C9ag5z3X7kPlf_3xAySQyey2Ma9Gg)

**Figure 1. App Authorization | TikTok for Business** pop-up window

  6. Click the **Confirm** button. A success message is displayed and the pop-up window closes automatically.

  7. Click the **Next** button. The **Enter app details** page is displayed on the wizard.

  8. Enter and select your app information in the corresponding fields:

     * **Label in Cerby:** It is the name to assign to your app integration in Cerby, and it will be displayed on the app card.

     * **Business ID:** It is the identifier of your TikTok Business Center. To find the ID, follow the instructions in the [How do I find my Business Center ID?](https://ads.tiktok.com/help/article/tiktok-business-center?lang=en#anchor-8) section of the [About TikTok Business Center](https://ads.tiktok.com/help/article/tiktok-business-center) official documentation.

     * **Password:** It is the password retrieved by Cerby when detecting your active session and granting access to the Cerby Asset Manager app.

**IMPORTANT:** Don’t change the prefilled value in this field.

     * **User management and login method:** It is the way your users log in to the app and determines if they must save their credentials in Cerby. You must select one of the following methods:

       * **Single sign-on (SSO):** Access is managed via your identity provider, and users log in via SSO authentication. They are not asked to save their credentials in Cerby.

       * **Username and password:** Account security and access are managed from Ceby, and users log in with their credentials after saving them in Cerby.

  9. Click the **Connect app** button. The wizard closes, and a success message box is displayed. 

The TikTok Business app card is displayed on the **Apps** view and an account
card is displayed in the **All accounts** view with the “Connect your account”
status.

The next step is 2\. Check for updates and import user data to Cerby, which
you must complete from your Cerby dashboard.

## **2\. Check for updates and import user data to Cerby**

To check for updates and import your user data to Cerby, which includes
members, ad accounts, and roles of your TikTok Business Center, you must
complete the following steps:

  1. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.

  2. Click the **More options** icon of the TikTok Business app card that you added. A drop-down list is displayed.

  3. Select the **Check for updates** option from the list. A message box is displayed with information about the user sync process.

**NOTE:** The check for updates and import process may take a few minutes
depending on the number of assets and users and because Cerby automatically
matches them to their corresponding Cerby account.

  4. Confirm that the **Check for updates** automation task has the “Completed” status by performing any of the following actions:

     * Click the **More details** button from the message box.

     * Select the **Automation** option from the left navigation drawer to open the **Automation** view.

The TikTok Business account and app cards are displayed on the **All
accounts** and **Apps** views, respectively, of each matched user. To connect
their user account to Cerby, matched users must follow the instructions in the
3\. Connect your TikTok for Business account to Cerby step.

{% hint style="info" %} **NOTE:** After adding the TikTok Business Center app
integration, Cerby automatically performs daily checks for updates, but you
can do them manually. When a user is deprovisioned from your IdP and a check
for updates is performed, Cerby generates a report and sends you an email to
confirm their removal from Cerby. Follow the instructions in the article
[Check for updates in your app and apply
report](https://help.cerby.com/en/articles/9046205-check-for-updates-in-your-
app-and-apply-report) to apply the report and remove deprovisioned users. {%
endhint %}

The next step is 3\. Connect your TikTok for Business account to Cerby, which
you must complete from your Cerby dashboard.

## **3\. Connect your TikTok for Business account to Cerby**

To connect your TikTok for Business account to Cerby, you must complete the
following steps:

  1. Select the **All accounts** option from the left navigation drawer. The **All accounts** view is displayed.

  2. Click the **Log in** button of the corresponding TikTok Business account card. The **Connect your Tiktok Business Account** dialog box is displayed.

  3. Enter the login credentials of your TikTok for Business user account.

  4. Click the **Connect account** button. The dialog box closes, and a success message box and a new account card for your user account are displayed.

The next step is 4\. Auto-claim the Owner role in Cerby, which you must
complete from your Cerby dashboard.

## **4\. Auto-claim the Owner role in Cerby**

The integration does not automatically match the **Owner** role in Cerby with
the **Admin** role in your TikTok Business Center; therefore, you must auto-
claim it. To do so, complete the following steps:

  1. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.

  2. Click the **More options** icon of the TikTok Business app card. A drop-down list is displayed.

  3. Select the **View Members** option from the list. The app details page is displayed with the **Members** tab activated and a table of users in the **User Overview** section. 

  4. Activate the **Unmatched users** tab from the **User Overview** section.

  5. Auto-claim the **Owner** role on the TikTok Business app integration by performing the following actions:

     1. Click the **Match user** button that is displayed when you hover over the corresponding user from the table. The **Match user** dialog box is displayed.

     2. Enter your username or email address in the **Match with** search bar. A list of users that match your search is displayed.

     3. Select the corresponding option from the list.

     4. Click the **Next** button. The **Select Cerby role** dialog box is displayed.

     5. Select the **Owner** option from the **Role** drop-down list.

     6. Click the **Match user** button. The dialog box closes, and a success message box is displayed.

**NOTE:** To verify that you have the correct roles, activate the **Onboarded
users** tab from the **User Overview** section. The **Owner** and **Admin**
roles must be displayed in the **Cerby Role** and **App access** columns for
your Cerby account.

The next step is 5\. Manage unmatched users, which you must complete from your
Cerby dashboard.

## **5\. Manage unmatched users**

After a check for updates, Cerby automatically matches users to their
corresponding Cerby accounts. Users who couldn’t be identified during the
check or who are not in the corporate directory are categorized as unmatched.
For these users, you can perform one of the following three actions:

  * Match and invite users

  * Remove unmatched users

  * Exempt unmatched users

All of these actions are performed from the **Unmatched users** tab of the
**User Overview** section inside the app details page, as shown in **Figure
2**.

![](gitbook/imagesWqB5AVNeUizmezoSp4O5fisBsFgu76UL4BO1eM-q2u3-2YzcSX_x0MvY4jmk6V-shwQtf6_zfi8ntxI0b-xR26sgzP0HtOlsTtfsn-
pksONwtJCGkOYDetlRG7LjEH0YanFmK7u0afEnkpvZYrxprVU)

**Figure 2.** **User Overview** section in the **Members** tab of the TikTok
Business app details page

{% hint style="danger" %} **IMPORTANT:** The actions you perform for unmatched
users propagate to the corresponding roles and permissions on assets. {%
endhint %}

### Match and invite users

To match and invite users to join your TikTok Business Center through Cerby,
you must perform the following steps:

  1. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.

  2. Click the **More options** icon of the TikTok Business app card. A drop-down list is displayed.

  3. Select the **View Members** option from the list. The app details page is displayed with the **Members** tab activated and a table of users in the **User Overview** section.

  4. Activate the **Unmatched users** tab from the **User Overview** section.

  5. Click the **Match user** button of the corresponding user. The **Match user** dialog box is displayed.

  6. Enter the username or email address of the user in the **Match with** search bar. A list of users that match your search is displayed.

  7. Select the corresponding option from the list.

  8. Click the **Next** button. The **Select Cerby role** dialog box is displayed.

  9. Select the corresponding role of the user on the TikTok Business app integration from the **Role** drop-down list:

     * **Owner:** This role enables sharing access and managing the app integration configuration.

     * **Collaborator:** This role enables only logging in to the TikTok for Business account.

  10. Click the **Match user** button. The dialog box closes, a success message box is displayed, and the user is moved to the **Onboardedusers** tab.

The TikTok Business account and app cards are displayed in the **All
accounts** and **Apps** views, respectively, of each matched user. To connect
their user account to Cerby, matched users must follow the instructions in the
3\. Connect your TikTok for Business account to Cerby step.

### Remove unmatched users

To remove unmatched users, you must perform the following steps:

  1. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.

  2. Click the **More options** icon of the TikTok Business app card. A drop-down list is displayed.

  3. Select the **View Members** option from the list. The app details page is displayed with the **Members** tab activated and a table of users in the **User Overview** section.

  4. Activate the **Unmatched users** tab from the **User Overview** section.

  5. Click the **More options** icon of the corresponding user. A drop-down list is displayed.

  6. Select the **Remove user** option from the list. The **Remove user?** dialog box is displayed.

  7. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from your TikTok Business Center.

### Exempt unmatched users

Exempted users keep their user accounts active for your TikTok Business
Center, but you cannot manage them through Cerby. To exempt unmatched users,
you must perform the following steps:

  1. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.

  2. Click the **More options** icon of the TikTok Business app card. A drop-down list is displayed.

  3. Select the **View Members** option from the list. The app details page is displayed with the **Members** tab activated and a table of users in the **User Overview** section.

  4. Activate the **Unmatched users** tab from the **User Overview** section.

  5. Click the **More options** icon of the corresponding user. A drop-down list is displayed.

  6. Select the **Exempt user** option from the list. The exempt user dialog box is displayed.

  7. Enter a reason for exempting the user in the **Provide a reason** field.

  8. Click the **Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

* * *

Now you are done. You can start managing and securing access to your TikTok
Business Center and its assets from Cerby.

The following are the supported features of the TikTok Business Center app
integration you can use:

  * [Join TikTok for Business and connect user account to Cerby](https://help.cerby.com/en/articles/9082605-join-tiktok-tiktok-for-business-and-connect-user-account-to-cerby)

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

