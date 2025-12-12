---
description: This article describes the benefits of Scout for workflow scouting to accelerate the building process of Cerby’s automated jobs.
---

# Explore Scout

With Cerby, you can be part of the engine that shapes the automated jobs you trigger to manage and protect your accounts and seat-based and paid social apps.

Scout is a browser extension that accelerates and improves the building process of automated workflows by capturing web interactions. The information Scout captures can lead to better-designed features, smoother workflows, and more user-friendly interfaces, directly benefiting you by making the applications you use more intuitive and efficient.

**Figure 1** shows how the Scout browser extension looks.

<figure><img src="../.gitbook/assets/AD_4nXdXAu1YH2unkib1NWwfAVlMDE58bdxT_bF8Hu74ZLo5VJXkEgA4lSEF2psFPE4FBvMbJrARdA3YavybL1tARO5zQ4zpBJwKeC33zIywNq8IoUqwsFXOu4ADy7yqCnPdR_Y9GdRPfjdluC_WgjD9o3_Q4qNa.png" alt="Screenshot of Scout"><figcaption></figcaption></figure>

**Figure 1.** Scout browser extension popup on top of a web browser

To start using Scout, you must request access to it to a Cerby workspace **Admin** or **Super Admin** , who provides you with an API key. When authorized, you can open Scout to capture your interactions in a specific browser tab.

The following are the manual business workflows and tasks you can capture so that the Cerby Integrations team builds the corresponding automation:

  * **Log in to your account:** Navigate to your app’s login page and authenticate.
  * **Update your account's password:** Access the account settings page and update your password.
  * **Turn on multi-factor authentication (MFA):** Navigate to your account security settings page and turn on MFA using Cerby.
​**Invite a user:** Add a new user to a seat-based app.

  * **Update a user’s role:** Update the role of a user or group (usually performed by an app admin) in your app.
  * **Remove a user:** Remove access of an existing user from an app (usually performed by an app admin).

{% hint style="danger" %}


**IMPORTANT:** Scout doesn’t capture or store input values entered in any field. When your organization has enabled this feature, only workspace **Admins** and **Super Admins** can authorize Scout. For more information, read the How Scout protects your privacy section.


{% endhint %}

* * *

# How Scout works

Scout captures all your user interface (UI) interactions on a web browser, such as clicks, scrolls, and overall navigation. This information is saved in a scouting report that you send to the Cerby Development team.

To get started, you must authenticate by providing an API key that you generate in the Cerby web app with the following scopes:

  * **Read automated jobs:** Enables reading automated job data.
  * **Write automated jobs:** Enables writing automated job data.

After authentication, you can start scouting your workflows in the current browser tab. All your interactions are captured as they occur, and you can stop the recording when you are done.

Before sending the scouting report, you can preview it using the following playback controls:

  * Play and pause
  * Progress bar
  * Full-screen mode
  * Speed selector
* * *

# How Scout protects your privacy

When using Scout to capture your UI interactions, Cerby prioritizes the protection of your sensitive information at all times. This section explains how Scout ensures the safety of your data and details what we capture and what not.

## What information Scout captures

To provide valuable insights while maintaining your privacy, Scout captures user interactions on a webpage considering the following:

  * **On-demand and tab-specific capture:** Scout captures user interactions from the specific browser tab the user specifies and operates strictly on demand. If a user does not actively start Scout it does not send any data to our servers.
  * **Interaction paths:** Scout captures user interactions from the tab, focusing on elements, such as input fields and buttons where users click. These data points are used to automatically create your app integration workflows.
  * **Playback of web content:** Cerby uses the Scout data to replay the web views and user interactions. Scout never records an actual video of the screen or browser tab.
  * **Masked input data:** Scout masks all input fields–such as usernames, email addresses, and other sensitive information–ensuring that your private data is not captured or made visible to Cerby.

Scout’s approach protects your privacy and security. It shares only what is necessary to build and maintain business workflows.

## What information Scout does _not_ capture

