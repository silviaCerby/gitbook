---
description: This article describes how to delete a collection in your workspace.
intercom_id: 8981974
---

# Delete a collection

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , **Users** , and **Guest Users**
* Collection **Owners**
* Only supported using the Cerby web app


{% endhint %}

As a collection **Owner** , you can delete a collection from your workspace. With this action, all workspace members and teams with shared access to the collection lose access to it, and you can choose to keep or delete the items.

{% hint style="info" %}


**NOTE:** Nested subcollections always become root collections after a deletion. For more information about subcollections, read the article [Explore Subcollections](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-subcollections).


{% endhint %}

To delete a collection, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Collections** option from the left menu. The **Collections** page is displayed.
  3. Click the **More options**(<figure><img src="../../../../.gitbook/assets/AD_4nXfq928eH6lW___VJhn6YkSzlvsBLWHdSZFfnaW1cPAOfvWfj__ce8kcI0ndYDqcrNKTdaYv47jSGGH_CLWU_vh8aELD-qdGfyXMWMp-gSlQ6XlSnmTdKYR4bVeTAZ4mXXEfUaodDURWwzLeDEp4Xg3i1QIk_1.png" alt=""><figcaption></figcaption></figure>) icon of the corresponding collection card. A drop-down menu is displayed.
  4. Select the **Delete collection** option. The **Delete collection?** dialog box is displayed.
  5. Select how you want to delete the collection:

     * **Delete the collection and access granted at the collection level:** Items within the collection remain in your workspace.

       1. Click the **Delete collection** button. The dialog box closes, and a success message is displayed.

     * **Delete the collection, the access, and the items inside it from your workspace:** Items within the collection are also deleted.
​**IMPORTANT:** Be careful when selecting this option because accounts and business hub integrations can be restored by their item **Owners** , but secrets cannot.

       1. Click the **Delete collection** button. A confirmation dialog box is displayed with the information of all the items to be deleted.
       2. Click the **Delete all items** button. The dialog box closes, and a success message is displayed.

{% hint style="info" %}


**NOTE:** When you delete a collection containing business hubs and assets, Cerby removes all users and team members from the external apps. For more information, read the article[ Manage access to business hubs and assets with collections](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/manage-access-to-business-hubs-and-assets-with-collections).


{% endhint %}

Now you are done.
