---
description: This article helps you solve issues and find quick answers to your questions when importing items from LastPass to Cerby.
---

# Password Manager Importer troubleshooting and FAQs

This article describes the most common issues related to using our [Password Manager Importer](https://help.cerby.com/en/articles/7175132-how-to-use-the-password-manager-importer) and helps you troubleshoot them. You can also find answers to the frequently asked questions (FAQs) when importing your items from LastPass to Cerby.

We have categorized the information as follows:

  * Import checklist
  * MFA options
  * Folder and item handling
  * LastPass account verification
  * Troubleshooting error messages
  * Post-import actions

The following sections describe the issues and FAQs, and provide solutions.

* * *

# Import checklist

The following subsections describe the requirements and conditions that you must meet to perform an import successfully.

## Who can import items from LastPass to Cerby?

Any workspace member can import items from LastPass to Cerby; however, they must have an active LastPass business account with **Administrator** access permissions on the shared folders to import.

## What checks should I mark before importing items?

To prevent most of the import issues with LastPass, Cerby recommends to make sure the following three requirements and conditions are met:

  * Your master password must have at least 12 characters, following LastPass requirements; however, Cerby recommends at least 16 characters to comply with enterprise best practices. If it’s less, update your master password in LastPass by following the instructions in the [Change your master password](https://support.lastpass.com/s/document-item?language=en_US&bundleId=lastpass&topicId=LastPass/change-master-password.html&_LANG=enus)﻿ official documentation.
  * The password iterations must be set to 600,000. Follow the instructions in the [Change your password iterations for LastPass﻿](https://support.lastpass.com/s/document-item?language=en_US&bundleId=lastpass&topicId=LastPass/change-password-iterations.html&_LANG=enus)﻿ official documentation to set the value of the **Password Iterations** field to **600,000**.
  * If you use the LastPass Authenticator app as the multi-factor authentication (MFA) option, you will be prompted to accept up to three push notifications during the import process, even when you enter verification codes.
* * *

# MFA options

The following subsections describe the common issues and questions related to your configured MFA options.

## I do not have an MFA option enabled on my account. What verification code should I enter?

You can leave the verification code field blank with the **Authenticator app** option selected. If you encounter more prompts to enter a verification code throughout the import process, just click **Next**.

## What to do if I use SMS messages as my MFA option?

Our Password Manager Importer does not support SMS as a MFA method. If you use SMS messages as your MFA option to authenticate to LastPass, you must enable the LastPass Authenticator app or Yubikey options as your default method.

To install and enable the LastPass Authenticator app, complete the following steps:

  1. Install the LastPass Authenticator app on your mobile phone. If prompted, allow notifications.

**NOTE:** Make sure to install the LastPass Authenticator app, not LastPass Password Manager. The app is available for the following operating systems:

     * [iOS](https://apps.apple.com/ag/app/lastpass-authenticator/id1079110004)
     * [Android](https://play.google.com/store/apps/details?id=com.lastpass.authenticator&hl=en&gl=US)

  2. Log in to your [LastPass](https://lastpass.com/?ac=1) account.
  3. Enable the LastPass Authenticator app as your MFA option by performing the following actions:
     1. Click the **Account Settings** button located at the bottom of the left navigation drawer. The **Account Settings** dialog box is displayed.
     2. Activate the **Multifactor Options** tab.
     3. Click the **Edit** icon of the **LastPass MFA** option.
     4. Click the **Pair device again** button.
     5. Enter your master password.
     6. Open the LastPass Authenticator app on your mobile phone.
     7. Tap the **Add account** button or **Add** (+) icon.
     8. Tap the **Scan QR code** button to open the camera.
     9. Scan the QR code. A success message is displayed.
     10. Click the **ACTIVATE** button located at the bottom of the setup page. The page closes, and a success dialog box is displayed.

The LastPass Authenticator app is now set up. The next time you log in to LastPass, you’ll be asked to authenticate by entering a verification code or accepting an identity challenge via a push notification on your mobile phone.

Try to perform an import again in Cerby. When prompted to enter your LastPass login credentials, select the **Authenticator app option** from the **Configured LastPass multi-factor (MFA) option** section and leave the verification code field blank. Keep the LastPass Authenticator app open as you'll receive three push notifications throughout the import process.

For more information on enabling the LastPass Authenticator app and Yubikey, read the [Set up LastPass to use the LastPass Authenticator app](https://support.lastpass.com/s/document-item?language=en_US&bundleId=lastpass&topicId=LastPass/lastpass_authenticator_set_up_overview.html)﻿ or [Enable YubiKey in LastPass](https://support.lastpass.com/s/document-item?language=en_US&bundleId=lastpass&topicId=LastPass/configure_yubikey_auth_app.html&_LANG=enus)﻿ official documentation.

## I use Yubikey and the LastPass Authenticator app for my account. Which one should I select as the MFA option?

When you have multiple MFA methods enabled for your LastPass account, you must select the option with the highest precedence, as follows:

  * Default MFA option
  * Yubikey
  * Authenticator app

Navigate to the **Multifactor Options** tab in your **Account Settings** in LastPass to know if you have set an MFA option as default. If the **Default Multifactor Option** field is blank, you must select the **Yubikey** option in Cerby when asked to enter your LastPass login credentials.

* * *

# Folder and item handling

The following subsections describe the common issues and questions related to how the Password Manager Importer handles folders and items.

## What are the common reasons why an item is not imported?

The following are the common reasons why an item is not imported:

  * When you don’t have **Administrator** access permissions on the shared folders to import.
In this case, make sure you have the appropriate permissions on the shared folders.

  * When the items are not supported by Cerby. Currently, you can import the following item types:
    * Password
    * Secure note
    * WiFi
    * Database
    * SSH keys
    * Server
    * Software license
    * Custom item

If you have unsupported items to import, you can use a secret or a custom item in Cerby to save them manually.

  * When the selected folders don’t have saved items.
  * When you or a user with shared access to a folder don’t have enough permissions to import an item due to its unavailability access rules. Also, when you don’t have editing or view privileges (meaning you were granted the **Hide** **Password** permissions, or the **Allow recipient to view password** option is unchecked) to an individually shared item that has a password field, such as a password or a WiFi.

In this case, make sure you have the **Owner** role on all of the items to import or ask the **Administrator** of the folder to import it. Upon a successful import, other users are granted access to the corresponding collection in Cerby.

  * When you attempt to import an item from an **Accepted Share Offers** folder, meaning that the item was individually shared with a user instead of adding the item to a shared folder.

In this case, you can duplicate the item and save it inside a shared folder to import it, or ask the item **Owner** to import it to Cerby.

## Can I import all my folders and subfolders in bulk to Cerby?

Yes, you can import all of your folders and subfolders in bulk to Cerby. In the **Select folders to import** page of the import wizard, click the **Add** icon of the **Select all folders** option to select all of the folders and subfolders on the list, as shown in **Figure 1**.

<figure><img src="../.gitbook/assets/BOkA52fd5RMe1hFvZ71TKkKHWTUVRS5mNMeuQfczSNHUt7niRwk3esNVjqJJ2OjEnBuTtgPHXnwTcr8BKsgEk_c-1LN21Dfq0lKIp4M9wxMIqND9T0kFXcV2N3KUneGJ6l1gwdi0X9xZSZXIORF2BHU.png" alt=""><figcaption></figcaption></figure>

**Figure 1.** **Select folders to import** page of the Password Manager Importer wizard

The number of folders, subfolders, and items determines the time it takes to import them. Cerby will notify you via email when the import is complete.

{% hint style="info" %}


**NOTE:** Please follow your organization’s rules for storing personal passwords and secure notes in Cerby. Review the list of folders to import before proceeding if you do not want to include your personal LastPass folders.


{% endhint %}

## Why can’t I see all my folders available for import?

You can only see the folders for which you have the **Administrator** permissions in LastPass.

## What happens to folders with unavailable items?

When importing items, Cerby applies the unavailability rules that you have set in LastPass for specific recipients. In addition to the collection that Cerby creates for you as the collection Owner, new collections are created for each specific user with different availability item rules.

## What happens to subfolders?

Subfolders in LastPass are identified as subcollections in Cerby, designated by a forward slash (/). All root folders and subfolders are synced and displayed in the **Select folders to import** page of the wizard.

Every subfolder you select in the wizard is imported as a subcollection in Cerby, following the hierarchical structure.

## How can I exclude my personal folders from the import?

Our Password Manager Importer is designed to ignore personal folders; however, in some cases, they are synced and available for selection in the import wizard.

Your personal folder will be identified by the folder's name, which is commonly your personal email address associated with your LastPass account. If you have multiple personal folders, Cerby recommends nesting them all under the folder named with your personal email address. Remember to also review the folders to import before proceeding.

* * *

# LastPass account verification

The following subsections describe the common issues and questions related to the account verification actions that LastPass performs during the import.

## What should I do if I don’t receive an email from LastPass to verify Cerby’s login attempt?

The verification email from LastPass can be delayed or not even sent. Cerby suggests waiting at least one minute before proceeding with the import process.

If you encounter an error when Cerby attempts to sync your folders, you may need to retry the import and check again for the verification email or any push notification sent to your LastPass Authenticator app.

## I’m encountering errors after entering verification codes. What should I do?

Throughout the import, you may be prompted multiple times to enter new verification codes to proceed. Ensure you have done the following to prevent errors:

  * Verify you don't have any pending LastPass notifications in your email inbox or the LastPass Authenticator app. If possible, leave the LastPass Authenticator app open all the time.
  * Enter a recently created code at every step if an MFA option is enabled.
  * Verify that you have entered your LastPass credentials correctly if it is the first time you enter a code.

## I’m not receiving MFA push notifications. What should I do?

If you have the LastPass Authenticator app enabled as an MFA option, sometimes LastPass sends push notifications with a delay.

Cerby recommends leaving the LastPass Authenticator app open throughout the import process to see when push notifications arrive and complete the verification challenges.

**IMPORTANT:** Even if you enter verification codes in the Password Manager Importer, you may be prompted to complete the verification challenges for all the push notifications. In total, you receive**three push** notifications in different steps of the import:

  * After entering your login credentials
  * After verifying Cerby’s location
  * After selecting the synced folders and confirming the import

---

* * *

# Troubleshooting error messages

The following subsections help you troubleshoot the most common error messages that LastPass sends when attempting to connect, sync folders, and import items to Cerby.

## Troubleshooting: “Credentials not found” message

LastPass may send the “Credentials not found” message after the step where you enter your login credentials, as shown in **Figure 2**.

<figure><img src="../.gitbook/assets/pWGuzb7Th63wIpY9rKApvRvEV5yWH03JlUk0LllMvN7ptsZNH6P-9PUbHFn1dK05BsaARzRxSI7dyPg5yvUCgOzbpnSd4SyGZYhXZrzCDQhZMHd2CFItYCjHvIDenY2wyW_7A4g1B7f1nMRGDAq8dMA.png" alt=""><figcaption></figcaption></figure>

**Figure 2.** Error dialog box with the “Credentials not found” message

Make sure that your username and master password are correct. If after several tries it does not work, and you’ve confirmed your login information is correct, wait 10 minutes before trying again.

## Troubleshooting: "Unknown error happened on login" message

LastPass may send the "Unknown error happened on login" message when it detects multiple requests in a given time (rate limiting), as shown in **Figure 3** ; therefore, Cerby is unable to proceed with the import.

<figure><img src="../.gitbook/assets/YFt83ti2TGjIQwOqEBNWQms67xqTK3KGt7esO5Luubv9hOZNw3Ee52VSTgF_1z9hOYt6VYDtIwdl7zC586R57a13p6S3kIA5hKYmNq5nQY0TsM3Khtquy8H4dU1jjbhmvfL0On8cHU5fizb1NrAP8PI.png" alt=""><figcaption></figcaption></figure>

**Figure 3.** Error dialog box with the “Unknown error happened on login” message

Before retrying, Cerby recommends making sure you meet the three requirements and conditions from the What checks should I mark before importing items? section.

## Troubleshooting: “Failed to enter correct password” message

LastPass may send the “Failed to enter correct password” message after the step where you enter your login credentials or even after selecting the folders to import, as shown in **Figure 4**.

<figure><img src="../.gitbook/assets/smMdhGMxYC6MKqCGPESNwUryrrOR3KiSnsYfUF0Y06xM00JTPeRMmebQwRqhAvf2yPxkp7qPWsCsQkyzRRQ2H8drllkqMbnL5efqNrMd7oUmG0e1qoaJ5azy5toA5GVn5zvlgPbKl1Gz6nF12PLr-lE.png" alt=""><figcaption></figcaption></figure>

**Figure 4.** Error dialog box with the “Failed to enter correct password” message

If you have MFA enabled with the LastPass Authenticator app, make sure you complete the verification challenges for the three push notifications sent by LastPass throughout the import process. Additionally, make sure you meet the three requirements and conditions from the What checks should I mark before importing items? section.

## Troubleshooting: “Unknown error happened on groups” message

LastPass may send the “Unknown error happened on groups” message after verifying Cerby’s location and before syncing your LastPass folders, as shown in **Figure 5**.

<figure><img src="../.gitbook/assets/kALyqWK_7P7qSBvmkAOOOBsNC47jSMhNnL__lJtbnjKBdZuK5Z6ya4kJp1lbJtYMJ7G-_03AWTZP4Vdy8jnpy8vKlpTvBX11j4wHQmiIEpMSA0LIHVD48bf5-kX7TDrJnLc1DsHWKYjyiNEQ2vocBc4.png" alt=""><figcaption></figcaption></figure>

**Figure 5.** Error dialog box with the “Unknown error happened on groups” message

This error happens when a LastPass shared folder is out of sync. To sync these folders, you must log in to LastPass, select one password for each shared folder and subfolder, and launch it. If you want to sync a folder with secure notes only, you must click the **Edit** button for one of them.

{% hint style="info" %}


**NOTE:** You don’t have to launch every password inside a folder and subfolder.


{% endhint %}

## Troubleshooting: “Waiting for approval of out-of-band LastPass Authenticator login” message

LastPass may send the “Waiting for approval of out-of-band LastPass Authenticator login” message when a push notification is missing or ignored in the LastPass Authenticator app, as shown in **Figure 6** ; therefore, Cerby is unable to proceed with the import.

<figure><img src="../.gitbook/assets/IDJVGfuZvmROpj2vpC0qdihz2MTeOWahWFQr0ECrZ2_c8l37iyb2KxRCvZTX07PaIqciVNzElk8nhEnpvxtk-u1TU9PUG_eJi7p6mKiKkhT0jJ6QQ6NTpV9JgLbLxt08WcfsMTi4T1DIV-mKTIyIEWI.png" alt=""><figcaption></figcaption></figure>

**Figure 6.** Error dialog box with the “Waiting for approval of out-of-band LastPass Authenticator login” message

If you have MFA enabled with the LastPass Authenticator app, make sure you complete the verification challenges for the three push notifications sent by LastPass throughout the import process.

## Troubleshooting: “Something unexpected happened” message

When a migration from LastPass is not completed because of an unexpected issue, the Cerby web app displays the “Something unexpected happened” error message in the **Import report** view, and an email is sent to the email registered in the LastPass account.

Both in the email message and the error message, Cerby provides a migration ID. To help you troubleshoot the issue, share this ID with the Cerby Customer Support team by emailing [support@cerby.com](mailto:support@cerby.com) or writing a message via the help chat in your Cerby dashboard describing the issue.

Additionally, before retrying the import, ensure you have checked the following:

  * Look in your email inbox for any messages from LastPass.
  * Verify you have entered the correct username and password. If you are copy-pasting, check for trailing spaces.
  * Use a new code each time a MFA verification code is requested throughout the import process.
* * *

# Post-import actions

The following subsections describe the common issues and questions after performing an import.

## Why do I see some accounts identified as duplicates in the import report?

Accounts are identified as duplicates when they have the same domain and username as another account in the Cerby workspace. This may mean that another user within your team has imported the account already or you have previously added the account to Cerby.

## What is an unmatched user?

Users identified as unmatched in the **Import report** view were not automatically matched during the import because they used an email address that couldn’t be identified, they are not in your corporate directory, or they don’t have access to Cerby.

You can invite external collaborators to join your Cerby workspace as guest users and grant them the access permissions they had in LastPass. For instructions on how to invite guest users after an import, read the [Guest users](https://help.cerby.com/en/articles/7175132-how-to-use-the-password-manager-importer#h_40dceb49ed) section from the [How to use the Password Manager Importer](https://help.cerby.com/en/articles/7175132-how-to-use-the-password-manager-importer) article, or see the [How to invite a guest user from the Password Manager Importer](https://help.cerby.com/en/articles/8432615-video-how-to-invite-a-guest-user-from-the-password-manager-importer) video.

## I performed a new import but want to see previous reports. How can I go back to a previous report?

Upon a successful migration, Cerby will send you an email with a unique link to the specific import. Opening the provided link will redirect you to the **Import report** view for that import attempt.

## Why do I see a previous and not the latest import in the **Import report** view?

The information of a previous import report is displayed on the **Import report** view if you leave this view open when transferring your items from LastPass. To display the latest report, wait until the import process is complete and refresh the page.
