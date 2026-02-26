---
description: "This article describes how to set up an Azure Key Vault integration to use your existing environment to manage your keys and encryption."
intercom_id: 9189942
---

# Set up an Azure Key Vault integration

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , and **Admins**
* If you are interested in this feature but don't see it available in your workspace, email our Sales team at [sales@cerby.com](mailto:sales@cerby.com).


{% endhint %}

With Cerby, you can set up an Azure Key Vault integration for your workspace to utilize external keys and Azure Key Management Service (KMS) for secure encryption of the accounts and secrets stored in Cerby. Also, you can leverage your existing Entra ID (formerly Azure) environment via a service principal to encrypt your data using your Azure vault key.

With a service principal, which is your app’s identity in the Microsoft Entra tenant, you can restrict access to your resources by the roles assigned to it. Therefore, this integration empowers you with granular access control and precise management over your cryptographic keys, enabling you to meet your compliance requirements and maintain control over your data security in the cloud.

{% hint style="danger" %}


**IMPORTANT:** Currently, Cerby supports creating only one cloud vault per provider. Therefore, you can only create one cloud vault with Azure external keys after setting up the Azure Key Vault integration.


{% endhint %}

* * *

## Requirements

The following are the requirements to set up an Azure Key Vault integration:

  * **Entra**
    * An Entra ID tenant
    * An active Entra ID account with permissions to create a service principal and on the resource groups, such as **User Access Administrator** or **Role-Based Access Control Administrator**. For more information, read the [Create a Microsoft Entra application and service principal that can access resources](https://learn.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal) official documentation
    * A registered Azure subscription. For more information, read the [Associate or add an Azure subscription to your Microsoft Entra tenant](https://learn.microsoft.com/en-us/entra/fundamentals/how-subscriptions-associated-directory#associate-a-subscription-to-a-directory) official documentation
    * The following values from Entra ID for the setup in Cerby:
      * Service Principal
        * Directory (tenant) ID
        * Application (client) ID
        * Client credentials or secret
      * Key Vault
        * Vault URI
        * Key vault name
  * **Cerby**
    * A Cerby workspace
    * A Cerby account with the **Workspace Super Admin** or **Workspace Admin** role
* * *

## Set up an Azure Key Vault integration

To set up an Azure Key Vault integration, you must complete the following main steps:

  1. [Create a service principal in Entra ID](set-up-an-azure-key-vault-integration.md#id-1.-create-a-service-principal-in-entra-id)
  2. [Create a key vault in Entra ID](set-up-an-azure-key-vault-integration.md#id-2.-create-a-key-vault-in-entra-id)
  3. [Generate a key in Entra ID](set-up-an-azure-key-vault-integration.md#id-3.-generate-a-key-in-entra-id)
  4. [Grant access to the key vault for the service principal in Entra ID](set-up-an-azure-key-vault-integration.md#id-4.-grant-access-to-the-key-vault-for-the-service-principal-in-entra-id)
  5. [Set up the Azure Key Vault integration in Cerby](https://docs.google.com/document/d/1rUMmsGogbCnhRSXId8U2obF7E5qQ0CcHxrlwGFf_VEs/edit#heading=h.235czvtmtmqt)

The following sections describe each main step.

### 1\. Create a service principal in Entra ID

To create a service principal in Entra ID, you must complete the following steps:

  1. Log in to the [Azure Portal](https://portal.azure.com/).
  2. Select the **Microsoft Entra ID** option from the **Azure services** section or the drop-down menu located at the top left of the page. The **Overview** page is displayed.
  3. Select the **App registrations** option from the left navigation drawer. The **App registrations** page is displayed.
  4. Create a new app by completing the following steps:
    1. Click the **New registration** button. The **Register an application** page is displayed.
    2. Enter a name for your app in the **Name** field.
    3. Click the **Register** button located at the bottom left of the page. The page closes, and a success message box and the new app are displayed on the **App registrations** page.
  5. Create a client secret for the new app by completing the following steps:
    1. Click the new app from the list of applications. The **Overview** page of the app is displayed.
    2. Click the **Add a certificate or secret** button from the **Essentials** section. The **Certificates & secrets** page is displayed with the **Client secrets** tab activated.
    3. Click the **New client secret** button. The **Add a client secret** flyout panel is displayed at the right.
    4. Enter a description for the client secret in the **Description** field.
    5. Select an expiration time from the **Expires** drop-down list.
    6. Click the **Add** button located at the bottom of the pane. The flyout panel closes, and a success message box and the new client secret are displayed.
    7. Copy the value of the client secret because you need it later in the [5. Set up the Azure Key Vault integration in Cerby](set-up-an-azure-key-vault-integration.md#id-5.-set-up-the-azure-key-vault-integration-in-cerby) main step.
  6. Select the **Overview** option from the left navigation drawer. The **Overview** page of the app is displayed.
  7. Copy the values of the following fields from the **Essentials** section because you need them later, in the [5. Set up the Azure Key Vault integration in Cerby](set-up-an-azure-key-vault-integration.md#id-5.-set-up-the-azure-key-vault-integration-in-cerby) main step:

     * **Application (client) ID**
     * **Directory (tenant) ID**

The next step is [2. Create a key vault in Entra ID](set-up-an-azure-key-vault-integration.md#id-2.-create-a-key-vault-in-entra-id).

### 2\. Create a key vault in Entra ID

To create a key vault in Entra ID, you must complete the following steps:

  1. Click the **Home** button located at the top left of the page.
  2. Click the **Create a resource** button from the **Azure services** section or the drop-down menu located at the top left of the page. The **Create a resource page** is displayed.
  3. Enter **key vault** in the search box.
  4. Select the **Key Vault** option. The **Key Vault** page is displayed.
  5. Click the **Create** button. The **Create a key vault** page is displayed.
  6. Enter the information or select the corresponding option in the following fields and drop-down lists:

     * **Subscription**
     * **Resource group**

     **IMPORTANT:** If you don’t have a resource group, click the **Create new** button located below the field to open a popup window and create the resource group.

     * **Key vault name**
     * **Region**
     * **Pricing tier**
     * **Soft-delete**
     * **Days to retain deleted vaults**
     * **Purge protection**

  7. Click the **Next** button. The **Access configuration** tab activates.
  8. Select the **Azure role-based access control (recommended)** option in the **Permission model** section, as shown in **Figure 1**.

<img src="../../../.gitbook/assets/image2.png" alt="">

**Figure 1. Permission model** section in the **Access configuration** tab, with the **Azure role-based access control** option selected

  9. Click the **Review + create** button. The page closes, and a success message box and the new key vault are displayed on the **Key vaults** page.
  10. Click the new key vault. The **Overview** page of the key vault is displayed.
  11. Copy the value from the **Vault URI** field because you need it later in the [5. Set up the Azure Key Vault integration in Cerby](set-up-an-azure-key-vault-integration.md#id-5.-set-up-the-azure-key-vault-integration-in-cerby) main step.

The next step is [3. Generate a key in Entra ID](set-up-an-azure-key-vault-integration.md#id-3.-generate-a-key-in-entra-id).

### 3\. Generate a key in Entra ID

To generate a key in Entra ID, you must complete the following steps:

  1. Select the **Keys** option from the left navigation drawer on the details page of your new key vault. The **Keys** page is displayed.
  2. Click the **Generate/Import** button. The **Create a key** page is displayed.
  3. Enter a name for the key in the **Name** field.
  4. Select the **RSA** and **4096** options from the **Key type** and **RSA key size** fields, respectively.

  **IMPORTANT:** Make sure those options are selected; otherwise, the integration will not work.

  5. Copy the value of the key name because you need it later in the [5. Set up the Azure Key Vault integration in Cerby](set-up-an-azure-key-vault-integration.md#id-5.-set-up-the-azure-key-vault-integration-in-cerby) main step.
  6. Click the **Create** button located at the bottom left of the page. The page closes, and a success message box and the new key are displayed on the **Keys** page.

The next step is [4. Grant access to the key vault for the service principal in Entra ID](set-up-an-azure-key-vault-integration.md#id-4.-grant-access-to-the-key-vault-for-the-service-principal-in-entra-id).

### 4\. Grant access to the key vault for the service principal in Entra ID

To grant permissions to the service principal for the key vault in Entra ID, you must complete the following steps:

  1. Select the**Access control (IAM)** option from the left navigation drawer on the details page of your new key vault. The Access control (IAM) page is displayed.
  2. Click the **Add role assignment** button from the **Grant access to this resource** section. The **Add role assignment** page is displayed with a list of roles.
  3. Select the corresponding role from the list.

  **IMPORTANT:** The role with the least access privileges is Key Vault Crypto User, and the role with the highest access is **Key Vault Administrator**.

  4. Click the **Next** button. The **Members** tab is activated.
  5. Click the **Select members** button. The **Select members** panel is displayed on the right, with a list of members.
  6. Enter the name of the service principal in the search box.
  7. Select the service principal.
  8. Click the **Select** button. The page closes, and a success message box is displayed.

  **NOTE:** You can confirm the successful role assignment by activating the **Role assignments** tab. The role you selected is displayed on a list, linked to the service principal.

The next step is [5. Set up the Azure Key Vault integration in Cerby](set-up-an-azure-key-vault-integration.md#id-5.-set-up-the-azure-key-vault-integration-in-cerby).

### 5\. Set up the Azure Key Vault integration in Cerby

To set up the Azure Key Vault integration in Cerby, you must complete the following steps:

  1. Log in to your [workspace](https://app.cerby.com/) using the Cerby web app. The Cerby dashboard is displayed.
  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed.
  3. Activate the **Privacy and Security** tab. A table with a list of vaults is displayed on the **Vault management** section, as shown in **Figure 2**.

<img src="../../../.gitbook/assets/image1.png" alt="">

**Figure 2.** Table with the list of vaults in the **Vault management** section of the **Privacy and Security** tab

  4. Click the **Create new vault** button. The **Create new vault** dialog box is displayed.
  5. Enter the vault name in the **Vault name** field.
  6. Select the **Azure External Keys** option from the **Strategy** drop-down list.

  **NOTE:** Select the **Set as default vault** option if you want to set the new vault as the default when adding an item to Cerby.

  7. Click the **Next** button. The **Configure the Azure vault** dialog box is displayed.
  8. Enter the values you have retrieved from Entra ID in the corresponding fields:

     * **Client ID**
     * **Tenant ID**
     * **Client Secret**
     * **Vault URL**
     * **Vault Key Name**

  9. Click the **Create vault** button. The dialog box closes, and a success message box is displayed.

Now you are done.