Cerby understands the critical importance of privacy and security for our customers; protecting your secrets is what we do best. We designed Scout to gather the data we require while omitting unnecessary or sensitive fields.

  * **Application credentials:** Scout does _not_ capture passwords or other credentials. Masked fields are automatically excluded from capture.
  * **User data entry:** Scout does not capture browser input fields.
  * **Headers and cookies** : Scout does not capture raw POST data, headers, or cookies.

We recognize that business application administrators have demanding workloads; therefore, we aim to alleviate that burden. Scout allows us to work asynchronously with our customers on their schedule, not ours. We believe in effective collaboration without requesting direct access to your applications or scheduling support sessions.

* * *

# Best scouting practices and tips

The following are the best scouting practices and general tips for scouting your workflows:

  * Think through all the steps necessary to perform the task to ensure nothing is missed.
  * Make sure you have a stable and reliable internet connection.
  * Record one task per scouting report, and perform only the relevant steps to complete that task.
  * Avoid scouting reports that are shorter than 15 seconds.
  * Review the scouting report for any mistakes or errors before submitting it to Cerby.
  * Select the appropriate task type and enter the name of your application before submitting the scouting to the Cerby Integrations team.

{% hint style="danger" %}


**IMPORTANT:** Notify Cerby when a new browser tab opens during scouting because this action could interfere with a successful scouting report.


{% endhint %}

The following sections contain specific recommendations to make sure you capture all relevant interactions for each workflow.

## Log in to your account

This workflow comprises all the steps you complete to log in to your account successfully.

The following are the scouting recommendations:

  1. Start scouting when you are on your app’s login page
  2. Enter your login credentials (username, password, and verification code when applicable) to access your app
​**IMPORTANT:** Record any interaction during the login process, such as captchas, dialog boxes, or forms where you enter additional login information. For example, employee number, phone number, or workspace selectors.

The following are additional workflows that Cerby recommends to scout:

  * Attempt to log in by entering incorrect login credentials and show what happens in your app, such as message boxes or notifications.
  * Log in using a different web browser and a different computer than you normally do, and show any additional interaction. You can even use incognito mode.
  * Close an active session (log out) before attempting to log in.

## Update your account's password

This workflow comprises all the steps you complete to access your account and update your password.

The following are the scouting recommendations:

  1. Start scouting on the page where you land right after logging in to your account.
  2. Navigate to the account security settings.
  3. Update the password. Typically, you must enter your old password.
  4. View the success message in your app.

Cerby also recommends scouting the workflow for the scenario where an incorrect password is entered during an update. Show what happens in your app, such as message boxes or notifications.

## Turn on MFA

This workflow comprises all the steps you complete to access your account and turn on MFA successfully.

The following are the scouting recommendations:

  1. Start scouting on the page where you land right after logging in to your account.
  2. Navigate to the account security settings.
  3. Turn on MFA with any authenticator app. Typically, these apps use time-based one-time passwords (TOTP) for authentication.
​**IMPORTANT:** Select the **Can’t scan code** option to turn on MFA with a secret key or token. If this option is unavailable, complete the setup as your app requires.

  4. View the success message in your app.

## Check for updates

This workflow comprises all the steps you complete as an admin to access your seat-based or paid social app, view the table of users with a seat in your app, and access your assets, if applicable.

The following are the scouting recommendations:

  1. Start scouting on the page where you land right after logging in to your account.
  2. Navigate to the page with the table of users or members. In this page, record the following actions:

     * Show all the roles and assets you can assign to a user. They are usually in clickable drop-down lists, but if they are not, navigate to the specific tables or tabs with roles and assets. Interact with all the relevant selectors and input fields.
     * Show the user details relevant to user management; typically, they are three: username, email, and role. If more details are relevant, such as phone number or location, show how to navigate to find or customize the corresponding input fields.
