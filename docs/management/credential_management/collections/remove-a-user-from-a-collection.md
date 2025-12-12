---
description: This article describes how to remove a user from a collection.
---

# Remove a user from a collection

{% hint style="info" %}


**Who can use this feature?**

  * Workspace**Owners** , **Super Admins** , **Admins** , **Users** , and **Guest Users**
  * Collection **Owners**
  * Supported using the Cerby web app and mobile app. For the mobile app instructions, read the article [Remove user from a collection using the Cerby mobile app](https://help.cerby.com/en/articles/9718660-remove-user-access-to-a-collection-using-the-cerby-mobile-app)


{% endhint %}

As a collection **Owner** , you can remove a user from a collection. With this action, the user loses access at the collection level to all the items within the collection. However, you can choose to grant them direct access to the items.

To remove a user from a collection, you must complete the following steps using the Cerby web app:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Collections** option from the left menu. The **Collections** page is displayed.
  3. Click the **Settings** (<figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1481536120/1eca4a12b24fde121832c095aa0a/AD_4nXcTuUI32R24x3fW2XHHCAqAf0iw1Oe8x8zklBLUvC8GU-I7ziw0SQ-NCNV6Zku1ndLJeFrYUWm4e60nAcrQ5DRPsax2h7cVAFkKFMv_aIdKojLr1vecWtl14NYRwA9ouyfyBU4oxQ?expires=1759320000&signature=b1c173c2b65e2de5079a55a8925a6da077b2ea39650caf96a60e9bd46122f785&req=dSQvF8x9m4BdWfMW3Hu4gflDvMsbbH%2BUukXtoZUPK5J3UI51s8B1z2sRJORN%0AUw%3D%3D%0A" alt=""><figcaption></figcaption></figure>) icon of the corresponding collection card. The collection details page is displayed with the **General** tab activated.
  4. Activate the **Members** tab. The **Members** table is displayed with a list of users who have shared access to the collection.
  5. Click the **More options** (<figure><img src="../.gitbook/assets/unnamed_71.png" alt=""><figcaption></figcaption></figure>) icon of the corresponding user. A drop-down menu is displayed.
  6. Select the **Remove from collection** option. A confirmation dialog box is displayed.
  7. Choose what to do with user access to the accounts, secrets, business hub integrations, and assets within the collection:

     * Select the **Remove account permissions shared through the collection** option to remove user access at the collection level. No direct access is granted to the items.
     * Unselect the **Remove account permissions shared through the collection** option to remove user access at the collection level but grant direct access to the items.
​**IMPORTANT:** In both scenarios, the user loses all access to the secrets within the collection.

  8. Click the **Remove from Collection** button. The dialog box closes, and a success message box is displayed.

{% hint style="info" %}


**NOTE:** When you remove a user from a collection containing business hubs and assets, Cerby triggers the automation jobs to remove this user from the external apps. For more information, read the article [Manage access to business hubs and assets with collections](https://help.cerby.com/en/articles/11102692-manage-access-to-business-hubs-and-assets-with-collections).


{% endhint %}

Now you are done.
