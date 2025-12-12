---
description: This article describes how to disable the registered trusted sessions and devices in your workspace.
---

# Disable trusted sessions and devices in your workspace

This article contains the steps you must follow to perform the following actions related to disabling trusted sessions in your workspace:

  * Disable the trusted sessions on your devices
  * Disable other members' trusted sessions in the workspace

The following sections detail the steps for each action.

{% hint style="info" %}


**NOTE:** Cerby does not completely remove a device because it keeps an audit of all the devices that have been used. Disabled devices cannot be re-enabled; however, you can set up again a device that was previously disabled.


{% endhint %}

* * *

# Disable the trusted sessions on your devices

As a **Workspace User** , you can disable the trusted session on the devices you have registered within your workspace.

To disable your trusted sessions, you must complete the steps corresponding to the Cerby client app you are using:

  * Cerby web app
  * Cerby mobile app
  * Cerby browser extension

The following sections contain the steps for each Cerby client app.

## Cerby web app

To disable a trusted session on a device using the Cerby web app, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using the Cerby web app.
  2. Click the user profile menu at the top right of the Cerby dashboard. A drop-down menu is displayed.
  3. Select the **My Profile** option. The **My Profile** page is displayed.
  4. Activate the **My trusted devices** tab. A table with the list of trusted devices you have set up is displayed.
  5. Click the **Remove** icon of the corresponding device. The **Remove device?** dialog box is displayed.
  6. Click the **Remove device** button. The dialog box closes, a success message box is displayed, and the device is displayed in the table with the **Removed** status.

## Cerby mobile app

**IMPORTANT:** Currently, it is not possible to disable trusted sessions on the Cerby mobile phone app. To disable a trusted session, you must use the Cerby web app.
---

## Cerby browser extension

To disable a trusted session on a device using the Cerby browser extension, you must complete the following steps:

  1. Open the Cerby browser extension popup.
  2. Log in to your Cerby workspace.
  3. Click the user profile icon located at the top right of the popup. The **My Profile** page is displayed.
  4. Click the **My trusted devices** option. The Cerby web app is displayed in a new tab with the **My trusted devices** tab activated on your profile page.
  5. Follow the steps from the [Cerby web app](https://docs.google.com/document/d/1zA7WuIsMs88jkqYwCqiyvdISDgD6QTERQAb3AAriXqg/edit#heading=h.nsldgubsdb9w) section to remove the trusted session.

* * *

# Disable other members' trusted sessions in the workspace

As a **Workspace Owner** , **Super Admin** , or **Admin** , you can disable the trusted devices that all users in your workspace have set up.

To disable a member’s trusted session on a device, you must complete the following steps using the Cerby web app:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using the Cerby web app.
  2. Select the **All members** option from the left navigation drawer. The **All members** view is displayed with a table of users.
  3. Click the corresponding user account from the table. The user details page is displayed.
  4. Activate the **Trusted devices** tab. A table with the list of trusted devices that the user has set up is displayed.
  5. Click the **Remove** icon of the corresponding device. The **Remove device?** dialog box is displayed.
  6. Click the **Remove device** button. The dialog box closes, a success message box is displayed, and the device is displayed in the table with the **Removed** status.

{% hint style="info" %}


**NOTE:** Cerby does not completely remove a device because it keeps an audit of all the devices that have been used. Disabled devices cannot be re-enabled; however, you can set up again a device that was previously disabled.


{% endhint %}
