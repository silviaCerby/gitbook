# Explore the Cerby Suggest Discovery Report

**Description:** This article describes the key features of the Cerby Suggest Discovery Report.

{% hint style="info" %} **Who can use this feature?** * Workspace**Owners** ,
**Super Admins** , and **Admins** * Only supported using the Cerby web app *
Only available for Cerby Suggest {% endhint %}

As a workspace **Owner** , **Admin** , or **Super** **Admin** with [Cerby
Suggest](https://help.cerby.com/en/articles/8839657-explore-cerby-
suggest#h_fc8479cdc5) enabled, you can use the Discovery Report to gain
insights into user interactions. These interactions are captured by Cerby
Suggest when users engage with the dialog box shown while attempting to create
an account for a sanctioned app. The report collects data on all login and
signup events detected by Cerby Suggest based on the app domain or URL
visited. As a result, you can track and monitor application usage across your
organization, ensure compliance, and identify any potential gaps.

**Figure 1** shows an example of the information displayed in the Discovery
Report, which you can access in the left navigation drawer.

![](images/AD_4nXdMFXGyrfdyH5AgqDPiGG52xSn6K6L7WqtLp7tGtHJEcJ7UBoMWWD-u0Ku1rmWInsIw3A4C0qnMVXweNH3_P0PdoASrQ8X6jEDI2qPVZyvjr3oKgn_DfjjbZhuL4TKhf7GqW4NI)

**Figure 1. Discovery Report** view for Cerby Suggest in the Cerby web app
dashboard

The Discovery Report outlines the following columns:

  * **URL:** It is the specific URL of the app that the user visited to log in or sign up.

  * **Sanctioned:** It indicates whether the app the user visited is approved for use within the organization. The following criteria determine the app’s status:

    * **Sanctioned:** The app is approved for use within the organization, meaning it is licensed.

    * **Not sanctioned:** The app is not licensed by the organization and, therefore, not approved for use.

  * **Secure Status: It indicates whether the URL uses a secure connection.**

    * **Secure:** The URL uses HTTPS, ensuring a secure connection.

    * **Not secure:** The URL uses HTTP or another protocol, which is considered insecure.

  * **Logins:** It tracks the total number of times the user logged in to the specified app URL.

  * **Signups:** It tracks the total number of times the user attempted to sign up for the specified app URL.

This article describes how to perform the following actions in the Discovery
Report:

  * Access the Discovery Report

  * View the event details in the Discovery Report

  * Filter the events of the Discovery Report

  * Download a CSV file of the Discovery Report

The following sections contain the steps for each action.

* * *

# **Access the Discovery Report**

To access the Discovery Report, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Discovery Report** option from the left navigation drawer. The **Discovery report** view is displayed with the user events detected by Cerby Suggest.

Now you are done.

* * *

# **View event details in the Discovery Report**

To see the details of the events in the Discovery Report, you must complete
the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Discovery Report** option from the left navigation drawer. The **Discovery report** view is displayed with the user events detected by Cerby Suggest.

  3. (Optional) Filter the information of the Discovery Report as desired. For more information about how to filter the events in the report, read the Filter events in the Discovery Report section.

  4. Click the corresponding event in the report. A dialog box is displayed with more information about the event, as shown in **Figure 2**.

![](images/AD_4nXcl_AqS1HIwK_UqUiZMduqYUWaNwz6wafXwzw1qVnXbCJjn9G-JDe4rpdnsF2uMSUCzdaEeH663f5hZyKTgMZ7P8Q7SCaEaCjtcWVis3V321c3z3VP2qdc2eYXe46hXaK9dNrM3tg)

**Figure 2. Discovery Report** event details dialog box

  * The event details dialog box includes the following information:

    * **Date:** The date and time when the event occurred.

    * **Event:** A description of the specific action or event.

    * **Workspace Member:** The name of the workspace member who triggered the event.

    * **App Username:** The username that the workspace member used for the application involved in the event.

    * **Captured in Cerby:** The **Saved** or **Not Saved** status if the event data was tracked by Cerby.

  * To filter the information in the event details dialog box, you can select any of the following options in the top menu:

    * **Logins:** Filters the login events performed by users.

    * **Signups:** Filters the signup events performed by users.

    * **No. of Users:** Filters events by the number of unique users who performed the logins or signups within the selected time frame.

    * **Last 60 Days:** Filters events by the date they occurred:

      * **Last 24 hours**

      * **Last 7 days**

      * **Last 15 days**

      * **Last 30 days**

      * **Last 60 days**

  * To view the profile of the workspace member who performed the event, you must complete the following steps:

    * Click the **More options** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1394750848/64406a0b060cdd540c081e4f2a11/AD_4nXdQ_scyZWVIv7D_GOR5fOtvyBuARal2S8PJXWyV6jxRepVjygS7zYxaDEolWRltgcF-Z1RnXzXSxiOinloVkHQy71q423zB9ygGlCqisYGgSE-gDtve4MnwMYBLPWROZgexmRwZsA?expires=1740528000&signature=cabf4f4dab5fa838bd2f7e401c1d5598927705b2ae573b80307e87154b457356&req=dSMuEs57nYlbUfMW3Hu4gVV%2BzdtDfkXXAU53oNjdVhD7Yju9RnaNWWrIeQdd%0AIg%3D%3D%0A)) button. A drop-down menu is displayed.

    * Click the **Member profile** option. The workspace member details page is displayed.

