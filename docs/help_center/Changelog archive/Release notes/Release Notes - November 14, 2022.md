# Release Notes - November 14, 2022

# New Features

  * [Creating a team manually](https://help.cerby.com/en/articles/6624225-how-to-use-teams#h_ed56caecdc) in Cerby with the members of your corporate directory is now supported.

  * Pinterest and Instagram are now supported with the automation to verify multi-factor authentication (MFA). Cerby checks if MFA is still active and has the correct secret key.

  * Reddit is now supported by automation to turn on MFA.

  * Apple is now supported with automatic login.

  * The automation to log in to Instagram is now updated to match the new user interface when switching accounts 

  * The automation for logging in to Linktree is now updated to match the new user interface and includes a verification code challenge via phone number. 

  * The automation to log in to Google now supports the time-based one-time password (TOTP) configuration.

  * Social media accounts are now reconnected to Sprinklr via an automation workflow after a password rotation.

  * To prevent login errors, the wait time before entering a one-time password when logging in automatically to a Twitter account has been increased.

  * The step where the user is requested to add a phone number to their TikTok account when logging in automatically is now skipped.

  * The speed when logging in automatically is now improved to handle the issue with Google forcing users to enter credentials even if another account is active.

  * The scenario where Cerby-managed email addresses or phone numbers are configured as MFA verification methods is now handled when turning on MFA automatically. Cerby looks for sent verification codes and turns on MFA based on a TOTP configuration.

  * A random wait time before entering TOTP is now implemented when logging in automatically to Twitter, Instagram, and non-supported apps with MFA enabled.

  * The TOTP device is now always saved, even when the automation workflow to turn on MFA fails.

  * User input in the search bar of the **Unknown users** tab now uses cache data to improve performance.

  * Server calls are now reused to reduce loading times in the Cerby web app dashboard.

  * The **Swap email** button in the account details page is no longer displayed for Instagram, Twitter, or TikTok accounts because Cerby-managed email addresses and phone numbers creation is a manual process.

  * The original sender's email address is now included in the header values for forwarded emails. With this feature, users can automatically reply to the original sender.

# Fixes

  * The issue with the account inbox only displaying emails and no SMS messages is fixed.

  * The issue with users being able to add themselves to a team when creating one or adding members is fixed.

  * The unusual login selector in Spanish and English is now handled when logging in automatically to Twitter.

  * The issue with the page breaking when switching between **Managed by Cerby** and **Unknown users** is fixed.

  * The issue with displaying the incorrect time in the account settings and **Shared Inbox** is fixed.

  * The issue with the scroll bar displayed over the checkboxes in the **Share Account** wizard via partnership is fixed.

  * The issue with searching for nonexistent collections in the **Collections** view and displaying a prompt to create a collection is fixed.

  * The issue with the timeout when syncing a Facebook Business Manager account with more than one thousand assets is fixed.

  * The issue with detecting the login state for Jotform when logging in automatically instead of throwing an error is fixed.

  * The issue with the Cerby mobile app for iOS not displaying app-specific account details when autofilling credentials after an expired session is fixed.

  * The issue of not keeping the user in the Profile screen after logging in automatically to TikTok has been fixed.

  * The issue with the checkboxes missing to select unknown users to remove from Facebook Business Manager and TikTok For Business accounts is fixed.

  * The issue with searching for nonexistent collections in the **Collections** view and displaying a prompt to create a collection is fixed.

