# Import your items from a CSV file to Cerby

## This article describes the key benefits of the CSV File Importer feature for safely migrating your items from a CSV file to Cerby.

| Who can use this feature? Workspace Owners, Super Admins, Admins, and Users Only supported using the Cerby web app |
| :---- |

With Cerby, you can seamlessly transition from a traditional enterprise password manager (EPM) by directly connecting to your Enterprise Password Manager (EPM) or using a CSV file.

The **CSV** **File Importer** feature in Cerby is designed to provide a universal and flexible method for migrating items by using exported CSV files as general-purpose import formats. Cerby ensures compatibility with your EPM, making it easier to transition to Cerby without extensive configuration or manual input.

| IMPORTANT: Currently, Cerby only supports CSV files exported from 1Password. |
| :---- |

With the **CSV File Importer** in Cerby, you gain the following benefits:

* **Streamlined migration:** You can import your data into Cerby from EPMs that support CSV exports, speeding up the onboarding process.  
* **Reduced setup time:** The CSV File Importer simplifies the data migration process, minimizing the need for manual entry and avoiding complex transition processes.

This article describes how to import your items to Cerby from a CSV file.

# **Requirements**

The following are the requirements to use the CSV File Importer in Cerby:

* A Cerby workspace  
* A Cerby user account with any workspace role, except **Guest Users** and **Login-Only**  
* A vault in your workspace created by a **workspace** **Admin**  
* A CSV file exported from your EMP that contains the items you want to import to Cerby

## **Supported CSV file format**

The format of the supported CSV file is compatible with 1Password’s export format and includes the following fields:

* Title  
* Website  
* Username  
* Password  
* One-time password\*  
* Favorite status\*  
* Archived status\*  
* Tags\*   
* Notes

| IMPORTANT: Consider the following important notes: Items marked with an asterisk (\*) are supported in the CSV file to import to Cerby. However, they are not mapped to any field in Cerby and are ignored in the import process. A Notes column is supported and imported. |
| :---- |

The file format does not include the following fields:

* Security questions  
* Linked items  
* Linked apps  
* Custom fields

# **Import rules**

The following import rules have been established for the CSV File Importer:

* All the imported items are automatically onboarded to Cerby. In the import report, you can see if any details are missing and enter them if necessary.  
* During the CSV import process, Cerby parses the file to extract your items and organizes them according to their type. After the file is parsed, Cerby aligns the imported fields with the following Cerby item types:  
  * Logins become accounts  
  * Secure notes become secrets  
  * Software licenses become software license items  
  * Passwords become accounts  
  * Databases become database items  
  * Servers become server items  
  * Wireless routers become WiFi items  
  * SSH Keys become SSH key items  
