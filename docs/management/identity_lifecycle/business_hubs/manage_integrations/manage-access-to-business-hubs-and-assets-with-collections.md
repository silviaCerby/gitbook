---
description: This article describes the key benefits of managing access to external apps via collections of business hubs and assets.
intercom_id: 11102692
---

# Manage access to business hubs and assets with collections

{% hint style="info" %}


**Who can use this feature?**

* Business hub **Owners**
* Only supported using the Cerby web app


{% endhint %}

In Cerby, collections simplify how you manage business hubs and their assets to propagate access to multiple paid social and seat-based apps.

Unlike sharing directly an individual business hub, which leads Cerby to immediately add and invite users to an external app, collections enable you to share multiple business hubs at a time and control user onboarding.

To optimize access propagation, Cerby introduces a preliminary claiming access step. The goal is to add and invite users only when they are ready to join the app and complete their account setup.

The following are the key benefits of managing access this way:

* **Reduced admin load:** IT admins and app owners can manage licenses and seats for external apps in bulk. Cerby also prevents expired invitation links and minimizes requests for resending invites.
* **User empowerment:** Users gain control over when they are ready to join an external app.
* **Consistent roles:** The roles you assign to the collection are automatically inherited across all nested items, including business hubs and assets. These roles apply at two levels:
    * **Cerby roles:** You can grant workspace members and teams the following roles on the business hub integration via the collection:
      * **Owner:** Members and teams can perform the supported [user and access management tasks](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-business-hubs) via the business hub, update the integration settings, and log in to the external app through Cerby. Additionally, collection **Owners** can see all assets within the business hub but not necessarily access everything.
      * **Collaborator:** Members and teams can only log in to the external app through Cerby.
    * **External app roles:** You can grant workspace members and teams specific app-level roles that you define when you add business hubs and assets to collections. These roles and permissions vary by app.
* **Automated user management tasks:** Depending on the configuration of your business hub, you can perform user management tasks directly in Cerby or extend the provisioning and deprovisioning capabilities of your identity provider (IdP). For more information, read the section [Extended user and access management from your IdP](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-business-hubs) of the article [Explore Business Hubs](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-business-hubs).

This article contains the following sections to describe how access management works for business hubs and assets within a collection:

* Sharing business hubs and assets via a collection
* Claiming access to a business hub and external app
* Updating access to business hubs and assets via a collection
* Removing access from business hubs and assets via a collection
* * *

## Sharing business hubs and assets via a collection

When you share business hubs and assets via a collection, you can grant access to multiple paid social and seat-based external apps for multiple workspace members and teams. Access propagation is powered by Cerby automation.

For workspaces configured with an IdP, you can base access decisions on IdP groups and use shared access to business hubs to ensure that users belonging to those groups have the appropriate access to the external apps.

After users claim access to a business hub or asset, Cerby handles the email invites and user account creation in the external app.

The claim access flow is displayed in the following scenarios:

* Sharing a collection containing business hubs and assets with other workspace users and teams who didn’t have access to the business hubs and assets individually or via another collection.
* Adding business hubs and assets to collections already shared with workspace users and teams.
* Adding users to a team with shared access to a collection containing business hubs and assets.

{% hint style="info" %}


**NOTE:** When users and teams have shared access to business hubs and assets multiple times, whether individually or via a collection, Cerby always assigns the highest hierarchical app role.


{% endhint %}

* * *

## Claiming access to a business hub and external app

The claim access flow empowers users to control when they receive an invitation to join an external app through Cerby. This flow comprises the following steps:

  1. A business hub is shared via a collection with workspace members and teams.****
  2. Cerby sends an email notification for users to claim access.****
  3. Users claim access to the external app through Cerby.
  4. Cerby adds and invites users to the external app.

{% hint style="info" %}


**NOTE:** Users who receive shared access as integration **Owners** via a collection can skip the claim access flow. This feature is helpful for IT admins who need oversight through Cerby but not a license or seat in the external app.


{% endhint %}

For detailed instructions on how to claim access, read the article [Claim access to a business hub and assets](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/claim-access-to-a-business-hub-and-assets).

* * *

## Updating access to business hubs and assets via a collection

When users and teams already have shared access to business hubs and assets, whether individually or via a collection, their role in the external app is updated when any of the following scenarios happen in a new collection access share or removal:

* Cerby upgrades their role if the new role assignment (through a collection, an item within the collection, or by joining a team) is higher.
* Cerby downgrades their role if access removal (from an existing collection, an item within the collection, or by leaving a team) happens and they retain lower access through another path.
* * *

## Removing access from business hubs and assets via a collection

Access to the external app is completely revoked when any of the following access removals happen in Cerby and users and teams don’t retain access to business hubs and assets through another path:

* Removing users from teams.
* Removing users and teams from collections.
* Removing business hubs and assets from a collection.
* Removing a collection containing business hubs and assets.
* * *

## Important considerations

The following are important considerations about managing access to business hubs and assets with collections:

* You cannot create collections through the regular wizard. Instead, you add existing business hubs and assets individually to existing collections.
* You can only add one business hub to a collection at a time, and it cannot be added to a different collection. Moreover, adding business hubs to subcollections is not supported.
* Sharing business hubs and assets via a collection always enforces the claims flow.
* Collections cannot be shared with [local partners](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-partners).
* The app roles to be assigned to workspace users and teams when they receive shared access to a collection are defined when you add a business hub or asset to a collection.
* You can manage assets as follows:
    * Assets can be added individually to a collection.
    * When a collection containing assets is shared, and the users claim access, Cerby adds and invites users to join the app and the assets.
    * Cerby sends invites to only claim assets when users already have access to a business hub.
    * Integration **Owners** can view all assets of a business hub but are not automatically granted access to them; they must claim or assign themselves if needed.
* You cannot update the app role from the table of integrations in the **Business hubs** tab of the collection details page.
* * *

## Related articles

The following articles contain more information about managing access to business hubs and assets with collections:

* [Add a business hub to a collection](https://cerby-test.gitbook.io/cerby-test/management/credential-management/collections/add-a-business-hub-to-a-collection)
* [Add an asset to a collection](https://cerby-test.gitbook.io/cerby-test/management/credential-management/collections/add-an-asset-to-a-collection)
* [Share a collection](https://cerby-test.gitbook.io/cerby-test/management/credential-management/collections/share-a-collection)
* [Claim access to a business hub and assets](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/claim-access-to-a-business-hub-and-assets)
* [Remove a user from a collection](https://cerby-test.gitbook.io/cerby-test/management/credential-management/collections/remove-a-user-from-a-collection)
* [Remove a team from a collection](https://cerby-test.gitbook.io/cerby-test/management/credential-management/collections/remove-a-team-from-a-collection)
* [Remove a business hub from a collection](https://cerby-test.gitbook.io/cerby-test/management/credential-management/collections/remove-a-business-hub-from-a-collection)
* [Remove an asset from a collection](https://cerby-test.gitbook.io/cerby-test/management/credential-management/collections/remove-an-asset-from-a-collection)
* [Join your external app and set up your business hub access](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/business-hubs/join-your-external-app-and-set-up-your-business-hub-access)
* [Delete a collection](https://cerby-test.gitbook.io/cerby-test/management/credential-management/collections/delete-a-collection)
