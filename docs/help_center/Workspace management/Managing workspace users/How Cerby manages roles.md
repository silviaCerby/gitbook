# How Cerby manages roles

**Description:** This article describes the existing roles in Cerby under the RBAC system and how they are managed.

At Cerby, we have implemented roles to determine the tasks, functions, or
activities each workspace member can or cannot do on our platform.

These roles consist of sets of permissions that are part of a role-based
access control (RBAC) system designed to maintain data security, streamline
access management, enhance collaboration, comply with regulations, and ensure
that sensitive information is protected.

The advantage of using role-based access management is that, after logging in
to a Cerby workspace, members are automatically granted permissions depending
on their role. For more information, read the Benefits of RBAC section.

Cerby manages roles at multiple levels. This article contains the description
of each role, which we have categorized as follows:

  * Workspace-level roles

  * Item-level roles

  * Team-level roles

  * Partnership-level roles

* * *

# **Workspace-level roles**

Workspace-level roles determine the features of the Cerby platform available
to the users, their access privileges, and their responsibilities. The actions
users can perform within a workspace according to their role can be
categorized as follows:

  * Workspace setup

  * Workspace management

  * User management

  * Security hygiene tasks

  * Item management

The following sections describe the actions for each category.

## **Workspace setup**

**Table 1** shows the actions users can perform to set up a workspace
depending on their role.

**Action**| **Guest user**| **Login-only**| **User**| **Admin**| **Super
Admin**| **Owner**  
---|---|---|---|---|---|---  
Perform the initial workspace setup from an invite.|  |  |  |  |  | Yes  
Set up single sign-on (SSO) and user provisioning with a corporate identity provider (IdP).|  |  |  | Yes*| Yes*| Yes  
Access and update the workspace configuration.|  |  |  | Yes| Yes| Yes  
  
* Read-only permissions

**Table 1.** Workspace setup actions

## **Workspace management**

**Table 2** shows the actions users can perform to manage a workspace
depending on their role.

**Action**| **Guest user**| **Login-only**| **User**| **Admin**| **Super
Admin**| **Owner**  
---|---|---|---|---|---|---  
Access the **Activity** view.| Yes|  | Yes| Yes| Yes| Yes  
View all events within the workspace and for all users through the **Activity** view.|  |  |  | Yes| Yes| Yes  
View the events for the items they are **Owners** through the **Activity** view.| Yes|  | Yes| Yes| Yes| Yes  
View the billable accounts through the **Billing** view.|  |  |  | Yes| Yes| Yes  
Access the **Automation** view.| Yes| Yes | Yes| Yes| Yes| Yes  
View all automation notifications through the **Automation** view.|  |  |  |  |  | Yes  
  
**Table 2.** Workspace management actions

## **User management**

**Table 3** shows the actions users can perform to manage other users
depending on their role.

**Action**| **Guest user**| **Login-only**| **User**| **Admin**| **Super
Admin**| **Owner**  
---|---|---|---|---|---|---  
Assign Cerby products available to users through the **Teams** view.|  |  |  | Yes| Yes| Yes  
Assign or update the workspace-level role of other users.|  |  |  | Yes| Yes| Yes  
Access the **All Members** view.|  |  | Yes| Yes| Yes| Yes  
View all workspace **Users** , **Guest users** , and **Login-only** users through the **All Members** view.|  |  |  | Yes| Yes| Yes  
Export a report of users and their accounts through the **All Members** view.|  |  |  | Yes| Yes| Yes  
View and invite **Guest users**.|  |  | Yes| Yes| Yes| Yes  
Remove any **Guest user**.|  |  |  | Yes| Yes| Yes  
Access the **Teams** view.| Yes|  | Yes| Yes| Yes| Yes  
Create and manage a self-managed team.|  |  | Yes| Yes| Yes| Yes  
Delete any self-managed team.|  |  |  |  |  | Yes  
Manage **Team Members** on all self-managed teams.|  |  |  |  |  | Yes  
Assign **Team Admins** for any self-managed team.|  |  |  | Yes| Yes| Yes  
View all teams and **Team Members** within a workspace.|  |  | Yes| Yes| Yes| Yes  
View the teams to which they have been assigned and the **Team Members**.|
Yes| Yes| Yes| Yes| Yes| Yes  
Access the **Distribution Lists** view.|  |  | Yes| Yes| Yes| Yes  
Create a distribution list.|  |  |  | Yes| Yes| Yes  
View all distribution lists within a workspace.|  |  |  | Yes| Yes| Yes  
Remove distribution lists to which they are **Owners**.|  |  |  | Yes| Yes| Yes  
Update the name of a distribution list, add or remove members, and delete distribution lists to which they are **Owners**.|  |  |  | Yes| Yes| Yes  
Access the **Partners** view.|  |  | Yes| Yes| Yes| Yes  
View all partnerships within the workspace.|  |  |  | Yes| Yes| Yes  
Add a host-guest partnership.|  |  | Yes| Yes| Yes| Yes  
Approve a host-guest partnership request in the host workspace.|  |  |  | Yes| Yes| Yes  
Accept a host-guest partnership request in the guest workspace.|  |  |  | Yes| Yes| Yes  
View all guest workspace members with access to the accounts shared through the partnership.|  |  |  | Yes| Yas| Yes  
Add and remove a local partner.|  |  |  | Yes| Yes| Yes  
Manage users in a local user workspace:

  * Add new users.
  * Update the workspace-level role of other users.
  * Reset multi-factor authentication (MFA).
  * Force password reset.
  * Remove users from the workspace.

