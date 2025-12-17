---
intercom_id: 6531764
---

# Release Notes - September 5, 2022

## New Features

* The left navigation drawer of the Cerby web app is now improved and can be collapsed and expanded. Also, the **Inbox** and **My Profile** are now displayed at the top of the dashboard.
* Credentials are now validated in the **Add Account** wizard when adding accounts through the password manager importer.
* The **Automation** view of the Cerby web app is now released to help users track all the automation processes of their accounts.
* Intercom is now integrated with the **Get help** button in the **Automation** view.
* Emails are now sent when automation jobs fail, and these messages contain a link to the **Automation** view.
* **Account Collaborators** can now not show an account's password when clicking the **Fill** button of the Cerby inline browser extension.
* Business center assets can now be filtered or always sorted the same way in the Cerby web app.
* Cerby-managed phone numbers are now the only verification method created when turning on multi-factor authentication (MFA) automatically for Pinterest.
* For security purposes, a blank screen is now displayed in the Cerby mobile app when switching apps.
* Cerby-managed email addresses are now available as verification methods for TikTok accounts.
* Swapping email addresses automatically is now only enabled for accounts with MFA configured through Cerby.
* The new **Finance** role is now mapped in Cerby to grant users **Manager** or **Analyst** roles in TikTok For Business accounts.
* Infinite scroll is now supported on the dashboard homepage.
* Users can now ignore assets and users when syncing Facebook Business Manager accounts.
* VK is now supported with automatic login.
* **Account Owners** are now listed in the **Flagged accounts** table of the **Policies** view.
* Discord is now supported with automatic login using a time-based one-time password (TOTP) and SMS as verification methods.
* A notification about the location (Ohio, US, or Jalisco, Mexico) of login attempts is now implemented when users initiate automation workflows from Cerby.
* The username value is now a required input when adding an account for an app not supported by Cerby.
* The username value is now displayed in the account settings.
* The **Onboard MFA** step is now removed from the **Add Account** wizard to ensure users add at least two factors before initiating automation workflows.
* The **All Access Mode** switch is now displayed on the account assets page for a business center account.
* The flow to create a Cerby-managed email is now updated with the process to configure auto-forwarded emails.
* Users can now manually configure the Cerby mobile app as an authenticator for MFA, as well as with an automation workflow, for apps managed by Cerby that support an authenticator app.

## Fixes

* The issue with the preloader of the homepage in the Cerby web app is fixed.
* The issue with not displaying the corresponding policy in the account card when turning on MFA with a Cerby-managed email address for TikTok is fixed.
* The issue with discarding the MFA verification code after closing the dialog box in the Cerby web app is fixed.
* The issue with the **Automation** view taking several seconds to load is fixed.
* The issue with retrieving the verification code from an SMS instead of an email address when turning off MFA automatically for a Snapchat account is fixed.
* The issue with being unable to click the **Update settings** button when editing the recipients for auto-forwarded emails is fixed.
* Users can no longer copy the password of a business center account from the Cerby mobile app.
* Users can no longer turn on and off MFA automatically from the Cerby web app when the phone number and email address are not managed by Cerby.
* The issue with account activity not being displayed in the **Activity** view after adding the accounts through the password manager importer is fixed.
* The issue with creating multiple collections by clicking repeatedly the **Create Collection** button in the **Create a Collection** wizard is fixed.
* The issue with being unable to search for unknown members in the **All members** view is fixed.
* The issue with the CAPTCHA detection when rotating a password automatically for a TikTok account using the Cerby mobile app is fixed.
* The issue with rotating passwords automatically for a TikTok account when prompted to use the phone number as a verification method is fixed.
* The issue with logging in automatically to a Mailchimp account with no visible error elements is fixed.
* The issue with the **We Detected An Unusual Login Attempt** dialog boxes when logging in automatically to a Twitter account is fixed.
* The issue with displaying swap email options for deleted accounts is fixed.
* The issue with the **Add a new app or service** button not working after entering text in the search bar of the **Add Account** wizard is fixed.
* The issue with the confirmation message box when changing the workspace role in the **All Members** view is fixed.
* The issues with the configuration of auto-forwarded emails are fixed.
