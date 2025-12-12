---
description: This article describes how to create a collection of items, such as accounts, secrets, business hubs, assets, and subcollections.
---

# Create a collection

{% hint style="info" %}


**Who can use this feature?**

  * Workspace**Owners** , **Super Admins** , **Admins** , **Users** , and **Guest Users**
  * Item **Owners**
  * Only supported using the Cerby web app
  * **IMPORTANT:** If you use local vaults, you must have already set up at least one [trusted session](https://help.cerby.com/en/articles/8142370-set-up-trusted-sessions-on-your-devices) on your devices.


{% endhint %}

As a workspace**Owner** , **Super Admin** , **Admin** , **User** , or **Guest User** , you can create a collection where you can add the accounts, secrets, business hub integrations, assets, and subcollections to which you have the **Owner** role.

With this action, you become the collection **Owner** , and when you share the collection with other workspace members and teams, you extend access to all the items within the collection under the role assigned at the collection level.

{% hint style="info" %}


**NOTE:** **Guest Users** cannot connect Cerby business hub integrations to external apps; therefore, they cannot add them to a collection.


{% endhint %}

In Cerby, you can create a collection in the following two ways:

  * Create a collection manually
  * Import collections from your password manager

The following sections describe each way.

* * *

# Create a collection manually

To create a collection manually, you must complete the following steps using the Cerby web app:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Collections** option from the left menu. The **Collections** page is displayed.
  3. Click the **Create collection** button located at the top right. A wizard is displayed on the **Create a collection** page.
  4. Enter a name for your collection in the **Collection name** field.
​**NOTE:** This page includes the **Create as subcollection** option. For more information about subcollections, read the article [Explore Subcollections](https://help.cerby.com/en/articles/8982445-explore-subcollections).

  5. Click the **Next** button. The **Add items to your collection** page of the wizard is displayed listing the items you own.
  6. Click the **Add**(<figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1481328643/0667f81a58c5e7a7fe37ac42c7e9/AD_4nXcXkA9uSdrmnOIUp4FEKVa5dOQgv_inKeFNHTAr0uAmTIptIuBit2C42NfgpuCrglPoRZb0mmUwg315TyvtQ_vD7B-esIkOtocJI-RF0fEB3iPrHJx8zV9qahQibS4JsF_hva-wzg?expires=1759320000&signature=9322676cacdee699b5665ba0f7af069eeeb817765d1d8fecee1ce0bd941b48b9&req=dSQvF8p8lYdbWvMW3Hu4gUkxTM1A%2BKudkV2cWGhtBRW60HCthV0JuuZ3JGm0%0Amg%3D%3D%0A" alt=""><figcaption></figcaption></figure>)icon of the item you want to add to your collection. The item is added to a list in the **Selected items** section.
  7. Repeat step 6 as necessary.
  8. Decide whether you want only to create the collection or create it and share it:

     * Create the collection:

       1. Click the **Create collection** button. The wizard closes, a success message box is displayed, and the new collection is added to the **Collections**.
​**NOTE:** You can share the collection later with other workspace members and teams by following the instructions in the article [Share a collection](https://help.cerby.com/en/articles/8981907-share-a-collection).

     * Create and share the collection:

       1. Click the **Share collection** button. The **Share access** page of the wizard is displayed.
       2. Enter the name of the member or team in the search bar. The members or teams that match the name are displayed on a list automatically.
       3. Select the member or team from the list to add them to the **Members and Teams** section.
       4. Repeat steps b and c as necessary.
       5. Select the role to assign on the collection to the members and teams from the **Access** drop-down menu:

          * **Owner:** Members and teams can share access to the collection, manage the item settings, and perform the actions of a **Collaborator**.
          * **Collaborator:** Members and teams can only log in to the accounts, view the secrets, and download the secret attachments.

**NOTE:** When you select a user with the **Login-only** role, they are listed in the **Login-Only** section. You can only select the **Collaborator** role for them.

       6. (Optional) Customize the message to send when you share the collection in the **Message** field.
       7. Click the **Share** button. The wizard closes, a success message box is displayed, and the new collection is added to the **Collections** page.

Now you are done.

* * *

# Import collections from your password manager

If your organization already uses an enterprise password manager (EPM) and you want to migrate your items to Cerby, including your storage structure (folders or vaults), our [Password Manager Importer](https://help.cerby.com/en/articles/7217206-migrate-your-items-from-your-enterprise-password-manager-to-cerby) feature is available to facilitate this process.

Currently, our importer supports migrations from LastPass and 1Password. LastPass folders and subfolders become Cerby collections and subcollections, whereas 1Password vaults become collections.

For more information and instructions, read the following articles:

  * [Migrate from LastPass to Cerby](https://help.cerby.com/en/articles/7175132-migrate-from-lastpass-to-cerby)
  * [Migrate from 1Password to Cerby](https://help.cerby.com/en/articles/9613378-migrate-from-1password-to-cerby)