​**NOTE:** Show the details of different users because sometimes the UI changes when it’s you or another user.

     * Show the table of active and invited users, when applicable. Invited means an invite was sent via email, but the user has not joined the app.
     * Resend an invitation already sent to a user who has not joined the app.
     * Use the search bar to find users with each of the following statuses:
       * Active user
       * Invited user
       * Nonexistent user
     * Navigate through a few user result pages, when applicable, to scout the pagination functionality.**** Preferably, navigate to the last page of results.
     * Navigate to the User details page and interact with all the selectors and input fields related to roles and assets.
     * Show the search feature when a search bar is present. Look for an existing and nonexistent user.

{% hint style="danger" %}


**IMPORTANT:** If your app supports assets and they are relevant to your team, scout all actions from step 2 by navigating to the table of users and assets. Additionally, cover the flow of displaying or retrieving the asset ID (whether in the URL or the user interface); sometimes, it requires navigating to the asset details page.


{% endhint %}

## Invite a user

This workflow comprises all the steps you complete as an admin to access your seat-based or paid social app, invite a new user to join your app, and grant them access to your assets, when applicable. Preferably, invite a dummy user whose email address you have access so you can complete the user account creation process.

The following are the scouting recommendations:

  1. Start scouting on the page where you land right after logging in to your account.
  2. Navigate to the page with the table of users.
  3. Invite the dummy user to your app. Cover the following scenarios:

     * Select a role for the user on the app and the assets, when applicable.
     * Fill out any information required by the app, such as employee number, department, or location, in additional dialog boxes and prompts.
     * Resend the invite when applicable.
     * Attempt to invite a user pending to join the app.

  4. Accept the invite to create the user account as the end user would do it.
  5. View the success message and active status of the invited user as an admin.
  6. Navigate through a few user result pages, when applicable, to scout the pagination functionality.

{% hint style="danger" %}


**IMPORTANT:** If your app supports assets that are relevant to your team, scout all actions from steps 2 to 6 by navigating to the table of users and assets. Preferably, scout the flow of only granting access to an asset for an existing user.


{% endhint %}

## Update a user’s role

This workflow comprises all the steps you complete as an admin to access your seat-based or paid social app and update the role of an active user on your apps and assets. Preferably, update the role of an existing dummy user.

The following are the scouting recommendations:

  1. Start scouting on the page where you land right after logging in to your account.
  2. Navigate to the page with the table of users.
  3. Navigate to a user details page, when applicable, and interact with all the selectors and input fields related to roles and assets.
  4. Update the role of the dummy user. Capture the following scenarios:

     * Show the role selectors and select multiple roles, when applicable. Sometimes apps have role restrictions based on your selection.
     * Show how to create and assign custom roles, when applicable.

  5. Save and apply the role update.
  6. View the success message and the new role of the dummy user.

{% hint style="danger" %}


**IMPORTANT:** If your app supports assets and they are relevant to your team, record all actions from steps 2 to 6 by navigating to the tables of users and assets. Preferably, scout the flow of only updating the role of an existing user on an asset.


{% endhint %}

## Remove a user

This workflow comprises all the steps you complete as an admin to access your seat-based or paid social app and remove an existing active user from your apps and assets, when applicable. Preferably, remove an existing active dummy user.

The following are the scouting recommendations:

  1. Start scouting on the page where you land right after logging in to your account.
  2. Navigate to the page with the table of users.
  3. Remove the dummy user from your app.
  4. View the success message in the user's table.
  5. Remove a dummy user pending to join the app, when applicable.

{% hint style="danger" %}


**IMPORTANT:** If your app supports assets and they are relevant to your team, record all actions from steps 2 to 6 by navigating to the tables of users and assets. Preferably, scout the flow of only removing access to an asset for an existing user.


{% endhint %}

# Related articles

The following articles contain more information about Scout:

  * [Install the Scout browser extension](https://help.cerby.com/en/articles/10046805-install-scout)
  * [Log in to Scout](https://help.cerby.com/en/articles/10046820-log-in-to-scout)
  * [Scout a workflow](https://help.cerby.com/en/articles/10046916-scout-a-workflow)
  * [Log out from Scout](https://help.cerby.com/en/articles/10046948-log-out-from-scout)
