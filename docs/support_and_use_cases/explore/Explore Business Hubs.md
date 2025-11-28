# Explore Business Hubs

**Description:** This article describes the key benefits of the Business Hubs to manage the users and assets of your external seat-based and paid social apps

With Cerby’s **Business Hubs** , you can connect all your external seat-based
and paid social apps–even disconnected or nonfederated apps–to your workspace
for centralized user and asset management.

Business hub integrations enable data synchronization between your apps and
Cerby, so you can use only one platform to automate the following user and
access management tasks:

  * Add users to your app

  * Remove users from your app

  * Update user roles in your app

When you have a Cerby workspace configured with an identity provider (IdP),
such as Okta or Entra ID, user and group provisioning and deprovisioning
events can trigger these management tasks. For more information about how this
identity lifecycle management approach works, read the section Extended user
and access management from your IdP.

The main goal is to ensure your employees and even your external collaborators
(contractors, agencies, or partners) have the right access at the right time
and with the least privileges. The following are other benefits of the
Business Hubs feature:

  * Extend single sign-on (SSO) to disconnected or nonfederated apps.

  * Track the progress of user management automated tasks.

  * Secure user access by requiring accounts to have multi-factor authentication (MFA) turned on and setting up password rotation policies.

  * Retrieve full audit trails for governance.

Business hub integrations are intended for apps that have collaboration spaces
(workspaces, teams, or dashboards) to which users access with different roles
and permissions. Admins manage user access by leveraging individual seats or
licenses instead of shared sessions. Some examples of seat-based and paid
social apps are Meta Business Manager, TikTok for Business, Apple, Asana,
Atlassian, Calendly, and GitHub.

To perform user and access management tasks, the following is the user data
synced between Cerby and your apps:

  * Users or members

  * App roles and permissions

  * Assets (only for the apps that support them), such as ad accounts, pages, pins, videos, and stories

  * Native partners (only for the apps that support them)

* * *

# **The Business Hubs page**

The **Business Hubs** page in the Cerby web app dashboard is the centralized
view of all your connected integrations, as shown in **Figure 1**. Through
this interface, you can manage user access to your external seat-based and
paid social apps.

![ Screenshot of the Cerby web app dashboard. The Business Hubs page is
displayed with a table of connected integrations and a wizard at the right
side of the page for connecting your app to
Cerby.](images/AD_4nXeiLDt5UT4k1b4b1OyNDlfKkK_0UTQpUUWsITR0kJZkreBldlcJd_HTqSqFPgrqLsgyCmObThCy41HLlW7h3lRegFh8mCTgIwbijSt9GE8yHeyKzJU8TtsWu-
SKpVtMZYb2K20Lnw)

**Figure 1.** **Business Hubs** page in the Cerby web app dashboard

In the **Business Hubs** page, you can view the list of business hubs that
have already been connected to your app. From there, you can navigate to the
business hub details page to explore more information, such as the table of
synced user data and the imported assets.

## Users tab

The **Users** tab, as shown in **Figure 2** , contains the tables listing all
users with access to your external app. This tab is accessible through the
business hub details page for business hub **Owners.**

![Screenshot of the Cerby web app dashboard. The business hub details page is
displayed with a table listing the Unmatched
users.](images/AD_4nXcrKNW5eKCsxw-A4LCk_fzcF3SbRP596Qj-
JUjcSMCl8yaHwkegnagEZRATiszI3VPMNHzKOU8w5ya0bGj302JS0YzwVjRDTAQOHxqeOTNzDPPeVlU-73pf1V1J-kLsMPXy_buV-A)

**Figure 2**. **Users** tab in the business hub details page

