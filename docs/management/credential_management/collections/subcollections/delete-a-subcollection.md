---
description: This article describes how to delete a subcollection from a parent collection, removing inherited access from top-level collections.
intercom_id: 8982989
---

# Delete a subcollection

To delete a subcollection, you must complete the following steps:

{% hint style="danger" %}


**IMPORTANT:** To delete a subcollection, you must have access as **Owner** to the settings of its parent collection.


{% endhint %}

1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
2. Select the **Collections** option from the left navigation drawer. The **Collections** view is displayed.
3. Expand the collection that contains the subcollection you want to remove.

   * Alternatively, you can search for the subcollection in the search bar.

4. Hover the mouse over the subcollection you want to share. A menu of icons is displayed.
5. Click the **More options** (<img src="../../../../../.gitbook/assets/unnamed_60.png" alt="">) icon. A menu is displayed.
6. Select the **Delete collection** option. The **Delete collection?** dialog box is displayed.
7. Select how you want to delete the collection:

   * **Keep account permissions for the same users and teams:** You will delete the subcollection but maintain the account, secrets, and subcollections within it in Cerby. When you select this option, the subcollections inside become root collections and are displayed in the **Collections** view.
   * **Delete all items in the collection:** You will delete all accounts, secrets, and subcollections inside it. When you choose this option, another **Delete collection?** dialog box is displayed. Click the **Delete all items** button to delete all items.
​**IMPORTANT:** Be careful when selecting this option. It is not possible to recover the items later.
