---
description: 
intercom_id: 6463843
---

# Release Notes - August 11, 2022

## New Features

* The following apps are now supported to log in automatically from Cerby:
  * Adobe
  * Airtable
  * Atlassian
  * Buffer
  * Dropbox
  * Emplifi
  * Eventbrite
  * Expedia
  * Flickr
  * GitHub
  * Grammarly
  * JWPlayer
  * LinkedIn
  * NewzDash
  * Otoy
  * Paypal
  * Sprinklr
  * Sprout Social
  * Strava
  * The Athletic
  * The Boston Globe
  * The Dallas Morning News
  * The Washington Post
  * TikTok Ads
  * TikTok For Business
  * Twitch
* Instagram, TikTok, and Snapchat are now supported to change the email address automatically for an email managed by Cerby.
* TikTok is now supported to turn off MFA automatically from the Cerby web and mobile apps.
* Users can now edit the access token for a Facebook Business Manager (FBM) account.
* The **Account Username** column is now displayed in the All members CSV report.
* An error message is now displayed when users enter an invalid token while onboarding or replacing tokens for an FBM account.
* Users can now invite and manage FBM members from Cerby, except the following cases:
  * When Page members have a pending review from Facebook.
  * When trying to remove members from Pixels.
* The Cerby web app now displays the recommended verification method for each app to turn on MFA automatically.
* The automation tasks related to MFA now verify if MFA is managed by Cerby for Twitter and Instagram accounts.
* FBM admins can now remove unmanaged members from Cerby.
* The **Add account** wizard for Snapchat Business accounts is now updated.
* Unknown users can now be deleted from the business center view in Cerby, and this removal is propagated to the business center.
* ​​The task to log in automatically to a Twitter account now prevents users from clicking anything and interrupting the process.
* A migration summary banner is now available after a password manager migration.
* ​​The sorting feature of the **Search account** bar in the Cerby browser extension is now available.
* The **Sort by** drop-down list in the **All Accounts** view of the web app is now available.
* The**Email Settings** dialog box is now available from the account details page to change recipients or remove the email address registered in Cerby.
* The **Inbox** tab is now available on the account settings page for accounts with a Cerby-managed email address.
* Filters in the **Shared Inbox** are now enabled by default if messages exist; if no messages exist, filters are disabled.
* A new confirmation dialog box is now available after creating a distribution list to receive the messages sent to the Cerby-managed email address.
* The in-field Cerby browser extension now only triggers auto-login if it detects the login form of a supported app.

## Fixes

* The issue with the task to rotate passwords automatically that is not detecting a Cerby-managed phone number in TikTok is fixed.
* The issue with the task to log in automatically to a Giphy account after configuring a Cerby-managed email address is fixed.
* The issue with the task to log in automatically and log out of a LinkTree account is fixed.
* The issue with the task to log in automatically to a Twitter account because of a new login screen is fixed.
* The issue with the loading screen when syncing data for a Pinterest Business account with incorrect credentials is fixed.
* The issue with being unable to remove FBM accounts with a large number of assets is fixed.
* The issues with the following error messages for Twitter are fixed:
  * When turning on MFA automatically and the task is unable to resolve a challenge because the account doesn't have a Cerby-managed email address.
  * When MFA is already turned on.
* The issue with users being able to click two times the **Invite user to Cerby** button is fixed.
* The issue with the FBM card getting stuck on the main page of the **Add account** wizard after selecting an FBM account and going back is fixed.
* The issues with TikTok requesting an email code rather than an SMS code when rotating passwords and turning on MFA automatically are fixed.
* The issue with not being redirected to FBM when clicking the corresponding account card is fixed.
* The issue with the empty state of the **Sync Data** report is fixed.
* The issue with displaying policy alerts in business center asset cards is fixed.
* The issue with the permission switches in the **Share Access** dialog box is fixed.
* The issue with handling the CAPTCHA when logging in automatically to a TikTok account is fixed.
* The issue with the task to log in automatically to a TikTok account when the login page is in Spanish is fixed.
* The issue with the task to turn off MFA automatically for a Twitter account is fixed.
* The issue with the new device screen when logging in automatically to a Similarweb account is fixed.
* The issue with not displaying the email of a recently added Hootsuite account in the corresponding account card is fixed.
* The issue with registering a Password retrieved event instead of Login attempt in the **Activity** view is fixed.
* The issue with empty text-only messages forwarded from a Cerby-managed email address is fixed.
* The issue with the misaligned **Date Range** drop-down list in the **Activity** view is fixed.
* The issue with the “All account collaborators” option enabled when no members exist for a group of recipients of forwarded emails is fixed.
* The issue with the missing empty state of the **Inbox** tab in the account details page is fixed.
* The issue with the Cerby browser extension auto-filling input fields in the account details page and **Add Account** wizard is fixed.
* The issue with the **Cancel** button when removing an email address from the **Email Settings** dialog box is fixed.
* The issue with running an automation task on a new tab in Safari is fixed.
* The issue with the task to log in automatically to a Domo account is fixed.
* The issue with the Cerby browser extension on Firefox not activating the in-field autofill is fixed.
