---
description: This article describes how to configure the sync safeguard threshold for your IdLCM integration to prevent accidental mass deprovisioning.
---

# Configure the sync safeguard threshold of your IdLCM Integration

{% hint style="info" %}


**Who can use this feature?**

  * Workspace**Owners, Super Admins,** and**Admins**
  * Only supported using the Cerby web app


{% endhint %}

As a workspace**Owner, Super Admin,** or**Admin** , you can configure the sync safeguard threshold of your IdLCM integration to prevent accidental loss of access for numerous users.

When you trigger an automation job to sync users, roles, and entitlements in your IdLCM integration with an external app, Cerby reviews the changes before applying them. If the number of deprovisions exceeds the defined threshold, Cerby halts the sync and no updates are applied. This safeguard prevents accidental mass deprovisioning.

To configure the sync safeguard threshold of your IdLCM integration, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Integrations** option from the left menu. The **Integrations** page is displayed.
  3. Click the **More options** (<figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1730603331/e690abe91dce4614438ef01101a5/ed5ac61b-c1cd-44d5-8368-a83b3a7d7296?expires=1759266000&signature=aad91b34132204c8e29b4eb9b343a85565705d65d80713039571de4b6fda66c8&req=dSckFs9%2BnoJcWPMW3Hu4gYhqhzTJd%2BgKQqkTn9sFp9abTFWcFMf3VjgCsCFC%0Akg%3D%3D%0A" alt=""><figcaption></figcaption></figure>) icon of the corresponding integration. A drop-down menu is displayed.
  4. Select the **Settings** option from the menu. The integration details page is displayed with the **Settings** tab activated.
  5. Activate the **Security settings** left tab.
  6. Set the **Threshold** slider to the desired value. By default, the threshold is set to 20%.
  7. Click the **Update** button. A success message box is displayed.

Now you are done.
