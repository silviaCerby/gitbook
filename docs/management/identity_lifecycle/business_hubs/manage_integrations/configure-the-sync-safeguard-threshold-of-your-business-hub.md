---
description: This article describes how to configure the sync safeguard threshold of your business hub to prevent unintended user removals.
---

# Configure the sync safeguard threshold of your business hub

{% hint style="info" %}


**Who can use this feature?**

  * Business hub **Owners**
  * Only supported using the Cerby web app


{% endhint %}

As a business hub **Owner** , you can configure the sync safeguard threshold of your business hub integration to prevent accidental loss of access for numerous users.

When you or a routine daily task triggers an automation job to sync users, roles, and assets between your business hub and your external app, Cerby reviews the changes before applying them. If the percentage of users or assets marked for removal exceeds the defined threshold, Cerby halts the sync, and no updates are applied. This safeguard prevents large-scale unintended removals.

{% hint style="info" %}


**NOTE:** You can monitor the progress of all automation jobs in the**Automation Log.**


{% endhint %}

To configure the sync safeguard threshold of your business hub integration, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
  3. Click the **More options** () icon of the corresponding business hub. A drop-down menu is displayed.
  4. Select the **Settings** option from the menu. The integration details page is displayed with the **Settings** tab activated.
  5. Expand the **Sync safeguard** section**.**
  6. Set the **Threshold** slider to the desired value. By default, the threshold is set to 20%.
  7. Click the **Update** button. A success message box is displayed.

Now you are done.
