---
description: This article describes the key benefits of the File Importer feature for safely migrating your items from a CSV file to Cerby.
intercom_id: 10290203
---

# Import your items from a CSV file to Cerby

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super** **Admins** , **Admins** , and **Users**
* Only supported using the Cerby web app


{% endhint %}

With Cerby, you can seamlessly transition from a traditional enterprise password manager (EPM) by directly connecting to your EPM or using a CSV file.

The **CSV File Importer** feature in Cerby is designed to provide a universal and flexible method for migrating items by using exported CSV files as a general-purpose import format. Cerby ensures compatibility with your EPM, making it easier to transition to Cerby without extensive configuration or manual input.

With the **CSV** **File Importer** in Cerby, you gain the following benefits:

* **Streamlined migration:** You can import your data into Cerby from EPMs that support CSV exports, speeding up the onboarding process.
* **Reduced setup time:** The CSV File Importer simplifies the data migration process, minimizing the need for manual entry and avoiding complex transition processes.

This article explains how to import your items from a CSV file to Cerby.

* * *

## Requirements

The following are the requirements to use the CSV File Importer in Cerby:

  * A Cerby workspace
  * A Cerby user account with any workspace role, except **Guest Users** and **Login-Only**
  * A vault in your workspace created by a **workspace** **Admin**
  * A CSV file exported that contains the items you want to import to Cerby

  **IMPORTANT:** Ensure your CSV file contains all the required fields for the import process. For more details on the expected fields, refer to the [Supported CSV file format](import-your-items-from-a-csv-file-to-cerby.md#id-supported-csv-file-format) section.

### Supported CSV file format

The format of the supported CSV file is compatible with 1Password’s export format and includes the following fields:

  * Title
  * URL
  * Username
  * Password
  * Notes

Refer to the [Appendix](import-your-items-from-a-csv-file-to-cerby.md#id-appendix) section to download a sample file.

* * *

## Import rules

The following import rules have been established for the CSV File Importer:

  * All the imported items are automatically onboarded to Cerby. In the import report, you can see if any details are missing and enter them if necessary.
  * During the CSV import process, Cerby parses the file to extract credentials and organizes them according to its item types. After the file is parsed, Cerby aligns the imported fields with the following Cerby item types:
    * Logins become accounts
    * Secure notes become secrets
    * Software licenses become software license items
    * Passwords become accounts
    * Databases become database items
    * Servers become server items
    * Wireless routers become WiFi items
    * SSH Keys become SSH key items
  * If your file contains a URL field, make sure you use the full URL path for every account, including the scheme or protocol (**`https://`**). With a full URL, Cerby can map accounts to their correct app or service provider. For example, use **`https://www.your-app.com`**.
* * *

## Import your items from a CSV file to Cerby

To import your items to Cerby, you must complete the following main steps:

  1. [Import your items from a file to Cerby](import-your-items-from-a-csv-file-to-cerby.md#id-1.-import-your-items-from-a-file-to-cerby)
  2. [Review the import report](import-your-items-from-a-csv-file-to-cerby.md#id-2.-review-the-import-report)
  3. [Take action on onboarded items](import-your-items-from-a-csv-file-to-cerby.md#id-3.-view-item-settings)

The following sections describe each main step.

### 1\. Import your items from a file to Cerby

To import your items to Cerby from a CSV file, you must complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Click the **Add item** button from the **All accounts** view. A drop-down list is displayed.
  3. Select the **Import from password manager** option. The **Import to Cerby** dialog box is displayed.
  4. Select the **From a file** option.
  5. Click the **Get started** button. The **Choose the file source** page is displayed.
  6. Select the EPM to which your CSV file belongs.
  7. Click the **Next** button. The **Upload your file** page is displayed.
  8. Upload the CSV file by following either of the following steps:

     * Drag and drop the CSV file inside the light blue area.
     * Click the **Or select a file** button and follow the instructions.

  9. Click the **Next** button. The **Select your vault** section is displayed with the list of vaults available in your workspace.
  10. Select the vault to which you want to assign the items to import.
  11. Click the **Next** button. The **Review your items** section is displayed with the list of identified items that comply and can be imported into Cerby.
  12. Click the **Confirm** button. The previous steps must display the check (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1336562891/152259451b0bee991dbf8d84f742/AD_4nXfQIWWgHkKYMrIl7ERe2MYoA4294ILneRSZAnxqz6XVuLjwDcK5eyqXsLbGpREl8mxoAzaQkO5FXnbcJLOFLYk-bacPD_wzZsM0xPs1fxqE0D2KNFheqU1kWF3OcBPDUuoVibAg?expires=1757808000&signature=91113709c741009720aca1d1f36565a4546040ee3ecd2ed18e4079c17ec273b6&req=dSMkEMx4n4lWWPMW3Hu4gfsReTTezQc5yvrZeMAByggrs48H3%2BL1zV50obpp%0ARg%3D%3D%0A" alt="">) icon to confirm everything is correct.
  13. Click the **Import items** button. The dialog box closes, and the **Import Report** view is displayed with the message “We’re importing your items from your password manager to Cerby.”

  **NOTE:** The process may take a few minutes, depending on the number of items to import. A success message box is displayed when the import is complete, and an email is sent.

The next step is [2. Review the import report](import-your-items-from-a-csv-file-to-cerby.md#id-2.-review-the-import-report), which you must complete from the **Import Report** view.

### 2\. Review the import report

The **CSV File Importer** transfers all the items saved in your CSV file to Cerby. After an import, all transferred items are displayed in the **Import report** view.

The **Import** **report** view contains the following sections:

  * **Accounts** **and Secrets:** It displays the number of items imported to Cerby. All accounts and secrets are onboarded to Cerby, even if they are duplicates or have details missing.
  * **Users:** It displays the number of users whose Cerby user accounts were matched or unmatched to your EPM's access permissions. By clicking the D**ownload unmatched users** **report** button, you can download a CSV file with a table of unmatched users.
  * **Imported items:** It displays a table with the imported items in the following four tabs:
    * **Pending review:** It displays the items with import issues.
    * **Onboarded items:** It displays the items onboarded to Cerby.
    * **Unmatched users:** It displays the users who were not automatically matched.
    * **Matched users:** It displays the users matched to their Cerby user account and the items to which they have access through Cerby.

    **NOTE:** The **Unmatched users** and **Matched users** sections do not display any information because, for the current release, the CSV File Import does not import users.

You can download a full import report in a CSV file by clicking the **Download latest report** button located at the top right of the **Import report** view. This report contains a table with all the imported items to help you verify that your items were successfully transferred from the file you imported to Cerby.

If you see items with the `skipped` or `failed` status, the report provides information about why Cerby did not import them, and you can take action to solve the issues. For more information about this report, read the section [How to interpret the downloadable import report](import-your-items-from-a-csv-file-to-cerby.md#id-how-to-interpret-the-downloadable-import-report).

The next step is [3. View item settings](import-your-items-from-a-csv-file-to-cerby.md#id-3.-view-item-settings).

### 3\. View item settings

After importing a collection, account, or secret to Cerby, you can view its settings from the **Import report** view. To do so, you must complete the following steps:

  1. Click the **Take action** button of the corresponding collection, account, or secret. A drop-down list is displayed.
  2. Select the **Collection** **settings** option. The corresponding item details page is displayed with the **Settings** tab activated.

Now you are done.

* * *

## How to interpret the downloadable import report

When you download a full import report in CSV format after transferring your items to Cerby, you can verify if all of your individual items were successfully transferred from the file.

The table contains detailed information about the import status of every item and permission. If an item is identified as having `skipped` or `failed` status, the**Import report** also describes why it was not imported, so you can solve the issue and try again.

The following glossary describes the terms used in the table:

  * **`Item type`:** It is a column header indicating the type of imported item.
  * **`Import status`:** It is a column header indicating the import status of an individual item: successful, skipped, or failed.
  * **`Status details`:** It is a column header indicating more information for interpreting the import status.
  * **`Item path`:** It is a column header indicating the vault name in the file you imported.
  * **`Item name`:** It is a column header indicating the item name as it was saved in the file you imported.
  * **`Item username`:** It is a column header indicating the username associated with the imported account. For the permission item type, it indicates the role assigned to an imported collection.
  * **`Item URL`:** It is a column header indicating the URL associated with the imported account.
  * **`Username`:** It is a column header indicating the user’s associated username to whom a collection was assigned. It only applies to the permission item type.
  * **`Successful` (import status):** It is a status indicating the item was successfully imported from the file you imported to Cerby.
  * **`Skipped` (import status):** It is a status indicating the item was intentionally omitted from the import. For more details, see the **Status** details column.
  * **`Failed` (import status): **It is a status indicating Cerby attempted to import the item but encountered issues. For more details, see the Status details column.
  * **`Empty_collection` (status details):** It is a value indicating the collection was skipped during the import because the file was empty.
  * **`Successful` (status details):** It is a value indicating the item was imported without issues.
  * **`Unknown_permission_error` (status details):** It is a value indicating the item import failed because of an unidentified error related to permissions, suggesting a potential issue with access rights.
  * **`User_not_found` (status details):** It is a value indicating the item import failed because Cerby could not find its associated user account, possibly due to a nonexisting account or identification mismatch.

The **Import Report** displays two statuses and values that help you determine a successful collection import. When you see `collection` as the item type in the corresponding column and the successful status and value, the vault from which you exported the file was imported to Cerby without any issues.

* * *

## Appendix

The following is a sample CSV file you can download to get started. It follows the required format for the import process and showcases how to structure and label each field. Use it as a reference or template when preparing your data.
