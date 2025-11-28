# How to use Teams

**Description:** This article describes how to configure and use the Teams feature in Cerby to share accounts with groups of users.

With Cerby, you can simplify user and access management through Teams. This
feature helps you and your company support groups of users assigned to
accounts or collections and apply changes in access rights and user account
provisioning automatically to all group members.

You have the following two options to create teams in Cerby:

  * Create a group of users in the corporate directory managed by your identity provider (IDP), such as Okta and Azure AD, and replicate it automatically as a team in Cerby.

  * Create a team manually in Cerby with the members of your corporate directory.

Currently, Cerby supports replicating groups from Okta as an IDP. With the
Group Push feature, existing Okta groups and their members are passed to the
Cerby app integration via the System for Cross-domain Identity Management
(SCIM) specification.

First, IT admins map these groups in the corporate directory in Okta to
replicate their corporate structure (for example, to map regions or
departments within a company). Then, **Workspace Admins** create teams in
Cerby based on the existing Okta group mapping via Group Push.

For the teams created manually in Cerby, you only have to follow the steps in
the **Create team** wizard.

When the team is available in Cerby, the following two roles are introduced:

  * **Team Member:** It is a role that determines whether a user is part of a team. Resources (accounts and collections) are shared with teams by users with the **Account Owner** role over these resources. The **Account Owner** or **Account Collaborator** role assigned to the team when sharing resources determines how all **Team Members** can use and access such resources. 

  * **Team Admin:** It is a role with permissions to manage the members of a specific team and see all the accounts and collections shared with the team. **Workspace Admins** can assign **Team Admins** after creating a team from the IDP, and **Team Admins** assume the role automatically when creating a team manually in Cerby.

This article describes how to configure and use the Teams feature in Cerby.

# Requirements

The following are the requirements to configure and use Teams in Cerby:

  * A workspace in Cerby

  * To create a team manually in Cerby:

    * Users already provisioned to your workspace via an IDP

  * To replicate automatically the group from your IDP:

    * A user account in Okta with privileges to manage the Cerby app integration, groups, and users in your Okta tenant 

  * A user account in Cerby with the **Workspace Admin** role

# Configure and create a team

To configure and create a team, you must complete the following steps
depending on the source of its members:

  * Automatically from a group in your IDP

  * Manually with members within Cerby

**IMPORTANT:** You can only configure and create a team following one of the
two options above, which means you can’t combine them.

The following sections describe each option.

## **Automatically from a group in your IDP**

