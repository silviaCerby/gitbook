---
description: 
intercom_id: 7828315
---

# Release Notes - April 25, 2023

## New Features

* Our platform keeps getting even more user-friendly. The Cerby browser extension v1.0.172 ([Firefox](https://addons.mozilla.org/en-US/firefox/addon/cerby-s-browser-extension/), [Google Chrome](https://chrome.google.com/webstore/detail/cerbys-browser-extension/clccplmaaeihbagbefjinmclielobnkb), [Microsoft Edge](https://microsoftedge.microsoft.com/addons/detail/cerbys-browser-extension/bbaiiaogfdgpbapebajffliefkfipoif), and [Safari](https://apps.apple.com/mx/app/cerby-web-extension/id1581820030?l=en&mt=12)) is now available with the feature to [save your credentials at login](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-browser-extension/autosave-an-account-at-login-or-signup-with-the-cerby-browser-extension).
You now have an easy and secure way to add accounts to Cerby when accessing an application manually through a login page using a web browser. Stay tuned because this is just the beginning.

* Talking about improvements. After reading these release notes, you’ll surely want to update your Cerby mobile app. The versions v1.0.79 for Android and v1.0.23 for iOS are now available with the following features:
    * A brand new account details screen where you can see the following:
      * Your login credentials
      * The verification codes when multi-factor authentication (MFA) is configured and managed by Cerby
      * The QR code scanner to configure MFA managed by Cerby
      * The members and teams with access to the account
      * The option to share an account with other workspace members and teams
    * Secrets are here! You can now view the secret details screen with the following information:
With Secrets supported, you can also:

      * The name and body of the secret
      * The file attachments
      * The members with access to the secret
      * The last modified and added dates
      * Download and view attachments.
      * Share a secret with other workspace members and teams.
* We have good news for IT admins! They can now automatically invite new users to join a [tenant](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-business-hubs) or remove them by performing provisioning and deprovisioning events in their identity provider (IdP). These events propagate from group assignments in the IdP to teams in Cerby.
* We've been busy flexing our security muscles and have implemented the Proof Key for Code Exchange (PKCE) protocol in the Cerby browser extension and mobile app. The goal is to protect all of our users against authorization code interception attacks. This protocol is available in the following versions:
So, next time you use the Cerby browser extension or mobile app, know that an additional security layer is in place for the authorization process. This way, we ensure that login credentials are securely managed and protected from potential threats without affecting your user experience.

    * Cerby browser extension v1.0.167 and subsequent versions
    * Cerby mobile app v1.0.79 for Android and v1.0.23 for iOS, and subsequent versions

## Security Fixes

* A potential hijacking vulnerability in the Cerby mobile app for Android is fixed.
