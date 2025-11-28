# How to Enable Okta User Provisioning with SCIM

**Description:** This article describes how to enable automatic user provisioning via SCIM with your Okta tenant.

With Cerby, you can configure automatic user provisioning for Okta using the
System for Cross-domain Identity Management (SCIM) specification to manage the
creation and synchronization of user accounts based on the user and group
assignments. This feature is available to all users who have both a valid Okta
tenant and a Cerby workspace.

When you enable user provisioning in an Okta app integration, you can automate
multiple critical tasks to downstream user management, ensuring that
configuration is performed once and propagated throughout the Cerby platform.

This article describes how to enable Okta user provisioning for the Cerby
platform with SCIM.

* * *

# **Supported features**

The following are the supported features of enabling Okta user provisioning
with SCIM:

  * **Push users:** Users assigned to the Cerby application in Okta are automatically able to access the Cerby clients (web app, mobile app, and browser extension); they are available to other users in Cerby for account sharing purposes.

  * **Update user attributes:** The following user attributes are automatically synchronized with the corresponding record in Cerby:

    * First name

    * Last name

    * Primary email 

  * **Push groups:** Users who are members of a group in Okta and assigned to the Cerby application are pushed in batches to the Cerby clients, and this grouping structure and its members are replicated in Cerby. 

  * **Deactivate users:** Deactivated users in Okta are automatically detected in Cerby, and their associated access grants in Cerby are removed. In some cases, additional follow-up actions, like password rotation, may occur in Cerby for privileged identities to which the deprovisioned user had access grants. See the Troubleshooting: Deactivated Users section for more information on the support that Cerby provides for this feature.

  * **Reactivate users:** Reactivated users in Okta will reappear as valid users in Cerby; however, account access grants must be reassigned in Cerby.

* * *

# **Requirements**

