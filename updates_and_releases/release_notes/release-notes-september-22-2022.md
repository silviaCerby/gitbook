---
intercom_id: 6582873
---

# Release Notes - September 22, 2022

## New Features

* Single sign-on through JumpCloud is now supported using a custom SAML application integration.
* The following apps are now supported to log in automatically from Cerby:
  * Teamworks
  * Salesforce
  * Dialpad
  * Udemy
* The **Automation** dashboard is now released.
* The account card is now removed when users confirm their identity on the Cerby mobile app (Android and iOS) when turning on **All-Access Mode**.
* A filter is now implemented to display only the distribution lists of the workspace when configuring auto forwarded emails.
* The onboarding dialog box for LinkedIn Ads is now available.
* Users can now disable manually the time-based one-time password (TOTP) of an account in the Cerby web app.
* All users are now unable to see the password of an account when an automation workflow is running through the Cerby browser extension, even if they click the **Show** button.

## Fixes

* The issue with the **Suspicious Login** page, which requests a verification code when performing an automatic login to a Snapchat account, has been fixed.
* The issue with entering long workspace names when logging in through the Cerby mobile app (Android and iOS) is fixed.
* The issue with the keyboard not hiding after leaving focus from the account search bar in the Cerby mobile app (iOS) is fixed.
* The issue with the Cerby mobile app (iOS) not opening to autofill credentials for the First Republic Bank mobile app is fixed.
* The issue with entering the verification code when turning on multi-factor authentication (MFA) automatically for a Twitter account is fixed.
* The issue with being able to auto-forward emails to any email address, and not only the ones associated with a workspace, is fixed.
* The issue with being able to insert any address instead of a distribution list when configuring auto-forwarded emails is fixed.
* The issue of not identifying if users are already logged in when they try to log in automatically to a Loom account has been fixed.
* The issue with being unable to remove unknown members for Snapchat Business and TikTok For Business is fixed.
* The issue with the Cerby mobile app not keeping the last state before going to the background and being reopened is fixed.
* The issue with logging in automatically to a Mailchimp account when prompted to enter an email verification code is fixed.

## Security Fixes

* A potential click-jacking configuration issue and iFrame vulnerability with the <https://app.cerby.com> site is fixed. Discovery credit: Shehbaz Khan.