The external app users are displayed in the following tables in the **User
Overview** section:

  * **Unmatched users:** This tab displays the users who were not automatically matched because they use an email address that couldn’t be identified or they are not in the corporate directory. The following details are provided for each user:

    * **Account members:** It lists the username given to the users in the external app.

    * **App access:** It lists the roles assigned to the users in the external app.

    * **Status:** It shows the status of the users within the Cerby onboarding process. The possible values are the following:

      * **External enrollee:** The user was discovered in the external app, but was not automatically matched.

  * **Onboarded users:** This tab displays the users matched to their Cerby user account. The following details are provided for each user:

    * **Account members:** It lists the username and email of the Cerby user accounts associated with the app user accounts.

    * **Cerby role:** It lists the roles assigned to the users on the business hub integration. The possible values are the following:

      * **Owner:** The user can share access and manage the integration. 

      * **Collaborator:** The user can only log in to the app.

      * **Manager:** The user**** can share access and log in to the app. 

      * **Mixed roles:** The user received access multiple times, resulting in more than one role.

    * **App access:** It lists the roles assigned to the users in the external app.

    * **Shared via:** It lists the methods by which the users were granted access to the external app. 

    * **Last used:** It is the date and time of the user's most recent activity.

    * **Security status:** It indicates the security status of the connected account. The possible values are the following:

      * **Pending Cerby onboarding:** The user is pending capture of their credentials in Cerby.

      * **Invite sent:** The user is pending acceptance of the invite from the external app.

      * **Invite failed:** The process of sending the user invite failed.

      * Cerby onboarded: The user has been matched to their Cerby account and has captured their credentials.

      * **Cerby only:** The user can access Cerby but not the external app.

      * Single Sign On: The user logs in via SSO. Hence, users are not asked to save their credentials in Cerby.

      * **Managed Outside Cerby:** The user logs in using their username and password; however, they are not asked to save their credentials in Cerby.

  * **Guest users:** This tab displays the users who were matched to user accounts but they don’t exist in the corporate directory, such as external collaborators. The following details are provided for each user:

    * **Account members:** It lists the username given to the users in the external app.

    * **Cerby role:** It lists the roles assigned to the users on the business hub integration. The possible values are the following:

      * **Owner:** The user can share access and manage the integration. 

      * **Collaborator:** The user can log in to the app.

      * **Manager:** The user**** can share access and log in to the app. 

      * **Mixed roles:** The user received access multiple times, resulting in more than one role.

    * **App access:** It lists the roles assigned to the users in the external app.

    * **Shared via:** It lists the methods by which the users were granted access to the external app. 

    * **Last used:** It is the date and time of the user's most recent activity.

    * **Security status:** It indicates the security status of the connected account. The possible values are the following:

      * **Invite sent:** The user is pending acceptance of the invite from the external app.

      * **Pending Cerby Onboarding:** The user is pending capture of their credentials in Cerby.

      * **Single Sign On:** The user logs in via SSO. Hence, users are not asked to save their credentials in Cerby.

  * **Exempted:** This tab displays the users exempted by an integration **Owner**. These users keep their app user account active but not manageable through Cerby. The following details are provided for each user:

    * **Account members:** It lists the username given to the users in the external app.

    * **App access:** It lists the roles assigned to the users in the external app.

    * **Reason for exemption:** It lists the reasons indicated by the integration Owner as to why the user was exempted. 

    * **Status:** It shows the status of the users within the Cerby onboarding process. In this case, it will always show as Exempt.

* * *

# **Key concepts**

**Table 1** contains the key concepts that are essential for understanding the
Business Hubs feature:

