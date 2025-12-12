---
description: This article describes how to add a server item to your Cerby workspace.
---

# Add a server item

{% hint style="info" %}


**Who can use this feature?**

  * Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
  * Available to the Cerby Automate and Cerby Protect products. Cerby Protect users must have already set up their [trusted devices](https://help.cerby.com/en/articles/8142370-how-to-set-up-and-manage-your-trusted-devices)
  * Only supported using the Cerby web app


{% endhint %}

You can add a server item and attachments to Cerby in the following two ways:

  * Add a server item manually
  * Import server items from LastPass

The following sections describe each way.

* * *

# Add a server item manually

To add a server item and, optionally, a file attachment, you must complete the following steps using the Cerby web app:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Secrets** option from the left navigation drawer. The **Secrets** view is displayed.
  3. Click the **Add secret** button. A drop-down list is displayed.
  4. Select the **Server** option from the list. The **Add Server** dialog box is displayed.
  5. Enter the information in the corresponding fields:

     * **Server label in Cerby:** It is the name of the server item that is always displayed on the secret card.
     * **Hostname:** It is the domain name or IP address of the server to which the user needs to connect.
     * **Username:** It is the user's login or account name associated with the server.
     * **Password:** It is the confidential authentication key or passphrase to access the server.
     * **Notes:** It is a space for additional information or personalized notes related to the database.

  6. Add an attachment optionally by performing the following actions:
     1. Click the **Add attachment** button. A file dialog box is displayed.
     2. Select the file you want to add as an attachment to the secret. For more information on the size limits and supported file formats, read the [Specifications](https://help.cerby.com/en/articles/7216784-explore-secrets#h_4d6ff4fb5e) section.
     3. Click the **Open** button. The file dialog box closes, and the file is displayed on the **Attachments** section.
     4. Repeat steps a to c as necessary.
  7. Select a vault where you want to save the secret from the **Vault** drop-down list.

**NOTE:** If you only have one vault, the **Vault** drop-down list is not displayed.

  8. Click the **Add Secret** button. The dialog box closes, and the secret details page is displayed.

Now you are done. You can start sharing your server items securely.

* * *

# Import server items from LastPass

To import server items from your password manager, including their file attachments, follow the instructions in the [How to use the Password Manager Importer](https://help.cerby.com/en/articles/7175132-how-to-use-the-password-manager-importer) article.

After importing your server items, you can start managing access to them securely.