* Ensure that if your file contains a URL field, you use the full URL path. For example, use [https://cerby.com](https://cerby.com). 

# **Import your items to Cerby from a CSV file**

To import your items to Cerby from a CSV file, you must complete the following main steps:

1. [Import your items to Cerby from a file](#1.-import-your-items-to-cerby-from-a-file)  
2. [Review the import report](#2.-review-the-import-report)  
3. [Take action on onboarded items](#3.-view-item-settings)

The following sections describe each main step.

## **1\. Import your items to Cerby from a file** {#1.-import-your-items-to-cerby-from-a-file}

To import your items to Cerby from a CSV file, you must complete the following steps:

1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.  
2. Click the **Add item** button from the **Accounts** view. A drop-down list is displayed.  
3. Select the **Import from password manager** option. The **Import to Cerby** dialog box is displayed.  
4. Select the **From a file** option.  
5. Click the **Get started** button. The **Upload your file** page is displayed.  
6. Upload the CSV file by completing either of the following steps:  
   * Drag and drop the CSV file inside the light blue area.  
   * Click the **Or select a file** button and follow the instructions.  
7. Click the **Next** button. The **Select your vault** section is displayed with the list of vaults available in your workspace.  
8. Select the vault to which you want to assign the items to import.  
9. Click the **Next** button. The **Review your items** section is displayed with the list of identified items that comply and can be imported into Cerby.  
10. Click the **Confirm** button. The previous steps must display the check (![][image1]) icon to confirm everything is correct.  
11. Click the **Import items** button. The dialog box closes, and the **Import Report** view is displayed with the “We’re importing your items from your password manager to Cerby” message.  
    **NOTE:** The process may take a few minutes, depending on the number of items to import. When the import is complete, a success message box is displayed, and an email is sent.

The next step is [2\. Review the import report](#2.-review-the-import-report), which you must complete from the **Import Report** view.

## **2\. Review the import report** {#2.-review-the-import-report}

The **CSV File Importer** transfers all the items saved in your CSV file to Cerby. After an import, all transferred items are displayed in the **Import report** view.

The **Import** **report** view contains the following sections:

* **Accounts** **and Secrets:** It displays the number of 1Password items imported to Cerby. All accounts and secrets are onboarded to Cerby, even if they are duplicates or have details missing.   
* **Users:** It displays the number of users whose Cerby user accounts were matched or unmatched to 1Password access permissions. You can download a CSV file with a table of unmatched users by clicking the **Download unmatched users report** button.  
* **Imported items:** It displays a table with the imported items in the following four tabs:  
  * **Pending review:** It displays the items with import issues.  
  * **Onboarded items:** It displays the items onboarded to Cerby.  
  * **Unmatched users:** It displays the users who were not automatically matched.  
  * **Matched users:** It displays the users matched to their Cerby user account and the items to which they have access through Cerby.   
    **NOTE:** The **Unmatched users** and **Matched users** sections do not display any information after because, for the current release, the CSV File Importer does not support importing users.

You can download a full import report in a CSV file by clicking the **Download latest report** button located at the top right of the **Import report** view. This report contains a table with all the imported items to help you verify that your items were successfully transferred from the CSV file.

If you see items with the skipped or failed status, the report provides information about why Cerby did not import them, and you can take action to solve the issues.

For more information about this report, read the section [How to interpret the downloadable import report](#how-to-interpret-the-downloadable-import-report).

The next step is [3\. View item settings](#3.-view-item-settings).

## **3\. View item settings** {#3.-view-item-settings}

After importing a collection, account, or secret to Cerby, you can view their settings from the **Import report** view. To do so, you must complete the following steps:

1. Click the **Take action** button of the corresponding collection, account, or secret. A drop-down list is displayed.  
2. Select the **Collection** **settings** option. The corresponding item details page is displayed with the **Settings** tab activated.

# **How to interpret the downloadable import report** {#how-to-interpret-the-downloadable-import-report}

When you download a full import report in CSV format after transferring your items to Cerby, you can verify if all of your individual items were successfully transferred from the file. 

The table contains detailed information about the import status of every item and permission. If an item is identified with the **skipped** or **failed** status, the import report also describes why it was not imported so you can solve the issue and try again.  
The following glossary describes the terms used in the table:

* **Item type:** It is a column header indicating the type of imported item.  
* **Import status:** It is a column header indicating the import status of an individual item: successful, skipped, or failed.  
* **Status details:** It is a column header indicating more information for interpreting the import status.  
* **Item path:** It is a column header indicating the vault name in the file you imported.  
* **Item name:** It is a column header indicating the item name as it was saved in the file you imported.  
* **Item username:** It is a column header indicating the username associated with the imported account. For the permission item type, it indicates the role assigned to an imported collection.  
* **Item URL:**  It is a column header indicating the URL associated with the imported account.  
* **Username:** It is a column header indicating the user’s associated username to whom a collection was assigned. It only applies to the permission item type.  
* **Successful (import status):** It is a status indicating the item was successfully imported from the file you imported to Cerby.  
* **Skipped (import status):** It is a status indicating the item was intentionally omitted from the import. For more details, see the **Status** details column.  
* **Failed (import status):** It is a status indicating Cerby attempted to import the item but encountered issues. For more details, see the Status details column.  
* **Empty\_collection (status details):** It is a value indicating the collection was skipped during the import because the file was empty.  
* **Successful (status details):** It is a value indicating the item was imported without issues.  
* **Unknown\_permission\_error (status details):** It is a value indicating the item import failed because of an unidentified error related to permissions, suggesting a potential issue with access rights.  
* **User\_not\_found (status details):** It is a value indicating the item import failed because Cerby could not find its associated user account, possibly due to a nonexisting account or identification mismatch.

The **Import Report** displays two sets of statuses and values that help you determine a successful import for collections. When you see collection as the item type in the corresponding column and the successful status and value, it means the 1Password vault from which you exported the file was imported to Cerby without any issues.

[image1]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAUCAYAAACNiR0NAAACXUlEQVR4XpWU208TQRTG+1+23RbaIm1jgNhijA8thAeUmpCgmJho4osxkRBbCSltgbU+eCmxSoISNKkXKiFIBJTe2F52Ps/sFro7W7Du5Es2M+f8Zs45c8bGGMNFUkktpmpSSeK6KJs4oYlGYj2J8VQMlxJDcKW8kNIe+BaCGMvewFrpA1RuJfp1A7bQxEQ6BteSD/ZVV1uS4d8FZ6Yf97YeoU62or8JeNwowf902ORsX3V2/mUObsNlFwYTIVShaBFZgNV6lWAjAuzfir6N4QgVYqAD5MkOz0dgX3FbHHrR8KtrhFR0IOi7/nhMyNl5onBlJ6JfpimPHtPaD3W/A7w8fxWOlb4ugO7aZNu4mbttiEhCtpyngrZgq6MBz2Kgp3D5phutb/i8V4B7aUADna6F3o0TiYAKFd+d5OHyRb2i7hd0757TnOHUDtmNAiviQDmCd2HIspm0NEjAJmw1pkBKmfMXP8jgmNI8m7sPx7J+8vTJG+yUdyk9YQtMBw5QWRp6yP2LfiFkCTOfHhK0hq0/X/FkP4Oaqmhd41junuvJ73f0kHkL+eNXYNcMzdDIyymc0L6/UcLc67ilskbNlWQdyEs9k3sAZ9orGOlwvzyCxMckHGkOM7egUQW2o/X3WacE4qMWo94kYXQ9ijI1oan1mqwF37P/bT0J0c1bKLKf1l7mKrUqdCeDVCCj0/n3c7J4l/JbsT4OZ28bjUO1QvcyoO0uAowKvY9gl/2yvIvtE+ovxakaNPKHG5jIT6Mv69eqyxVcC2OqMItttkfVb5h8BODF4qfgORbnu+kvDsPCMisMdfIAAAAASUVORK5CYII=>