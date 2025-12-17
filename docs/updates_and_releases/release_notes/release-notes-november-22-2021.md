---
intercom_id: 5758752
---

# Release Notes - November 22, 2021

## New Features

* Applications not managed by Cerby are now displayed with a domain name when listed on the browser extension, the mobile application, and the **All Accounts** view of the web application.
* Accounts with a phone number managed by Cerby are now able to use OTP codes for MFA.
* The user experience is now improved when accessing and refreshing the Shared Inbox in the web application.
* Users can now store backup codes when enabling MFA and remove them when disabling MFA in Pinterest and Twitter. Manual saving of backup codes is also available.
* Owners of Pinterest business accounts can now sync existing members and Ad Accounts when they are onboarded to Cerby.
* Owners of Pinterest accounts can now determine their business ID when they are onboarded to Cerby. With this ID, they are considered business accounts.
* Users are now able to enable and disable MFA for their account when provisioning the phone number.

## Fixes

* Users can no longer duplicate accounts when adding them to the same collection in the web application.
* The Shared Inbox no longer displays the number of result pages if results are less than 20.
* The search bar of the browser extension no longer accepts lengthy texts entered by users.
* Functionalities of the Shared Inbox related to asynchronous tasks (such as FBM sync and message deletion) are no longer affected.
* The **Refresh** button in the Create Email Address pop-up window of the web application is improved.
* The search bar of the browser extension no longer changes its size when clicking it.
* The loading animation of the browser extension no longer displays two sizes of the animation icon.
* The issues with auto login when using the Firefox browser extension are fixed.
* The issues with displaying FBM accounts in the modal when clicking the **View all accounts** button in the dashboard of the web application are fixed.
* The issues with displaying the number of FBM accounts in both the list and grid views of the dashboard in the web application are fixed.
* The issues with editing the text in the search bar after performing a search in the mobile application are fixed.
* Accounts from another workspace are no longer displayed when switching between workspaces. Users must log in every time they change workspace.
* Admins can now disable users provisioned through SCIM when these users have never logged in to Cerby.
* Phone numbers provisioned and managed by Cerby are now displayed correctly with the US country code.
