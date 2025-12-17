---
description: This article describes how to share a collection with other workspace members and teams.
intercom_id: 8981907
---

# Share a collection

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , **Users** , and **Guest Users**
* Collection **Owners**
* Supported using the Cerby web app and mobile app. For the mobile app instructions, read the article [Share a collection using the Cerby mobile app](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-mobile-app/collections/share-a-collection-using-the-cerby-mobile-app)


{% endhint %}

As a collection **Owner** , you can share a collection with other workspace members and teams and select the role to assign to them on the collection. With this action, you extend access to all the items within the collection.

The following rules are applied to items, subcollections, members, and teams when sharing a collection:

* The role you select on the collection (**Owner** or **Collaborator**) is the same role that other members and teams will have on all the accounts, secrets, business hubs, and assets within the collection.
* When your collection has subcollections, you are also sharing access to all nested subcollections and their items, inheriting the permission settings bottom-down.
* When your collection already has business hub integrations and assets within, Cerby sends the corresponding emails for users to claim access to the integration. For more information, read the article [Manage access to business hubs and assets with collections](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/manage-access-to-business-hubs-and-assets-with-collections).
* Members with the **Login-only** and **Guest user** workspace roles can only be granted the **Collaborator** role on a collection.

To share a collection, you must complete the following steps using the Cerby web app:

1. Log in to your [Cerby](https://app.cerby.com/) workspace.
2. Select the **Collections** option from the left menu. The **Collections** page is displayed.
3. Click the **Share**(<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1481364251/4c687886ce44983e75b6f7a2d304/AD_4nXegaXoUF8_54QeQY36Cxxq2fhp4zCs8ot8VywKRI1WrhIXd2RS_6bUoqWfHLPkNZO8qRLGCE9Q59L_v1ty5fvFf-G1tLzH71luHyye9S1h63Ukdf2swtZuNN4llQpA1yKdT-ycRIE4Qm1eI3HM98BcrMKo?expires=1765908000&signature=b4c3145e597e206e36b2c0aa11f80363cc79e2fbe6323c4b34e0e7b1a890b9cf&req=dSQvF8p4mYNaWPMW3Hu4gdVoTB79SICI4Oe7Fqwzv4D%2FaEGq%2FzF5dJc9tknN%0AoA%3D%3D%0A" alt="">) icon that appears when hovering over the corresponding collection card. The **Share Access** dialog box is displayed.
​**TIP:** You can also open the **Share Access** dialog box by performing the following actions:

   1. Click the **Settings** (<img src="../../../../.gitbook/assets/unnamed_66.png" alt="">) icon of the corresponding collection card. The collection details page is displayed with the **General** tab activated.
   2. Click the **Share** button located at the top right of the page. The **Share Access** dialog box is displayed.
4. Enter the name of the member or team in the search bar. The members or teams that match the name are displayed on a list automatically.
5. Select the member or team from the list to add them to the **Members and Teams** section.
6. Repeat steps 4 and 5 as necessary.
7. Select the role to assign to the members and teams on the collection from the **Access** drop-down menu:

   * **Owner:** Members and teams can share access to the collection, manage the item settings, and perform the actions of a **Collaborator**.
   * **Collaborator:** Members and teams can only log in to the accounts, view the secrets, and download the secret attachments.

   **NOTE:** When you select a member with the **Login-only** or **Guest User** role, you can only select the **Collaborator** role for them.

8. (Optional) Customize the message to send when you share the collection in the **Message** field.
9. Click the **Share** button. The wizard closes, and a success message box is displayed.

{% hint style="info" %}


**NOTE:** When you share a collection containing business hubs and assets, Cerby sends emails for users to claim access to the integration. After users claim access, Cerby adds these users to the external apps. For more information, read the article [Manage access to business hubs and assets with collections](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/manage-access-to-business-hubs-and-assets-with-collections).


{% endhint %}

Now you are done.
