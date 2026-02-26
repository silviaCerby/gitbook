---
description: "This article describes the latest enhancements and bug fixes to improve your experience using Cerby."
intercom_id: 13225817
---

# Release Notes - December 23, 2025

## New features

The following are the new features and improvements we released across the Cerby platform:

### Proactive security, enhanced

Building on our initial launch, the **Security Hub** evolves into an actionable command center for your workspace. While the first version of this feature focused on identifying orphaned accounts, our latest update introduces a card with the latest automation tasks that had issues and a card with the total number of accounts, as shown in **Figure 1**.

<img src="../.gitbook/assets/76d42e6e-b1d8-4ba2-bb7c-fb8dc4b413ab.png" alt="Screenshot of the Cerby web app dashboard. The Security hub page is displayed with cards containing the tasks with issues blocking automation, the total workspace accounts, and the orphaned accounts">

**Figure 1. Security hub** page in the Cerby web app dashboard

The card with automation task issues is a powerful user interface (UI) component that monitors the health of your automated workflows. You can now identify and take action on disruptions in user access termination, access management, and data synchronization in real time.

By bridging the gap between identifying risks and taking action, the Security Hub ensures that no misconfiguration or failed automation goes unnoticed. To dive deeper into these new capabilities, read our updated article [Explore Security Hub](https://help.cerby.com/en/articles/10492095-explore-security-hub).

### Instant visibility into your integrations

Business hub integrations are the backbone of your user and access management strategy, and now you can monitor their health at a glance. We’ve introduced a new **Status** column on the **Business Hubs** page, providing real-time transparency into how your integrations are performing.

This update enables business hub **Owners** and **Managers** to instantly see if an integration is healthy, requires a manual sync, or needs a configuration review, as shown in **Figure 2**.

<img src="../.gitbook/assets/c12e2865-cc08-4c81-bd6a-84bbf43b3ba7.png" alt="Screenshot of the Cerby web app dashboard. The Business Hubs page is displayed with a table of business hubs connected to Cerby and the Status column indicating the status of each integration">

**Figure 2.** **Business Hubs** page in the Cerby web app dashboard

The new status tracking covers every stage of the integration lifecycle. From "Under validation" for new connections to specific alerts like "Review service account", the Cerby platform proactively flags exactly what needs your attention. By providing clear, actionable statuses, Cerby ensures that your business hubs remain functional and secure without requiring manual, constant checks.

To learn more about what each status means and how to keep your integrations healthy, read the article [View the status of your business hub integration](https://help.cerby.com/en/articles/12599528-view-the-status-of-your-business-hub-integration).

### Expanding control in app setting restrictions

Building on our existing safeguards for passwords and members, we’ve expanded the capabilities of the **App setting restrictions** feature. Cerby can now identify and restrict account deletion attempts from users in an application, providing you with even tighter control over the lifecycle of the accounts saved in your workspace.

This enhancement ensures that critical accounts aren't permanently removed without oversight. To learn how to add account deletion safeguards to your workspace, read our updated article:[ Explore App setting restrictions](https://help.cerby.com/en/articles/10276184-explore-app-settings-restrictions).

### Cerby web app

Check out what’s new in our Cerby web app:

* Users can now close the dialog box at any time when they create a Cerby-managed email address. The **Close** icon was missing from the experience.
* We’ve removed the **Forward** option from the **More options** drop-down menu in the account **Inbox** for accounts with Cerby-managed phone numbers. The action of forwarding an SMS message to an email address is not supported.
* For a more intuitive experience, the newest secrets are now displayed at the top of the **Secrets** page by default, ensuring that the sensitive information you’ve just saved in Cerby is instantly accessible.

### Cerby mobile app

Dive into the newest additions to our Cerby mobile app:

* We’ve redesigned the onboarding experience on Android to ensure a smoother, more intuitive start for every user, as shown in **Figure 3**.

<img src="../.gitbook/assets/9095b921-1f4d-4e14-b52a-d25a840896df.png" alt="Screenshot of the Cerby mobile app. The Turn on Autofill screen is displayed in the onboarding carousel">

**Figure 3.** **Turn on Autofill** screen in the onboarding carousel of the Cerby mobile app for Android

After logging in for the first time, users will now see an onboarding carousel that guides them through the following steps:

1. Turn on Autofill
2. Set up a trusted device
3. Turn on biometrics
4. Enable notifications

With this enhancement, released in version 1.0.226, we aim to ensure that users successfully configure the Cerby mobile app on their first attempt.

  * Regarding UI enhancements, we redesigned the secret details and collection settings screens, enhancing layout clarity and visual consistency. You can see the new experience from versions iOS v1.0.276 and Android v1.0.226 onwards.
  * We improved the message displayed to users when they open the account details screen or the quick actions, looking for one-time verification codes. We now tell them to perform a login attempt to their account so that the code is generated and sent to the Cerby-managed method configured for multi-factor authentication (MFA). This enhancement was released in iOS v1.0.274 and Android v1.0.224.
* * *

## Fixes

Take note of the issues addressed and resolved by the Development team behind the Cerby platform:

### Cerby web app

* The issue with the business hub sharing wizard was fixed to ensure custom asset roles and app roles are correctly displayed and categorized. This fix addresses inaccuracies previously detected in integrations like JetBrains and Mixpanel.
* The issue with Meta Business Manager, where revoking unmatched users failed to remove them from the native console, despite the automation job being marked as successful in Cerby, was fixed. This ensures that users no longer reappear during the next sync.
* The issue where pending invitations persisted on assets (for example, in Google Ads) even after a user was successfully deleted from Cerby has been fixed. Now, all invites are automatically removed when a user is deleted from Cerby.
* The issue of being unable to share accounts with Login-Only users in guest workspaces, after establishing a host-guest partnership, has been fixed.
* The issue where users lost access to accounts after a SAML group change was fixed, ensuring that account and secret access are properly restored when group assignments are updated.
* The issue where a workspace member was downgraded from **User** to**Login-Only** but was still able to see the **Share** button in a collection they owned was fixed. The fix ensures that users with restricted roles, such as **Login-Only** , do not see conflicting options, providing a more consistent and secure user experience aligned with their current privileges.
* The issue with messages being displayed for the wrong account in the inbox has been fixed.
* The issue where some account passwords couldn’t be retrieved in workspaces with Azure Key Vault integrations was fixed.
* The issue with prompting business hub **Managers** and **Owners** of a Meta Business Manager integration to connect their personal Facebook account, even when this action is not necessary, was fixed.

### Cerby browser extension

* The issue with the Cerby logo of the inline menu being displayed in the **Password** field of an account login page, instead of the first input field, was fixed.
* The issue where the Cerby logo in the inline menu became unresponsive after an autofill action on a **Password** field was fixed. This fix also eliminates a bug that caused an erroneous “OTP not managed” message on fields without an MFA requirement.
* The issue with the in-context alert for incorrect login credentials not displaying the buttons for taking action (review credentials or notify account owner) was fixed.
* The issue with not switching the **Fill** buttons in the inline menu when manually transitioning between fields (for example, between the **Username** and **Password** fields) was fixed.
* The issue where users were locked out of auto-signing into Okta for 90 seconds if their Okta session expired has been fixed. The extension now correctly identifies when users are redirected to the Okta sign-in page and resets the login process instantly. Therefore, as soon as they sign back in, Cerby can complete the auto-login process to their apps without any delays or in-progress errors.

### Cerby mobile app

* The issue with not redirecting users to the account details screen after sharing an account was fixed in iOS v1.0.276.
* The issue with account preselection not working with disabled biometrics was fixed in Android v1.0.226, improving login reliability.
* The issue with duplicated notifications in Android was fixed in v1.0.226, improving clarity and reducing visual noise for end users.
