---
description: "This article describes how to filter jobs in the Automation Log using the Cerby web app."
intercom_id: 11713438
---

# Filter jobs in the Automation Log

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super** **Admins** , and **Admins**
* Only supported using the Cerby web app


{% endhint %}

As a workspace **Owner** , **Super** **Admin** , or **Admin** , you can narrow down the jobs displayed in the [Automation Log](https://help.cerby.com/en/articles/11642287-explore-the-automation-log) by applying the filters on the top menu.

These filters help you isolate specific automation jobs based on job type, status, and app. Filtering enables you to monitor large activity volumes, troubleshoot issues, or review recent identity, access, and account management changes.

To filter jobs in the Automation Log, you must complete the following steps using the Cerby web app:

1. Log in to your [Cerby](https://app.cerby.com/) workspace.
2. Select the **Automation** option from the left navigation drawer. The **Automation Log** page is displayed.
3. Apply any of the following filters located at the top of the page:

   * **Filter by status:** The following are the statuses you can filter the results by:
     * **Not completed:** If even a single nested job fails.
     * **Retrying:** If a single nested job is retrying.
     * **Running:** If a single nested job is still running.
     * **Started:** If nothing is running, but at least one nested job has started.
     * **Queued:** It is the default state if no jobs have started.
     * **Completed:** Only if all nested jobs are finished successfully.
   * **Filter by task:** The following are the tasks you can filter the results by:
     * **Adding users:** It involves creating a user account and inviting a new user to a seat-based or paid social app.
     * **Syncing users:** It involves retrieving the user and asset data from a seat-based or paid social app.
     * **Updating user roles:** It involves updating the existing role of a user within a seat-based or paid social app.
     * **Removing users:** It involves removing users from a seat-based or paid social app.
     * **Rotating passwords:** It involves rotating the password of an account.
     * **Turning on MFA:** It involves turning on multi-factor authentication (MFA) for an account with a Cerby-managed method.
     * **Turning off MFA:** It involves turning off MFA for an account.
   * **Filter by app:** The Cerby-managed apps and integrations, you can filter the results by.

Now you are done.