The following are the requirements to enable Okta user provisioning with SCIM:

  * An Okta tenant

  * A user account in Okta with privileges to manage the Cerby app in your Okta tenant

  * A user account in Cerby with the **Workspace Owner** role

  * Users or groups from your directory already assigned to the Cerby app integration in Okta. You must have already done the assignments as part of the [How to Configure SSO Between Cerby and Okta with SAML](https://help.cerby.com/en/articles/5457568-how-to-configure-sso-between-cerby-and-okta-with-saml) article

  * The Cerby SAML-based app integration must be set up and deployed. You must have already deployed the app as part of the [How to Configure SSO Between Cerby and Okta with SAML](https://help.cerby.com/en/articles/5457568-how-to-configure-sso-between-cerby-and-okta-with-saml) article

  * A SCIM API authentication token. Follow the instructions in the [How to Retrieve the SCIM API Authentication Token from Cerby](https://help.cerby.com/en/articles/5683294-how-to-retrieve-the-scim-api-authentication-token-from-cerby) article to retrieve the token

**NOTE:** If you need to regenerate the SCIM API authentication token, see the
Regenerating the SCIM API authentication token section.

* * *

# **Enabling Okta User Provisioning with SCIM**

To configure automatic Okta user provisioning, you must complete three main
steps:

  1. Configure Cerby to support provisioning with Okta

  2. Configure automatic user provisioning to Cerby

  3. Configure Group Push between Okta and Cerby

The following sections describe each main step.

## **1\. Configure Cerby to Support Provisioning with Okta**

Cerby has enabled by default the provisioning support for Okta. You must only
follow the instructions from the [How to Retrieve the SCIM API Authentication
Token from Cerby](https://help.cerby.com/en/articles/5683294-how-to-retrieve-
the-scim-api-authentication-token-from-cerby) article to retrieve the SCIM API
authentication token.

The next step is 2\. Configure automatic user provisioning to Cerby.

* * *

## **2\. Configure Automatic User Provisioning to Cerby**

To configure automatic user provisioning to Cerby, you must complete the
following steps:

  1. Log in to the [Okta Admin Console](https://developer.okta.com/login/) of your organization.

  2. Click the **Applications** button from the **Applications** drop-down list located in the left navigation drawer. The **Applications** page is displayed, as shown in **Figure 1**.

![](images/yxMdW7L-wlko6MR-O3RU-
FX7UigRb5KkmdKeiJyCxbi3NIsyF5_4q9uYMEHTzH9QMAaVQAUA5pnC-
IVnK5cKqJx2KTYhTjybwV8c-YDb-
JV_OllWHOd9ZgCxJ1wmosSRmr6k_tY7PTW2658istAR48q_Q4NZnz87ut6nTXV4ztU75edMwsu4w9qmug)

**Figure 1. Applications Page in the Okta Admin Console**

  3. Select the **Cerby** option from the list of applications. The **Cerby** application page is displayed with the **General** tab activated, as shown in **Figure 2**.

![](images/rTofB5ZCjLmFkCpRhodyNOz4UfYpQs9pHRJWjudsjRuNUQi6F3IwfIEe_Lijrvc-
zwgnq3y2Uf5ORhHtiT9CxKTfr23N5sefLNTg8Ka5VmnbOMaD__0Cg5YNt1wQcyi5SRjoqfl6fspPVk1aHp0NGzCWfKJB-
qFPgAkGBWJE2IdKgFLVyiyb2666qg)

**Figure 2. General Tab in the Cerby Page**

  4. Configure the provisioning integration by performing the following actions:

     1. Activate the **Provisioning** tab.

     2. Click the **Integration** button located in the left panel. The **Integration** section is displayed in the main panel, as shown in **Figure 3**.

![](images/uFuG_YYkpFZBqSj2yl90OSAsN4BbHRIho7F-vU-
TbCeyKGLyuR0M7Tj8Rbfep5olXG0LwTGXsWzLRpFP1Phfyf8r6nIcxoAjZ9oxkhaXNgY3oqfcVwjXHmnSs1RtL11Vj5CuSwWlGfk3jBAGPY7E7XvnVBDPomUJVJBxwUt7nSkRiueFORTN7yQOSw)

**Figure 3. Integration Section in the Provisioning Tab**

     3. Select the**Enable API integration** option.

     4. Paste the SCIM API authentication token in the **API Token** field. You retrieved this token in step 1\. Configure Cerby to support provisioning with Okta.

     5. Click the **Save** button.

  5. Configure the sign-on settings by performing the following actions:

     1. Activate the **Sign On** tab. A success message box is displayed.

     2. Click the **Edit** button from the **Settings** section. The input fields in the **Sign on methods** and **Credentials details** sections are enabled.

     3. Select the **Email** option from the **Application username format** drop-down list.

     4. Click the **Save** button. A success message box is displayed.

  6. Configure the application username format by performing the following actions:

     1. Activate the **Provisioning** tab.

     2. Click the **To App** button located in the left panel. The **Provisioning to App** section is displayed in the main panel, as shown in **Figure 4**.

![](images/Ds9pCFgfUfkymaGIXoXdXnhPvIcRXTQ8I40YBfcteS0DRBVpLvraXIhELOtLySXsBg5vp4ZWNtRyzmJJoOBvj_3PNy0vYcGCPnu2RdBA9A_nmb8LGYIKGSJxcFU1EcNLatb0OhySsQOWG4vgklZtVtxWP1mQZna5cCqvwIKtiSPUmWXILirR732LFg)

**Figure 4. Provisioning to App Section in the Provisioning Tab**

     3. Select the **Enable** checkbox of the following options:

        * **Create Users**

        * **Update User Attributes**

        * **Deactivate Users**

**IMPORTANT:** Make sure that the username and email values for the user being
pushed to Cerby are the same.

     4. Click the **Save** button. A success message box is displayed.

The next step is 3\. Configure Group Push between Okta and Cerby.

## **3\. Configure Group Push between Okta and Cerby**

To configure the Group Push feature between Okta and Cerby, you must complete
the following steps from the **Cerby** application page in Okta:

  1. Activate the **Push Groups** tab. The Push Groups to Cerby page is displayed, as shown in **Figure 5**.

![](images/ZEg349nXH36LMFs-
_pWAF5l_0wz529X_RyLlcKVZ9t0ZGSnVXyQ6ESnYBWApOba87J1JV8LJBFZNbWodpnqFbKDoJpB4jwZ_hiYV1-d_hMkU0see2uZsr_oj9B2RcpHHkqsIu4dkBWB57-6FvXKnXugS6ZPWE4o_I3-pekGBUS9teSutomdxAce_nw)

**Figure 5. Push Groups Tab**

  2. Select the **Find groups by name option** from the **Push Groups** drop-down list. The **Push groups by name** section is displayed in the main panel.

**TIP:** You can select the **Find groups by rule** option to search among
multiple groups when they meet a specific rule.

  3. Enter the name of the group you want to push to Cerby in the **Enter a group to push…** field. The group is displayed automatically below the input field.

  4. Select the group. The **Group** section is displayed below, as shown in **Figure 6**.

![](images/EjjurT8WzzIh6OM2dYhZxRrNdrocBJI01rXEXY0-qsvo-
Wqp8xEU5bEj2wJIcL0SjFNH6jD_-
iO4YrN83EUArp7QlIUDG5It_gSQ_nvN25CuIEeNLtS6jaJQpSd0-byqnOaf8fdk8V8Betzc4OIt2Lu6vtEd8-7Hf5vxKAiAypBoNjY67e0T4AF2_g)

**Figure 6. Group Section**

  5. Select the corresponding option from the **Match result & push action** drop-down list:

     * **Create Group:** Select this option when the group does not exist in Cerby, so it is pushed from Okta.

     * **Link Group:** Select this option when the group exists in Cerby and is already linked to Okta. Use the drop-down to find the existing group.

  6. Click the **Save** button. The panel closes and the **Push Groups to Cerby** page is displayed. When the group is pushed to Cerby, an **Active** status is displayed in the **Push Status** column.

**NOTE:** To verify if the group was successfully pushed to Cerby, access the
**Teams** view in your Cerby dashboard. The group and its members are
displayed in the main section of the **Teams** view.

Now you are done.

* * *

# **Troubleshooting: Deactivated Users**

Deactivated users in Okta are also deactivated in Cerby. It means that these
users are not able to log in to the application, but their data remains
available to other Cerby admins as disabled users.

To permanently delete the users' data, contact Cerby by sending an email to
[support@cerby.com](mailto:support@cerby.com).

* * *

# **Troubleshooting: Reprovisioned users**

After configuring Okta user provisioning with the Cerby app integration
through the SCIM specification, some existing users might not be reprovisioned
automatically. Instead, their usernames are removed and added under the new
email address.

When this scenario occurs, the following error message is displayed on the
**Assignments** tab of the **Cerby** application page: “User was assigned this
application before Provisioning was enabled and not provisioned in the
downstream application. Click Provision User.”

To solve the user reprovisioning problem, you can complete the steps of one of
the following two alternatives:

  * Retry the failed tasks

    1. Click the **Tasks** button from the **Dashboard** drop-down list located in the left navigation drawer. The **Tasks** page is displayed.

    2. Identify the tasks with the failed**** status.

    3. Select the group assigned to the Cerby app integration.

    4. Click the **Retry Tasks** button.

  * Remove and add users manually

    1. Open the **Cerby** application page.

    2. Activate the **Provisioning** tab.

    3. Click the **To App** button located in the left panel. The **Provisioning to App** section is displayed in the main panel.

    4. Click the **Edit** button to activate the checkboxes.

    5. Deselect the **Enable** checkbox of the **Deactivate Users** option, as shown in **Figure 11**.

![](images/rnvyH2uAGPaau2zd4kgSn9PGo1YB_ZZeqaNIwEfNHTwO2WKqjY1enkbCIR_CLZWwuLhqehYTgnE-c83j3602vi1ygBHdCU2SZjZh1qcd38IE6CwYcMUpXZI3MrwoWw4TpZk5_9a-NZb3wlowQtJaT1k0rMRphRo8fjUcZPitapx2nBKxfrM8ieY-
PQ)

**Figure 11. Deactivate Users Option in the Provisioning to App Section**

    6. Click the **Save** button located at the bottom of the page.

    7. Remove the users with the error from the Okta group assigned to the Cerby app integration.

    8. Add the corresponding users back to the Okta group.

    9. Repeat steps 4, 5, and 6 to select the **Enable** checkbox of the **Deactivate Users** option.

* * *

# **Troubleshooting: Users can’t log in to Cerby; invalid SAML configuration**

If users can’t log in to Cerby while getting the “Invalid SAML configuration”
error, it might be due to a SAML assertion. You can verify if the error is
caused by a SAML assertion by following the steps in the [Capturing a SAML
Assertion](https://support.hashicorp.com/hc/en-
us/articles/1500005371682-Capturing-a-SAML-Assertion) article. If you find
that it is a SAML assertion issue, contact us at
[support@cerby.com](mailto:support@cerby.com), and we'll guide you through the
resolution process.

* * *

# **Regenerating the SCIM API Authentication Token**

To regenerate the SCIM API authentication token, complete the following steps:

  1. Send an email with your request to [support@cerby.com](mailto:support@cerby.com). The Cerby team regenerates the SCIM API authentication token.

  2. Receive the response email from Cerby to confirm that the token was successfully regenerated.

  3. Complete the instructions from the [How to Retrieve the SCIM API Authentication Token from Cerby](https://help.cerby.com/en/articles/5683294-how-to-retrieve-the-scim-api-authentication-token-from-cerby) article to retrieve the new token.

**NOTE:** The Cerby team is currently developing a self-service solution for
regenerating the SCIM API authentication token. To regenerate the token, the
Cerby team members must validate their identity.

