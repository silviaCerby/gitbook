---
description: This article describes the key benefits of the Partners feature that enables you to collaborate with external parties through Cerby.
---

# Explore Partners

With Cerby, you have a secure and controlled way to collaborate with external parties, such as contractors, agencies, vendors, and clients, through **Partners**.

This feature helps you and your company support sharing access to your items and business hub integrations with collaborators who don't belong to your domain and don’t have access to your Cerby workspace through your identity provider (IdP), such as Okta or Entra ID.

After adding a partner to your Cerby workspace, access to your items and seat-based and paid social apps is centralized in Cerby. Therefore, your company retains control over these items and apps, and gains visibility into their usage by external collaborators. We understand that, for you, having visibility of end-user actions is a significant effort in preventing security risks and facilitating effective collaboration.

**Figure 1** shows the **Partners** page in the Cerby web app dashboard, where you can manage your partnerships.

<figure><img src="../.gitbook/assets/AD_4nXeChnY4WU6ChlJXiSH2R1f73t69Gdv542XrTKuSbLL1O1q7GHteNz1Y6zbOnA8x5rRsUV5-XoBxgevAo1lDqxhzKmeDXgEFW8dQIO2qs_pttk_MAbE2fbA5acSqk5aB6z5gG5CvsQ.png" alt="Screenshot of the Cerby web app dashboard. The Partners page is displayed with the Add a partner dialog box on top of it"><figcaption></figcaption></figure>

**Figure 1.** **Partners** view in the Cerby web app dashboard

Currently, Cerby supports the following ways to add and collaborate with your partners:

  * Host-guest partnership
  * Local partner
  * Native partner

The following sections describe each way.

* * *

# Host-guest partnership

