# Turn on and manage prompted account autosave in the workspace

**Description:** This article describes how to turn on and manage the Prompted autosave setting at the workspace level, applicable to all workspace users.

{% hint style="info" %} **Who can use this feature?** * Workspace **Super**
**Admins** and **Admins** * Only supported using the Cerby web app {% endhint
%}

As a workspace **Admin** or **Super Admin** , you can configure how users
capture new account credentials and specify the domains for which the browser
extension displays the **Add a new account to Cerby** dialog box.

With the **Prompted autosave** setting, Cerby detects login and signup
attempts on all or specific domains and prompts all workspace users to save
their accounts through the browser extension.

The following are the prompted account autosave settings you can manage:

  * Turn on Prompted autosave in the workspace

  * Manage the domains for Prompted autosave

  * Add a domain to Prompted autosave

  * Remove domains from Prompted autosave

{% hint style="danger" %} **IMPORTANT:** To learn how Cerby manages roles with
the account autosave feature, refer to the article [Explore Account
Autosave](https://help.cerby.com/en/articles/9500455-explore-account-
autosave#h_da5abb0156). {% endhint %}

* * *

# **Turn on Prompted autosave in the workspace**

To turn on the **Prompted autosave** setting in the workspace, you must
complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using the Cerby web app.

  2. Select the **Settings** option from the left menu. The **Workspace Configuration** page is displayed with the **General** tab activated.

  3. Activate the **Extension settings** tab. The **Prompted autosave** left tab is displayed activated.

  4. Activate the switch in the **Prompted account autosave for allowed and excluded domains** section to turn on the **Prompted autosave** setting for all workspace users. The following occurs:

     * A success message is displayed.

     * The information about the user who modified the setting, the date, and time is updated.

     * The **Select your domain preferences for the prompted account autosave** drop-down menu is displayed. This menu contains the options to configure the domains for which the Cerby browser extension displays the **Add a new account to Cerby** dialog box:

       * Autosave accounts for all domains

       * Autosave accounts only for allowed domains

       * Exclude domains from account autosave 

For more information, read the Manage the domains for Prompted autosave
section.

     * Depending on the option selected in the **Select your domain preferences for the prompted account autosave** drop-down menu, a field is displayed to search or enter the name of the apps to add to a list of allowed or excluded domains.

     * Depending on whether you have added allowed or excluded domains, these domains are listed below. 

Now you are done.

* * *

# **Manage the domains for Prompted autosave**

If the **Prompted autosave** setting is turned on in the workspace, you can
configure which domains Cerby will display the **Add a new account to Cerby**
dialog box. Therefore, users can choose to save their credentials as a new
account.

The following are the available options for managing this setting:

  * **Autosave accounts for all domains**

    * The Cerby browser extension will display the **Add a new account to Cerby** dialog box for all domains where any workspace user enters their login or signup credentials.

  * **Autosave accounts only for allowed domains**

    * The Cerby browser extension will display the **Add a new account to Cerby** dialog box only for the domains added to the list of allowed domains. To configure this list, read the following sections:

      * Add a domain to Prompted autosave

      * Remove domains from Prompted autosave

  * **Exclude domains from account autosave**

    * The Cerby browser extension will not display the **Add a new account to Cerby** dialog box for the domains added to the list of excluded domains. To configure this list, read the following sections:

      * Add a domain to Prompted autosave

      * Remove domains from Prompted autosave

**IMPORTANT:** If an app in the list of allowed or excluded domains is also
included in the **Enforced autosave** setting, the **Enforced autosave** chip
appears next to it. In this case, enforced autosave takes priority over
prompted autosave, and the account is saved automatically when a user logs in
or signs up for an account in that domain.  
---  
  
* * *

# **Add a domain for Prompted autosave**

After turning on the **Prompted autosave** setting and selecting the option to
allow or exclude domains, as described in the Manage the domains for Prompted
autosave section, you can start adding domains to their corresponding lists.

To add a domain for the **Autosave accounts only for allowed domains** or
**Exclude domains from account autosave** option, you must complete the
following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using the Cerby web app.

  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed with the **General** tab activated.

  3. Activate the **Extension settings** tab. The **Prompted autosave** left tab is displayed activated.

  4. Click the **Search for your app or type the domain** field.

  5. Enter the domain you want to add in the field. As you type, the search narrows down the results, updating the list of matches in real time.

  6. Select the domain you want to add. The domain is added to the allowed or excluded list below. 

  7. Repeat steps 4 to 6 as needed to add multiple domains.

Now you are done. If you added an allowed domain, Cerby will display the **Add
a new account to Cerby** dialog box the next time any workspace user logs in
or signs up for an account in this domain. If you added an excluded domain,
Cerby will display the dialog box for all domains, except for the one in the
excluded list.

* * *

# **Remove domains from Prompted autosave**

When you already have a list of allowed or excluded domains for the **Prompted
autosave** setting, you can remove them according to your organization's
needs.

To remove one or multiple domains from **Prompted autosave** , you must
complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using the Cerby web app.

  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed with the **General** tab activated.

  3. Activate the **Extension settings** tab. The **Prompted autosave** left tab is displayed activated.

  4. (Optional) Narrow down the list of domains to remove by using the following alternatives:

     * Search for the domain you want to remove from the list by clicking the **Search** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1583074957/11a12289e9edca60b5bd5b4d4601/AD_4nXdCucIpuKmNZafxWwBGlkSOtnM9DIyfyiGS0u4JKpDgF6em4WvtDUtYlHEyQH014dZJo1ff7ggf72jdb-MMGnZHmmruiC7cgNsjmYON8F7yz-cQTFadOPY91ye_rTE4sBf5ugx7DQ?expires=1750734000&signature=30cb5c62b5971f2831cce1988eecde24d79d7983ff791cbd0d4387289a662acf&req=dSUvFcl5mYhaXvMW3Hu4gXk1DeJIIFj%2FYy51zvKMwDWojqCH10ouF%2B4%2FtK0U%0AEg%3D%3D%0A)) icon, which displays the search field. As you type, a list of all matches is displayed below in real time.

     * Sort the list by recently added, earlier added, A to Z, or Z to A by clicking the **Sort by** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1583075181/fbecde43eb19c6a89f7958ce4305/AD_4nXchqnoWDYc1wF-YCofu5x5SsAzIFY3zLpZCohiPWaGAYfpoRvDBnMomRfWpD1zhGGRJ97fGVDs7iwjUHfqcE4H9zT3npjEWCec26HuXfFpAT2WOj6TV4z88YEI0av7o_FBnLK_U?expires=1750734000&signature=d99a68eb93505b60ccd13a1e00f54e2e6bea724b35e0f722c2e6a8861c6300ba&req=dSUvFcl5mIBXWPMW3Hu4gWuAgbedpILxmy5591bKQxJlcYoeKeG1%2Fl7IQwe0%0ALg%3D%3D%0A)) icon next to the search field.

  5. Remove one or multiple domains as follows:

     * **One domain**

       1. Click the **Remove from list** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1583075452/cbd1c84ecbb0b245b5ff1a3d4927/AD_4nXftOD2LhC2Z6zRJ1CAKGbF4IQHpVI7gdS5VuGgI-x_4PuQ0vmtgj-me7R1BFilc34J-1U4E28xk1wASKxw5V_-fiBn8NVZR9hU1sbGTxzKjNiM1_dRuk3ZM5Ws2imRcmTgLmR9C?expires=1750734000&signature=a1810da532634dd0d35d33a5cf4a760e1d6de0adb542e0a08d7ef3f16c13c24c&req=dSUvFcl5mIVaW%2FMW3Hu4gR9hsYueMjsfPG73AA9gpjhY1Mn1W70Ie%2FBcfFHt%0AoA%3D%3D%0A)) icon on the right side of the domain name. A success message appears, and the domain is removed from the list.

     * **Multiple domains**

       1. Select the domains you want to remove from the list. A menu is displayed at the bottom of the page indicating the number of domains you have selected.

