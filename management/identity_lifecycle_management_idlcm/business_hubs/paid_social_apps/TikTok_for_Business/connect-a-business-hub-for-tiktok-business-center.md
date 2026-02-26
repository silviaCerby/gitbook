---
description: "This article describes how to connect a business hub to centrally manage users and assets of TikTok Business Center from Cerby."
intercom_id: 6273647
---

# Connect a business hub for TikTok Business Center

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* Only supported using the Cerby web app


{% endhint %}

As a user with any workspace role in Cerby, except **Guest User** and **Login-Only** , you can connect a business hub integration to centrally manage the users and assets of your TikTok Business Center.

When you connect the business hub, you become its **Owner** , and you can perform the following user and access management tasks through automated tasks or API calls executed by the Cerby agent:

* Check for updates
* Add users
* Update user roles
* Remove users

**TIP:** For more details about the automated tasks of a business hub, how it works, and the supported apps, read the article [Explore Business Hubs](https://help.cerby.com/en/articles/6831152-explore-apps).
---

Additionally, you can perform the following actions to manage access to your TikTok Business Center for external collaborators:

* Invite users to your workspace as[ guest users](https://help.cerby.com/en/articles/8392946-how-to-invite-a-guest-user-to-your-workspace) or[ local partners](https://help.cerby.com/en/articles/8980877-explore-partners#h_7e4add33a2), with secure credentials provided and managed by Cerby.
* Connect a[ native partner](https://help.cerby.com/en/articles/8980877-explore-partners#h_e7fa9c355c) to your workspace to gain visibility into the partner’s users with shared access to the assets of your TikTok Business Center. For more information, read the article [Connect a TikTok for Business native partner to Cerby](https://help.cerby.com/en/articles/9082765-connect-a-tiktok-for-business-native-partner-to-cerby).

This article provides instructions on how to connect a business hub for TikTok Business Center. For other app-specific articles and videos, review the[ Connecting business hubs for your apps](https://help.cerby.com/en/collections/10289415-connecting-your-apps) and[ Connecting business hubs for your paid social apps](https://help.cerby.com/en/collections/12330234-connecting-business-hubs-for-your-paid-social-apps) collections in the Cerby Help Center.

* * *

## Requirements

The following are the requirements to connect a business hub:

  * A Cerby workspace
  * A Cerby user account with the workspace **Owner** , **Super Admin** , **Admin** , or **User** role
  * A collaboration space (workspace, team, or dashboard) in TikTok Business Center
  * Groups configured in your identity provider (IdP) if you want to leverage automatic user provisioning and deprovisioning from your apps based on group assignment events. For more information, read the article [Manage app members from your IdP](https://help.cerby.com/en/articles/9046188-manage-app-members-from-your-idp)
  * An automation account, meaning an active user account with a native **Admin** role in your TikTok Business Center to be used as a service account. For instructions and recommendations on how to create and configure this account, read the article [Create a service account for your business hub](https://help.cerby.com/en/articles/9830816-create-an-automation-or-service-account-for-your-business-hub)
  * The user management and login method for your business hub identified to select the corresponding option when connecting your app. For more information, read the **User management and login method** section of the article [Explore Business Hubs](https://help.cerby.com/en/articles/6831152-explore-apps)
  * A business ID. You can find the ID in the following ways:
    * **In the address bar:** When you are logged in to your TikTok Business Center, the ID is displayed in the address bar as part of the URL. It’s the number that comes after **`org_id=`**. For example, **`8453921765042398123`** in **`https://business.tiktok.com/manage/overview?org_id=845392176504239812`3**. Copy the value and paste it when connecting the business hub.
    * **In the business settings:** When you are logged in to your TikTok Business Center, select the **Business setting** option from the left menu. The ID is displayed in the **Business Center Information** section below the name of your business center, as shown in **Figure 1**.

<img src="../../../../../../.gitbook/assets/33ec24d4-6181-4b0e-97ff-685e43f79746.png" alt="">

**Figure 1. ID** in the **Business Center Information** section

  * Your browser must be configured to allow pop-ups. Follow the corresponding instructions to allow pop-ups:
    * [Google Chrome](https://support.google.com/chrome/answer/95472?hl=en)
    * [Microsoft Edge](https://support.microsoft.com/en-us/search?query=allow%20pop%20ups%20in%20edge)
    * [Mozilla Firefox](https://support.mozilla.org/en-US/kb/pop-blocker-settings-exceptions-troubleshooting)
    * [Safari](https://support.apple.com/guide/safari/block-pop-ups-sfri40696/mac)
* * *

## Connect a business hub for TikTok Business Center

To connect a business hub for TikTok Business Center, you must complete the following main steps from the Cerby web app dashboard:

  1. [Add a business hub and connect it to your TikTok Business Center](connect-a-business-hub-for-tiktok-business-center.md#h_52a57de538)
  2. [Check for updates to import users, roles, and assets to Cerby](connect-a-business-hub-for-tiktok-business-center.md#h_5aac0a4fdb)
  3. [Connect your TikTok Business Center user account to the business hub](connect-a-business-hub-for-tiktok-business-center.md#h_7c31e445e9)
  4. [Auto-claim the Owner role in Cerby](connect-a-business-hub-for-tiktok-business-center.md#h_4b3077f446)
  5. [Manage unmatched users](connect-a-business-hub-for-tiktok-business-center.md#h_2f57ad164a)

The following sections describe each main step.

### 1\. Add a business hub and connect it to your TikTok Business Center

To add a business hub and connect it to your TikTok Business Center, you must complete the following steps:

{% hint style="danger" %}


**IMPORTANT:** Make sure you are logged in to your TikTok For Business account in a separate tab within the same web browser window. Cerby identifies this account to connect your TikTok Business Center to the Cerby Asset Manager through the **App Authorization | TikTok For Business pop-up** window in steps 5 and 6.


{% endhint %}

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
  3. Click the **Connect Business Hub** button located at the top-right corner of the page. The **Connect your Business Hubs to Cerby** dialog box is displayed.
​**TIP:** Select the **Don’t show this again** option to skip this step the next time you connect a new business hub.

  4. Click the **Get started** button. A wizard is displayed on the **Select app** page.
  5. Select **TikTok Business** from the catalog. The **Grant access to Cerby** page is displayed on the wizard with the **App Authorization | TikTok for Business** pop-up window on top, as shown in **Figure 2**.

<img src="../../../../../../.gitbook/assets/0FVFAb1a0_3uSitn-_o0yP-4wVMpXogHaoKMJikMlwEo7s5OJBaEJhAcSMQs3ymYlRnmeIP_IxGvRFX5KnIH4jlTZ2km52RKBNxAVeji0b8aO620gKlqIwbDw_C9ag5z3X7kPlf_3xAySQyey2Ma9Gg.png" alt="">

**Figure 2. App Authorization | TikTok for Business** pop-up window
​

  6. Click the **Confirm** button. A success message is displayed, and the pop-up window closes automatically.
  7. Click the **Next** button. The **Enter app details** page is displayed on the wizard.
  8. Enter and select your app information in the corresponding fields:

     * **Label in Cerby: It is the name to assign to your business hub in Cerby, and it will be displayed on the business hub card.**
     * **Business ID:** It is the unique identifier of your TikTok Business Center. For instructions on how to find it, read the [Requirements](https://docs.google.com/document/d/1HIw9bVSBwpQ8ESYOJVY-lFv_3tK1lfaO-KQv_jJ_Yhs/edit?tab=t.0#heading=h.wxmv4kvterhj) section.
     * **Password:** It is the password retrieved by Cerby when detecting your active session and granting access to the Cerby Asset Manager app.
​**IMPORTANT:** Don’t change the prefilled value in this field.

     * **User management and login method:** It is the way your users log in to the app and determines whether they must save their login credentials as a Cerby account connected to the business hub. You must select one of the following methods:
       * **Single sign-on (SSO):** Access is managed by your IdP, and users log in with SSO authentication. They are not asked to save their credentials in Cerby.
       * **Username and password:** Cerby manages account security and access, and users log in with their credentials after saving them in Cerby.

  9. Click the **Connect app** button. The wizard closes, and a success message box is displayed.
The corresponding business hub is also displayed on the **Business Hubs** view.

The next step is [2. Check for updates to import users, roles, and assets to Cerby](connect-a-business-hub-for-tiktok-business-center.md#h_5aac0a4fdb).

### 2\. Check for updates to import users, roles, and assets to Cerby

To check for updates in your app to identify and import users, roles, and assets to Cerby, you must complete the following steps:

  1. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
  2. Click the **More options** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1772455934/3e6592a0a24db234537ce37606b1/80c660ea-931a-4a5c-9c75-87e91bb2a0ef?expires=1760238000&signature=662f24e2997595a04461562ce98ffcf0d1cba1f69834de900a3051ea12741955&req=dScgFM17mIhcXfMW3Hu4gTTZfzN%2BUACCDMvuvPfLf0RdfO22DxbLTLXF5RUz%0AuQ%3D%3D%0A" alt="">) icon of the corresponding business hub card. A drop-down menu is displayed.
  3. Select the **Settings** option from the menu. The business hub details page is displayed with the **Settings** tab activated.
  4. Click the **Sync** button located at the top right of the page. A message box is displayed with information about the process.
​**NOTE:** The check and import process may take a few minutes, depending on the number of users and assets, and because Cerby automatically matches users to their corresponding Cerby user accounts.

  5. Confirm that the automated task to check for updates has the “Completed” status by performing any of the following actions:

     * Click the **More details** button in the message box.
     * Select the **Automation** option from the left menu to open the **Automation** page with a list of automated tasks and their status.

     **NOTE:** Cerby automatically performs daily checks for updates for all business hubs, but you can trigger them manually, as described in this section. For more instructions, read the article Sync your app users with your business hub.

The next step is [3. Connect your TikTok Business Center user account to the business hub](connect-a-business-hub-for-tiktok-business-center.md#h_7c31e445e9).

### 3\. Connect your TikTok Business Center user account to the business hub

To connect your TikTok Business Center user account to the business hub so Cerby can manage and protect it, you must complete the following steps:

  1. Select the **Accounts** option from the left menu. The **All accounts** page is displayed.
  2. Click the **Log in** button of the corresponding TikTok Business account card. The **Connect your TikTok Business Account** dialog box is displayed.
  3. Enter the login credentials of your TikTok Business Center user account.
  4. Click the **Connect account** button. The dialog box closes, and a success message box and a new account card are displayed.

The next step is [4. Auto-claim the Owner role in Cerby](connect-a-business-hub-for-tiktok-business-center.md#h_4b3077f446)

### 4\. Auto-claim the Owner role in Cerby

When your Cerby account has a different email than your TikTok profile, the integration does not automatically match the **Owner** role in Cerby with the **Admin** role in your TikTok Business Center. Therefore, you must manually claim ownership.

To claim the **Owner** role for your business hub, you must complete the following steps:

  1. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
  2. Click the **More options** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1772455603/17de17d78a636821249776964ca6/3133e98f-8bdd-479e-889e-b3ffa0300220?expires=1760238000&signature=14a2c071c57837419ba5c648e4182e4325482e843fae029aa41f35ecf9f89ba4&req=dScgFM17mIdfWvMW3Hu4gfJGJNipDAzvRP66XOI9zoaiOxviXUN9aReGXYnA%0ATA%3D%3D%0A" alt="">) icon of the corresponding business hub card. A drop-down menu is displayed.
  3. Select the **View Members** option from the menu. The business hub details page is displayed with the **Users** tab activated.
  4. Activate the **Unmatched** users tab from the**User Overview** section.
  5. Auto-claim the **Owner** role on the TikTok Business integration by performing the following actions:
    1. Click the **Match user** button that is displayed when you hover over the corresponding user in the table. The**Match user** dialog box is displayed.
    2. Enter your username or email address in the **Match with** search bar. A list of users that match your search is displayed.
    3. Select the corresponding option from the list.
    4. Click the **Next** button. The **Select Cerby role** dialog box is displayed.
    5. Select the **Owner** option from the role drop-down list.
    6. Click the **Match user** button. The dialog box closes, and a success message box is displayed.

{% hint style="info" %}


**NOTE:** To verify that you have the correct roles, activate the **Onboarded** **users** tab from the **User Overview** section. The **Owner** and **Admin** roles must be displayed in the **Cerby role** and **App access** columns for your Cerby account.


{% endhint %}

The next step is [5\. Manage unmatched users](https://docs.google.com/document/d/1oeSbrLoewVWqUOFaoHXdoAK4LSFLIXW-TpUL5G_bYYE/edit#heading=h.xnn3mvf6dst8).

### 5\. Manage unmatched users

During a check for updates, Cerby automatically matches app members to the Cerby user accounts that correspond to their email addresses, including existing [guest users](https://help.cerby.com/en/articles/8392946-explore-guest-users) and [local partners](https://help.cerby.com/en/articles/8980877-explore-partners#h_7e4add33a2). Manual matching is required when apps don't provide email addresses and for app members using personal or external accounts that couldn’t be identified or are not in the corporate directory.

To view the status of the imported app members, you must complete the following steps:

  1. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
  2. Click the **More options** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1772455782/dfb9ca445a9deb4c9fc1f5907753/b4c4f12a-922d-4db1-889b-994001bebc76?expires=1760238000&signature=ad265f1ed44512a615beb4f4721e1779bf860060d04b501121e652af69bca2f2&req=dScgFM17mIZXW%2FMW3Hu4gSPstEMgzyc3U%2F%2FKcttC5H%2BDr8iPXOIM1%2B%2FAKWO3%0Anw%3D%3D%0A" alt="">) icon of the corresponding business hub card. A drop-down menu is displayed.
  3. Select the **View Members** option from the menu. The business hub details page is displayed with the **Members** tab activated.
App members are displayed in the following tabs of the **User Overview** section:

     * **Unmatched users:** This tab displays the users who were not automatically matched.
     * **Onboarded users:** This tab displays the users matched to their Cerby user account.
     * **Guest users:** This tab displays the users who were matched to an existing Cerby user account, but don’t exist in the corporate directory, such as external collaborators.

For unmatched users, you can perform one of the following actions:

  * [Match users](connect-a-business-hub-for-tiktok-business-center.md#h_535e23f0db)
  * [Remove unmatched users](connect-a-business-hub-for-tiktok-business-center.md#h_96e082cfa2)
  * [Exempt unmatched users](connect-a-business-hub-for-tiktok-business-center.md#h_04fe2717d5)

The following sections describe each action.

#### Match and invite users

To match users, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

  1. Click the **Match user** button of the corresponding user. The **Match user** dialog box is displayed.
  2. Enter the username or email address of the user you want to match and invite in the **Match with** field. The user is displayed on a list.
  3. Select the user from the list.
  4. Click the **Next** button. The **Select Cerby role** dialog box is displayed.
  5. Select the role to assign to the user on the business hub **Cerby role** drop-down menu:

     * **Owner:** This role enables sharing access and managing business hub settings in Cerby.
     * **Collaborator:** This role enables logging in to the app from Cerby only.

  6. Click the **Match user** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Onboarded** **users** tab.

#### Remove unmatched users

To remove unmatched users, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

**IMPORTANT:** When removing an unmatched user, Cerby performs an automated task to revoke the user’s seat and permissions in your TikTok Business Center.
---

  1. Click the **More options** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1772455934/3e6592a0a24db234537ce37606b1/80c660ea-931a-4a5c-9c75-87e91bb2a0ef?expires=1760238000&signature=662f24e2997595a04461562ce98ffcf0d1cba1f69834de900a3051ea12741955&req=dScgFM17mIhcXfMW3Hu4gTTZfzN%2BUACCDMvuvPfLf0RdfO22DxbLTLXF5RUz%0AuQ%3D%3D%0A" alt="">) icon of the corresponding user. A drop-down menu is displayed.
  2. Select the **Remove user** option from the menu. The **Remove user?** dialog box is displayed.
  3. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from the app via an automated task.

#### Exempt unmatched users

Exempted users keep their user accounts or seats active in your app, but you cannot manage them through Cerby.

To exempt unmatched users, you must complete the following steps from the **Unmatched users** tab of the business hub details page:

  1. Click the **More options** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1772456044/e2715a827d3eb221ef4bb34ec253/c553b00c-cbe7-42e7-98c8-8012a22b8e6f?expires=1760238000&signature=1c25b298ddff9511e815cdea42e44cac9826ae2b639a2e895219388132b468fa&req=dScgFM17m4FbXfMW3Hu4gQJBT1EbZtSB9CgVBeU8N1%2FV3NnPxaKXQIvgrOIO%0Aqg%3D%3D%0A" alt="">) icon of the corresponding user. A drop-down menu is displayed.
  2. Select the **Exempt user** option from the menu. The exempt user dialog box is displayed.
  3. Enter a reason for exempting the user in the **Provide a reason** field.
  4. Click the **Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

* * *

## Use your business hub

The following are the supported features of business hubs you can use:

  * [Join TikTok for Business and connect user account to Cerby](https://help.cerby.com/en/articles/9082605-join-tiktok-tiktok-for-business-and-connect-user-account-to-cerby)[Add users to your app via a business hub](https://help.cerby.com/en/articles/9045790-invite-new-app-members)
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
