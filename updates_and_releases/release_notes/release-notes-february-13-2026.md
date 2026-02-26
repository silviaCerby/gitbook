---
description: "This article describes the latest enhancements and bug fixes to improve your experience using Cerby."
intercom_id: 13729971
---

# Release Notes - February 13, 2026

We’re closing out Q4 with a final round of enhancements and a new way of staying in touch. Moving forward, we will be transitioning to **quarterly release notes** to offer a more strategic view of our platform's evolution.

Along with this new cadence, we are excited to announce that our **[Support Portal](https://support.cerby.com/)** is now available for submitting tickets directly to our Technical Support team. This portal enables you to create and track your support requests in a centralized and streamlined way.

If you require visibility into all tickets within your workspace, beyond those you have personally submitted, please reach out to your **Customer Success (CS) manager**. They are also available to assist with any questions regarding new releases between our quarterly updates.

* * *

## New features

The following are the new features and improvements we released across the Cerby platform:

### Cerby web app

Check out what’s new in our Cerby web app:

  * We disabled the **Rotate password** button on the account details page for accounts that use Google single sign-on (SSO) for authentication.
  * We now display chips in the list of apps within the **App setting restrictions** page to indicate which restriction types were activated.

### Cerby browser extension

Explore the latest features in our Cerby browser extension:

  * We now show a confirmation message when a user uninstalls the Cerby browser extension.
  * In workspaces with local vaults, we now stop automated logins when users haven’t set up a trusted session for their Cerby browser extension.
  * When users don’t have an active session in the Cerby browser extension, the account autosave prompt now displays the **Don’t ask to save for this website again** option.
  * We have now disabled the inline menu in input fields where the content of a page is blocked by the **App setting restrictions** feature.
  * We now enforce multi-factor authentication (MFA) for Cerby accounts in local workspaces. Users cannot interact with the Cerby browser extension until they turn on MFA to access Cerby.

### Cerby mobile app

Dive into the newest additions to our Cerby mobile app:

  * We now support Chrome's new virtual view structure and HTML metadata in the autofill service for Android. This enhancement, available in v1.0.231 and later, ensures that password and username injection remains fully compatible with Chrome version 137 and above, providing a seamless login experience as browser standards evolve.
  * A new loading mechanism is now available in the account details screen to enhance security and performance. Passwords are now decrypted only when a user explicitly chooses to reveal or copy them, ensuring that sensitive credentials are not materialized in memory until they are strictly needed. This enhancement is available in Android v1.0.231 onwards.
  * The collections interface on Android was redesigned to provide a cleaner and more efficient browsing experience. This update, available in v1.0.231 and later, introduces standardized list layouts, refined item sizing, and a new sub-collection carousel, making it easier to navigate.
  * The launching apps experience is now improved by adding support for native applications and prioritizing redirect URLs. The goal is to ensure a faster, more reliable transition when opening managed web pages or native apps directly from the account details screen and quick actions. This enhancement is available in Android v1.0.231 onwards.

### Cerby API

Check out the new endpoints available in our[ developer portal](https://developer.cerby.com/) to perform the following actions with the Cerby API:

  * Accounts
    * [The account schema](https://developer.cerby.com/#the-account-schema) with the following attributes:
      * `businessId`
      * `cerbyManagedEmail`
      * `cerbyManagedPhone`
      * `hasBackupCode`
      * `hasPasskey`
      * `hasTotp`
      * `lastLoginBy`
      * `lastPasswordChange`
      * `mfaEnabled`
      * `mfaTypes`
    * [The account TOTP schema](https://developer.cerby.com/#the-account-totp-code-schema) now includes information about the account’s time-based one-time password (TOTP) codes.
    * [Retrieve the TOTP code of an account](https://developer.cerby.com/#retrieve-the-totp-code-of-an-account)
  * Collections
    * [Create a collection](https://developer.cerby.com/#create-a-collection)
  * Users
    * [The user schema](https://developer.cerby.com/#the-user-schema) now includes an `mfaStatus` attribute that indicates whether MFA is turned on for guest and local users and the date when it was turned on.
  * Teams
    * [The team account schema](https://developer.cerby.com/#the-team-account-schema)
    * [The team secret schema](https://developer.cerby.com/#the-team-secret-schema)
    * [The team collection schema](https://developer.cerby.com/#the-team-collection-schema)
    * [The team member schema](https://developer.cerby.com/#the-team-member-schema)
    * [List the accounts of a team](https://developer.cerby.com/#list-the-accounts-of-a-team)
    * [List the secrets of a team](https://developer.cerby.com/#list-the-secrets-of-a-team)
    * [List the collections of a team](https://developer.cerby.com/#list-the-collections-of-a-team)
    * [List the members of a team](https://developer.cerby.com/#list-the-members-of-a-team)
    * [Create a self-managed team](https://developer.cerby.com/#create-a-self-managed-team)
    * [Update a team](https://developer.cerby.com/#update-a-team)
    * [Delete a self-managed team](https://developer.cerby.com/#delete-a-self-managed-team)
    * [Add members to a self-managed team](https://developer.cerby.com/#add-members-to-a-self-managed-team)
  * Integrations
    * [The integration user schema](https://developer.cerby.com/#the-integration-user-schema) now includes a `dynamicFields` attribute with additional user attributes in the external app, which represent custom fields or properties specific to the integration.
* * *

## Fixes

Take note of the issues addressed and resolved by the Development team behind the Cerby platform:

### Cerby web app

  * The issue with being able to assign the **Team Admin** role to a **Guest User** via an API request was fixed, matching the behavior in the user interface (UI).
  * The issue with being able to downgrade the role of a workspace **Super Admin** to an **Admin** was fixed.
  * The issue with Snapchat Ads assets not being correctly shared with IdP-managed teams was fixed.
  * The issue where automation job error logs would display broken image links for non-existent screenshots was fixed. We now validate that error screenshots are successfully stored before generating access links in the Automation Log.
  * The issue where accounts would still be displayed as orphaned in the Security Hub even after a new owner was assigned and the page was refreshed was fixed. The orphan flag is now automatically updated upon owner assignment, ensuring accurate real-time reporting of account security status.
  * The issue of not removing access to assets in an external app after a team member’s removal from a business hub was fixed.
  * The issue where some account names are missing from the table of messages in the Shared Inbox was fixed.

### Cerby browser extension

  * The issue with page redirects when users log in to their accounts from the Okta dashboard was fixed. Users were not correctly redirected to the app after the completion of the automated login.

### Cerby mobile app

  * The issue where search options were unavailable within drop-down menus of the **Create Account** screen on iPad was fixed in iOS v1.0.278. By updating these menus to a form sheet presentation, the app now fully supports search functionality on tablet devices, allowing for easier navigation of large lists.
  * The issue with being unable to share an account via a public link from the global search results was fixed in iOS v1.0.278.
  * The issue with users being logged out frequently from the Cerby mobile app was fixed in Android v1.0.230.
  * The issue where the Cerby mobile app would occasionally crash when navigating back quickly through multiple screens was fixed in Android v1.0.230. We’ve added defensive safety checks to the navigation stack to ensure stability.
  * The issue with being unable to turn on MFA from the account details screen in the Cerby mobile app for self-managed accounts was fixed in iOS v1.0.277.
* * *

## Security fixes

  * We’ve upgraded our login security to further protect customer privacy. Our systems now provide generic feedback during the login process to Cerby, ensuring that sensitive information about your workspace remains invisible to unauthorized parties.
  * We enforced our multi-factor authentication (MFA) requirements for guest and local users. Now, they cannot add, view, or update accounts and secrets in any of our client apps (Cerby web app, browser extension, and mobile app) if they haven’t turned on MFA for their Cerby account.
