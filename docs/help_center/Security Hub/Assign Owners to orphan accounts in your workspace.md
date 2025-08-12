# Assign Owners to orphan accounts in your workspace

**Description:** This article describes how to assign Owners to orphan accounts in your workspace through the Security Hub.

{% hint style="info" %} **Who can use this feature?** * Workspace**Owners** ,
**Super Admins** , and **Admins** * Only supported using the Cerby web app {%
endhint %}

In Cerby, an **orphan account** is an account that remains active even though
it no longer belongs to an active workspace member, meaning that there’s no
valid Owner assigned to it. For example, if a workspace member is
deprovisioned from the workspace and is the **Owner** of an account, the
account becomes an orphan.

Orphan accounts can pose a security risk if overlooked, as they still hold
access privileges without being actively monitored.

As a workspace **Owner** , **Super Admin** , or **Admin** , you can quickly
identify all orphan accounts in the workspace through the Security Hub and
proactively assign one or more Owners to them. Additionally, by not having
Owners, the following account management capabilities are lost in Cerby:

  * Sharing or removing access from the account.

  * Updating the account settings.

  * Managing account security, such as multi-factor authentication (MFA) and password rotations.

  * Monitoring user events through the [Activity](https://help.cerby.com/en/articles/10128402-explore-activity) view.

{% hint style="danger" %} **IMPORTANT** : There is a known issue where an
account is still considered orphaned if no active user in the workspace is
assigned as the **Owner** , even when one or more teams have access to that
account. {% endhint %}

* * *

# Assign Owners to orphan accounts in your workspace

To assign one or more **Owners** to orphan accounts in your workspace, you
must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Security Hub** option from the left navigation drawer. The **Security Hub** view is displayed.

  3. Click the **Assign Owners** option in the **Workspace health** section. The **Orphan accounts** page is displayed with information about orphan accounts.

  4. Select one or multiple orphan accounts to assign one or more Owners:

     * For one account:

       1. Click the **More options** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1385894653/95763be04b27bc4c8fcf148ca6fb/AD_4nXe7Ju9hvw5Y74CVQRrHM6njSFTz5B4CJf-eUMzGj86tV3DwSUGImCvf5K7stjKMnpgAisTsmI-wEbaoQiBapjX9DbLxnBc7dzzUeszJYecXJmWvdhzRcYdKIo6sCz7s-L8mOj-N?expires=1743768000&signature=10c2646c97c226e420f6b1cb26b778ae8071122717db97c5d690b014adc842a3&req=dSMvE8F3mYdaWvMW3Hu4gTn7nCUfhb5Ikmjx%2F3neWSHZPuP6FdkzcjIDyK9r%0Ajw%3D%3D%0A)) icon at the right of the orphan account. A drop-down menu is displayed.

     * For multiple accounts:

       1. Select the orphan accounts using the checkboxes at the left of the account names. A menu is displayed at the bottom of the page indicating the number of orphan accounts you have selected.   
​**IMPORTANT:** You can only select 20 accounts at a time.

  5. Select the **Assign Owner** option. The **Assign Owner** dialog box is displayed.

     1. Enter the name of the member in the search bar. The members that match the name are displayed on a list automatically.

     2. Select the corresponding member from the list. The member is listed in the field.

     3. Repeat steps a and b as necessary to select multiple members.

**IMPORTANT:** Only 20 workspace members can be assigned as **Owners** at a
time.

  6. Click the **Next** button. The **Assign account Owners** dialog box is displayed.

  7. (Optional) Write a custom message in the **Message** field to the members who will be assigned as **Owners**.

  8. Click the **Assign Owners** button. The assigned Owners receive an email notifying them of their assignment. A success message is displayed, and the selected orphan accounts are removed from the list.

Now you are done.

* * *

# **Understand the temperature widget for the orphan accounts**

A temperature widget is placed at the top right corner of the **Orphan
accounts** page, as shown in **Figure 1**.

![](gitbook/imagesAD_4nXesvYUowBGu9XBevH4ImtSm9lsWCBxEupHS9NpTRmWDYUv2bFoguAZUQXKnfE7lHkKV-
pXGOXSU_KUq7DMeduf2g0Sj_T16QPZKkuadO2JqZcFLEyR4IaNkolDD5Wihhs3A0uQ_)

**Figure 1**. The **Temperature widget** is located at the top right corner of
the **Orphan accounts** page

The characteristics of the temperature widget for orphan accounts are the
following:

  * **Color-coded:** The widget displays a range of colors that represent the volume and severity of orphaned accounts. The colors represent the following:

    * `Green` means zero accounts are orphaned

    * `Yellow` means less than five accounts are orphaned

    * `Orange` means less than 10 accounts are orphaned

    * `Red` means more than or equal to 10 accounts are orphaned

  * **Real-time data:** As new orphaned accounts are detected or existing ones get assigned an Owner, the temperature widget updates automatically. 

  * **Thresholds and alerts:** The widget provides a quick visual gauge of the number of orphaned accounts and the relative risk they pose to your workspace. If the number of orphaned accounts exceeds a defined safe limit, the widget shifts to a higher temperature, signaling the need for attention.

* * *

# **View the Owner assignations for orphan accounts in the Activity view**

You can track when orphan accounts have been assigned to an **Owner** through
the **[Activity](https://help.cerby.com/en/articles/10128402-explore-
activity)** view in Cerby using the following filter in the **Event** field:

  * Account Owner Assigned

To learn more about the events in the **Activity** view and how to filter
them, refer to the following articles:

  * [Filter events in the Activity view](https://help.cerby.com/en/articles/10128410-filter-events-in-the-activity-view)

  * [Monitor events in the Activity view](https://help.cerby.com/en/articles/10128426-monitor-events-in-the-activity-view)

