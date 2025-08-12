# Release Notes - October 26, 2021

# New Features

  * The **Validate Credentials** action is now optional when adding an account with the web application.

  * The following steps are now improved when adding accounts with the browser extension:

    * Successful account creation

    * Account creation form

    * Cerby-generated account description

  * The **Contact Creation** section in the account details and the **Shared Inbox** section are now only displayed in Cerby workspaces.

  * The original email and phone number are now stored, so users don't lose them when changing the account settings to an email managed by Cerby.

  * Authorized users are now allowed to disable other users from the **All Members** page in SAML workspaces.

  * Users are now able to see the time in the **Received at** field and sort emails descendingly when using the **Shared Inbox** in the web application.

  * The email address and phone number managed by Cerby are now displayed in the **Details** section of the **Account Settings** page in the web application.

  * Users can now onboard a Twitter account when entering a password with a weak security level in the **Add Account** page of the web application.

  * Cerby-managed emails and phone numbers are now assigned and updated in the **Account Settings** page of the web application after being created.

  * Users without permission to read the details of other accounts on the **All members** page now receive the correct error message.

  * Google-connected profiles are now displayed in the profile settings of the web application.

  * The browser extension flow for YouTube is now available.

  * Workspace owners and admins are now the only users who can see the **View SCIM Authentication Token** feature in the **Directory Sync** section of the **IDP Settings** tab in the web application. Also, only they can see the **Show Token** pop-up window after a mobile identity challenge.

  * Users can now use the **Forward Message** feature from the **Shared Inbox** page in the web application.

  * Users can now filter emails based on the date selected in the **Date range** drop-down list of the **Shared Inbox** in the web application.

  * Workspace owners are now able to send emails to the personal email address of users when synchronizing users from Facebook. This email contains a link to log in to Cerby.

  * Users can now search for other users by entering their name or email in the search box of the **All members** page in the web application.

  * Users can now use the **Virtual Inbox** page to manage all of the emails received from different accounts.

  * The Cerby Assets Manager application is now updated to version 11.0 or higher of the Facebook Marketing API.

  * Users are now able to see the associated emails related to the accounts they have permissions in the **Shared Inbox** page; those accounts are provisioned with a Cerby-managed email.

  * The Cerby Menu is now automatically opened if a user has only one account in a domain or if it is a multi-step form in the browser extension.

  * Admin users are now prompted to synchronize Cerby with the latest information when they try to modify permissions to nonexistent users in Facebook Business Manager (FBM).

  * Users now receive a notification email when they are linked from an FBM synchronization process to access their FBM assets with Cerby.

  * The browser extension now detects if logos of other password managers are displayed in the logging-in fields. If other password managers are present, the Cerby extension drawer is displayed outside the logging-in fields; if not present, the Cerby logo is displayed inside the logging-in fields.

  * Users with FBM admin permissions are now able to share Facebook Ad accounts to themselves, and this account propagates to Facebook.

  * The instructions on how to add Cerby's Asset Manager App in FBM are now improved with information to identify Cerby as software support for businesses.

  * The auto-logging feature is now available for mentimeter.com.

  * Users without admin permissions are now unable to see or access the **Policies** page in the web application.

  * Users that have not joined but have been invited to Cerby are now displayed with a **Pending** status in the **Account Members** list of the **All members** page in the web application.

  * Users are now able to use a shortcut from the dashboard menu card to the members view of the accounts in the web application.

  * Users can now go directly to the **Activity** page, with preloaded analytics for an account, when selecting the **View Account Activity** option from the menu card of the dashboard in the web application.

  * The accounts in the **All members** page removed by users and owners of a Google Ads or Manager account are now also removed correctly on Google Account.

  * Users and owners of a Google Ads or Manager account are now able to modify the account permissions of their team members in **Account Settings** with the web application.

  * Users owners of a YouTube account are now able to modify the account permissions of their team members in **Account Settings** with the web application.

  * Users are now able to share access to a Google Ad or Manager account and initiate the right invitation flow if the user in question does not have access to the account.

  * Synchronization with existing Facebook users is now always performed before users can share an FBM account and assets.

  * A user interface for retrieving the SCIM authorization token is now available in the web application.

  * Users without admin permissions are now able to see only their own activity and the accounts for which they are owners in the web application. Admin users can see all of the activities and accounts across the workspace.

  * The logging-in process is now improved, so the browser extension pre-fills the information of the last used account when prompted with a MFA field.

  * Cerby account owners are now able to revoke access to FBM assets in the web application for the following scenarios: 

    * When users are removed from collections

    * When assets are removed from collections

    * When collections are deleted

# Fixes

  * The **Cancel** and **Save** buttons are now at the top of the **Policies** page in the web application and don't overlap with other buttons.

  * The **Save Code** pop-up window is now correctly displayed when entering a code or security key to enable MFA with the web application.

  * The email and phone number inputs are now disabled in the **Edit Account Details** page of the web application for the cases where Cerby manages the email and phone number.

  * The **Group by** feature that filters accounts by app or service now displays the total number of accounts in the **All accounts page** of the web application.

  * The Cerby workspace now displays search results as the user enters information in the search box of the web application.

  * The Twitter logging-in flow is now unblocked when users are prompted to enter their email.

  * Users can now add a Twitter account without validating credentials using a non-Cerby workspace in the web application.

  * The **Show Password** button is now displayed in the **Account Settings** of an application account on the Cerby workspace after a push notification.

  * Users can now enter emojis in the search box of the **All Accounts** page without causing an error in the web application.

  * Users without permission to read the details of other accounts on the **All members** page now see the correct error message.

  * Usernames on the **All members** page are now reformatted for Pinterest accounts in the web application.

  * The email and username are now used as pivots when Azure provisioned is detected as an upstream identity provider.

  * The new Twitter logging-in flow is now supported in the Cerby extension. Users are able to log in automatically.

  * Workspace owners and admins are now the only users that can see the **IDP Settings** tab in the web application.

  * The **Cancel** and **Save** buttons are now displayed on the upper right side of the **Edit My Profile** page in the web application.

  * Admin users are now able to revoke FBM admin access.

  * The view in list mode now takes up the whole screen in the web application.

  * Users are now able to scan the QR code using an iOS mobile device when configuring MFA for a Mailchimp account.

  * The **Account Members** list in the **All members** page now displays the correct page when navigating across the result pages in the web application.

  * The last access information displayed both in the dashboard cards and the **Activity** page is now synchronized.

  * Users are now redirected to the correct FBM page when they don't have assets (for example, other accounts shared with them).

  * The percentages of protected and flagged accounts for security actions such as MFA and password rotation are now calculated considering all accounts (managed and unmanaged).

  * Users can now remove other users from FBM assets in shared Facebook collections. 

  * The user experience of the search bar in the browser extension is now improved.

  * The Cerby menu is now only displayed by the browser extension when necessary after landing on a page.

  * The mobile application does not display an error screen after receiving and accepting notifications when the session has expired.

  * Users now click only once on the **Login** button to access the next screen in the mobile application.

  * The Cerby logo and extension are now displayed on the MFA input fields when logging in to Instagram.

  * Users are now unable to create collections using special characters such as emojis in the web application.

  * The user interface has now the following improvements in the **Sync Data** wizard of the web application:

    * Fixed height and scrollable containers in the **Sync Data** wizard window.

    * Cerby user or email input always visible.

    * Disabled users on the list when they are not selected.

