# Release Notes - November 30, 2023

# New Features

The following are the new features and improvements we released across the
Cerby platform:

  * We introduced the **Super Admin** role to our role-based access control (RBAC) system to provide you with more granularity on your management actions. Super Admins can do the following in a Cerby workspace:

    * Manage product assignments to Cerby Protect and Cerby Automate.

    * View the items to which all teams have shared access.

    * Turn on **All-Access Mode** to view all accounts in a workspace.

For more information, read the [How Cerby manages
roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles)
article.

  * Based on your feedback, we now support accounts with IP addresses as the login URL.

## **Cerby web app**

Check out what’s new in our Cerby web app:

  * You spoke, and we listened! We changed the default one-click action of the account cards in your Cerby dashboard. Now, you are redirected to the account details page instead of initiating an automatic login.

  * We made the following improvements and changes to the Password Manager Importer:

    * The time to import items was substantially reduced due to code optimization. 

    * Long folder names synced with LastPass are now displayed with an ellipsis to make it easier to navigate through the list of folders to import.

    * Imported folders can be reimported in case you have missing items or user access permissions.

  * New to [Cerby Protect](https://help.cerby.com/en/articles/8358920-get-started-with-cerby-protect) and to the concept of trusted devices? We improved our messaging in the Cerby web app, in-context alerts, and the inline menu of the Cerby browser extension. We want to let you know clearly when you must set up a trusted device to access the accounts and secrets stored in your workspace vault.  
Remember that a trusted device can be only one of the three Cerby client apps:
Cerby web app, browser extension, and mobile app.

  * Did you ever feel hesitant when deleting an account from Cerby? We improved our confirmation message to let you know that you’re deleting an individual account, not your entire Cerby account.  
Additionally, to shorten the account deletion process, we removed the push
notification to confirm your identity with the Cerby mobile app. We value your
time.

  * You can now rename your self-managed teams by clicking the **Edit** icon next to the team name after selecting it from the list in the **Teams** view.

  * We made it easier to invite external collaborators to join your Cerby workspace after an item import from LastPass. You can now invite multiple guest users by selecting them from the **Unmatched users** tab of an import report and clicking the **Invite as guests** button. 

  * Item **Owners** can now select multiple users from the **Members** tab to remove them in bulk from accounts and secrets. The table is automatically refreshed.

Our Tenants feature and business center integrations received some love:

  * Admins of a Meta Business Manager integration can now select in Cerby the user management and login method for their users:

    * **Username and password:** Users are prompted to save their login credentials in Cerby, and admins can secure access to the Meta Business Manager with multi-factor authentication (MFA) and password rotation. 

    * **Single sign-on (SSO):** Users authenticate to Meta Business Manager with their identity provider, which means they are not prompted to save their login credentials in Cerby.

  * When you perform a check for updates, disabled users in your app are now skipped during the automatic account match in Cerby.

  * You can now share tenants and business center integrations with self-managed teams, which triggers the corresponding user provisioning and invite tasks. This feature is available only to license-based and paid social media apps that support bulk actions.

  * Tenant owners can now resend themselves an invite from Cerby to create their account and join the app. Just click the corresponding **Resend invite** button from the **Onboarded users** tab inside the **Members** tab of the tenant details page.

  * Business center integration owners can now add an automation account that Cerby will use to perform RPA-based automation tasks. Just click the **Add account** button from the business center details page, and a dialog box will guide you through the process of selecting an existing account or adding a new one to Cerby.

  * IT admins can now set up the **Share with assets** dialog box to be displayed when inviting users to a Pinterest Business Center integration. 

  * **Owners** of a Meta Business Manager integration can now revoke an invite sent to a user from the **Members** tab of the business center details page. 

## **Cerby browser extension**

Our Cerby browser extension keeps evolving with the following features and
improvements:

  * You can now click a button in the extension popup to add an account and a secret. You are redirected to the corresponding dialog box in a new tab to complete the process through the Cerby web app. In a future release, you’ll be able to do it directly on the browser extension.

  * The inline menu of the Cerby browser now displays your accounts faster after you click the Cerby logo inside an input field. 

  * The password generator now keeps the same strength rules you set whenever you close the browser extension and come back to this feature.

  * The **Accounts** tab of the Cerby browser extension popup now only displays active accounts. Previously, you could also view disabled accounts.

  * The Cerby logo is now displayed inside the input fields of a login page even when you don’t have an active session in the Cerby browser extension. When clicking on the logo, you are prompted to log in to Cerby.

  * We’ve standardized the following actions that account Collaborators can perform through the inline menu of the Cerby browser extension in v1.0.243:

    * Use the **Fill** button to fill in the password for managed accounts.

    * Use the **Copy** icon or the **Fill** button to paste or fill in the password for self-managed accounts.

# Fixes

## **Cerby web app**

  * The issue with redirecting external users to an unknown website when clicking the **Go to website** button of an account public link is fixed. Also, we are displaying the missing fields when sharing self-managed accounts. 

  * The issue with displaying “Mixed role” as the Cerby role in the **Members** tab of the account details page when users only have one role imported from LastPass is fixed. This value is only displayed when users have multiple **Collaborator** and **Owner** roles after importing their items. 

  * The issue with displaying a previous import report with pending items instead of the latest report is fixed. This issue was happening even when the latest import from LastPass was successful.

  * The issue with skipping imported collections from LastPass is fixed. Sometimes, these collections were removed from Cerby before performing a new import. 

  * The issue with being unable to view a secret even after accepting the push notification to confirm the user’s identity is fixed.

  * The issue with the Password Manager Importer identifying LastPass passwords as subfolders when they have a forward slash in their names is fixed. 

  * The issue with encountering a loading process deadlock when switching between teams after navigating through different pages in the **Members** tab of the **Teams** view is fixed.

  * The issue with performing an automated password rotation from a tenant in Cerby for the service account instead of a specific user account is fixed.

  * The issue with displaying incorrectly the “Connect your account” message for a tenant card when using the top search bar of the Cerby dashboard is fixed.

  * The issue with not refreshing the list of users in the **Members** tab after sharing a tenant asset in Cerby is fixed.

## **Cerby browser extension**

  * The issue with not displaying the password generator in the inline menu when creating an account through a signup page is fixed in v1.0.239.

  * The issue with not filling in the password when clicking the **Use password** button in the inline menu is fixed in v1.0.239.

  * The issue with adding a self-managed account twice with the Save credentials at login feature is fixed in v1.0.239.

  * The issue with opening multiple inline menus when switching between fields is fixed in v1.0.240.

  * The issue with the inline menu not supporting IP or non-fully qualified domains is fixed in v1.0.240.

  * The issue with not displaying the dialog box to update the login details of an existing account in Cerby when detecting a signup event is fixed in v1.0.242.

  * The issue with displaying the workspace selection page instead of the login page when clicking the **Log in** button for a specific workspace through the inline menu is fixed in v1.0.243.

  * The issue with being unable to collapse the inline menu after opening it is fixed in v1.0.243.

  * The issue with not detecting a successful login through the Save credentials at login feature after an unsuccessful login due to incorrect credentials is fixed in v1.0.245.

  * The issue with the inline menu disappearing outside of the visible browser view is fixed in v1.0.250. 

  * The issue with not detecting logins through the Save credentials at login feature when the website domain changes is fixed v1.0.252.

## **Cerby mobile app**

  * The issue with not copying the MFA verification code after autofilling the login credentials for a Hootsuite account is fixed in iOS v1.0.99.

# Security Fixes

  * We disabled the HTTP cache stored by mobile apps for requests with sensitive information in iOS v1.0.99 and Android v1.0.118.

