# Explore the Automation Log

**Description:** This article describes the key benefits and settings for using and understanding Cerby’s Automation Log best.

With Cerby, you can use the **Automation Log** to trace every critical step of
each automation job triggered to perform identity, account, and user
management tasks, from provisioning users in an app to logging in securely to
your accounts.

This log shows the precise automation status in the target app, so you always
know how your users, credentials, and security settings are being protected
and synchronized.

The following are the benefits of Cerby’s Automation Log:

  * **Transparency:** You can see exactly what is running, where it came from, and why it was triggered.

  * **Speed:** You can quickly identify stalled or incomplete jobs that Cerby triggers.

  * **Accountability:** You can trace every update to its source, helping you audit changes across all apps.

{% hint style="danger" %} **IMPORTANT:** You must be a workspace **owner** ,
**super** **admin** , or **admin to access the Automation Log**. {% endhint %}

* * *

# Key concepts

**Table 1** contains the key concepts that are essential for understanding the
Automation Log.

Concept| Description  
---|---  
**Automation job**|  An automation job is a single execution of an automated
process. It includes details such as when it started, its current status, and
related logs. Jobs can be scheduled to run at specific times or triggered by
system events or user actions; also, they can trigger nested jobs to
accomplish a task. Automation jobs perform identity, account, and access
management tasks. For example, provisioning a user like John Doe in an app or
rotating the password for a Marketing account. In the Automation Log, each
recorded execution is called an automation job, and a specific ID is assigned.  
Nested job| Some automation jobs involve executing one or more jobs as part of
the process. All jobs are nested into one and called nested jobs for those
cases.  
  
**Table 1. Automation Log key concepts**

* * *

# **The Automation Log page**

The **Automation Log** page in the Cerby web app dashboard is the centralized
view of all the automation jobs triggered within your Cerby workspace, as
shown in **Figure 1**.

![](gitbook/imagesAD_4nXcNsmJwAhqLyI_0eHnG1C06TfgbDDGbIOBVPZME_lC-
LMvF07s49cbMvptXyxhxg7pUnvtnjiIDWn-
oSmc7gTYt_TCFpRZvTcm4Zf5vX2DkObtc2gEj4AB_DsYRgOPuaV3WaRiK)

**Figure 1.** **Automation Log** page in the Cerby web app dashboard

The following is the information you can find in each column of the Automation
Log:

  * **Status:** The current phase of each automation job. For more information, refer to the Status types section.

  * **Target:** The specific resource affected by the job. For example, accounts, business hubs, and teams.

  * **Actor:** The entity that triggered the job. For example, Cerby or a user.

  * **Task:** The identity, account, or user management action to be accomplished with the job. For more information, refer to the Task types section.

  * **Trigger:** The underlying rule or context that triggered the job. For more information, refer to the Trigger types section. 

  * **Created at:** The date and time when the job was triggered.

  * **Updated at:** The date and time of the most recent status change.

  * **View all jobs:** The link that opens the list of jobs included in a nested job.

## **Task types**

To provide valuable insights within your workspace, the Automation log
captures the following tasks:

  * **Adding users:** It involves creating a user account and inviting a new user to a seat-based or paid social app.

  * **Syncing users:** It involves retrieving the user and asset data from a seat-based or paid social app.

  * **Updating user roles:** It involves updating the existing role of a user within a seat-based or paid social app.

  * **Removing users:** It involves removing users from a seat-based or paid social app.

  * **Rotating passwords:** It involves rotating the password of an account.

  * **Turning on MFA:** It involves turning on multi-factor authentication (MFA) for an account with a Cerby-managed method.

  * **Turning off MFA:** It involves turning off MFA for an account.

  * **Logging in:** It involves logging in to an account by entering the login credentials saved in Cerby, including verification codes if MFA is managed by Cerby.

## **Trigger types**

The following are the sources that add a new log entry displayed in the
Automation log:

  * **Web app: A manual action performed by a user via the Cerby interface.**

  * **Workspace policy: A scheduled daily sync for business hub updates.**

  * **Password policy:** A policy per app that enforces password rotations for all accounts within a workspace belonging to the same app.

  * **SCIM: An event triggered by an identity provider (IdP) and propagated to Cerby via the System for Cross-domain Identity Management (SCIM) protocol.**

  * **Team events: A change in the structure, roles, or permissions of a Cerby team.**

  * **Collection events: A change in a Cerby collection.**

  * **Universal Logout: A manual action performed by a user via the Cerby interface or an Okta Universal Logout event extended to a workspace that initiates Cerby’s Universal Logout.**

  * **Cerby API: A call made to the platform using[Cerby’s API](https://developer.cerby.com/#welcome-to-the-cerby-developer-portal).**

  * **Cerby Admin API:** A call made to the platform to perform manual admin actions in customer workspaces.

## **Status types**

The following are the statuses for each log entry displayed in the Automation
log:

  * **Not completed:** If even a single nested job fails.

  * **Retrying:** If a single nested job is retrying.

  * **Running:** If a single nested job is still running.

  * **Started:** If nothing is running, but at least one nested job has started.

  * **Queued:** It is the default state if no jobs have started.

  * **Completed:** Only if all nested jobs are finished successfully.

