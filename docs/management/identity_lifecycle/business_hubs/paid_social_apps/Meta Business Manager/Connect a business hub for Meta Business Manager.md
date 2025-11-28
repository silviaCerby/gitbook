# Connect a business hub for Meta Business Manager

**Description:** This article describes how to connect a business hub to centrally manage the users and assets of Meta Business Manager from Cerby.

{% hint style="info" %} **Who can use this feature?** * Workspace**Owners** ,
**Super Admins** , **Admins** , and **Users** * Only supported using the Cerby
web app {% endhint %}

As a user with any workspace role in Cerby, except **Guest User** and **Login-
Only** , you can connect a business hub integration to centrally manage the
users and assets (such as Facebook Pages and Ad accounts) of Meta Business
Manager (now Meta Business Portfolio).

When you connect the business hub, you become its **Owner** , and you can
perform the following user and access management tasks through automated tasks
and API calls executed by the Cerby agent:

  * Check for updates

  * Add users

  * Update user roles

  * Remove users

{% hint style="success" %} **TIP:** For more details about the automated tasks
of a business hub, how it works, and the supported apps, read the article
[Explore Business Hubs](https://help.cerby.com/en/articles/6831152-explore-
apps). {% endhint %}

Additionally, you can perform the following actions to manage access to your
Meta Business Manager for external collaborators:

  * Invite users to your workspace as [guest users](https://help.cerby.com/en/articles/8392946-how-to-invite-a-guest-user-to-your-workspace) or [local partners](https://help.cerby.com/en/articles/8980877-explore-partners#h_7e4add33a2), with secure credentials provided and managed by Cerby.

  * Connect a [native partner](https://help.cerby.com/en/articles/8980877-explore-partners#h_e7fa9c355c) to your workspace to gain visibility on the partner’s users with shared access to the assets of your Meta Business Manager. For more information, read the article [Connect a Meta Business Manager native partner to Cerby](https://help.cerby.com/en/articles/8986246-connect-a-meta-business-manager-native-partner-to-cerby).

This article provides instructions on how to connect a business hub for
ChatGPT. For other app-specific articles and videos, review the [Connecting
business hubs for your
apps](https://help.cerby.com/en/collections/10289415-connecting-your-apps) and
[Connecting business hubs for your paid social
apps](https://help.cerby.com/en/collections/12330234-connecting-business-hubs-
for-your-paid-social-apps) collections in the Cerby Help Center.

* * *

# **Requirements**

The following are the requirements to connect the business hub:

  * Meta Business Manager

    * A user account with the **Full control** role on your Meta Business Manager

    * An existing primary page associated with your Meta Business Manager. For instructions, read the article [Change your primary Page in Meta Business Suite or Business Manager](https://www.facebook.com/business/help/1809771339071540?id=180505742745347)

    * The user management and login method for your business hub identified to select the corresponding option when connecting your app. For more information, read the **User management and login method** section of the article [Explore Business Hubs](https://help.cerby.com/en/articles/6831152-explore-apps)

    * The Business Manager ID of your Meta Business Manager. To find it, complete the instructions in the article [Find your business ID in Meta Business Manager](https://www.facebook.com/business/help/1181250022022158?id=180505742745347)

  * Cerby

    * A Cerby workspace

    * A Cerby user account with the **Owner** , **Super Admin** , **Admin** , or **User** role

    * Groups configured in your identity provider (IdP) If you want to leverage automatic user provisioning and deprovisioning from your apps based on group assignment events. For more information, read the articles available in the [Managing users via an IdP and business hub](https://help.cerby.com/en/collections/12330182-managing-users-via-an-idp-and-business-hub) collection in the Cerby Help Center

* * *

# **Connect a business hub for Meta Business Manager**

To connect a business hub for Meta Business Manager, you must complete the
following main steps in Meta and the Cerby web app dashboard:

  1. Connect your Meta Business Manager to the Cerby Assets Manager app

  2. Create a system user in Meta Business Manager

  3. Generate a token for the Meta Business Manager system user

  4. Add a business hub and connect it to Meta Business Manager 

  5. Check for updates to import users, roles, and assets to Cerby

  6. Connect your Meta Business Manager user account to the business hub

  7. Auto-claim the Owner role in Cerby

  8. Manage unmatched users

The following sections describe each main step.

## 1\. Connect your Meta Business Manager to the Cerby Assets Manager app

To connect your Meta Business Manager to the Cerby Assets Manager app, you
must complete the following steps:

  1. Log in to your [Meta Business Manager](https://business.facebook.com/).

  2. Navigate to your business portfolio.

  3. Select the **Settings** option from the left navigation drawer. The **Settings** view is displayed.

  4. Select the **Apps** option from the **Accounts** drop-down menu in the left pane. The **Apps** page is displayed.

  5. Click the **Add** button. The **What do you want to do?** dialog box is displayed.

  6. Select the **Request access to an app ID** option. The **Request an app** dialog box is displayed.  
​**NOTE:** If the **How Will You Work With Cerby, Inc.?** dialog box is
displayed instead the **Request an app** dialog box, complete the following
steps:

     1. Select the **Other** option.

     2. Enter **Security provider to help with identity and access governance** in the **Other** input field.

     3. Click the **Next** button. The **Request an app** dialog box is displayed.

  7. Enter **2965389650414399** in the **App ID** field.

  8. Click the **Request app** button. The dialog box closes.

The next step is 2\. Create a system user in Meta Business Manager.

## 2\. Create a system user in Meta Business Manager

To create a system user with an **Admin** role in Meta Business Manager, you
must complete the following steps in your Meta Business Manager:

{% hint style="info" %} **NOTE:** Meta allows having only one system user with
an **Admin** role. If you already have a system user, you can reuse it for
this configuration. {% endhint %}

  1. Select the **System users** option from the **Users** drop-down menu in the left pane. The **System users** page is displayed.

**NOTE:** If you have already created a system user with an **Admin** role,
continue to step 6.

  2. Click the **Add** button. The **Create system user** dialog box is displayed.

  3. Enter a name for the system user in the **System user name** field. For example, **Cerby**.

  4. Select the **Admin** option from the **System user role** drop-down menu.

  5. Click the **Create system user** button. The dialog box closes, and the **Cerby** system user is displayed on the **System users** page, as shown in **Figure 1**.

![](images/AD_4nXfOxtp_tx3Qa6qXKLTNjmt0-MTrU6Gy6b2034a-1IqeaXFhaXEb5TibbbH23tX1nizu4O4CYH8uw58qOE7POt7mNTdSriqgz6RfaIOc4pdCcn3Ziee3AoCPBJbkMugbaUVxxt7dfw)

**Figure 1.** **System Users** page

  6. Note down the **ID** of the system user.

  7. Contact the Cerby Support team via email at [support@cerby.com](mailto:support@cerby.com) or through the help chat to let them know that you have requested access to the Cerby Assets Manager app. Also, you must share the system user **ID** with them.

{% hint style="danger" %} **IMPORTANT:** Take the following into
consideration: * Meta may restrict user management actions from Cerby (add,
update, and remove users) for at least seven days after creating a system
user. Therefore, Cerby recommends waiting seven days to start managing access
to Meta Business Manager through your business hub. * You must wait until the
Cerby Support team grants you access to the Cerby Assets Manager app to
continue. On the **Apps** page, the Cerby Assets Manager app must change its
status from “Request sent” to active with the “Cerby, Inc. owns this” message.
{% endhint %}

The next step is 3\. Generate a token for the Meta Business Manager system
user.

## 3\. Generate a token for the Meta Business Manager system user

To generate a token for the Meta Business Manager system user, you must
complete the following steps in your Meta Business Manager:

  1. Select the **System users** option from the **Users** drop-down menu in the left pane. The **System users** page is displayed.

  2. Select the system user with the **Admin** role. A collapsible pane is displayed to the right with the details of the system user.

  3. Click the **Generate token** button. The **Generate token** wizard is displayed on the **Select app** page, as shown in **Figure 2**.

![](images/AD_4nXc2RyJPo2_-crNzOV38LP1-aTgEf6ILd-
xfKy_cV4vYAELtE8xWVsFKLDxAoUIl5fmBCnyK_O-4udUdo76hlIlbyK2fc63kjSl3-bRjMRgYDLneSQklTdkANiwmuCw50DJU9bMG)

**Figure 2.** **Select app** page of the **Generate token** wizard

  4. Select the **Cerby Assets Manager** option from the **Select app** drop-down menu.

  5. Click the **Next** button. The **Set expiration** page of the wizard is displayed.

  6. Select the **Never** option from the **Token expiration** section.

  7. Click the **Next** button. The**Assign permissions** page of the wizard is displayed. 

  8. Select the following options from the **Select permissions** drop-down menu:

     * **ads_management**

     * **business_management**

     * **catalog_management**

     * **pages_manage_metadata**

     * **pages_read_engagement**

     * **pages_show_list**

  9. Click the **Generate token** button. The **Done** page of the wizard is displayed with the token.

  10. Click the **Copy** button to copy the token so you can save it, because you need it later.

  11. Click the **Done** button. The wizard closes.

The next step is 4\. Add a business hub and connect it to Meta Business
Manager.

## 4\. Add a business hub and connect it to Meta Business Manager

To add a business hub and connect it to Meta Business Manager, you must
complete the following steps in the Cerby platform:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.

  3. Click the **Connect Business Hub** button located at the top-right corner of the page. The **Connect your Business Hubs to Cerby** dialog box is displayed.  
​**TIP:** Select the **Don’t show this again** option to skip this step the
next time you connect a new business hub.

  4. Click the **Get started** button. A wizard is displayed on the **Select app** page.

  5. Select **Meta Business** from the catalog. The **Enter app details** page is displayed on the wizard.

  6. Enter and select your app information in the corresponding fields:

     * **Label in Cerby:** It is the name to assign to your business hub in Cerby, and it will be displayed on the business hub card.

     * **Access Token:** It is the token that you’ve previously generated in your Meta Business Manager.

     * **Business ID:** It is your Meta Business Manager ID. For instructions on how to find it, read the Requirements section.

     * **App Id:** It is the ID of the Cerby Assets Manager app to which you requested access previously: **2965389650414399**.

     * **User management and login method:** It is the way your users log in to the app and determines whether they must save their login credentials as a Cerby account connected to the business hub. You must select one of the following methods:

       * **Single sign-on (SSO):** Access is managed by your identity provider, and users log in with SSO authentication. They are not asked to save their credentials in Cerby.

       * **Username and password:** Cerby manages account security and access, and users log in with their credentials after saving them in Cerby.

  7. Click the **Connect app** button. The wizard closes, and a success message box is displayed.   
The corresponding business hub is also displayed on the **Business Hubs**
page.

The next step is 5\. Check for updates to import users, roles, and assets to
Cerby.

## 5\. Check for updates to import users, roles, and assets to Cerby

To check for updates in your app to identify and import users, roles, and
assets to Cerby, you must complete the following steps in the Cerby platform:

  1. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.

  2. Click the **More options** (![](images/AD_4nXewApJOBZXewpFew1XrkjC6rCssB5Upy2WRCW8fpJjw2Zmj0xzSkEgw3tUBvW6lyQC2RihdmxzJ6KKXG1pvMGfAeaQnjZUGnThkBo5vdisjtu8WvqHXLgT1_7-xOwkkFy5umyicPg)) icon of the corresponding business hub card. A drop-down menu is displayed.

  3. Select the **Settings** option from the menu. The business hub details page is displayed with the **Settings** tab activated.

  4. Click the **Sync** button located at the top right of the page. A message box is displayed with information about the process.  
​**NOTE:** The check and import process may take a few minutes depending on
the number of users, and because Cerby automatically matches users to their
corresponding Cerby user account.

  5. Confirm that the automated task to check for updates has the “Completed” status by performing any of the following actions:

     * Click the **More details** button from the message box.

     * Select the **Automation** option from the left menu to open the **Automation** page with a list of automated tasks and their status.

{% hint style="info" %} **NOTE:** Cerby automatically performs daily checks
for updates for all business hubs, but you can trigger them manually, as
described in this section. For more instructions, read the article [Sync your
app users with your business
hub](https://help.cerby.com/en/articles/9046205-check-for- updates-in-your-
app-and-apply-report). {% endhint %}

The next step is 6\. Connect your Meta Business Manager user account to the
business hub.

## 6\. Connect your Meta Business Manager user account to the business hub

To connect your Meta Business Manager user account to the business hub so
Cerby can manage and protect it, you must complete the following steps:

  1. Select the **Accounts** option from the left menu. The **All accounts** page is displayed.

  2. Click the **Log in** button of the corresponding Meta Business account card. The **Connect your Meta Business Account** dialog box is displayed.

  3. Enter the login credentials of your Meta Business Manager user account.

  4. Click the **Connect account** button. The dialog box closes, and a success message box and a new account card are displayed.

The next step is 7\. Auto-claim the Owner role in Cerby.

## 7\. Auto-claim the Owner role in Cerby

When your Cerby account has a different email than your Facebook profile, the
integration does not automatically match the **Owner** role in Cerby with the
**Admin** role in your Meta Business Manager. Therefore, you must manually
claim ownership.

To claim the **Owner** role for your business hub, you complete the following
steps:

  1. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.

  2. Click the **More options** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1376309103/ce732ce8cd0407784ebc8e5928e7/AD_4nXfXuUnOmShgtXpsfPrlbhMbcNpSpI92eb95e3OXYs1Tl1BP47ScdETDHa10Q_TK_dvriew4wnJpI53pK_eKPZ8sq8wIOsfTvi5rLw5nENnKnnqou616GGdsRt9vcfVIAEVmEdwHCQ?expires=1760238000&signature=23bcaee3155e1c8a9d9053b6ef6395f9b79e110bdec61d9ba5e0388d9b882af2&req=dSMgEMp%2BlIBfWvMW3Hu4gcGgQkiqFynYC0jA8vXkcHky1nVa4L9QOBFSCR69%0A2Q%3D%3D%0A)) icon of the Meta Business card. A drop-down menu is displayed.

  3. Select the **View Members** option from the menu. The business hub details page is displayed with the **Users** tab activated.

  4. Activate the **Unmatched users** tab in the **User Overview** section.

  5. Auto-claim the **Owner** role on the business hub by completing the following steps:

     1. Click the **Match user** button that is displayed when you hover over the corresponding user from the table. The **Match user** dialog box is displayed.

     2. Enter your username or email address in the **Match with** search bar. A list of users that match your search is displayed.

     3. Select the corresponding option from the list.

     4. Click the **Next** button. The **Select Cerby role** dialog box is displayed.

     5. Select the **Owner** option from the drop-down menu.

     6. Click the **Match user** button. The dialog box closes, and a success message box is displayed.

{% hint style="info" %} **NOTE:** To verify that you have the correct roles,
activate the **Onboarded** users tab in the **User Overview** section. The
**Owner** and **Admin** roles must be displayed in the **Cerby Role** and
**App access** columns for your Cerby account. {% endhint %}

The next step is 8\. Manage unmatched users.

## 8\. Manage unmatched users

During a check for updates, Cerby automatically matches app members to the
Cerby user accounts that correspond to their email addresses, including
existing [guest users](https://help.cerby.com/en/articles/8392946-explore-
guest-users), [local
partners](https://help.cerby.com/en/articles/8980877-explore-
partners#h_7e4add33a2), and [native
partners](https://help.cerby.com/en/articles/8980877-explore-
partners#h_e7fa9c355c). Manual matching is required when apps don't provide
email addresses and for app members using personal or external accounts that
couldn’t be identified or are not in the corporate directory.

To view the status of the imported app members, you must complete the
following steps:

  1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.

  2. Click the **More options** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1376309103/ce732ce8cd0407784ebc8e5928e7/AD_4nXfXuUnOmShgtXpsfPrlbhMbcNpSpI92eb95e3OXYs1Tl1BP47ScdETDHa10Q_TK_dvriew4wnJpI53pK_eKPZ8sq8wIOsfTvi5rLw5nENnKnnqou616GGdsRt9vcfVIAEVmEdwHCQ?expires=1760238000&signature=23bcaee3155e1c8a9d9053b6ef6395f9b79e110bdec61d9ba5e0388d9b882af2&req=dSMgEMp%2BlIBfWvMW3Hu4gcGgQkiqFynYC0jA8vXkcHky1nVa4L9QOBFSCR69%0A2Q%3D%3D%0A)) icon of the corresponding business hub card. A drop-down menu is displayed.

  3. Select the **View Members** option from the menu. The business hub details page is displayed with the **Members** tab activated.  
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

  5. Select the role to assign to the user on the business hub **Cerby role** drop-down menu:

     * **Owner:** This role enables sharing access and managing business hub settings in Cerby.

     * **Collaborator:** This role enables only logging in to the app from Cerby.

  6. Click the **Match user** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Onboarded** **users** tab.

### **Remove unmatched users**

To remove unmatched users, you must complete the following steps from the
**Unmatched users** tab of the business hub details page:

{% hint style="danger" %} **IMPORTANT:** When removing an unmatched user,
Cerby performs an automated task to revoke the user’s seat and permissions in
Meta Business Manager. {% endhint %}

  1. Click the **More options** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1376309103/ce732ce8cd0407784ebc8e5928e7/AD_4nXfXuUnOmShgtXpsfPrlbhMbcNpSpI92eb95e3OXYs1Tl1BP47ScdETDHa10Q_TK_dvriew4wnJpI53pK_eKPZ8sq8wIOsfTvi5rLw5nENnKnnqou616GGdsRt9vcfVIAEVmEdwHCQ?expires=1760238000&signature=23bcaee3155e1c8a9d9053b6ef6395f9b79e110bdec61d9ba5e0388d9b882af2&req=dSMgEMp%2BlIBfWvMW3Hu4gcGgQkiqFynYC0jA8vXkcHky1nVa4L9QOBFSCR69%0A2Q%3D%3D%0A)) icon of the corresponding user. A drop-down menu is displayed.

  2. Select the **Remove user** option from the menu. The **Remove user?** dialog box is displayed.

  3. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from the app via an automated task.

### **Exempt unmatched users**

Exempted users keep their user accounts or seats active in your app, but you
cannot manage them through Cerby.

To exempt unmatched users, you must complete the following steps from the
**Unmatched users** tab of the business hub details page:

  1. Click the **More options** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1376309103/ce732ce8cd0407784ebc8e5928e7/AD_4nXfXuUnOmShgtXpsfPrlbhMbcNpSpI92eb95e3OXYs1Tl1BP47ScdETDHa10Q_TK_dvriew4wnJpI53pK_eKPZ8sq8wIOsfTvi5rLw5nENnKnnqou616GGdsRt9vcfVIAEVmEdwHCQ?expires=1760238000&signature=23bcaee3155e1c8a9d9053b6ef6395f9b79e110bdec61d9ba5e0388d9b882af2&req=dSMgEMp%2BlIBfWvMW3Hu4gcGgQkiqFynYC0jA8vXkcHky1nVa4L9QOBFSCR69%0A2Q%3D%3D%0A)) icon of the corresponding user. A drop-down menu is displayed.

  2. Select the **Exempt user** option from the menu. The exempt user dialog box is displayed.

  3. Enter a reason for exempting the user in the **Provide a reason** field.

  4. Click the **Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

* * *

# **Use your business hub**

The following are the supported features of business hubs you can use:

  * [Join Meta Business Manager and connect your profile and account to Cerby](https://help.cerby.com/en/articles/9082571-join-meta-business-manager-and-connect-your-profile-and-account-to-cerby)

  * [Add users to your app via a business hub](https://help.cerby.com/en/articles/9045790-invite-new-app-members)

  * [Provision users to your apps via an IdP and business hub](https://help.cerby.com/en/articles/11040540-provision-users-to-your-apps-via-an-idp-and-business-hub)

  * [Remove users from your app via a business hub](https://help.cerby.com/en/articles/9046186-remove-app-members)

  * [Remove teams from your app via a business hub](https://help.cerby.com/en/articles/11038640-remove-teams-from-your-app-via-a-business-hub)

  * [Deprovision users from your apps via an IdP and business hub](https://help.cerby.com/en/articles/11040570-deprovision-users-from-your-apps-via-an-idp-and-business-hub)

  * [Update user roles in your app via a business hub](https://help.cerby.com/en/articles/9046201-update-the-app-members-roles)

  * [Update user roles in your apps via an IdP and business hub](https://help.cerby.com/en/articles/11040590-update-user-roles-in-your-apps-via-an-idp-and-business-hub)

  * [Sync your app users with your business hub](https://help.cerby.com/en/articles/9046205-check-for-updates-in-your-app-and-apply-report)

  * [Protect your app user accounts via a business hub](https://help.cerby.com/en/articles/9046212-protect-your-app-user-accounts-via-a-business-hub)

  * [Log in to your app via a business hub](https://help.cerby.com/en/articles/9046222-log-in-to-your-app)

  * [Track the activity of business hub users](https://help.cerby.com/en/articles/9046226-track-activity-on-app-members-user-accounts)

  * [Remove a business hub](https://help.cerby.com/en/articles/9046230-remove-an-app)

