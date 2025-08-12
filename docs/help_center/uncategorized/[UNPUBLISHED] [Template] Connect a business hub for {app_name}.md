# [UNPUBLISHED] [Template] Connect a business hub for {app_name}

**Description:** This article describes how to connect a business hub to centrally manage the {scope} of {app_name} from Cerby.

{% hint style="info" %} **Who can use this feature?** * Workspace**Owners** ,
**Super Admins** , **Admins** , and **Users** * Only supported using the Cerby
web app {% endhint %}

As a user with any workspace role in Cerby, except **Guest User** and **Login-
Only** , you can connect a business hub integration to centrally manage the
{scope} of {app_name}.

When you connect the business hub, you become its **Owner** , and you can
perform the following user and access management tasks through
{implementation} executed by the Cerby agent:

{supported_workflows_list}

{% hint style="success" %} **TIP:** For more details about the automated tasks
of a business hub, how it works, and the supported apps, read the article
[Explore Business Hubs](https://help.cerby.com/en/articles/6831152-explore-
apps). {% endhint %}

{workflows_notice}

This article provides instructions on how to connect a business hub for
{app_name}. For other app-specific articles and videos, review the [Connecting
business hubs for your
apps](https://help.cerby.com/en/collections/10289415-connecting-your-apps) and
[Connecting business hubs for your paid social
apps](https://help.cerby.com/en/collections/12330234-connecting-business-hubs-
for-your-paid-social-apps) collections in the Cerby Help Center.

* * *

# **Requirements**

The following are the requirements to connect a business hub:

  * A Cerby workspace

  * A Cerby user account with the **Owner** , **Super Admin** , **Admin** , or **User** role

  * A {collaboration_space} in {app_name}

  * Groups configured in your identity provider (IdP) if you want to leverage automatic user provisioning and deprovisioning from your apps based on group assignment events. For more information, read the articles available in the [Managing users via an IdP and business hub](https://help.cerby.com/en/collections/12330182-managing-users-via-an-idp-and-business-hub) collection in the Cerby Help Center

  * An automation account, meaning an active user account with a native **{role}** role in {app_name} to be used as a service account. For instructions and recommendations on how to create and configure this account, read the article [Create an automation or service account for your business hub](https://help.cerby.com/en/articles/9830816-create-an-automation-or-service-account-for-your-business-hub)

{SSO_requirement}

{BId_requirement}

* * *

# **Connect a business hub for**{app_name}

To connect a business hub for {app_name}, you must complete the following main
steps from the Cerby web app dashboard:

  1. Add a business hub and connect it to {app_name}

  2. Check for updates to import {scope_steps} to Cerby

  3. Connect your {app_name} user account to the business hub

  4. Manage unmatched users

The following sections describe each main step.

## 1\. Add a business hub and connect it to {app_name}

To add a business hub and connect it to {app_name}, you must complete the
following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.

  3. Click the **Connect Business Hub** button located at the top-right corner of the page. The **Connect your Business Hubs to Cerby** dialog box is displayed.  
​**TIP:** Select the **Don’t show this again** option to skip this step the
next time you connect a new business hub.

  4. Click the **Get started** button. A wizard is displayed on the **Select app** page.

  5. Select **{business_hub_name}** from the catalog. The **Enter app details** page is displayed on the wizard.

  6. Enter and select your app information in the corresponding fields:

     * **Label in Cerby:** It is the name to assign to your business hub in Cerby, and it will be displayed on the business hub card.

{identifier_field}

     * **User management and login method:** It is the way your users log in to the app and determines whether they must save their login credentials as a Cerby account connected to the business hub. You must select one of the following methods: 

{login_methods_list}

  7. Click the **Next** button. The **Select automation account** page is displayed with a list of existing {app_name} accounts.

  8. Select the automation account you have previously added to Cerby, as described in the Requirements section.  
​**NOTE:** If you don’t have an automation account, you are prompted to add
it. Make sure you read Cerby’s recommendations on how to configure it in the
article [Create an automation or service account for your business
hub](https://help.cerby.com/en/articles/9830816-create-an-automation-or-
service-account-for-your-business-hub). You may need to add the account first
and then add the business hub.

  9. Click the **Connect app** button. The wizard closes, and a success message box is displayed.   
The corresponding business hub is also displayed on the **Business Hubs** view

The next step is [2\. Check for updates to import {scope_steps} to
Cerby](https://help.cerby.com/en/articles/9046120-connect-an-
app#h_9c6531cf9a).

## 2\. Check for updates to import {scope_steps} to Cerby

To check for updates in your app to identify and import {scope_steps} to
Cerby, you must complete the following steps:

  1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.

  2. Click the **Settings** (![](gitbook/imagesAD_4nXeByVHBSTSp-KuNiohUPzRJ81cmUV-g-W-qM7ABEk0mzfVRcsTnC9XD_6mAQBQObGIKbGJWpnxScMGm_cT3R4uzEzVW0ZAsqkGoo-cmatfJC_I2vgLsWIrLnwQAUqoT_5Llg9mz)) icon of the corresponding business hub card. The business hub details page is displayed with the **Settings** tab activated.

  3. Click the **Check for updates** button located at the top right of the page. A message box is displayed with information about the process.  
​**NOTE:** The check and import process may take a few minutes depending on
the number of {scope}, and because Cerby automatically matches users to their
corresponding Cerby user account.

  4. Confirm that the automated task to check for updates has the “Completed” status by performing any of the following actions:

     * Click the **More details** button from the message box.

     * Select the **Automation** option from the left navigation drawer to open the **Automation** view with a list of automated tasks and their status. 

{% hint style="info" %} **NOTE:** Cerby automatically performs daily checks
for updates for all business hubs, but you can trigger them manually, as
described in this section. For more instructions, read the article [Sync your
app users with your business
hub](https://help.cerby.com/en/articles/9046205-check-for- updates-in-your-
app-and-apply-report). {% endhint %}

The next step is 3\. Connect your {app_name} user account to the business hub.

## 3\. Connect your****{app_name} user account to the business hub

To connect your {app_name} user account to the business hub so Cerby can
manage and protect it, you must complete the following steps:

  1. Select the **Accounts** option from the left navigation drawer. The **Accounts** view is displayed.

  2. Click the **Log in** button of the corresponding {business_hub_name} account card. The **Connect your {business_hub_name} Account** dialog box is displayed.

  3. Enter the login credentials of your **{app_name}** user account.

  4. Click the **Connect account** button. The dialog box closes, and a success message box and a new account card are displayed.

The next step is 4\. Manage unmatched users.

## 4\. Manage unmatched users

During a check for updates, Cerby automatically matches app members to the
Cerby user accounts that correspond to their email addresses, including
existing [guest users](https://help.cerby.com/en/articles/8392946-explore-
guest-users) and [local
partners](https://help.cerby.com/en/articles/8980877-explore-
partners#h_7e4add33a2). Manual matching is required when apps don't provide
email addresses and for app members using personal or external accounts that
couldn’t be identified or are not in the corporate directory.

To view the status of the imported app members, you must complete the
following steps:

  1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.

  2. Click the **More options** (![](gitbook/imagesAD_4nXewApJOBZXewpFew1XrkjC6rCssB5Upy2WRCW8fpJjw2Zmj0xzSkEgw3tUBvW6lyQC2RihdmxzJ6KKXG1pvMGfAeaQnjZUGnThkBo5vdisjtu8WvqHXLgT1_7-xOwkkFy5umyicPg)) icon of the corresponding business hub card. A drop-down list is displayed.

  3. Select the **View Members** option from the list. The business hub details page is displayed with the **Members** tab activated.  
App members are displayed in the following tabs of the **User Overview**
section:

     * **Unmatched users:** This tab displays the users who were not automatically matched.

     * **Onboarded users:** This tab displays the users matched to their Cerby user account. 

     * **Guest users:** This tab displays the users who were matched to an existing Cerby user account but it doesn’t exist in the corporate directory, such as external collaborators.

For unmatched users, you can perform one of the following actions:

  * Match users

  * Remove unmatched users

  * Exempt unmatched users

The following sections describe each action.

### **Match users**

To match users, you must complete the following steps from the **Unmatched
users** tab of the business hub details page:

  1. Click the **Match user** button of the corresponding user. The **Match user** dialog box is displayed.

  2. Enter the username or email address of the user you want to match and invite in the **Match with** field. The user is displayed on a list.

  3. Select the user from the list.

  4. Click the **Next** button. The **Select Cerby role** dialog box is displayed.

  5. Select the role to assign to the user on the business hub **Cerby role** drop-down list:

     * **Owner:** This role enables sharing access and managing business hub settings in Cerby.

     * **Collaborator:** This role enables only logging in to the app from Cerby.

  6. Click the **Match user** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Onboarded users** tab.

### **Remove unmatched users**

To remove unmatched users, you must complete the following steps from the
**Unmatched users** tab of the business hub details page:

{% hint style="danger" %} **IMPORTANT:** When removing an unmatched user,
Cerby performs an automated task to revoke the user’s seat and permissions in
{app_name}. {% endhint %}

  1. Click the **More options** (![](gitbook/imagesAD_4nXewApJOBZXewpFew1XrkjC6rCssB5Upy2WRCW8fpJjw2Zmj0xzSkEgw3tUBvW6lyQC2RihdmxzJ6KKXG1pvMGfAeaQnjZUGnThkBo5vdisjtu8WvqHXLgT1_7-xOwkkFy5umyicPg)) icon of the corresponding user. A drop-down list is displayed.

  2. Select the **Remove user** option from the list. The **Remove user?** dialog box is displayed.

  3. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from the app via an automated task.

### **Exempt unmatched users**

Exempted users keep their user accounts or seats active in your app, but you
cannot manage them through Cerby.

To exempt unmatched users, you must complete the following steps from the
**Unmatched users** tab of the business hub details page:

  1. Click the **More options** (![](gitbook/imagesAD_4nXewApJOBZXewpFew1XrkjC6rCssB5Upy2WRCW8fpJjw2Zmj0xzSkEgw3tUBvW6lyQC2RihdmxzJ6KKXG1pvMGfAeaQnjZUGnThkBo5vdisjtu8WvqHXLgT1_7-xOwkkFy5umyicPg)) icon of the corresponding user. A drop-down list is displayed.

  2. Select the **Exempt user** option from the list. The exempt user dialog box is displayed.

  3. Enter a reason for exempting the user in the **Provide a reason** field.

  4. Click the **Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

# **Use your business hub**

The following are the supported features of business hubs you can use:

{references}

