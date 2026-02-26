---
description: "This article describes the latest enhancements and bug fixes to improve your experience using Cerby."
intercom_id: 12872483
---

# Release Notes - November 18, 2025

## New features

The following are the new features and improvements we released across the Cerby platform:

### Cerby web app

Check out what’s new in our Cerby web app:

* The Cerby web app now ensures no account is left behind when it comes to security. We've integrated our password generator directly into the account saving process, in the **Add account** dialog box, as well as when editing a password in the account details page, as shown in **Figure 1**.

<img src="../../../.gitbook/assets/c836e2bc-bd2c-4b73-8c9d-b60fb29c2fc5.png" alt="">

**Figure 1.** **Password generator** dialog box in the account details page

It’s never been easier to give every single one of your accounts the strong login credentials it deserves.

* Flexibility is the keyword! As a user who connects a business hub for your app, you can now select how you want Cerby to handle the way users save and connect their app user accounts to the integration.
* A dialog box is displayed for you to choose if you want Cerby to prompt users to save their login credentials for the business hub or if you want to let Cerby autosave the accounts when users log in to the app, as shown in **Figure 2**.

<img src="../../../.gitbook/assets/ea4a925f-91cc-4b2f-8eed-054e9720a0e2.png" alt="">

**Figure 2. User management and login** dialog box

* Tired of scrolling? We've given the **Secrets** page a major organizational upgrade. You can now sort and filter your secrets like a pro. Find that critical login detail or important key in seconds.
You can filter by category or secret type, and sort by alphabetical order, creation date, and last updated date.

* We've implemented under-the-hood optimizations to the **Users** table in the business hub details page. This improvement directly addresses load time latency, significantly improving performance and responsiveness when viewing and interacting with large lists of users.

### Cerby browser extension

Explore the latest features in our Cerby browser extension:

* Ever wondered why the Cerby browser extension didn’t work properly in incognito mode or private tabs? Well, that’s because this browsing mode is not supported; therefore, some features may not work as expected. If you need the full user experience, Cerby recommends using a standard browser window.
So, we started showing this information in disclaimer banners and messages.

* Talking about showing messages in the extension. We have implemented an in-context alert to provide you with clear guidance when you encounter verification challenges in multi-factor authentication (MFA) methods that Cerby does not manage. This alert aims to unblock you by explaining the situation and offering actionable next steps, preventing you from being blocked without clear direction.
* The user experience of logging in to an app with Google single sign-on (SSO) was improved as follows:
  * Clicking on a Google SSO account card in the browser extension now redirects users properly to the intended URL. The goal is to ensure correct behavior for federated authentication flows when users access their accounts via the extension.
  * We've added a Google SSO chip to the browser extension popup and inline menu to improve visibility into authentication types.
* The password generator is now available in the inline menu at all times, even if the input field is not selected or the Cerby browser extension has no active session. The goal is to ensure you can consistently generate strong passwords across all your login attempts.
* We implemented a technical security measure known as the frame-ancestors directive. This measure strengthens our platform's defense against user interface (UI) injection attacks, helping to keep your account data secure and aligned with best security practices.

### Cerby mobile app

Dive into the newest additions to our Cerby mobile app:

* We now support MFA with biometrics from versions iOS v1.0.264 and Android v1.0.216 onward to protect sensitive operations in the Cerby mobile app, such as viewing a secret. This approach ensures that sensitive operations are only authorized by you. Additionally, we’ve enabled biometric locking on the Android app, requiring fingerprint or facial recognition when reopening from the background.
* To provide greater visibility and security, account **Owners** can now find a new **Activity** section on the account details screen, as shown in **Figure 3**.

<img src="../../../.gitbook/assets/605e6ffe-7313-4c29-8018-c14c9e6cc061.png" alt="">

**Figure 3.** **Activity** screen related to an account

This feature allows you to quickly monitor the last seven days of events and actions associated with the account. This feature was released in iOS v1.0.268 and Android v1.0.216. For more information, read the article [View the details of an account using the Cerby mobile app](https://help.cerby.com/en/articles/12454986-view-the-details-of-an-account-using-the-cerby-mobile-app).

* Your data privacy is our priority. From version v1.0.264 onward, the Cerby mobile app for iOS includes a security rule that automatically hides sensitive account information if a screenshot or screen recording is detected. This feature ensures your credentials are kept private and secure, even if a capture is accidentally triggered.
* Access common tasks instantly! We've completed and released a bottom drawer across iOS v1.0.271 and Android v1.0.222 where you can retrieve one-time codes or copy passwords much faster, saving you clicks and speeding up your daily logins.
* From the **Accounts** tab, just tap the **More options** () icon of an account, and a list of options will be displayed in the bottom drawer, as shown in **Figure 4**.

<img src="../../../.gitbook/assets/72549de6-602a-41db-849c-7cf6aa398b9e.png" alt="">

**Figure 4.** Quick actions bottom drawer

  * We've made crucial performance updates that we released for iOS v1.0.264, aiming to prevent app hangs at startup and during autofill.
* * *

## Fixes

Take note of the issues addressed and resolved by the Development team behind the Cerby platform:

* The issue with some failed logins for Pinterest was fixed. This fix improves how the platform handles app-specific errors, ensuring that you can reliably access your Pinterest accounts without automation job failures.

### Cerby web app

* The issue with missing information in the **Last viewed** column within the **Members** tab of the secret details page was fixed.
* The Meta sync issue that caused Cerby permissions to not reflect correctly in native Meta consoles was fixed, ensuring asset-level access is honored. Additionally, we resolved inaccuracies when displaying user matchings for Meta.
* The issue when creating an API key, due to the date picker not allowing users to select an expiration date, was fixed. The picker only allowed users to select the current date.
* The issue with some **Login-Only** users being assigned as account **Owners,** when they can only have a **Collaborator** role, was fixed.
* The issue where the password policy check wasn't correctly identifying reused passwords was fixed, ensuring users get accurate, real-time feedback during password creation.

### Cerby browser extension

* The issue with auto-login tasks failing for users on Safari and Apple devices was fixed. Reliable support is now restored for securely autofilling passwords.

### Cerby mobile app

* The issue with a memory leak in iOS that was causing performance degradation when navigating between accounts was fixed in iOS v1.0.244 and Android v1.0.205.

### CLI

  * The issue where the Cerby CLI was blocked from running on macOS due to missing crypto configurations was fixed, restoring access for developers using Apple environments.
* * *

## Security fixes

* We’ve addressed a security vulnerability where workspace **Admins** were able to disable MFA checks for higher-privileged users, like workspace **Super Admins** and **Owners**.