|  |  |  | Yes| Yes| Yes  
Invite guest users to join Cerby through the**All Members** view or the Password Manager Importer.|  |  | Yes| Yes| Yes| Yes  
  
**Table 3.** User management actions

## **Security hygiene tasks**

**Table 4** shows the security hygiene tasks users can perform depending on
their role.

**Action**| **Guest user**| **Login-only**| **User**| **Admin**| **Super
Admin**| **Owner**  
---|---|---|---|---|---|---  
Automate turning on MFA for all Cerby-managed accounts through the **Policies** view.|  |  |  | Yes| Yes| Yes  
Automate rotating passwords for all Cerby-managed accounts through the **Policies** view.|  |  |  | Yes| Yes| Yes  
  
**Table 4.** Security hygiene tasks

## **Item management**

**Table 5** shows the actions users can perform to manage items depending on
their role.

**Action**| **Guest user**| **Login-only**| **User**| **Admin**| **Super
Admin**| **Owner**  
---|---|---|---|---|---|---  
Access the **Import report** view.|  |  | Yes| Yes| Yes| Yes  
Import items into Cerby through the [Password Manager Importer](https://help.cerby.com/en/articles/7175132-how-to-use-the-password-manager-importer).|  |  | Yes| Yes| Yes| Yes  
Add an account, secret, or collection to Cerby.|  |  | Yes| Yes| Yes| Yes  
Save accounts at login and signup.|  |  | Yes| Yes| Yes| Yes  
Access the **Apps** view.|  |  | Yes| Yes| Yes| Yes  
Connect an app integration to Cerby.|  |  | Yes| Yes| Yes| Yes  
Share items to which they have the **Owners** role and assign the item role to other users (read the Item-level roles section).|  |  | Yes| Yes| Yes| Yes  
Share items to which they have the **Owner** role with any **Guest User** of a local partner.| Yes**|  | Yes| Yes| Yes| Yes  
Turn on **All-Access Mode** to view all accounts within the workspace and recover accounts by reassigning account **Owners**.|  |  |  |  | Yes| Yes  
View all the items shared with all teams.|  |  |  |  | Yes| Yes  
  
** Only when accounts are shared with the **Manager** role

**Table 5.** Item management actions

* * *

# **Item-level roles**

Item-level roles determine the actions users can perform on items, and they
can be categorized as follows according to the item type:

  * Accounts

  * Secrets

  * Collections

The following sections describe the actions for each item type.

## **Accounts**

**Table 6** shows the actions users can perform on accounts depending on their
role.

**Action**| **Manager**| **Collaborator**| **Owner**  
---|---|---|---  
Log in to an account.| Yes| Yes| Yes  
View the account details.| Yes| Yes| Yes  
Copy the password of an account.| Yes| Yes| Yes  
View the [account notes](https://help.cerby.com/en/articles/8076365-how-to-
save-and-manage-account-notes) and [custom
fields](https://help.cerby.com/en/articles/8076378-how-to-add-and-manage-
custom-fields-for-your-accounts) of an account.| Yes| Yes| Yes  
View the password of an account.|  |  | Yes  
Update the account details.|  |  | Yes  
Share an account with other users.| Yes**+|  | Yes  
Manage shared access to accounts:

  * View the members and teams with shared access to an account.
  * Add and remove **Collaborators** from an account.
  * Change the role of other users and teams on an account.

|  |  | Yes  
Manage the account security by turning on MFA or rotating passwords automatically from Cerby.|  |  | Yes*  
Manage second factors (Cerby-managed email address and phone number) for an account.|  |  | Yes  
View the **Shared Inbox**.| Yes| Yes| Yes  
View account activity.|  |  | Yes  
Delete an account.|  |  | Yes  
  
*** They can request access for other users.

**Table 6.** Actions on accounts

## **Secrets**

**Table 7** shows the actions users can perform on secrets depending on their
role.

**Action**| **Collaborator**| **Owner**  
---|---|---  
View the content of a secret.| Yes| Yes  
Update the details of a secret (name, body, and attachments).|  | Yes  
Manage shared access to secrets:

  * View the users and teams with shared access to a secret.
  * Share a secret with other users.
  * Add and remove **Collaborators** from a secret.
  * Change the role of other users and teams on a secret.

|  | Yes  
Delete a secret.|  | Yes  
  
**Table 7.** Actions on secrets

## **Collections**

**Table 8** shows the actions users can perform on collections depending on
their role.

**Action**| **Collaborator**| **Owner**  
---|---|---  
View the accounts and secrets within a collection.| Yes| Yes  
View the collection details.| Yes| Yes  
Update the collection details.|  | Yes  
Manage shared access to secrets:

  * View the users and teams with shared access to a collection.
  * Share a collection with other users.
  * Add and remove **Collaborators** from a collection.
  * Change the role of other users and teams on a collection.

|  | Yes  
Delete a collection.|  | Yes  
  
**Table 8.** Actions on collections

* * *

# **Team-level roles**

Team-level roles determine the actions users can perform on a self-managed
team. **Table 9** shows these actions.

**Action**| **Team Member**| **Team Admin**  
---|---|---  
Receive access as **Owner** or **Collaborator** to the items shared through
the team.| Yes| Yes  
View all the accounts, secrets, and collections shared with the team.| Yes|
Yes  
Manage the **Team Members** of a self-managed team:

  * Add and remove **Team Members**.
  * Assign **Team Admins**.

|  | Yes  
Remove a self-managed team.|  | Yes  
  
**Table 9.** Actions on teams

* * *

# **Partnership-level roles**

Partnership-level roles determine the actions users can perform on host and
guest workspaces and on local partners. **Table 10** shows the actions on a
host-guest partnership:

**Action**| **Manager**| **Guest workspace Admin**| **Host workspace Admin**|
**Partnership Owner**  
---|---|---|---|---  
Share accounts to which they have the **Owner** role with a guest workspace.|  |  |  | Yes  
Remove accounts shared with a guest workspace. |  |  |  | Yes  
Receive access as **Collaborator** or **Manager** to the accounts shared through the partnership.|  | Yes|  |   
View all guest workspace members with access to the accounts shared through the partnership.|  |  | Yes| Yes  
Manage users in the host workspace.|  |  | Yes|   
Manage users in the guest workspace.|  | Yes|  |   
Send requests to item **Owners** from the host workspace asking them to share an account.| Yes|  |  |   
Remove a host-guest partnership.|  | Yes| Yes| Yes  
  
**Table 10.** Actions on host-guest partnerships

**Table 11** shows the actions users can perform on a local partner:

**Action**| **Manager**| **Guest user**| **Guest Admin**| **User**| **Host
Admin**  
---|---|---|---|---|---  
Share items to which they have the **Owner** role with a local partner.|  |  |  |  | Yes  
Receive access as **Collaborator** or **Manager** to the accounts shared through a local partner.|  |  | Yes|  |   
Send requests to item **Owners** asking them to share an account.| Yes|  |  |  |   
Invite **Guest Users** to a local partner.|  |  | Yes|  | Yes  
Assign a **Host Admin** to a local partner.|  |  |  |  | Yes  
Manage guest members of a local partner:

  * Update the role of **Guest Admins** and **Guest Users**.
  * Remove**Guest Admins** and **Guest Users** from a local partner.

|  |  | Yes|  | Yes  
  
**Table 11.** Actions on local partners

* * *

# **Benefits of RBAC**

The following are the benefits of using the RBAC system in Cerby:

  * **Enhanced security:** Access to sensitive data and features is restricted. Only users with specific roles can perform critical actions, reducing the risk of unauthorized access and data breaches.

  * **Access control:** Fine-grained control over what users can and cannot do. Administrators can assign roles and permissions according to each user's job responsibilities.

  * **Compliance and auditing:** Organizations can implement access controls and audit trails, which are essential for demonstrating data security and compliance with industry and legal standards.

  * **Streamlined onboarding and offboarding:** New employees can be quickly assigned the appropriate roles and permissions while departing employees can have their access revoked just as easily.

  * **Efficient collaboration:** Users have the necessary access to work together effectively. RBAC allows organizations to balance the need for collaboration with the need for data security.

  * **Resource management:** RBAC assists in optimizing resource allocation. It ensures that resources are used efficiently and that access to costly or limited resources is restricted to only those who require them.

  * **Transparency:** RBAC offers transparency in access control, making it clear who has access to what resources and why. This transparency can foster trust and accountability within an organization.

