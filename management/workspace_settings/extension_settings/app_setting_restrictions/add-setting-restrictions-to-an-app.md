---
description: "This article describes how to add password, member, or account restrictions to an app."
intercom_id: 10276341
---

# Add setting restrictions to an app

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super Admins** , and **Admins**
* Only supported using the Cerby web app
* Workspace users must have the Cerby browser extension installed and logged in


{% endhint %}

As a workspace **Owner** , **Super Admin** , or **Admin** , you can control how users change password and member settings and delete accounts in specific apps using the **[App setting restrictions](https://help.cerby.com/en/articles/10276184-explore-app-settings-restrictions)** feature.

To add an app and configure setting restrictions for it, you must complete the following steps:

1. Log in to your [Cerby](https://app.cerby.com/) workspace using the Cerby web app.
2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed with the **General** tab activated.
3. Activate the **Extension settings** tab.
4. Activate the left **App settings restrictions** tab.
5. Click the **Add app** button. A wizard is displayed with the list of apps you can add.
6. Select the app you want to add to the list. The **Set up restrictions for your app** page of the wizard is displayed.
**TIP:** You can use the search bar to find the app.

7. Select the setting you want to restrict from the left menu:
8. Activate the switch for the restriction in the main section of the wizard.
9. Select the restriction level for the setting:

   * **Fully block:** Cerby will block the password or member settings in the app, as well as account deletion, preventing any updates.
   * **Prompt users to Cerby:** Cerby will recommend users update the app’s password or user settings through Cerby while still enabling them to make the changes directly in the app, including account deletion.

10. Click the **Apply restrictions** button. The wizard closes, a success message box is displayed, and the selected app is added to the **App settings restrictions** list.

{% hint style="danger" %}


**IMPORTANT:** Take the following into consideration about this feature:

* Restrictions take five minutes to be applied in the app.
* Restrictions apply only to workspace **Users**. Workspace **Owners** , **Admins** , and **SuperAdmins** are unaffected by these restrictions.


{% endhint %}

Now you are done. Users will see error messages blocking them or recommending to use Cerby for any change in the app.

You can edit the message users see when attempting to change password or member settings and deleting accounts by following the instructions in the article [Customize the user message for setting restrictions](https://help.cerby.com/en/articles/10276389-customize-the-user-message-for-setting-restrictions).