Now you are done.

* * *

# **Filter events in the Discovery Report**

The **Discovery Report** view has a search bar and the following three filters
at the top of the page to refine the results displayed in the table:

  * **Date:** It specifies a time frame for which you want to view data in the Discovery Report. The default filter is **Last 60 days** , but you can select any of the following options:

    * **Last 24 hours:** Filters data for the last 24 hours.

    * **Last 7 days:** Filters data for the past 7 days.

    * **Last 15 days:** Filters data for the last 15 days.

    * **Last 60 days:** Filters data for the past 60 days. 

  * **Sanctioned and not sanctioned:** It distinguishes between applications that are approved and licensed for use within the organization (**Sanctioned**) and those that are not licensed or authorized (**Not Sanctioned**). The Discovery Report displays the information of both the sanctioned and not sanctioned apps by default.

  * **Secure and unsecure status:** It determines whether the URLs users visit are secure or not. **Secure** refers to URLs that use HTTPS, indicating an encrypted and protected connection, while **Unsecure** refers to URLs that use HTTP, which do not provide the same level of security. The Discovery Report displays the information of both the secure and unsecure status by default.

To filter events in the Discovery Report for Cerby Suggest, you must complete
the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Discovery Report** option from the left navigation drawer. The **Discovery report** view is displayed with the user events caught by Cerby Suggest.

  3. Filter the report using the following fields:

     * Sanctioned and not sanctioned

       1. Click the **Sanctioned and not sanctioned** field at the top menu. A drop-down menu is displayed.

       2. Select the apps you want to display on the Discovery Report using the following options:

          * **Sanctioned and not sanctioned**

          * **Sanctioned only**

          * **Unsanctioned only**

     * Secure and unsecure status

       1. Click the **Secure and unsecure status** field at the top menu. A drop-down menu is displayed.

       2. Select the apps you want to display on the Discovery Report using the following options:

          * **Secure and unsecure status**

          * **Secure status only**

          * **Unsecure status only**

The Discovery Report filters the information displayed according to the
selected filters.

Now you are done.

* * *

# **Download a CSV file of the Discovery Report**

To download a CSV file of the Discovery Report for Cerby Suggest, you must
complete the following steps:

**IMPORTANT:** This feature is temporarily unavailable in Cerby. The Cerby
team is working on restoring this known issue. If you need support, contact us
at [support@cerby.com](mailto:support@cerby.com).  
---  
  
  1. Log in to your [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Discovery Report** option from the left navigation drawer. The **Discovery report** view is displayed with the user events caught by Cerby Suggest.

  3. Click the **Download CSV** button at the top right of the page. The **Export Discovery report in CSV format** dialog box is displayed.

  4. Select the date range for the data you want to download in the **Date range** field:

     * **Last 24 hours**

     * **Last 7 days**

     * **Last 15 days**

     * **Last 60 days**

  5. Click the **Export CSV** button. When the report is ready to download, an email is sent to your address.

Now you are done.