**TIP:** To deselect all domains, you have two alternatives in the menu at the
bottom: the **Deselect all** button and the **Close selection**
(![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1581084592/a1353a4e2e3124e1a749df7c69a9/AD_4nXcuUaDNGYU635FW5TAOTDGFJ0x_UH_MYFaSO8i7IcAG84WKYrsQ4bWTjIU7My3cyPXdszBfIf0lvUQMYMh8ebLcpxSKFzYp2PPBqQDinqdTeJtmf_XfPRLBtWJ2-fM_kuTds9CY?expires=1750734000&signature=d95ede45e0b4053150a6e1b478cadcc92e6622b8f39a06c45b76d8b74a93ab30&req=dSUvF8l2mYRWW%2FMW3Hu4gSb0Engn68WgBY%2F5XnDccOlycTwY3iFdOMWpCDNO%0AIg%3D%3D%0A)![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1583075713/a32b9542d646c483b25830ee6d27/AD_4nXfpcGdEFFgd5WkK8MloflB0rFAdY4BvxZo_o90gBBCJ1Fz5BfC42M4jKvQo1CMAL22mNVQT-
qecuFxV-
TIIo3yFms_klj0xX0vGaebFy8nycGwnavJnWSvCJ2Gn8IR_GgckpiOA?expires=1750734000&signature=e3703f8b9e4cb43311d7f1a857a14739b4574cc17083f38def4bd5ad7c5f47fb&req=dSUvFcl5mIZeWvMW3Hu4gbvOo8anXem0K9HEkd5RudnEDaJs%2BT24NACIP1aZ%0ALg%3D%3D%0A))
button, which also closes the menu.

       2. Click the **Remove from list** option in the menu at the bottom. A success message appears, and the selected domains are removed from the list. 

Now you are done.

