---
description: This article describes how to add a database item to your Cerby workspace.
intercom_id: 8705340
---

# Add a database item

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* You must have already set up your [trusted devices](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/trusted-devices/set-up-trusted-sessions-on-your-devices)
* Only supported using the Cerby web an mobile apps


{% endhint %}

You can add a database item and attachments to Cerby in the following two ways:

* [Add a database item manually](add-a-database-item.md#id-add-a-database-item-manually)
* [Import database items from LastPass](add-a-database-item.md#id-import-database-items-from-lastpass)

The following sections describe each way.

* * *

## Add a database item manually

To add a database item and, optionally, a file attachment, you must complete the following steps using the Cerby web app:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Secrets** option from the left navigation drawer. The **Secrets** view is displayed.
  3. Click the **Add secret** button. A drop-down list is displayed.
  4. Select the **Database** option from the list. The **Add Database** dialog box is displayed.
  5. Enter the information in the corresponding fields:

     * **Database label in Cerby:** It is the name of the database item that is always displayed on the secret card.
     * **Type:** It is the type of database, such as MySQL, PostgreSQL, MongoDB, or other database management systems.
     * **Hostname:** It is the unique identifier of the server or machine name where the database is hosted.
     * **Port:** It is a numerical value of the specific communication endpoint on the server where the database is listening for incoming connections.
     * **Database:** It is the name of the specific database within the database server that the user wants to access or manage.
     * **Password:** It is the authentication key or passphrase required to access the database.
     * **SID:** It identifies a particular Oracle instance in a distributed network environment.
     * **Alias:** It is a user-defined name that can be used as a reference for the database.
     * **Notes:** It is a space for additional information or personalized notes related to the database.

  6. Add an attachment optionally by performing the following actions:
     1. Click the **Add attachment** button. A file dialog box is displayed.
     2. Select the file you want to add as an attachment to the secret. For more information on the size limits and supported file formats, read the [Specifications](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-secrets) section.
     3. Click the **Open** button. The file dialog box closes, and the file is displayed on the **Attachments** section.
     4. Repeat steps a to c as necessary.
  7. Select a vault where you want to save the secret from the **Vault** drop-down list.

  **NOTE:** If you only have one vault, the **Vault** drop-down list is not displayed.

  8. Click the **Add Secret** button. The dialog box closes, and the secret details page is displayed.

Now you are done. You can start sharing your database items securely.

* * *

## Import database items from LastPass

To import database items from your password manager, including their file attachments, follow the instructions in the [How to use the Password Manager Importer](https://cerby-test.gitbook.io/cerby-test/management/credential-management/item-importer/migrate-from-lastpass-to-cerby) article.

After importing your database items, you can start managing access to them securely.
