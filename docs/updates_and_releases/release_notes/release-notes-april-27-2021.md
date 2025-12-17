---
intercom_id: 5457529
---

# Release Notes - April 27, 2021

## New Features

* The SAML-based [Cerby Azure AD integration](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/aad.cerby?tab=Overview) is now live in the Azure Ad App Gallery.
* Initial release of Facebook Business Manager support. Users can now import Facebook Business Manager assets and share them with corporate users via their personal Facebook profile. Beta release only.
* Initial release of Collections support. Users can now create collections and group accounts into those collections.
* In page updates on MFA onboarding and Password Rotations are now available, enabling users to understand when the backend task has been completed without updating the page.
* Account tiles in the Cerby web dashboard now show the last time a user logged in to an account.
* User experience improvements to make web dashboard styles more consistent from page to page.
* Users can now add additional domains in which they can access credentials for “unmanaged” applications.
* One-click autofill of passwords and MFA codes is now possible for supported sites.

## Fixes

* Deleted accounts are no longer shown in the mobile app account listing view.
* Field detection has been improved to reduce false positives.
* Disabling MFA for an account was not enforcing a separate identity challenge.
* Better session management within a tab to ensure a page reload does not block usage of manual credential insertion.
* Account sharing for Google identity powered workspaces now works even when the user has not shared their name with Cerby.
* In page credential insertion now logs a “Manual Login Attempt” in the Activity report.

## Known Issues

* Android mobile app requires a hard swipe right to exit the QR scan view.
* Analytics for the Android mobile app incorrectly report iOS instead of Android.
