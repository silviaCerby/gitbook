# Release Notes - November 9, 2021

# New Features

  * Users are now able to delete emails from the Shared Inbox in the web application.

  * The phone number is now a required value to create a VK and OK.ru account.

  * The web application now supports MFA backup codes for Twitter and Pinterest. Users can store MFA custom backup codes.

  * You can now use the **Reload** button to retrieve the latest messages in the Shared Inbox.

# Fixes

  * Pop-up windows no longer close when using the browser navigation buttons in the web application.

  * The **Accounts** tab no longer displays a date in the **Last Used** column when accounts have never been accessed in the web application.

  * Users can no longer edit the Cerby-managed email and phone number in the **Edit Account Details** section of the **General** tab in the web application.

  * The password rotation process is no longer interrupted when users click the **Edit Account Details** button to enter information while the process is still running in the background.

  * The mobile application no longer enables users to copy MFA OTP codes when codes have not arrived. 

  * Confirmation requests in the mobile application no longer display empty messages.

  * The mobile application no longer displays an incomplete email address when clicking the user avatar. 

  * The search placeholder of the mobile application is improved.

  * The issues with forwarding and deleting emails in the Shared Inbox are fixed.

  * Users are no longer unable to forward or delete emails in the Shared Inbox.

  * Users are no longer duplicated when using SCIM and JIT configurations with Okta and Azure AD.

  * The issue with TikTok messages not arriving in the Shared Inbox is fixed.

# Known Issues

  * Users who don’t finish the initial configuration of a workspace cannot resume the process if they exit the page or the token expires.

  * The web application does not correctly display the left side navigation menu of the dashboard because of the detected screen resolution using Firefox.

  * The mobile application does not correctly work when users lose Internet connection while performing an action.

