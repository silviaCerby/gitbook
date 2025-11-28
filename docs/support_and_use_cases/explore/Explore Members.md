# Explore Members

**Description:** This article describes what members are in Cerby and the actions they can perform in your workspace.

At Cerby, members are individuals with a user account to access an
organization’s workspace.

When a workspace is connected to an identity provider (IdP), such as Okta or
Entra ID, user accounts are synced with the corporate directory. Therefore,
their access to Cerby can be automatically granted or revoked by IT admins
based on provisioning and deprovisioning events, respectively, in the IdP.

Meanwhile, user accounts in local user workspaces are provisioned by Cerby and
managed by IT admins. For more information, read the article[ How to create
and configure a local user
workspace](https://help.cerby.com/en/articles/8011381-how-to-create-and-
configure-a-local-user-workspace).

* * *

# The All Members page

The **All Members** page, as shown in **Figure 1** , contains tables with all
the workspace members and guest users. This page is accessible only to
workspace**Admins** , **Super Admins** , and **Owners**.

![Screenshot of the Cerby web app dashboard. The All Members page is displayed
with a table of workspace members](images/AD_4nXd6m5UNS-
r-f6fZupvX_oATIaCjNoF55Wz3a24tnjPEzXmoN5Li8e6VYRO4Ysol1DctkWql1GzX14JoBd-
at0-f7w5l-Nol_0h2RFJLHi-wZJA5zHLdwUAYrf2CnPMnhiroaJRVcA)

**Figure 1. All Members** page in the Cerby web app dashboard

The table in the **All Members** tab provides information about workspace
members in the following columns:

  * **Account members:** It lists the username and email address of each member.

  * **Workspace role:** It lists the workspace role of each member:

    * **Owner**

    * **Super Admin**

    * **Admin**

    * **User**

    * **Login-Only**

For more information about roles, read the article [How Cerby manages
roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-
roles?q=universal+logout).

  * **Accounts:** It lists a More button for each member to view all the accounts to which the member has shared access as **Owner** or **Collaborator**.

  * **Team:** It lists a **More** button for each member to view all the teams to which the member belongs.

  * **Status:** It lists the status of the member:

    * **Active:** It means the Cerby user account was created and configured. 

    * **Pending:** It means the Cerby user account was created, but the member has not configured it.

    * **Removed:** It means the Cerby user account was removed from the Cerby workspace.

  * **Joined date:** It lists the date when each member’s Cerby user account was configured.

  * **Last activity:** It lists the date when each member was last active in the workspace.

  * **Unnamed column:** The table contains an unnamed column that lists a **More options** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1430748619/412757144fdaeb9b72db6b6d6a1b/AD_4nXfKlOryjrhC0V6wseYu-FNoywsgwWH_dyefALz2A-_PYXNDcGbohBoI-diEUoklZhrb8kk2x5JJVpw-LS5Tze_QbUNyRT19rDrFvepx4_CoAAGbJyR4D0ZfHTD7BnTeUMNqZyR1Qw?expires=1748466000&signature=9ff5135d26afc35048b522d0788b895a01bb80d113f7ea12a218d2fe638b1592&req=dSQkFs56lYdeUPMW3Hu4gXiJQ8cy18N5anV4miUxAgvhbEMkXHghXBOUTs%2Fy%0AvQ%3D%3D%0A)) icon for each member with the following options in a drop-down menu:

    * **Export:** It exports the member details in a CSV file.

    * **Trigger Universal Logout:** It triggers the [Cerby Universal Logout](https://help.cerby.com/en/articles/10496392-trigger-cerby-universal-logout) feature.

    * **Remove from workspace:** It removes the member from the workspace by disabling their user account.

The table in the **Guests** tab provides information about users with the
**Guest User** workspace role. It contains the same columns as the table in
the **Members** tab, except for **Workspace role** ; additionally, in the
**More options** drop-down menu, you can select the **Reset** **MFA** and
**Force Password Reset** options.

The **All Members** page also contains a search bar to look up workspace
members by their name or email address.

An **Export**
(![](images/AD_4nXe4FMrWC_BwPNVhTrNbTmbM2T-eFyAxiib1shX_VaPpdxvUM89CDeT9Wn00QF5aUYrXtpmU9IZShy_sNfk1DLkHTkHLEPPlmv9QLym6JL6EQf1kSFBNOmh_EgSOC9kO9_yY_UVD))
icon located at the top right of the page enables you to export the
information of the members table in a CSV file. For more information, read the
article Export the workspace members.

