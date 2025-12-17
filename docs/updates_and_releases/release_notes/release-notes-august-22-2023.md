---
intercom_id: 8284690
---

# Release Notes - August 22, 2023

## New Features

* We heard you, IT and System admins. We now have a way to deploy the Cerby browser extension to your corporate computers using an MDM service and a configuration file.

With this solution, you can install the extension on MacOS and Windows for the following web browsers:

* Safari
* Microsoft Edge
* Mozilla Firefox
* Google Chrome

For more information, contact our Customer Support team by sending an email to [support@cerby.com](mailto:support@cerby.com) or a message through the help chat of the Cerby dashboard.

* Prepare the holding back tears emoji. We’ve tuned up the Tenants feature with the following releases:
  * Application assets such as ad accounts, pixels, and pages are now supported, and you can manage access to them through Cerby:
    * Assign assets to a user
    * Edit the user’s native role on assets
    * Remove the assets assigned to users

Just click the **Manage assets** button of the corresponding user in the **Members** tab of the tenant details page, and a dialog box will help you assign assets, as shown in **Figure 1**.

<img src="../../../.gitbook/assets/1_lQ9oIyzWW7rrzT2VcRLOYX6TwP9D8SGBheTKsOELSB5FIR4PZHStww9MLya5gAPhl_l6Qt4NYERbaRHLLQVwneD10KrWj0innSS42zsKadVzcMxPcZUqsDE9rPszO1WeYQ6rYedgGGQ4w5lzq2lNo.png" alt="Screenshot of the Assign assets dialog box in front of the tenant details page, where you can assign tenant assets to a user and edit the user’s native role on assets.">

**Figure 1.** **Assign assets** dialog box

* When logging in automatically, tenant service accounts now redirect users to the corresponding collaboration space.
* Great news for all the workspaces using Google as their identity provider and the GSuite directory. **Account Owners** and **Secret Owners** can now share items with users who have not yet logged in to the workspace. Cerby will send them an invite through email to ask them to log in.
* Have you ever looked for end-user documentation about Cerby? We made it easier to access our Help Center from the dashboard. Just click **Help and products** from the left navigation drawer, and a drop-down list will be displayed. Select the **Help Center** option, and we will open the Cerby Help Center on a new tab. Happy reading!

## Fixes

### Cerby web app

* The issue with viewing the password of an account twice and being shown the **Add MFA Backup Codes** dialog box in the second view attempt is fixed.
* The issue with the **Download CSV** button in the **Activity** view not performing the intended action is fixed.

### Cerby browser extension

* The issue with the Cerby browser extension falling into a loading loop when scrolling down and getting to the bottom of a list of accounts is fixed in v1.0.196.
* The issue with the automated task to log in to an account from the Cerby browser extension not being interrupted when the user closes the web browser tab is fixed in v1.0.197.
* The issue with the in-context alerts not being dismissed when clicking the **Close** icon is fixed in v1.0.197.

### Cerby mobile app

* The issue with the Cerby mobile app crashing at launch when users have poor network connectivity is fixed in Android v1.0.97.
* The issue with the Cerby mobile app not copying the time-based one-time password (TOTP) to the clipboard during login for Twitter is fixed in iOS v1.0.64 and Android v1.0.98.
* The issue with the Cerby mobile app for iOS crashing when fast-scrolling through the Password Autofill list of accounts is fixed in v1.0.64.
* The issue with the Cerby mobile app not launching when users tap a push notification is fixed in v1.0.99. In this case, the app was previously closed before receiving the push notification.
* The issue with push notifications logging users out of the Cerby mobile app is fixed in iOS v1.0.66 and Android v1.0.100.
