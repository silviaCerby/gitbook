---
description: "This article describes how to scout a workflow on your app, consisting of the steps you take to complete a task in a browser tab."
intercom_id: 10046916
hidden: true
noIndex: true
---

# Scout a workflow

{% hint style="info" %}


**Who can use this feature?**

* Cerby workspace**Owners** , **Super Admins** , and **Admins**
* Only supported using the Scout browser extension


{% endhint %}

As a workspace **Owner** , **Super Admin** , **Admin** , or **user** , you can use the [Scout browser extension](https://help.cerby.com/en/articles/9774431-explore-scout) to perform workflow scouting on your apps and help accelerate the process of building the automated tasks you use in Cerby.

Scout captures all the user interface (UI) interactions you perform on a web browser, such as clicks, scrolls, and overall navigation, to complete a specific task on your app. The workflows or tasks you can scout are the following:

* **Log in to your account:** It comprises the flow of navigating to your app’s login page and entering your login credentials (username, password, and verification code when applicable) to access your app.
* **Invite a user to your app:** It comprises the flow of logging in to your seat-based or paid social app as an admin and inviting a new app member.
* **Remove a user from your app:** It comprises the flow of logging in to your seat-based or paid social app as an admin and removing an existing app member.
* **Update a user's role in your app:** It comprises the flow of logging in to your seat-based or paid social app as an admin and updating the role of an app member.
* **Turn on multi-factor authentication (MFA):** It comprises the flow of logging in to your account, navigating to the account security settings, and turning on MFA with Cerby as an authenticator app.
* **Update your account's password:** It comprises the flow of logging in to your account, navigating to the account security settings, and updating the password.

**IMPORTANT:** Cerby doesn’t store any input values you enter during the workflow scouting; additionally, these values are masked.
---

This article describes how to scout a workflow.

* * *

## Scout a workflow

To scout a workflow, you must complete the next steps:

  1. Open a new browser tab.

  **IMPORTANT:** Scout records all your UI interactions in the current tab, such as clicks, scrolls, and overall navigation. If you change the tab, it’ll keep scouting, but it won’t capture any data.

  2. Open the Scout browser extension. Depending on whether you have an active session or not, one of the following screens are displayed:

     * The **Scout your workflows** screen is displayed if you have an active session.

       1. Continue to step 3.

     * The **Welcome to Scout!** screen is displayed if you don’t have an active session.

       1. [Log in to Scout](https://help.cerby.com/en/articles/10046820-log-in-to-scout).
       2. Continue to step 3.
  3. Click the **Start scouting** button. The **Scouting** screen is displayed, and Scout starts recording your interactions in the current browser tab.
​**NOTE:** The extension popup closes when you click any element in the browser tab, but it keeps recording.

  4. Complete the task from start to finish.

  **NOTE:** You can cancel the current scouting anytime and discard it by clicking the **Cancel** button. The **Scout your workflows** popup is displayed again.

  5. Open the Scout browser extension when you are done. The **Scouting** screen is displayed.
  6. Click the **Stop** button. The **Send your scouting report** screen is displayed with the length and the number of actions saved in the scouting.

  **TIP:** Click the **Preview** button to see the recording before sending it to Cerby. A new browser tab opens where you can preview the scouting report. To learn more about the controls of this page, read the [Preview your recording](scout-a-workflow.md#preview-your-scouting-report) section.

  7. Enter and select the corresponding details of your scouting report from the following fields:

     * **Scouting report name:** It is the name to assign to the recording.
     * **App name:** It is the name of the app you are recording. You can select it from the drop-down list or enter its name and select the **Create** option if the app is not in the list.
     * **Task type:** It is the type of task you performed. You can select the corresponding option from the drop-down list or the **Other** option if the task is not in the list.
     * **Task name:** It is the name of the task you performed. This field appears when you select **Other** from the **Task type** drop-down list.

  8. Click the **Send** button. The **Scouting report successfully sent!** screen is displayed.
  9. Click the **Got it** button. The Scout browser extension popup closes.

Now you are done.

* * *

## Preview your scouting report

The following are the controls available to preview your scouting report in a new browser tab when clicking the **Preview** button after step 6 of the [Scout a workflow](scout-a-workflow.md#scout-a-workflow) section:

  * **Play/Pause:** Starts or pauses the scouting report.
  * **Progress bar:** Moves the scouting report forward or backward. You can also click anywhere on the bar to jump to a specific point in the recording.
  * **Fullscreen:** Plays the scouting report in fullscreen mode. Press the ESC key or click the icon again to exit fullscreen.
  * **Speed controllers:** Play the scouting at the following speeds:
    * 1x
    * 2x
    * 4x
    * 8x
* * *

## Troubleshooting

The following are the potential issues you may encounter when using Scout and the proposed actions to troubleshoot them:

  * **Unable to send your scouting report:** This error message means that the scouting report couldn’t be sent due to an unexpected issue.

    1. Click the **Try again** button to send the scouting report again.

  * **Unable to scout your workflow:** This error message means that the Scout browser extension couldn't generate the scouting report due to an unexpected issue.

    1. Click the **Try again** button to scout your workflow again from the start.

  * **Unable to process your scouting report:** This error message means that the Scout browser extension couldn't process the scouting report because it was recorded for less than 15 seconds.

    1. Click the **Try again** button to scout your workflow again from the start.

    **IMPORTANT:** The recording must be at least 15 seconds long.

  * **Blank recording when previewing the scouting report:** This error occurs when the Scout browser extension doesn’t capture your UI interactions correctly due to an unexpected issue. Cerby is unable to detect this error, so you can only identify it when you [preview the scouting report](scout-a-workflow.md#preview-your-scouting-report) and see a blank recording.

    1. Open the Scout browser extension. The **Send your scouting report** screen is displayed.
    2. Click the **Cancel** button. The **Scout your workflows** screen is displayed.
    3. Click the **Start scouting** button to scout your workflow again from the start.
