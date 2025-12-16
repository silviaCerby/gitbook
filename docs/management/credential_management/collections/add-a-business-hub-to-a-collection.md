---
intercom_id: 11102018
description: This article describes how to add a business hub to an existing collection.
---

# Add a business hub to a collection

{% hint style="info" %}
**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* Collection and business hub **Owners**
* Only supported using the Cerby web app
{% endhint %}

As a collection and business hub **Owner** , you can add a business hub integration to an existing collection. With this action, all workspace members and teams who already have shared access to the collection are automatically granted access to the business hub with the collection-level role.

To add a business hub to a collection, you must complete the following steps using the Cerby web app:

1. Log in to your [Cerby](https://app.cerby.com/) workspace.
2. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.
3.  Click the **More options** (

    ) icon of the corresponding business hub card. A drop-down menu is displayed.
4. Select the **Add to Collection** option from the menu. A wizard is displayed on the **Add to collection** page.
5. Select the corresponding collection from the list or look it up using the search bar.
6. Click the **Next** button. The **Define App Role** page of the wizard is displayed.
7. Select the role or roles to assign to other members and teams in the external app when you share the collection. Depending on whether the external app supports assets, the following happens:
   * When the app supports assets, the **Next** button is displayed:
     1. Click the **Next** button. The **Assign assets** page of the wizard is displayed with the different asset types organized in tabs, a list of available assets in the left section, and a **Role** section to the right.
     2. Select the assets to share with other users and teams when you share the collection.
     3. Select the role to assign to users and teams on the assets.
     4. Activate the next asset type tab.
     5. Repeat steps b to d as necessary.
     6. Click the **Add to collection** button. The wizard closes, and a success message box is displayed.
   * When the app doesn’t support assets, the **Add to collection** button is displayed:
     1. Click the **Add to collection** button. The wizard closes, and a success message box is displayed.

{% hint style="info" %}
**NOTE:** For existing members and teams in the collection, Cerby sends emails for users to claim access to the business hub. After they claim access, Cerby adds these users to the external apps. For more information, read the article [Manage access to business hubs and assets with collections](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/manage-integrations/manage-access-to-business-hubs-and-assets-with-collections).
{% endhint %}

Now you are done.
