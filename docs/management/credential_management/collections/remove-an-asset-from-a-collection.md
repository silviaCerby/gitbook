---
description: This article describes how to remove an asset from a collection.
---

# Remove an asset from a collection

{% hint style="info" %}


**Who can use this feature?**

  * Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
  * Collection, business hub, and asset **Owners**
  * Only supported using the Cerby web app


{% endhint %}

As a collection **Owner** , you can remove an asset from a collection. When you take this action, you must choose whether to remove or keep the access that users and teams have to the asset through the collection.

To remove an asset from a collection, you must complete the following steps using the Cerby web app:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Collections** option from the left menu. The **Collections** page is displayed.
  3. Click the **Settings** () icon of the corresponding collection card. The collection details page is displayed with the **General** tab activated.
  4. Activate the **Assets** tab.
  5. Click the **More options**() icon of the corresponding asset. A drop-down menu is displayed.
  6. Select the **Remove from Collection** option from the drop-down menu. A confirmation dialog box is displayed.
  7. Choose what to do with access granted to the business hub through the collection:

     * Remove access granted through the collection:

       1. Select the **Remove account permissions shared through the collection** option.

     * Keep access granted through the collection as individual access:

       1. Unselect the **Remove account permissions shared through the collection** option.
  8. Click the **Remove from Collection** button. The dialog box closes, and a success message box is displayed.

{% hint style="info" %}


**NOTE:** If in step 7 you selected to remove access granted through the collection, Cerby initiates in the background automation jobs to remove users from the external app only when users and teams don’t have other access grants to the business hub.


{% endhint %}

Now you are done.
