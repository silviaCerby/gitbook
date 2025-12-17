---
intercom_id: 5457523
---

# Release Notes - May 25, 2021

## New Features

* [Okta integration](https://www.google.com/url?q=https://www.okta.com/integrations/cerby/&sa=D&source=editors&ust=1621978900746000&usg=AOvVaw1Zky2I0sq4G8r5lhuwQVn1) now supports provisioning and deprovisioning via SCIM.
* Initial Facebook app integration has been approved by Facebook (App ID: 2965389650414399).
* Data Export UI is now available for Activity Report.
* Facebook support - it is now possible to share Facebook ad assets and page assets to other users within your Cerby workspace.
* Collections support - it is now possible to add accounts to existing Collections.
* Collections support - it is now possible to bulk share all accounts belonging to a Collection.
* For non-IDP-backed Cerby accounts, MFA support is now available.

## Fixes

* Now able to fully log out of SAML-based Okta workspaces.
* Click space for Collections is expanded so clicking on the Collections header fully expands the Collection.
* The Ad Account name is now pulled correctly from Facebook.
* Browser Extension: When no matches are found for a login form based on domain, the search bar will not appear until the user clicks on **View All Accounts**.
* iOS Password Manager extension now observes longer sessions and does not error out after three hours.

## Known Issues

* Facebook App must be owned and/or a child of the main Facebook Business Manager account in order to be able to invite other Facebook Business Manager users.
* Facebook account linking button overflows display container in certain browsers.
* The last password rotation is not being shown in the **Account Settings** view.
* QR code scanning does not work for longer OTP seeds (30+ characters).
* The logged-in state is not immediately detected in the iOS and Android Cerby mobile apps.
