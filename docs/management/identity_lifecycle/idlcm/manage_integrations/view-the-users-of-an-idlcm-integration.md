---
intercom_id: 11644266
description: This article describes how to view the users of an IdLCM integration.
---

# View the users of an IdLCM integration

{% hint style="info" %}
**Who can use this feature?**

* Workspace**Owners, Super Admins,** and**Admins**
* Only supported using the Cerby web app
{% endhint %}

As a workspace**Owner, Super Admin,** or**Admin** , , you can access the integration details page to view the users of your IdLCM integration.

The **Users** tab, as shown in **Figure 1** , provides a centralized view of all users with access to your Cerby-integrated app, helping you manage their access efficiently.

![](../../../.gitbook/assets/30968ea2-7703-4dbf-8c1a-e500ec33a866.png)

**Figure 1. Users** tab in the integration details page

The table in the **Users** tab provides information about external app users in the following columns:

* **User:** Indicates the username and email of the Cerby user accounts matched with the external app user accounts. This column is empty for\*\*\*\* unmatched\*\*\*\* users\*\*.\*\*
* **Username in app:** Indicates the username assigned to the user in the external app.
* **App access:** Lists the roles assigned to the user in the external app. **TIP** : If the user has been granted multiple roles, select the corresponding user from the list to display a side drawer with the details of the assigned roles.
* **Active in app:** Indicates whether the user account is active in the external app.
* **Upstream user ID:** Represents the unique identifier of the user in the identity provider (IdP), such as Okta or Entra ID.
* **Provisioning state:** Indicates the status of the user. The possible values are the following:
  * **Provisioning awaiting** : The user provisioning job is queued and waiting to start
  * **Provisioning ongoing** : The user provisioning process is in progress
  * **Provisioning failed** : The user provisioning process failed
  * **Onboarded** : The user account was successfully created in the external app
  * **Update awaiting** : The user update job is queued and waiting to start
  * **Update ongoing** : The user update process is in progress
  * **Update failed** : The user update process failed
  * **Delete awaiting** : The user deprovisioning job is queued and waiting to start
  * **Delete ongoing** : The user deprovisioning process is in progress
  * **Delete failed** : The user deprovisioning process failed
  * **Deleted** : The user account was successfully removed from the external app
