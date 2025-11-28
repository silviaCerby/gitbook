# Add settings restrictions to an app

**Description:** This article describes how to add password or member settings restrictions to an app.

{% hint style="info" %} **Who can use this feature?** * Workspace **Owners** ,
**Super Admins** , and **Admins** * Only supported using the Cerby web app *
Workspace users must have the Cerby browser extension installed and logged in
{% endhint %}

To add an app to the **App settings restrictions** list for setting
restrictions, you must complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace using the Cerby web app.

  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed with the **General** tab activated.

  3. Activate the **App settings restrictions** tab. 

  4. Click the **Add app** button. A wizard is displayed with the **Add an app to apply settings restrictions** page and the list of apps you can add.

  5. Select the app you want to add to the list. The **Set up restrictions for your app** page of the wizard is displayed. 

**TIP:** You can use the search bar to find the app.

  6. Select the setting you want to restrict in the left menu.

  7. Activate the switch in the **Restrict password settings** section, as shown in **Figure 1**. 

![](images/AD_4nXc3tBuGC1cKYA01OWrnnqDKzAnuZmw-W0DV6TffNtN-
Ay_M5ILKH2uGQacXHMqhvh2jV9P_BqMIpDCpLyO2Uk49b9SZnmNq6_n1vJmSaSghP1oJuHacwbwSIwD84fY8KJAABozaCQ)

**Figure 1. Set up restrictions for you app** page of the wizard with the
options to restrict password or member settings

  8. Select the restriction level for the setting: 

     * **Fully block:** Cerby will block the password or user settings in the app, preventing any updates.

     * **Monitor and prompt to Cerby:** Cerby will recommend users update the app’s password or user settings through Cerby while still enabling them to make the changes directly in the app.

  9. Click the **Apply restrictions** button. A success message appears, and the selected app is added to the **App settings restrictions** list. 

**IMPORTANT:** Restrictions take five minutes to apply in the app and apply
only to workspace **Users**. Workspace **Owners** , **Admins** , and **Super**
**Admins** are unaffected by these restrictions.

Now you are done. Users will see an error message restricting them from
modifying the setting or an information message recommending they use Cerby
for any modification. You can modify the message users see when attempting to
modify the setting by following the steps in the article [Customize the user
message for setting
restrictions](https://help.cerby.com/en/articles/10276389-customize-the-user-
message-for-setting-restrictions).

