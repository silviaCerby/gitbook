---
description: "This article describes the information of the Users tab for a business hub."
intercom_id: 10971965
hidden: true
noIndex: true
---

# View the users of your business hub

{% hint style="info" %}


**Who can use this feature?**

* Business hub **Owners** and**Managers**
* Only supported using the Cerby web app


{% endhint %}

As a business hub **Owner** or**Manager,** you**** can manage and protect your external app users directly from the **Users** tab in your business hub integration. This tab provides a centralized view of all users and teams with access to your app, enabling you to perform the following tasks:

* Add users and teams to your app
* Remove users and teams from your app
* Update user roles
* Protect your user accounts
* Match and exempt users
* Download the list of users in a CSV file

The **Users** tab, as shown in **Figure 1** , groups users and teams into two independent tables, each with relevant details to help you manage access efficiently.

<img src="../../../../../.gitbook/assets/image_22.png" alt="">

**Figure 1. Users** tab in the business hub details page

The **Users** table provides information about external app users in the following columns:

* **User:** It lists the username and email of the Cerby user accounts matched with the app user accounts. This column is empty for**** unmatched**** users**.**
* **Username in <app>:** It lists the username given to the users in the external app.
* **< app> access:** It lists the roles assigned to the users in the external app.
​**IMPORTANT** : If the user has been granted multiple roles, click the **More** **options** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1445341684/73027a843c233f57eee8672cdfcc/AD_4nXe9QT7Gj8ToQ6w0LHL_tpUxLgGYGB-OYi697c9cYbePkGOzoelBjbWdTLX6n8S6M-zH9t5jj_6AGkcbFxGsQo80xwKGHJP9EA26QXN2H_d2cxAXysEYhUbPal7qCR8qoifoVlS3?expires=1747170000&signature=e487d978220de26749eee7b96f6862867afb937763729a90875073e47f214450&req=dSQjE8p6nIdXXfMW3Hu4gdr24cpOtB48XZaSPbXgBkRFtXiL7CgPNVMWo7rL%0A%2BQ%3D%3D%0A" alt="">) icon and select the **Overview** option to see the assigned role details.

* **Assets:** It indicates the number of assets assigned to the users in the external app.
​**NOTE:** If multiple assets have been assigned to a user, click the **More options**(<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1445341684/73027a843c233f57eee8672cdfcc/AD_4nXe9QT7Gj8ToQ6w0LHL_tpUxLgGYGB-OYi697c9cYbePkGOzoelBjbWdTLX6n8S6M-zH9t5jj_6AGkcbFxGsQo80xwKGHJP9EA26QXN2H_d2cxAXysEYhUbPal7qCR8qoifoVlS3?expires=1747170000&signature=e487d978220de26749eee7b96f6862867afb937763729a90875073e47f214450&req=dSQjE8p6nIdXXfMW3Hu4gdr24cpOtB48XZaSPbXgBkRFtXiL7CgPNVMWo7rL%0A%2BQ%3D%3D%0A" alt="">) icon and select the **Overview** option for the assets details.

* **Type:** It indicates the method by which the users were granted access to the external app. The possible values are the following:
  * **Individual** : The access was directly granted.
  * **< group name>:** The access was granted via a team.
  * **Multiple:** The access was granted by multiple sources.
* **Last used:** It is the date and time of the user's most recent activity.
* **Status:** It indicates the status of the users. The possible values are the following:
  * **Removed:** The user was removed from the app. The removal could be triggered by the identity provider (IdP), Cerby, or the app itself.
  * **Unmatched user:** The user was synced during a check for updates, but Cerby couldn't match it with a Cerby user account.
  * **Exempted:** The user was exempted from the business hub integration, meaning their account or seat remains active in the app but cannot be managed through Cerby.
  * **Inviting** : The user invite is queued or in progress.
  * **Pending invite claim:** The user needs to accept the invite to join the app.
  * **Awaiting user login:** The user needs to log in to the app and capture their credentials.
  * **Awaiting update:** The user’s update is queued or in progress.
  * **Pending user claim:** The user needs to claim access to the app.
  * **Invite expired:** The user invite has expired.
  * **Awaiting deprovisioning:** The user account deprovisioning is queued or in progress.
  * **Invite failed:** The process to send the user invite failed.
  * **Deprovisioning failed:** The user account deprovisioning failed.
  * **Update failed:** The user role update failed.
  * **Sync failed:** The check for updates failed for this user.

  **NOTE:** If the user has no status chip, it means they have been successfully onboarded, and Cerby has nothing to report.

Meanwhile, the **Teams** table provides information about the external app teams in the following columns:

* **External application team:** It lists the names of the teams in the external app.
* **App role:** It lists the roles assigned to the teams in the external app.
* **Type:** It indicates the native name of the teams in the external application. For example, team, collection, or group.
