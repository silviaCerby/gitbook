---
description: 
intercom_id: 6818448
---

# Release Notes - December 12, 2022

## New Features

* The [Android v1.0.70](https://play.google.com/store/apps/details?id=com.cerby) and [iOS v.1.0.18](https://apps.apple.com/us/app/cerby/id1533747684) versions of the Cerby mobile app are now available with features such as the following:
    * A new onboarding process
    * A welcome card to set up the missing configuration
    * Support for tenant accounts, as part of the Tenants feature release
    * Support for displaying a screen when the mobile phone has no internet
    * The keyboard is now hidden when scrolling through lists of accounts
    * Minimum support updated for Android 8 and iOS13
    * Analytics events
    * The icons of the account cards for non-supported apps now display initials
    * The current provider lost after re-logging in is fixed
* In-context alerts are now available in the Cerby browser extension v1.0.149 for supported apps. This feature provides users visibility into the following:
Users can activate or deactivate in-context alerts from the **Settings** screen of the browser extension.

    * What happens in every step of an automation workflow
    * Why an automation workflow failed and what to do next
    * What to do when an automation workflow requires user intervention to continue
* Slack is now supported with automatic login and password rotation.
* Outkick is now supported with automatic password rotation and MFA enrollment.
* Users can now enter usernames with dots when adding a TikTok account through the **Add Account** wizard.
* The user avatar is now improved in the **Members** tab of the **Collections** view.
* The flow to create an account from the Cerby browser extension is now removed.
* Password rotation is now disabled from the account details page if an account does not have a Cerby-managed email address.
* Autofill for MFA in the Cerby web app is now turned on by default for all new accounts.
* The loading time of the **Collections** view is now improved.
* The **Verify Your Identify** screen is now implemented as part of the automatic login for Salesforce and Hootsuite.
* An email confirmation screen is now implemented during an automatic password rotation for a Pinterest account.

## Fixes

* The issue with the **Activity** view displaying unknown users for any account activity in Firefox is fixed.
* The issue with the time-based one-time password (TOTP) seed for an Amazon Seller account not being accepted because of its length in Cerby when turning on multi-factor authentication (MFA) is fixed.
* The issue with exporting members from the **All members** view is fixed.
* The issue with the account card avatar flickering is fixed in the Cerby browser extension.
* The issue with the MFA enrollment automation failing because of a dialog box asking to access contacts for an Instagram account is fixed.
* The issue with the **Forward Message** button taking some time to activate in the **Forward Message** dialog box is fixed.
* The issue with loading the dashboard after performing a password manager migration for the first time is fixed.
* The issue with being unable to remove a Cerby-managed email address because the **Cerby-managed email settings** dialog box disappears is fixed.
* The issue with the **Add Account** wizard taking some time to complete the process of adding an account is fixed.
* The issue with the infinite scroll performing the same call multiple times for the same page is fixed.
* The issue with the Cerby browser extension stuck in the logging in state for TikTok and not allowing other logins is fixed.
* The issue with the **grouped by** component changing the size and distribution of account cards is fixed.
* The issue with logging out automatically from a Loom account is fixed.
* The issue with not opening a new tab when logging in to a different account from the same app using the Cerby browser extension is fixed.
* The following issues related to the Partners feature are fixed:
    * The host workspace losing members visibility of shared accounts.
    * Guest users being able to own host accounts and grant owner access.
* The issue with the load times of 4 to 5 seconds for the Cerby web app and browser extension is fixed.

## Security Fixes

* A potential click-jacking configuration issue with the <http://app.cerby.com> site affecting the web server is fixed. Discovery credit: Kunal Mhaske.
* A potential cross-workspace issue is fixed. Member ids are now validated in groups through SCIM to see if users belong to a workspace.
