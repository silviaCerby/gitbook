# Use the Scout checklist for best results

**Description:** This article includes quick tips and a must-do checklist for obtaining the best results in your scouted workflows.

The workflows or tasks you can scout are the following:

  * Log in to your account

  * Update your account's password

  * Reset your account’s password

  * Turn on MFA

  * Turn off MFA

  * Check for updates

  * Invite a user

  * Update a user’s role

  * Remove a user

{% hint style="danger" %} **IMPORTANT:** You must use a Chrome-based browser
to install and use Scout. Refer to the following articles for more
information: * [Explore
Scout](https://help.cerby.com/en/articles/9774431-explore-scout) * [Install
Scout](https://help.cerby.com/en/articles/10046805-install-scout) * [Scout a
workflow](https://help.cerby.com/en/articles/10046916-scout-a-workflow) {%
endhint %}

* * *

# **Log in to your account**

**Quick tips**

  * Start scouting on the app’s login page

  * Scout the SSO login flow, if using it 

  * Capture a clean credential entry (user + password + code)

  * Show successful and failed login states

  * Switch user session on Chrome for edge cases

  * End with a fresh logout to reset the state

**Must‑do checklist**

  * Scout the correct login flow

  * Include the IdP login or starting point, if using SSO

  * Scout an incorrect login flow with bad credentials

  * Scout all error messages

  * Scout MFA or CAPTCHA prompts

  * Include all error messages displayed

  * Scout a login from a secondary Chrome session

  * Scout a logout flow

* * *

# **Update your account's password**

**Quick tips**

  * Start scouting on the first post‑login page

  * Show the navigation to the account security settings

  * Capture success and error messages

  * Keep the old password field visible

  * End with the confirmation message

**Must‑do checklist**

  * Scout the correct password update

  * Scout failed attempts with the wrong and old password

  * Capture success and error messages, toasts, and other elements

  * Show the login flow with the updated password

* * *

# **Reset your account’s password**

**IMPORTANT:** This workflow has significant limitations and is not generally
recommended. For exceptional cases, consult with the Cerby support team at
[support@cerby.com](mailto:support@cerby.com).  
---  
  
**Quick tips**

  * Start scouting on the app’s login page

  * Use the "Forgot password" option

  * Type your recovery method (email or phone) 

  * Send the recovery message

  * Capture success and error messages

  * End with the confirmation message

**Must‑do checklist**

  * Capture the steps to find the "Forgot password" option

  * Scout the process after clicking the recovery message link

  * Email the `.eml` file from the email at [support@cerby.com](mailto:support@cerby.com), if received

  * Reset the password

  * Log in again to the app

* * *

# **Turn on MFA**

**Quick tips**

  * Start scouting on the first post‑login page

  * Show the navigation to the MFA settings

  * Scout the email received to turn on MFA, if received

  * Scout the token or secret key setup

  * Scout the backup codes if offered

**Must‑do checklist**

  * Scout the correct setup with an authenticator app

  * Show the setup via a secret key, selecting “can’t scan QR code.” 

  * Email the `.eml `file or SMS received at [support@cerby.com](mailto:support@cerby.com), if received

  * Capture the success message

  * Show backup codes, if any, and how to save them

* * *

# **Turn off MFA**

**Quick tips**

  * Start scouting on the first post‑login page

  * Show the navigation to the MFA settings

  * Scout the process to turn off MFA

  * End with showing the confirmation message

**Must‑do checklist**

  * Scout the identity verification process if the app requires it

  * Email the .eml file from the email or SMS received at [support@cerby.com](mailto:support@cerby.com), if received

  * Capture the success message

  * Log in to the app without MFA

* * *

# **Check for updates**

**Quick tips**

  * Start scouting on the first post‑login page

  * Show the selection of your workspace in the app when available

  * Show the navigation to the users' table

  * Scroll through roles, assets, and user states

  * Search for active, invited, and nonexistent users

  * Show pagination to the last page

  * End with opening and showing at least one drawer with both user and asset details

**Must‑do checklist**

  * Scout all role and asset drop-down menus

  * Scout all available roles for the app

  * Navigate through the different user tables when available

  * Show details of active and inactive users

  * Show all user search states, such as no results and partial matches

  * Navigate through a couple of result pages to the last page

* * *

# **Invite a user**

**Quick tips**

  * Start scouting on the first post‑login page

  * Show the navigation to the users' table

  * Use a testing user’s email for invites

  * Scout all role and asset drop-down menus in the invite dialog box

  * Resend an invite to all pending users

  * Scout the reactivation of users when available

  * End with accepting the invite as the end user

**Must‑do checklist**

  * Scout initial invite with role and asset drop-down menus

  * Attempt to invite a user with missing required fields (show error message)

  * Invite an existing user

  * Invite a pending user who has not accepted the invitation yet

  * Scout the flow of resending a user invite

  * Show the flow of resending a user invite

  * Accept the user invite and show the success message

  * Navigate through a couple of result pages if the user's table is long

* * *

# **Update a user’s role**

**Quick tips**

  * Start scouting on the first post‑login page

  * Show the navigation to the user's table

  * Open the user details page

  * Scout all role drop-down menus and custom role paths

  * Show multi‑role selections and any restrictions

  * Scout the assignment of roles for onboarded and pending users

  * End with a success message with the new role visible

**Must‑do checklist**

  * Scout all role selector interactions

  * Scout the flow of creating a custom role, if available

  * Save and confirm the new role

  * Capture the success message

* * *

# **Remove a user**

**Quick tips**

  * Start scouting on the first post‑login page

  * Show the navigation to the users' table

  * Show the deactivation of users when available

  * Remove both active and pending users

  * Capture confirmation and success messages

  * End with showing the removed state

**Must‑do checklist**

  * Scout the removal of an active user

  * Scout the removal of a user with a pending invite

  * Capture the confirmation dialog box

  * Show the success message in the table

  * Scout asset‑specific removal when available

  * Scout the flow of removing access to an asset, if available

  * Scout a search for a nonexistent user (shows “No results” message)

