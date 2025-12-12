---
description: 
---

# Release Notes - March 30, 2021

# New Features

  * [Okta/SAML Integration](https://www.okta.com/integrations/cerby/) published.
  * [Edge Browser Extension](https://microsoftedge.microsoft.com/addons/detail/cerbys-browser-extension/bbaiiaogfdgpbapebajffliefkfipoif?hl=en-US) published.
  * The session refresh is now supported for Web app and Browser extensions provided you have configured Cerby as a custom Okta app, an Okta/SAML app, or is Google Identity powered.
  * Account validation is now available at the time of account creation.

# Fixes

  * The issue where a second Unmanaged application could not be created with the same username as from another Unmanaged application.
  * It is now possible to close the password injection menu by clicking off the menu or pressing ESC.
  * The state is now maintained when copying values from the browser extension in the browser navigation menu.
  * It is now possible to refresh the Activity and All Members pages without an S3 error.
  * The account name was cut off in the browser extension.
  * It is now possible to add an Unmanaged app URL with more than 50 characters.

# Known Issues

  * MFA identity challenge is currently not issued when attempting to edit the IDP settings for a workspace.
  * OTP secret is oddly displayed for deleted accounts, showing the full OTP URL instead of just the text secret.
  * OS and Device dimensions are not shown for mobile logins in the Activity Report.
  * Location is not shown in browser-based logins in the Activity Report.