**Concept**| **Description**  
---|---  
**App role**|  It is the role assigned to a user in a seat-based or paid
social app. These roles vary depending on the app.  
**Asset** | It is a resource or entity associated with and managed by seat-based and paid social apps for specific purposes, like advertising and marketing. In Cerby, assets are properties of a business hub.   
**Asset role**|  It determines the actions users can perform on an asset in
the external app.  
**Automated job**|  It is an app-specific task executed by Cerby using
technology that automates repetitive tasks in login and signup interfaces.  
**Business ID**|  It is the unique identifier assigned to the collaboration
space (workspace, team, dashboard, business manager, or business center) of an
external app. This ID is not always required.  
**Cerby agent**|  It is the component of the Cerby platform that executes the
automated jobs to perform user and access management tasks on connected apps.  
**Cerby role**|  It is the role of users and teams on a business hub
integration in Cerby. These roles are similar to the ones you have on
accounts.  
**Check for updates**|  It is the automated task that extracts user data from
your app to sync it with Cerby.  
**Claim invite or access**|  It is a flow in which users decide when to
receive an invite to join an app. Claiming an invite or access is mandatory
when sharing a business hub integration through a collection.  
**Connected account**|  It is a user account added to Cerby and associated
with an integration that enables users to log in to an app from Cerby via an
automated task.  
**External app**|  It is a seat-based or paid social app connected to Cerby
through a business hub integration.  
**Guest user**|  It is a user who was matched to their Cerby guest user
account but doesn’t exist in the corporate directory.  
**Integration**|  It is the connector between Cerby and the collaboration
space of your seat-based or paid social app. It enables you to invite and
remove users from your apps, as well as update their roles, via automated
tasks.  
**Integration onboarding**|  Is the process of creating, configuring, and
connecting a business hub for your app.  
**Local partner**|  It is an external collaborator with access to your Cerby
workspace, to whom you can directly share access to your items and assets.  
**Native partner**|  It is a business or organization (agency, media planner,
or consultant) already existing as a partner in your paid social apps for
collaboration purposes in ad campaigns.  
**Onboarded user**|  It is a user who was matched automatically to their Cerby
user account during a check for updates or manually from the table of
unmatched users.  
**Service account**|  It is an app account added to Cerby and associated with
an integration to execute automated user management tasks.  
**Unmatched user**|  It is a user who was not automatically matched to their
Cerby user account during a check for updates because they use an email
address that couldn’t be identified or they are not in the corporate
directory.  
  
**Table 1.** Business hub key concepts

* * *

# **How business hub integrations work**

Cerby's business hub integrations are connectors between Cerby and your
external apps. These connectors enable you to centralize user access
management for all your apps and assets (if supported) in one interface.

To connect a business hub to an external app, you need an associated [service
account](https://help.cerby.com/en/articles/9830816-create-an-automation-or-
service-account-for-your-business-hub) or token, and provide specific details
about your app. With this information, the Cerby agent can access your app
server-side to perform the supported user and access management tasks through
automated jobs or API calls.

{% hint style="info" %} **NOTE:** Whenever supported by the app, Cerby
prioritizes API calls over automated jobs. {% endhint %}

