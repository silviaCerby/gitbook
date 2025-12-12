---
description: 
---

# Release Notes - October 17, 2022

# New Features

  * The [Teams](https://help.cerby.com/en/articles/6624219-what-are-teams) feature is now available to help our customers share accounts quickly and securely with groups of users. Currently, users can create teams from their Okta groups, but for the subsequent releases, Azure AD groups will be supported, as well as teams built from scratch with any member of the corporate directory in Cerby.
  * The [Partners](https://help.cerby.com/en/articles/6634285-what-are-partners) feature is now available to help our customers share access to their accounts securely with external parties without handing over the username and password.
  * Quora is now supported with the automatic login workflow.
  * Users with **All-Access Mode** can now see all the accounts within a workspace when using the Cerby mobile app.
  * The **General** tab, when displaying the details of an account, is now renamed **Settings**.
  * Social media accounts are now reconnected to Sprinklr and Emplifi after performing a password rotation in Cerby.
  * The "Not started" status is now implemented in the **Automation Center** for the MFA enrollment and password rotation automation workflows that didn't start because the user must perform one of the following actions:
    * Review and validate the account credentials
    * Create and configure a Cerby-managed email address
    * Configure MFA with a verification method managed by Cerby
  * The **Members** tab and the **All Members** view now display account members alphabetically by default for all accounts.
  * Searching for collections is now supported in the Cerby mobile app.
  * The column titles in the table with account details when filtering accounts as a list in the **All accounts** view are now updated to match the fields used to create an account in Cerby.
  * Background syncs for business center accounts now run automatically every 24 hours for subscribed workspaces.
  * The **My Profile** page now displays all the business center profiles connected to Cerby.
  * Unknown users are now displayed in the **All members** report export.
  * An access-blocked screen is now displayed on rooted and jailbroken mobile phones for security purposes.
  * The Cerby mobile app for Android now refreshes every 10 seconds to reflect adding or removing an account on the Cerby web app.

# Fixes

  * The issue with logging in automatically to a LinkTree account through the Cerby web app when waiting for a CAPTCHA to be solved is fixed.
  * The issue with being unable to connect the Facebook profile when sharing access to a Meta Business Manager account is fixed.
  * The issue with identifying the verification method (SMS or email address) to retrieve the verification code when logging in automatically to a TikTok account through the Cerby web app is fixed.
  * The issue with reloading the account settings in the Cerby web app and breaking the page is fixed.
  * The issue with not loading the corresponding LinkedIn Ad page when accessing from the account asset card in the Cerby web app is fixed.
  * The issue with long delays when inserting a time-based one-time password (TOTP) to log in to a Twitter account is fixed.
  * The issue with pagination for distribution lists beyond the third results page is fixed.
  * The issue with users being able to modify distribution lists is fixed.
  * The issue with losing the session after accepting an identity challenge in the Cerby mobile app is fixed.
  * The issue with being unable to access a business center asset from the account assets view is fixed.
  * The issue with users invited via Cerby to a business center account and displayed with the **To remove** status when generating a sync report is fixed.
  * The issue with the TOTP seed for a Discord account not being accepted when saving the code in the Cerby web app is fixed.
  * The issue with displaying business center assets in the **Workspace Policies** view for accounts with username, password, and MFA managed by Cerby is fixed.
  * The issue with hiding the MFA configuration when adding a phone number managed by Cerby to a Discord account with MFA turned on is fixed.