To configure and create a team from a group in your IDP by using the only
supported option with Okta, you must complete the following steps:

  1. Create a group in Okta. For more instructions, see the [Manage groups](https://help.okta.com/en/prod/Content/Topics/users-groups-profiles/usgp-groups-main.htm) official documentation in the Okta Help Center.

  2. Assign the group to the Cerby app integration in Okta. For instructions, see the [Assign Users and Groups to the Cerby App](https://help.cerby.com/en/articles/5457568-how-to-configure-sso-between-cerby-and-okta-with-saml#h_75528a1136) section in the [How to Configure SSO Between Cerby and Okta with SAML](https://help.cerby.com/en/articles/5457568-how-to-configure-sso-between-cerby-and-okta-with-saml) article.

  3. Configure the Group Push feature to push the Okta group to Cerby. For instructions, see the [Configure Group Push between Okta and Cerby](https://help.cerby.com/en/articles/5457593-how-to-enable-okta-user-provisioning-with-scim#h_7a240472ca) section in the [How to Enable Okta User Provisioning with SCIM](https://help.cerby.com/en/articles/5457593-how-to-enable-okta-user-provisioning-with-scim) article.

  4. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.

  5. Select the **Teams** option from the left navigation drawer. The **Teams** view is displayed with the group and users you pushed from Okta, as shown in **Figure 1**.

**NOTE:** Okta groups and users correspond to Cerby teams and members.

![Teams View of the Cerby
Dashboard](images/PuljkfG4RaeQl8SbvaXe6KSqvi2CzzaNuofS8poPzAfOFwY9a2gum1t7unV0fkLepMK8cmXHW6a6mqUVf3KnP22qKJwNh9BoC2E2wGbyTZJRxmMvPkdySuH4wWjCULT9cbONvRmYnynRy69MEEUmBPhpIcZIJT_3CRNG-
DAgLhxa73C6_3DW8bBu6g)

**Figure 1. Teams View of the Cerby Dashboard**

Now you are done. Continue to the Use the supported features of Teams section.

## **Manually with members within Cerby**

To create a team manually by adding the members of your corporate directory
within Cerby, you must complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Teams** option from the left navigation drawer. The **Teams** view is displayed.

  3. Click the **Add** or **Create team** button depending on whether you have previously created a group or not. The **Create team** wizard is displayed with the **Name your team** page.

  4. Enter the name of the team in the **Name** field.

  5. Click the **Next** button. The **Add members** page is displayed.

  6. Enter in the search bar the name or email address of the member you want to add to the new team. The users that match the search criteria are displayed in a list.

  7. Select the corresponding user from the list. The **Members** section and the selected user are displayed.

  8. Repeat steps 6 and 7 as necessary.

  9. Click the **Create team** button. The wizard closes, and the new team and a success message box are displayed.

Now you are done. Continue to the Use the supported features of Teams section.

# Use the supported features of Teams

The following are the supported features of Teams:

  * Map new groups and manage group mapping

  * Add or remove users from groups automatically

  * Add or remove members from teams manually

  * Assign a Team Admin

  * Share and remove access to accounts

  * See teams and team members in Cerby

  * Manage or access accounts

  * Track activity on the shared accounts

  * Remove a team manually

The following sections describe each feature.

* * *

## **Map new groups and manage group mapping**

IT admins can create new groups in Okta according to changes in the corporate
directory. They can also monitor the status of Group Push to manage the group
mapping to the Cerby app integration.

For new Okta groups to be mapped to Cerby as teams, you must complete the
following steps:

  1. Create the group in Okta. For more information, see the [Manage groups](https://help.okta.com/en/prod/Content/Topics/users-groups-profiles/usgp-groups-main.htm) instructions from the Okta Help Center.

  2. Assign the group to the Cerby app integration. Follow the instructions to assign groups from the [How to Configure SSO Between Cerby and Okta with SAML](https://help.cerby.com/en/articles/5457568-how-to-configure-sso-between-cerby-and-okta-with-saml#h_75528a1136) article.

  3. Push the new group to Cerby. Follow the instructions to configure Group Push from the [How to Enable Okta User Provisioning with SCIM](https://help.cerby.com/en/articles/5457593-how-to-enable-okta-user-provisioning-with-scim) article.

According to your company's needs, you can manage the group mapping to Cerby.
To do so, you must complete the following steps in Okta:

  1. Select the **Applications** option from the **Applications** drop-down list located in the left navigation drawer. The **Applications** page is displayed.

  2. Select the **Cerby** option from the list of applications. The **Cerby** application page is displayed with the **General** tab activated.

  3. Activate the **Push Groups** tab. The **Push Groups to Cerby** page is displayed.

  4. Select the corresponding option from the **Push Status** drop-down list:

     * **Activate group push:** This option activates the group sync and starts pushing members.

     * **Deactivate group push:** This option pauses the group sync, but the group remains in Cerby. Any action over a group member in Okta (adding or removing them) is not passed to Cerby.

     * **Unlink pushed group:** This option removes the group permanently from Okta and Cerby. When you select it, **the Unlink Pushed Group** dialog box is displayed with two options:

       * **Delete the group in the target app:** This option deletes the group and all its associated members.

       * **Leave the group in the target app:** This option stops pushing members and keeps the group in Cerby.

     * **Push Now:** This option pushes members immediately and syncs Okta and Cerby.

* * *

## **Add or remove users from groups automatically**

When user provisioning is enabled through SCIM, and the Group Push is
configured with an **Active** status for a determined group in Okta, any
change in the users assigned to that group propagates to Cerby automatically.

IT admins can add or remove users from the group, which causes the
corresponding changes to the team and team members in Cerby. In the case of
users being deprovisioned from the corporate directory, they are automatically
removed from all the groups and teams they are members in Okta and Cerby,
respectively.

To see if the Okta group has an **Active** status and the mapping is updated
in Cerby, you must complete the following steps:

  1. Log in to the [Okta Admin Console](https://developer.okta.com/login/) of your organization.

  2. Select the **Applications** option from the **Applications** drop-down list located in the left navigation drawer. The **Applications** page is displayed.

  3. Select the **Cerby** option from the list of applications. The **Cerby** application page is displayed with the **General** tab activated.

  4. Activate the **Push Groups** tab. The **Push Groups to Cerby** page is displayed with a table of groups, as shown in **Figure 2**.

![Push Groups Tab in
Okta](images/CpQfTBAk4PKkNfXgMHOQld5iFvbR_Ay87h4duFk__uoRmcd30y9G6dsU-
SRakyEQfR_gF_YN6sCtHwik41ECDUIjcdhBMgs2AVnWAYdBD5uxZfzeCYG_XsBX9gGrxPFVlPF_vaWU9epYm9LGHUuqka3knebh2i9u-z0CvxtMzjS817S5cPe3UpIGdQ)

**Figure 2. Push Groups Tab**

  5. Verify the date and time of the last push and the Group Push status for the corresponding group. You can see this information under the **Last Push** and **Push Status** columns of the table.

**NOTE:** If Group Push was not updated recently, you can perform a manual
push. If the push status is **Inactive** , you can reactivate it. For more
information on performing both actions, see the Map new groups and manage
group mapping section.

* * *

## **Add or remove members from teams manually**

**Team Admins** can add or remove one or multiple members from a team created
manually in Cerby by performing the following steps from the **Teams** view:

  * Add one or multiple members

    1. Select the team from the **Your teams** list. The team members are displayed on a list in the main panel with the **Members** tab activated.

    2. Click the **Add members** button. The**Add members** dialog box is displayed.

    3. Enter in the search bar the name or email address of the member you want to add to the team. The users that match the search criteria are displayed in a list.

    4. Select the corresponding user from the list. The **Member** section and the selected user are displayed.

    5. Repeat steps 3 and 4 as necessary.

    6. Click the **Add members** button. The dialog box closes, and the new members and a success message box are displayed.

  * Remove a member

    1. Select the team from the **Your teams** list. The team members are displayed on a list in the main panel with the **Members** tab activated.

    2. Click the **More options** icon of the corresponding user. A drop-down list is displayed.

    3. Select the **Remove from team** option from the list. The **Remove member from a team** dialog box is displayed.

    4. Click the **Remove member** button. The dialog box closes and a success message box is displayed.

**NOTE:** When removing a member from a team, they automatically lose all
access to the accounts shared via a team.

* * *

## **Assign a Team Admin**

**Team Admins** can assign other users with the **Team Member** role as **Team
Admins** for the following user management tasks:

  * Add or remove members from teams manually

  * Remove a team manually

To assign a **Team Admin** , you must complete the following steps from the
**Teams** view:

  1. Select the team from the **Your teams** list. The team members are displayed on a list in the main panel with the **Members** tab activated.

  2. Click the **More options** icon of the corresponding user. A drop-down list is displayed.

  3. Select the **Assign team admin** option from the list. The **Make this member the Team Admin?** dialog box is displayed.

  4. Click the **Done** button. The dialog box closes and a success message box is displayed.

* * *

## **Share and remove access to accounts**

After creating a team in Cerby, even without any member assigned, **Account
Owners** can start sharing and removing access to accounts with teams within
the same workspace.

To share an account with a team, you must complete the following steps from
the **All accounts** view in the Cerby dashboard:

  1. Click the **Share Account** icon from the corresponding account card. The **Share Access** dialog box is displayed, as shown in **Figure 3**.

![Share Access Dialog
Box](images/PcQXok_JHe0fCPsL6mLhDKGoZPYkTKZGbCD71-4adSqmO9LBMnOn0i8Tm9PghmvfhytzPNXiHE9UuxS5A7Vq3OsBq7dWxvzDNeYqjBNYl_o0dWx-
svmc4l5tPMtT_cQCZyv1KoTyDy8-6Mo7PZV_VGp3_pWpU1-JARUyI7k5OqpjF0YfI9Tm4N4whQ)

**Figure 3. Share Access Dialog Box**

  2. Enter the name of the team in the search bar. The teams that match the name are displayed on a list below the search bar.

  3. Select the corresponding team from the list. The **Team** section is displayed with the team you selected.

**TIP:** Repeat steps 2 and 3 to select multiple teams.

  4. Select the corresponding role of the team over the account from the **ROLE** drop-down list:

     * **Owner:** This role enables sharing access and managing the account configuration.

     * **Collaborator:** This role enables only logging in to the account.

**NOTE:** The role assigned to the team applies to all the team members.

  5. Click the **Confirm** button. The **Confirm members** dialog box is displayed with all the team members on a list.

  6. Click the **Confirm** button. The dialog box closes and a success message box is displayed.

**NOTE:** When new users are assigned to a group from the IDP and then passed
and mapped to Cerby, access to the accounts already shared with the team is
granted automatically.

To remove an account from a team, you must complete the following steps from
the **Teams** view:

  1. Select the corresponding team from the list in the **Your teams** section. The team details are displayed in the main panel with the **Members** tab activated.

  2. Activate the **Accounts** tab.

  3. Click the **More actions** icon of the corresponding account. A drop-down list is displayed.

  4. Select the **Remove from team** option. The **Remove account from team** dialog box is displayed.

  5. Click the **Remove account** button. The dialog box closes and a success message box is displayed.

* * *

## **See teams and team members in Cerby**

No matter their role, all users can see the existing teams within a workspace
listed in the **Teams** view. However, only users with the **Team Member**
role and **Team Admins** can see the members of their team and all the
accounts shared with them.

To see the members and accounts of a team, you must complete the following
steps from the **Teams** view:

To see the members and accounts of a team, you must complete the following
steps:

  1. Select the team from the **Your teams** list. The team members are displayed on a list in the main panel with the **Members** tab activated.

  2. Activate the **Accounts** tab to display the list of accounts shared with the team.

* * *

## **Manage or access accounts**

When an account is shared with a team, the role assigned over this resource
determines what all team members can do.

With an **Account Owner** role, team members can log in to the accounts
through Cerby and manage the account settings. For example, they can turn on
multi-factor authentication (MFA) or create an email address and phone number
managed by Cerby. To access the account settings, click the **Settings** icon
from the corresponding account card in the**All Accounts** view.

With an **Account Collaborator** role, team members can only log in to the
accounts through Cerby. Access them as you normally would, via the account
cards in the **All accounts** view.

* * *

## **Track activity on the shared accounts**

Users and team members with the **Account Owner** role assigned over the
shared accounts can see the activity log for these accounts.

To track the activity on the shared accounts, you must go to the **Activity**
view, where you can perform the following actions:

  * See the **Activity Log** table with information in the following columns:

    * **Time:** It is the time when the user activity was registered.

    * **Event:** It is the type of activity performed by the user, for example, **Login To Cerby** or **Account Added To Collection**.

    * **Account:** It is the label of the account in Cerby related to the user activity.

    * **App:** It is the application related to the user activity.

    * **User:** It is the name of the user in Cerby who performed the activity.

    * **Location:** It is the geographical location of the user.

    * **OS:** It is the operating system of the user’s device.

    * **Device:** It is the user’s device from where the activity was registered.

  * Download the activity report in a CSV file by clicking the **Download CSV** button.

* * *

## **Remove a team manually**

**Team Admins** can remove a team created manually in Cerby by performing the
following steps from the **Teams** view:

**IMPORTANT:** When removing a team, all team members lose all access to the
accounts shared via a team automatically.

  1. Select the team from the **Your teams** list. The team members are displayed on a list in the main panel with the **Members** tab activated.

  2. Click the **More options** icon located at the top right of the section with the team details. A drop-down list is displayed.

  3. Select the **Remove team** button. The **Remove team** dialog box is displayed.

  4. Click the **Remove team** button. The dialog box closes and a success message box is displayed.