Right after connecting a business hub, the first automated job Cerby performs
is a check for updates. This job involves syncing user data (users, roles, and
assets if supported) with your external app and matching users with their
Cerby user accounts, whether provisioned by an IdP or by Cerby, such as [guest
users](https://help.cerby.com/en/articles/8392946-explore-guest-users) and
[local partners](https://help.cerby.com/en/articles/8980877-explore-
partners#h_7e4add33a2).

For apps supporting the [native
partners](https://help.cerby.com/en/articles/8980877-explore-
partners#h_e7fa9c355c) feature, you can also gain visibility on the users who
access your assets to run ad campaigns on your partner's side.

With the user matching, Cerby knows on which users perform the access
management tasks triggered by a business hub. For matched users, Cerby
displays a business hub account card. Depending on the user login method
selected by integration **Owners** , users might be prompted to connect their
app user accounts to Cerby. With this connection, you can secure access for
these users with policies to turn on MFA and rotate passwords.

If your workspace is integrated with an IdP, you can perform all the supported
access management tasks for your external apps based on user and group
provisioning and deprovisioning events. For more information, read the section
Extended user and access management from your IdP.

**Figure 3** shows a diagram of how a business hub integration in Cerby is
connected to your IdP and your external app.

![](images/AD_4nXfuvcO1Ku-4DbwjpcXBfVT0zjFHJFzV-M4F92CwfJ32vUljWtVXuCQeyUuT_ct7IHR6J0C-Pcn_zyUAGiBsFR5JVSE8f4Ddx2aE24Ipb9k8kandahHmwNo7l7YBvw-8vmS0QBO8sw)

**Figure 3.** Diagram of a Cerby business hub integration

The main functionalities of a business hub integration are the following:

  * User and access management tasks

  * Extended user and access management from your IdP

  * Business hub integration management in Cerby

  * External app role management

  * User management and login method

  * Connected account management

The following sections describe each functionality.

## User and access management tasks

The following are the user and access management tasks you can perform on your
external apps via a business hub integration:

{% hint style="info" %} **NOTE:** The availability of management tasks varies
from app to app. For example, for some apps it is not possible to update roles
because they only support one role natively. {% endhint %}

  * **Check for updates:** The Cerby agent syncs the user data of your external app and generates a report listing all users, including their roles and assets (if supported).

  * **Add users:** The Cerby agent creates the user accounts in your external app with the specified roles, including assets (if supported), triggering the corresponding invites through email.

  * **Update user roles:** The Cerby agent updates the native user roles in your external app and its assets (if supported).

  * **Remove users:** The Cerby agent removes the user accounts from your external app, including assets (if supported).

Additionally, Cerby supports the following automated tasks for partners that
natively exist on paid social apps, such as Meta Business Manager or TikTok
For Business:

  * **Monitor partners:** The Cerby agent syncs, upon [native partner](https://help.cerby.com/en/articles/8980877-explore-partners#h_e7fa9c355c) onboarding, the data of the partner’s users who have shared access to the assets you own or that a partner shared with your paid social app, including their roles and the list of assets. 

  * **Manage partner assets:** The Cerby agent assigns, upon native partner onboarding, roles and assets to a specific native partner of your app.

## Extended user and access management from your IdP

When you have a workspace configured with an IdP, using the SCIM standard for
automatic user provisioning, you can extend the provisioning capability to the
user and access management tasks of a business hub.

To achieve this extended identity lifecycle management functionality, Cerby
leverages user and group provisioning and deprovisioning from your IdP to
create, update, and remove Cerby teams. These teams have shared access to a
business hub integration with specified roles or permissions both in Cerby and
the external app, including assets (if supported). Each team has a specific
set of roles assigned.

**Figure 4** shows how users are provisioned and deprovisioned from IdP
events, triggering the corresponding tasks in the external app.

![Diagram of a Cerby business integration leveraging identity provider events.
The diagram shows the multiple systems involved, such as the identity
provider, Cerby, and the external app, and the components, such as users,
groups, teams, the business hub integration, and user and acces management
tasks.](images/AD_4nXcL3yeqghP4bQ6DN79odnxiUKoxNRwxl1hszGSuitIHwtljZ3B3NZU3bVmZlXrzvzKal_auzL8h7rQRiw8LDrk1IVgh_1puU0_mGXxhjk2ppgxFuMDuBNdWcDj1sJVfw3Yfge09Aw)

**Figure 4.** Extended user and access management tasks from IdP user and
group provisioning and deprovisioning events.

With this setup, Cerby detects automatically when users are added or removed
from IdP groups, deleted, and deactivated, and propagates these changes to the
external app based on the role that the corresponding Cerby teams have on the
business hub integration.

For role updates, you must complete a two-step process that involves adding
users to the new IdP group and then removing them from the old group. The goal
is to avoid triggering user account removals from the external app.

## Business hub integration management in Cerby

A business hub integration is like other regular accounts you add, protect,
and manage through Cerby because users and teams are granted access to them
with the **Owner** or **Collaborator** role. Also, you can group business hubs
in a collection.

However, sharing and removing access to an integration is the way you trigger
the automated tasks to add and remove users from your external app.

The management actions you can perform on a business hub integration are the
following:

  * Cerby role assignments

  * Integration sharing

The following sections describe each action.

### **Cerby role assignments**

As mentioned above, Cerby role assignments on business hub integrations are
similar to accounts.

The user who connects a business hub for their app becomes the integration
**Owner**. After they perform the first check for updates, all matched users
automatically receive shared access to the business hub with the
**Collaborator** role.

Only integration **Owners** can share a business hub integration and assign
the following Cerby roles to other users and teams:

  * **Owner:** It enables users and teams to perform the supported user and access management tasks via the business hub. They can also update the business hub settings and log in to the external app through Cerby.

  * **Collaborator:** It enables users and teams to only log in to the external app through Cerby.

  * **Manager:** It enables users and teams to perform the supported user and access management tasks via the business hub and log in to the external app through Cerby.

When assigning the **Owner** role, you can choose whether to grant users and
teams a seat on the external app. If you don't grant them a seat, they can
still perform user and access management tasks for other users and teams. This
option is helpful for IT admins who need to manage access but don't require a
licensed user account.

Before assigning a user with an **Owner** role, you must ensure you have
previously shared the service account with them. Otherwise, the user will
automatically be granted the **Security Manager** role, limiting their
capabilities to only executing user management tasks from the business hub via
automation.

On the other hand, when assigning the **Collaborator** role to other users and
teams, Cerby always executes the automated task to add them to the external
app.

For more information about roles on business hubs, read the article [How Cerby
manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-
roles).

### **Integration sharing**

In addition to assigning different Cerby roles, sharing a business hub
integration has different outcomes depending on whether you share one or
multiple integrations within a collection.

When you share one integration with other users and teams, Cerby automatically
executes the automated jobs to add them to the external app. Therefore, all
users receive their invites to join the app.

If your app supports assets, you can also share them individually with other
users and teams. In this case, Cerby executes the automated jobs to add users
both to the external app and to the assets because they typically follow a
hierarchical structure.

When you share a collection of business hub integrations with other users and
teams, Cerby waits until users claim access to execute the automated tasks to
add them to the external app. Therefore, invites are also sent after they
claim access.

The goal is to prevent invites from expiring and users from having to reach
out to integration **Owners** for a new invite.

If your app supports assets, you can add individual assets to a collection.
When you share the collection, Cerby waits until users claim access to execute
the automated jobs to add users both to the external app and to the assets.

## External app role management

For all business hub integrations, Cerby maps all the roles and permissions
supported by the external app. These roles are independent of the ones
described in the Cerby role assignments section because they determine what
users can do in the app.

During a check for updates, Cerby syncs these roles and permissions to match
them with the corresponding workspace users. This information is displayed in
the tables of users and teams within the business hub details page, where you
can also trigger automated tasks to update user and team roles in your app.
For more information, read the articles [Update user roles in your app via a
business hub](https://help.cerby.com/en/articles/9046201-update-the-app-
members-roles) and [Update team member roles in your app via a business
hub](https://help.cerby.com/en/articles/11139474-update-team-member-roles-in-
your-app-via-a-business-hub).

When you share a business hub or a collection of business hubs with other
users and teams, you specify which app role to assign to them. When Cerby
executes the automated job to add the users to the external app, these roles
are assigned.

Cerby has a weighted role management system to determine which role to assign
to users when they have shared access to a business hub integration in
multiple ways. This weighted system only applies to external apps with
hierarchical roles (for example, **Admins** , **Managers** , **Editors** , and
**Viewers**), and Cerby always assigns users the highest role based on their
existing access grants.

When the external apps have nonhierarchical permissions (for example, **Add
Comments** , **Delete** **Files** , **View Campaigns** , and **Create
Campaigns**), the weighted system is not relevant.

It’s important to note that roles and permissions vary from app to app.

## User management and login method

The user management and login method of a business hub integration is the way
your users log in to the external app. This method also determines whether
they must save their login credentials as a Cerby account connected to the
business hub.

You can select one of two user management and login methods depending on the
setup of your app:

  * **Single sign-on (SSO):** Access is managed via your IdP, and users log in via SSO authentication. In this case, users are not asked to save their credentials in Cerby, and they continue accessing their seat-based and paid social apps as usual.  
​**NOTE:** Google social login is supported through your IdP. Okta is used to
access your Google account and establish an authenticated session, which can
then be used to log in to your external app.

  * **Username and password:** Account security and access are managed from Cerby, and users log in to their external apps through Cerby. In this case, users are asked to save their credentials in Cerby and connect them to the business hub integration; therefore, you can implement and automate the following security policies on user accounts:

    * Turn on MFA

    * Rotate passwords

## Connected account management

Business hub integrations rely on connected accounts for automated logins to
external apps. A connected account links a user’s Cerby account to their
individual account on an external app, allowing seamless and secure access.

In contrast, service accounts are not tied to individual users. Instead, they
are linked directly to a business hub and are connected by the integration
**Owner**. Service accounts are typically used by the Cerby agent to perform
automated jobs, such as user management, rather than to log in to external
apps on behalf of a specific user.

When users are invited to a seat-based or paid social application, they must
accept the invite, create an account in the app, and connect that account to
Cerby. This connected account is what enables them to access the external app
through Cerby.

