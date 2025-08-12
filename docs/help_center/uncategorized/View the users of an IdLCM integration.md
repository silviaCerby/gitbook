# View the users of an IdLCM integration

**Description:** This article describes how to view the users of an IdLCM integration.

{% hint style="info" %} **Who can use this feature?** * Integrations
**Owners** and**Managers** * Only supported using the Cerby web app {% endhint
%}

As an integration **Owner** or**Manager** , you**** can access the integration
details page to view the users of your IdLCM integration.

The **Users** tab, as shown in **Figure 1** , provides a centralized view of
all users with access to your Cerby-integrated app to help you manage their
access efficiently.

![](gitbook/imagesimage.png)

**Figure 1. Users** tab in the integration details page

The **Users** table provides information about external app users in the
following columns:

  * **User:** It lists the username and email of the Cerby user accounts matched with the app user accounts. This column is empty for**** unmatched**** users**.**

  * **Username in app:** It lists the username given to the users in the external app.

  * **App access:** It lists the roles assigned to the users in the external app.  
​**IMPORTANT** : If the user has been granted multiple roles, click the
**More** **options**
(![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1584910891/ad1def47c4ff1e0278ae6ea03966/AD_4nXcLtrIeLzlxsdoOAxu3n7B0FXivh3A1ZmlifdIV0w7yV47c-24JXNIWby2O22jsHVFLwmIpUjDx3VC5pfGPLMP70_jTLTYPhrMFl179mxfwNZ1xIZY4b7QL003QO40L_qEJ3QG60w?expires=1750842000&signature=fd293c90c063fc0921d161a49f3613c027976ff865c519ab098043e4f581410a&req=dSUvEsB%2FnYlWWPMW3Hu4gR%2ByYoT13XazhyJNnAr0bCk0BWul3kcRxTO8BYOF%0AWw%3D%3D%0A))
icon and select the **Overview** option to view more details of the assigned
role.

  * **Entitlements:** It indicates the number of assets assigned to the users in the external app.  
​**NOTE:** If multiple assets have been assigned to a user, click the **More
options**(![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1584910891/ad1def47c4ff1e0278ae6ea03966/AD_4nXcLtrIeLzlxsdoOAxu3n7B0FXivh3A1ZmlifdIV0w7yV47c-24JXNIWby2O22jsHVFLwmIpUjDx3VC5pfGPLMP70_jTLTYPhrMFl179mxfwNZ1xIZY4b7QL003QO40L_qEJ3QG60w?expires=1750842000&signature=fd293c90c063fc0921d161a49f3613c027976ff865c519ab098043e4f581410a&req=dSUvEsB%2FnYlWWPMW3Hu4gR%2ByYoT13XazhyJNnAr0bCk0BWul3kcRxTO8BYOF%0AWw%3D%3D%0A))
icon and select the **Overview** option to view more details of the assets.

  * **Last used:** It is the date and time of the user's most recent activity.

  * **Login method:** It indicates the user login method. The possible values are the following:

    * **Pending user login:** The user needs to log in to the app and capture their credentials. 

    * **Pending user claim:** The user needs to accept the invite to join the app. 

    * **< connected account name>: **The user logs in to the external app via username and password credentials captured in Cerby. 

    * **< App name> <SSO label>: **The user logs in to the external app via SSO authentication.

  * **Active in app:** It indicates if the user account is active in the external app.

  * **Provisioning state:** It indicates the status of the user. The possible values are the following:

    * **Removed:** The user was removed from the app. The removal could be triggered by the identity provider (IdP), Cerby, or the app itself.

    * **Unmatched user:** The user was synced, but Cerby couldn't match it with a Cerby user account.

    * **Exempted:** The user was exempted from the IdLCM integration, meaning their account or seat remains active in the app but cannot be managed through Cerby.

    * **Inviting** : The user invite is queued or in progress. 

    * **Awaiting update:** The user’s update is queued or in progress. 

    * **Invite failed:** The process of sending the user invite failed. 

    * **Removing:** The user account deprovisioning is queued or in progress.

    * **Removed failed:** The user account deprovisioning failed.

    * **Update failed:** The user role update failed.

    * **Sync failed:** The check for updates failed for this user.

    * **Invite expired:** The user invite has expired.

