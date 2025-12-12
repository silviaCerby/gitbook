---
description: This article describes the key benefits of managing access to external apps via collections of business hubs and assets.
---

# Manage access to business hubs and assets with collections

{% hint style="info" %}


**Who can use this feature?**

  * Business hub **Owners**
  * Only supported using the Cerby web app


{% endhint %}

In Cerby, collections simplify how you manage business hubs and their assets to propagate access to multiple paid social and seat-based apps.

Unlike sharing directly an individual business hub, which immediately triggers the corresponding automation jobs to add and invite users to an external app, collections enable you to share multiple business hubs at a time and control user onboarding.

To optimize access propagation, Cerby introduces a preliminary claiming access step. The goal is to trigger and execute the referred automation jobs only when users are ready to join the app and complete their account setup.

The following are the key benefits of managing access this way:

  * **Reduced admin load:** IT admins and app owners can manage licenses and seats for external apps in bulk using Cerby automation. By triggering jobs only after users claim access, Cerby also prevents expired invitation links and minimizes requests for resending invites.
  * **User empowerment:** Users gain control over when they are ready to join an external app.
  * **Consistent roles:** The roles you assign to the collection are automatically inherited across all nested items, including business hubs and assets. These roles apply at two levels:
    * **Cerby roles:** You can grant workspace members and teams the following roles on the business hub integration via the collection:
      * **Owner:** Members and teams can perform the supported [user and access management tasks](https://help.cerby.com/en/articles/6831152-explore-business-hubs#h_0cc7b04140) via the business hub, update the integration settings, and log in to the external app through Cerby. Additionally, collection **Owners** can see all assets within the business hub but not necessarily access everything.
      * **Collaborator:** Members and teams can only log in to the external app through Cerby.
    * **External app roles:** You can grant workspace members and teams specific app-level roles that you define when you add business hubs and assets to collections. These roles and permissions vary by app.
  * **Automated user management tasks:** Depending on the configuration of your business hub, you can perform automated user management tasks directly in Cerby or extend the provisioning and deprovisioning capabilities of your identity provider (IdP). For more information, read the section [Extended user and access management from your IdP](https://help.cerby.com/en/articles/6831152-explore-business-hubs#h_05107885b1) of the article [Explore Business Hubs](https://help.cerby.com/en/articles/6831152-explore-business-hubs).

This article contains the following sections to describe how access management works for business hubs and assets within a collection:

  * Sharing business hubs and assets via a collection
  * Claiming access to a business hub and external app
  * Updating access to business hubs and assets via a collection
  * Removing access from business hubs and assets via a collection
* * *

# Sharing business hubs and assets via a collection

When you share business hubs and assets via a collection, you can grant access to multiple paid social and seat-based external apps for multiple workspace members and teams. Access propagation is powered by automation jobs executed by a Cerby agent.

These automation jobs, triggered after users claim access, handle email invites and user account creation in the external apps. If you have configured IdP groups pushed as Cerby teams with shared access to business hubs via collections, Cerby detects automatically when users are added or removed from IdP groups, deleted, or deactivated. Then, Cerby propagates these changes to the external app through automation.

If your app supports assets, you can add these items individually to a collection for sharing them with other users and teams. In this case, after an access claim, Cerby executes the automated jobs to add and invite users both to the external app and to the assets because they typically follow a hierarchical structure.

The following actions trigger the claim access flow and the automation jobs to add and invite users to an external app:

  * Sharing a collection containing business hubs and assets with other workspace users and teams who didn’t have access to the business hubs and assets individually or via another collection.
  * Adding business hubs and assets to collections already shared with workspace users and teams.
  * Adding users to a team with shared access to a collection containing business hubs and assets.

{% hint style="info" %}


**NOTE:** When users and teams have shared access to business hubs and assets multiple times, whether individually or via a collection, Cerby always assigns the highest hierarchical app role.


{% endhint %}

* * *

# Claiming access to a business hub and external app

The claim access flow empowers users to control when they receive an invitation to join an external app through Cerby. This flow works as follows:

  1. **Cerby sends a notification.** When an integration **Owner** shares a business hub via a collection with workspace members and teams, Cerby sends an email notification to the corresponding recipients, inviting them to claim access to the external app through Cerby.
  2. **Users claim access to the external app through Cerby.** The users click a link in the email message, which redirects them to their Cerby workspace. The account card of the business hub is displayed in the Cerby web app dashboard with the “Claim your invite” status. They must click the account card and complete the instructions to claim access.
  3. **Cerby triggers the automation jobs to add and invite users to the external app.** After the users claim access, Cerby triggers the automated jobs to add and invite the corresponding users and team members to the external app. They then receive the actual invitation email from the app itself to join.

{% hint style="info" %}


**NOTE:** Users who receive shared access as integration **Owners** via a collection can skip the claim access flow. This feature is helpful for IT admins who need oversight through Cerby but not a license or seat in the external app.


{% endhint %}

For detailed instructions on how to claim access, read the article [Claim access to a business hub and assets](https://help.cerby.com/en/articles/12457509-claim-access-to-a-business-hub-and-assets).

* * *

# Updating access to business hubs and assets via a collection

When users already have shared access to business hubs and assets, whether individually or via a collection, their role can be updated through an automation job when any of the following scenarios happen:

  * Sharing business hubs and assets individually or via a collection with workspace users and teams, where the new app role assigned is hierarchically higher.
  * Adding workspace users to a team that already has shared access to a business hub or asset, where the external app role assigned is hierarchically higher.
  * Removing workspace users from teams that already have shared access to a business hub or asset, but they keep access individually or via another collection with a hierarchically lower app role.
  * Removing business hubs and assets from a collection, but workspace users and teams keep access individually or via another collection with a hierarchically lower app role.

{% hint style="info" %}


**NOTE:** The automation jobs to execute access updates happen immediately without triggering the claim access flow.


{% endhint %}

* * *

# Removing access from business hubs and assets via a collection

When users and teams don’t have access assigned individually or through another collection, their access to business hubs and assets is removed in the following scenarios:

  * Removing workspace users from teams that already have shared access to a business hub and assets.
  * Removing workspace users and teams from collections containing business hubs and assets.
  * Removing business hubs and assets from a collection.

**NOTE:** Cerby asks you if you want to remove access granted at the collection level or keep access at the item level.

  * Removing a collection containing business hubs and assets.

**NOTE:** Cerby asks you if you want to remove access granted at the collection level or remove the collection, the access, and the items inside the collection.

{% hint style="info" %}


**NOTE:** The automation jobs to execute access removals happen immediately.


{% endhint %}

* * *

# Important considerations

The following are important considerations about managing access to business hubs and assets with collections:

  * You cannot create collections through the regular wizard. Instead, you add existing business hubs and assets individually to existing collections.
  * You can only add one business hub to a collection at a time, and it cannot be added to a different collection. Moreover, adding business hubs to subcollections is not supported.
  * Sharing business hubs and assets via a collection always enforces the claims flow.
  * Collections cannot be shared with [local partners](https://help.cerby.com/en/articles/8980877-explore-partners#h_7e4add33a2).
  * The app roles to be assigned to workspace users and teams when they receive shared access to a collection are defined when you add a business hub or asset to a collection.
  * You can manage assets as follows:
    * Assets can be added individually to a collection.
    * When a collection containing assets is shared, and the users claim access, Cerby triggers and executes automation jobs to add and invite users to join the app and the assets because that’s the typical hierarchical structure.
    * Cerby sends invites to only claim assets when users already have access to a business hub.
    * Integration **Owners** can view all assets of a business hub but are not automatically granted access to them; they must claim or assign themselves if needed.
  * You cannot update the app role from the table of integrations in the **Business hubs** tab of the collection details page.
* * *

# Related articles

The following articles contain more information about managing access to business hubs and assets with collections:

  * [Add a business hub to a collection](https://help.cerby.com/en/articles/11102018-add-a-business-hub-to-a-collection)
  * [Add an asset to a collection](https://help.cerby.com/en/articles/11102036-add-an-asset-to-a-collection)
  * [Share a collection](https://help.cerby.com/en/articles/8981907-share-a-collection)
  * [Claim access to a business hub and assets](https://help.cerby.com/en/articles/12457509-claim-access-to-a-business-hub-and-assets)
  * [Remove a user from a collection](https://help.cerby.com/en/articles/8432313-remove-a-user-from-a-collection)
  * [Remove a team from a collection](https://help.cerby.com/en/articles/8981940-remove-a-team-from-a-collection)
  * [Remove a business hub from a collection](https://help.cerby.com/en/articles/12457407-remove-a-business-hub-from-a-collection)
  * [Remove an asset from a collection](https://help.cerby.com/en/articles/12457450-remove-an-asset-from-a-collection)
  * [Join your external app and set up your business hub access](https://help.cerby.com/en/articles/9046232-join-your-external-app-and-set-up-your-business-hub-access)
  * [Delete a collection](https://help.cerby.com/en/articles/8981974-delete-a-collection)
