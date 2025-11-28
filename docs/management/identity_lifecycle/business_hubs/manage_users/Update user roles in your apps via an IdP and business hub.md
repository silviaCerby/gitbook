# Update user roles in your apps via an IdP and business hub

**Description:** This article describes how to update the user roles in your external seat-based and paid social apps via an IdP and business hub.

{% hint style="info" %} **Who can use this feature?** * IT admins with a
tenant in an identity provider * Business hub **Owners** * Only supported
using the Cerby web app {% endhint %}

As an IT admin collaborating with a business hub **Owner** , you can update
user roles in your external seat-based and paid social apps via your identity
provider (IdP), such as Okta or Entra ID, and a business hub.

For this identity lifecycle management functionality to work, Cerby leverages
user and group provisioning from the IdP to update Cerby teams. These teams
must have shared access to a business hub integration with specific roles or
permissions both in Cerby and the external app, including assets if supported,
as shown in **Figure 1**.

Additionally, you must complete any of the following two-step processes to
avoid triggering automated user removals from your external app:

  * IdP group reassignment

    1. Add the user to the IdP group that corresponds to the new role you want them to have in the external app.

    2. Remove the user from the IdP group that corresponds to the old role.

  * Individual share in Cerby

    1. Share the business hub integration in Cerby individually with the user and assign them the new role you want them to have in the external app.

    2. Remove the user from the IdP group that corresponds to the old role.

![Diagram of a Cerby business integration leveraging identity provider groups.
The diagram shows the multiple systems involved, such as the identity
provider, Cerby, and the external app, and the components, such as users,
groups, teams, the business hub integration, and the update user role
management
task](images/AD_4nXfSgqlBMVtqCqPSMmHdpz5sLwQfh5PmoDZtUYiWp0RPUEWPKaIKXwYMBOvH36VsPfe_wVe6toj0u7M_Vz86dMm-
aTWVcJao7hFF_--knGqVlHjozig-wxVwUGDLlWgR-kAOwRqs)

**Figure 1.** User deprovisioning in external apps from IdP events

With this approach, Cerby identifies the users who keep shared access to the
business hub integration whether individually or through another team, and
determines their role based on all their existing access grants. Therefore,
Cerby triggers the automated tasks to update user roles in the external app as
follows:

  * When the new assigned role is higher, Cerby triggers the task upon IdP group assignment or individual share.

  * When the new assigned role is lower, Cerby triggers the task upon user removal from the IdP group with the old role. 

* * *

# **Requirements**

The following are the requirements to update user roles in your apps via your
IdP and business hub:

  * A user account in your IdP with privileges to manage an app integration

  * A Cerby workspace integrated with your IdP for single sign-on (SSO) and automatic user provisioning using the SCIM protocol. Refer to the [Creating and setting up your workspace](https://help.cerby.com/en/collections/5819419-creating-and-setting-up-your-workspace) collection for instructions according to your IdP

  * Groups created and configured in your IdP to be used for user provisioning and deprovisioning. For instructions, read the articles according to your IdP:

    * [How to Enable Okta User Provisioning with SCIM](https://help.cerby.com/en/articles/5457593-how-to-enable-okta-user-provisioning-with-scim)

    * [Configure automatic user and group provisioning with Entra ID via SCIM](https://help.cerby.com/en/articles/5638472-configure-automatic-user-and-group-provisioning-with-entra-id-via-scim)

  * A business hub connected to Cerby to which you have the **Owner** role

  * The IdP-based teams must have shared access to the business hub integration. For instructions on how to do it, read the article [Add users and teams to your app via a business hub](https://help.cerby.com/en/articles/9045790-add-users-and-teams-to-your-apps-via-a-business-hub); you must follow the process to add a team

* * *

# **Update user roles in your apps via your IdP and business hub**

To update user roles in your external apps via your IdP and business hub, you
must complete the following steps depending on how you want the users to keep
access to the business hub integration:

  * IdP group reassignment

    1. Log in to the IdP admin console or center of your organization.

    2. Add users or members to the groups assigned to the Cerby app integration with the role you want them to have. For instructions, read the official documentation of your IdP:

       * **Okta:** [Manually assign people to a group](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-assign-group-people.htm)

       * **Entra ID:** [Add members or owners of a group](https://docs.azure.cn/en-us/entra/fundamentals/how-to-manage-groups#add-members-or-owners-of-a-group)

    3. Remove the users or members from the old group. For instructions, read the official documentation of your IdP:

       * **Okta:** [Remove people from a group](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-remove-group-people.htm)

       * **Entra ID:** [Remove members or owners of a group](https://docs.azure.cn/en-us/entra/fundamentals/how-to-manage-groups#remove-members-or-owners-of-a-group)

  * Individual share

    1. Log in to your [Cerby](https://app.cerby.com/) workspace.

    2. Complete the instructions in the article [Add users and teams to your app via a business hub](https://help.cerby.com/en/articles/9045790-add-users-and-teams-to-your-apps-via-a-business-hub) to share the business hub integration individually with the role you want the user to have.

    3. Log in to the IdP admin console or center of your organization.

    4. Remove the corresponding users or members from the old group. For instructions, read the official documentation of your IdP:

       * **Okta:** [Remove people from a group](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-remove-group-people.htm)

       * **Entra ID:** [Remove members or owners of a group](https://docs.azure.cn/en-us/entra/fundamentals/how-to-manage-groups#remove-members-or-owners-of-a-group)

Given that IdP users and groups are automatically provisioned and
deprovisioned from your Cerby workspace, Cerby triggers the automated tasks to
update user roles in the external app, including assets if supported, as
follows:

    * When the new assigned role is higher, Cerby triggers the task upon IdP group assignment or individual share.

    * When the new assigned role is lower, Cerby triggers the task upon user removal from the IdP group with the old role.

Now you are done.

