---
description: 
intercom_id: 7240033
---

# Release Notes - April 6, 2023

## New Features

* The [Password Manager Importer](https://cerby-test.gitbook.io/cerby-test/updates-and-releases/marketing-articles/migrate-your-items-from-your-enterprise-password-manager-to-cerby) is now available in the Cerby web app. This feature enables you to sync and import to Cerby, in one go, the following items you have saved in your password manager:
After the import, you can start managing, protecting, and sharing your items through Cerby.

    * Folders as collections
    * Password as accounts
    * Secure notes and their attachments as secure notes
    * User access permissions for shared folders
* [Secrets](https://cerby-test.gitbook.io/cerby-test/updates-and-releases/marketing-articles/what-are-secrets) are now available in the Cerby web app. This feature enables you to save important information and attachments securely in Cerby, in an encrypted environment, and share them with your colleagues.
* The Cerby mobile app [v1.0.23](https://apps.apple.com/us/app/cerby/id1533747684) for iOS and [v1.0.79](https://play.google.com/store/apps/details?id=com.cerby&hl=en&gl=US) for Android are now available with features such as the following:
    * Improvements to the login process
    * Users can log back in with saved credentials
    * Improvements in the user interface for large screens
* A message is now displayed in the Cerby browser extension about notifications sent to an **Account Owner** when help is needed to log in to an account automatically.
* Users who receive an email about a request to share access to their account via a partnership are now redirected to the **Members** tab within the account details page.

## Fixes

* The following issues were fixed in the latest release of the Cerby mobile app for iOS and Android:
    * Being unable to tap the **Scan code** button using an iOS iPhone 13 Pro Max.
    * A network error screen appearing briefly.
    * Displaying verification codes in two lines in the account details screen (iOS).
    * The content not centered in the onboarding screens.
    * The related tenant screen breaking when displaying multiple tenants.
* The issue with not displaying a date in the **Last Used** column of the table in the **Members** tab of an account details page is fixed.
* The issue with the sender being unable to see if the receiver has accepted an invite to access a tenant, as well as the option to rotate the password, is fixed. This information is displayed in the **Members** tab of the tenant details page.
* The issue with accessing the email settings from the account details page is fixed.
* The issue with events in the **Automation** view not being correctly grouped by date is fixed.
* The issue with entering a long name for a collection in the **Share Collection** wizard is fixed.

## Security Fixes

* Potential email flooding vulnerabilities in the [Pricing](https://www.cerby.com/pricing) and [Contact Us](https://www.cerby.com/about-us/contact-us) pages of the Cerby website are fixed. Report credit: Milan Jain and Love Yadav.