A host-guest partnership enables you to establish a secure connection between an existing host workspace and a guest workspace created for this purpose. Both workspaces are managed by their respective **Admins** , and the guest workspace is configured as a [local user workspace](https://help.cerby.com/en/articles/8011381-create-and-configure-a-local-user-workspace).

Through this connection, you can share accounts with external collaborators invited as users in the guest workspace. With this partnership type, you retain complete control over the shared accounts and gain visibility on their usage.

With this partnership type, Cerby introduces the following roles, as described in **Table 1**.

**Role**| **Description**
---|---
Partnership**Owner**|  It is a role assigned automatically to the user from the host workspace who adds the partnership. With this role, they can perform the following actions:

  * Manage the partnership they own.
  * Share accounts with the guest workspace.

Host workspace **Admin**|  It is a user from the host workspace who has the **Admin** role. With this role, they can perform the following actions:

  * Manage any partnership.
  * Approve or decline any attempt to add a host-guest partnership.

Guest workspace **Admin**|  It is a user from the guest workspace who has the **Admin** role. With this role, they can perform the following actions:

  * Manage users in the guest workspace.
  * Accept or decline any partnership request from the host workspace.

Account **Manager**|  It is an account-level role assigned by the partnership**Owner** when sharing an account with the guest workspace; by default, it is assigned to the guest workspace **Admin**. With this role, they can perform the following actions:

  * Log in to accounts shared with them.
  * Request access to accounts for other guest workspace members.

**IMPORTANT:** Account **Managers** cannot manage the account security settings.

**Table 1.** Host-guest partnership roles and their descriptions

Any user in the host workspace can add a host-guest partnership. To establish the connection, you send a partnership request that must be approved by a host workspace **Admin** and accepted by a guest workspace **Admin**.

After adding the partnership, only you as a partnership **Owner** can share accounts with the guest workspace and assign one of the following roles over the accounts:

  * **Collaborator:** Guest workspace members can only log in to shared accounts.
  * **Manager:** Guest workspace members can log in to shared accounts and request access to these accounts for other members.

For more information about roles, read the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

{% hint style="danger" %}


**IMPORTANT:** A host workspace can have multiple host-guest partnerships. However, they can only establish one connection with the same guest workspace.


{% endhint %}

* * *

# Local partner

A local partner enables you to invite external collaborators who don't belong to your domain directly to your workspace, without creating a separate guest workspace. These collaborators become a subgroup or organization of guest users to whom you can share your accounts.

In this partnership type, you retain full control over the accounts you share, and you can perform user management tasks on the guest users. For example, you can add or remove external collaborators from your workspace as needed.

Additionally, as guest users are part of your workspace, using an identity provided and managed by Cerby, you can share your accounts either with the local partner or directly with the guest users.

With this partnership type, Cerby introduces the following roles, as described in **Table 2**.

**Role**| **Description**
---|---
**Host Admin**|  It is a role assigned by the workspace **Admin** to another workspace user when adding a local partner. With this role, they can perform the following actions:

  * Manage the local partner and its guest users.
  * Overlook the activities the local partner’s users do in your workspace.
  * Assign the **Host Admin** role to other workspace users.
  * Share accounts with the local partner.

**Guest Admin**|  It is a role assigned by the workspace **Admin** to a guest user when adding a local partner. With this role, they can perform the following actions:

  * Manage other **Guest Users** and their access to the workspace.
  * Propagate access to the accounts that **Host Admins** shared with them as account **Managers**.

**NOTE:** **Guest Admins** can’t add other local partners, import items from LastPass, or view workspace users, policies, or settings.
**Guest User**|  It is a role assigned to an external collaborator invited to join a Cerby workspace with limited access to items and assets, enough to perform their activities.
Account **Manager**|  It is an account-level role assigned by the **Host Admin** when sharing an account with the local partner; by default, the role is assigned to the **Guest** **Admin**. With this role, they can perform the following actions:

  * Log in to accounts shared with them.
  * Propagate shared access to the accounts with other **Guest Users**.

**Table 2.** Local partner roles and their descriptions

Only as a workspace**Admin** , you can add a local partner to your workspace. While adding it, you can designate any workspace user, including you, as the **Host Admin** , granting you control over who can manage the partnership and external collaborators.**** Also, you must designate and invite a **Guest Admin** to join your workspace.

The following are the benefits of having **Host** and **Guest Admins** :

  * **Delegate ownership:** **Host Admins** can invite and assign other workspace users as **Host Admins** , sharing control and responsibility over the partnership.
  * **Expand collaboration:** **Host Admins** can invite external collaborators from the partner's organization, selecting between granting them **Guest Admin** privileges for management capabilities within the partnership only or **Guest User** access for limited access, visibility, and interaction.
  * **Delegate user invites:** **Guest Admins** can invite external collaborators to your workspace as **Guest Users**.
  * **Propagate access to accounts:** With the account **Manager** role, **Guest Admins** can share with other **Guest Users** the accounts that were initially shared with them by **Host Admins**.

For more information about roles, read the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

* * *

# Native partner

A native partner is a business or organization (agency, media planner, or consultant) already existing as a partner in your paid social apps for collaboration purposes in ad campaigns.

By connecting your partner to Cerby, you gain visibility on the users who access your assets from your partner's side. This level of visibility is not even achievable through the business manager of your paid social app, such as Meta Business Manager or TikTok for Business.

With this partnership, Cerby does not introduce any new role because it is a read-only capability. The user who connects a native partner is the App Owner in Cerby.

After establishing the partnership, you can sync and import the information of the partner’s users with shared access to your assets, providing you with a granular and centralized oversight of your business manager.

{% hint style="danger" %}


**IMPORTANT:** You can only add a native partner in Cerby if you have shared at least one asset with a partner in your paid social app or vice versa.


{% endhint %}

Unlike a local partner, where external collaborators exist in your workspace using an identity and account managed by Cerby, the user management capabilities remain in the paid social apps when you connect with a native partner. Therefore, your partners don’t have to use Cerby.

Currently, Cerby supports the Native Partner feature for the following paid social apps:

  * Meta Business Manager
  * TikTok For Business
  * Pinterest Business Manager
