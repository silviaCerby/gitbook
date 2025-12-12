---
description: 
---

# Release Notes - October 12, 2023

# New Features

  * We're exhilarated to announce the release of Cerby Protect, a highly requested product that has been in development this year.

Cerby Protect is our enterprise password management offering designed to provide you with a seamless security experience when accessing your corporate sensitive data and collaborating with your coworkers and external parties.

With this product, Cerby introduces two main features to empower you to leverage a Zero Knowledge architecture, where Cerby has no knowledge or access to the decryption keys and the data stored in your vaults:

    * Local encryption for the vaults you use to save your accounts and secrets.
    * Trusted devices implementation to make sure only the Cerby client apps (web app, browser extension, and mobile app) registered by users can access and decrypt the encrypted vaults.

What are you waiting for? Take a look at the [Get started with Cerby Protect](https://help.cerby.com/en/articles/8358920-get-started-with-cerby-protect) article to learn more about the benefits and supported features. Also, check out the **Vault strategy** section in the **Privacy and security** tab of the workspace settings page, as shown in **Figure 1**.

<figure><img src="../.gitbook/assets/cQKkRVyc7bdqtpo5JAnSJN8aDAGQA-gfSWQg_24pZWaECsb6nI0FzAEmqJanZIKCNMH77kt2hjS-0dhJsWl3zVMtfYQQYruaCU3DLOVkpCFO3QbR-0ELyXnSsf0x-Gx2ihQ14y6b9rskCL64Xk37fFc.png" alt=""><figcaption></figcaption></figure>

**Figure 1.** **Vault strategy** section in the **Privacy and security** tab

  * Good news never comes alone. You can access now the following features as part of the Cerby Protect release:
    * A password generator is available through the Cerby browser extension, as shown in **Figure 2**. You can use it to generate secure customized passwords that meet the requirements of your applications or service providers by selecting the password strength rules.

<figure><img src="../.gitbook/assets/oPgxkESOs3hnhPzy8WZYkzUuym9Y8gJABCSlRkeE41IszP36K5qzqIgst9NWkrcTiStjD3_ye3L-wFwOEovmU1wqNjp8-xJ_WOc0XrRmRF18l4zmc3rX0xp2KEu_BrK8F1QVQhTqaqAKy21rwSGgAkQ.png" alt=""><figcaption></figcaption></figure>

**Figure 2.** **Password generator** page in the Cerby browser extension popup

For more information, read the [How to generate secure passwords using the Cerby browser extension](https://help.cerby.com/en/articles/8377075-how-to-generate-secure-passwords-using-the-cerby-browser-extension) article.

    * The **Add item** button is available through the **All accounts** view. With this button, a drop-down list is displayed with the following options to select the type of item to add to Cerby:
      * **Account**
      * **Secret**
      * **Collection**
      * **Import from password manager**

The goal is to save you steps when adding an item to Cerby. Each option takes you to the corresponding dialog box.

    * Installing the Cerby browser extension is recommended but not required for Cerby Protect users. If you want to leverage the magic of the automatic login, you better install it.
    * With the support for trusted devices, we introduce the user profile icon in the browser extension.
    * With the release of trusted devices, we introduce the user profile icon in the Cerby browser extension with the following options:
      * **My trusted devices**
      * **Log Out**
  * Cerby now supports automatic login through the Cerby browser extension on http:// websites.
  * **Workspace Admins** can now assign Cerby products to teams via the **Teams** view.
  * We have recharged our Password Manager Importer based on your feedback and the needs of Cerby Protect users. Here’s what’s new:
    * Only users with **Administrator** permissions on the LastPass shared folders can perform an import to Cerby.
    * Shared folders can only be imported one time to avoid duplicate items.
    * All items are imported, regardless if they have all of the item details.
    * Batch imports are now supported to transfer multiple shared folders with numerous items.
    * The importer provides more visibility on errors by displaying the error messages sent by LastPass. The goal is to make it easier to know what happened and solve the issue.
    * Items are imported to the default vault, whether it is a cloud or local vault.
    * The unavailability rules that you set in LastPass for specific recipients are applied to the imported items.
  * We keep thinking about different ways to safeguard your information. Now, when you open any dialog box in your Cerby dashboard using the web app, the background is blurred.
  * New to Cerby? This feature was crafted especially for you. Our Cerby browser extension now preloads the name of the workspace you have been assigned and logged in previously using the Cerby web app.
  * We’ve been working on our flexibility. With the release of Cerby Protect and the changes to our Password Manager Importer, you can now add accounts with no passwords, and all the Cerby client apps support it.
  * After creating a secret, you are now redirected to the secret details page.
  * We wanted you to have the numbers and visibility you need to make informed decisions. **Workspace Admins** can now see the number of active users within a workspace through the **All members** view. Previously, this number included deactivated users.
  * For a consistent user experience, we’ve tuned up the actions that users can perform on managed and self-managed accounts according to their roles:
    * Owners
      * They can edit the account details, view passwords, and copy passwords through the Cerby web app.
      * They can edit the account details (after being redirected to the Cerby web app), view passwords, and copy passwords through the Cerby browser extension.
      * They can copy passwords through the Cerby mobile app.
      * They can view, copy, and fill in all the input fields for managed and self-managed apps using the inline menu.
    * Collaborators
      * They can only copy passwords through the Cerby web app, browser extension, and mobile app.
      * They can only fill in the **Password** field for managed apps using the inline menu.
      * They can only copy and fill in the **Password** field for self-managed apps using the inline menu.

**NOTE:** These changes were released in the Cerby browser extension v1.0.228 and the Cerby mobile app in iOS v1.0.95 and Android v1.0.111.

  * We’ve streamlined the process of deleting an account. Now, you don’t have to accept an identity challenge from a push notification on your Cerby mobile app.
  * We did it for collections, and now it’s the turn of accounts. The limit on the **Account label** when adding or editing an account for self-managed apps is now set to 100 characters.
  * Our Tenants feature and business centers keep evolving to suit your needs:
    * We’ve implemented a multi-step navigation for Pinterest Ads that takes you back to the tenant **Assets** page.
    * Role updates now propagate when tenant admins invite members to multiple teams assigned via groups from the identity provider (IdP).
    * Now, you can set up your authentication method and identity provider to support single sign-on (SSO). Cerby can redirect you to the corresponding login page and prevent the provisioning automation workflow from sending invites to users who belong to an IdP.
    * You can now select multiple tenant assets to share them with other users. Previously, you had to select them one at a time.
    * We’ve got you covered in case the account creator no longer has access to a business center. You can now run policy checks for updates as a tenant owner.

# Fixes

## Cerby web app

  * The issue with being unable to find all the Google Workspace users assigned to Cerby when sharing an item is fixed. Previously, users had to log in to Cerby to be searchable.
  * The issue with being unable to find new users added to a workspace when sharing a secret is fixed.
  * The issue with sending a warning message box about a duplicate team name after adding users to a team, and not in the step where you enter the name, is fixed. Additionally, the list of users added to the team is preserved when navigating through the **Create team** wizard.
  * The issue with deleted accounts being displayed in the **All accounts** view when changing from the grid to the list layout is fixed.
  * The issue with displaying the **View** icon in all the fields inside the **Account details** section is fixed.
  * The issue with the security widget in the account details page being displayed momentarily with the “Your account is protected” status instead of the real status is fixed.
  * The issue with being unable to remove users from a Meta Pixel asset through a tenant is fixed.
  * The issue with importing from LastPass the body of a secret without line breaks is fixed.
  * The issue with not displaying the **All account collaborators** option when setting up the auto-forward feature for the messages you’ll receive in a new Cerby-managed email address is fixed.
  * Users with the **Collaborator** role on a secret can no longer access the secret details page from the **Teams** view.
  * The issue with typing and at the same time retrieving the list of users from the corporate directory when sharing a secret is fixed. Previously, the “Something wrong happened” message was displayed.
  * The issue with non-**Workspace Admins** being able to download the list of users from the **All Members** view is fixed.

## Cerby mobile app

  * The issue with not clearing immediately the cache when logging out from a workspace and logging in to a different workspace is fixed in iOS v1.0.79 and Android v1.0.105. The Cerby mobile app no longer displays the accounts from the first workspace.
  * The issue with WeChat accounts crashing the Cerby mobile app when accessing the account details screen is fixed in iOS v1.0.86 and Android v1.0.107.
