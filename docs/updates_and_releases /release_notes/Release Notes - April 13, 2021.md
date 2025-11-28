# Release Notes - April 13, 2021

# New Features

  * Restyled browser extensions for Chrome, Edge, and Firefox.

  * The Cerby menu option is now available in the browser context menu to activate credential insertion in any undetected field.

  * Health check to determine whether MFA is still available for certain social media applications.

  * Update Twitter login logic to prioritize logging in with the username instead of the account’s email address.

# Fixes

  * Pen test fixes are needed to ensure that MFA device and account deletion actions are always authenticated.

  * Activity report performance improvements to load large data sets beyond 7+ days. 

  * Browser detection to direct users to the appropriate browser plugin store.

  * Password autofill on Android is now working for Instagram.

  * Firefox extension fixes for credential one-click autofill and autofill of MFA authentication code for Instagram. 

  * Fix for showing the OTP secret correctly for deleted accounts within the Cerby dashboard to enable easier offboarding of an account.

# Known Issues

  * MFA fields are not detected for one-click autofill in browsers. 

  * Logins initiated by in-browser credential insertion are not shown currently in the Activity report.

