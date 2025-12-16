---
description: This article describes how to view the status of your IdLCM integration in Cerby.
intercom_id: 12875217
---

# View the status of your IdLCM integration

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super** **Admins** , and **Admins**
* Only supported using the Cerby web app


{% endhint %}

As a workspace **Owner** ,**Super Admin** , or **Admin,** you can view the status of all the existing IdLCM integrations directly in the**Integrations** page.

When you create the first integration in your workspace for an external app, Cerby schedules a validation process to confirm that the integration is correctly configured and working in your environment.

After validation, the integration status might change over time due to account misconfigurations or changes in the external app affecting Cerby automation. In any case, viewing the status helps you quickly determine if the integration is working correctly, if it requires your attention, or if Cerby is actively addressing an issue or failed automation.

To view the status of your IdLCM integration, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Select the**Integrations** option from the left menu. The **Integrations** page is displayed with a table of integrations and a column indicating their status, as shown in **Figure 1.**
​
**Figure 1.** The**Integrations** page in the Cerby web app dashboard

You can see your integration status under the **Status** column. The following are the possible statuses:

<figure><img src="../../../../../.gitbook/assets/2450d35c-a899-4fff-842c-c82cecb68ed8.png" alt=""><figcaption></figcaption></figure>

     * **Under validation:** The integration has been successfully connected to an external app, and Cerby is currently validating if it works correctly in your environment.
​**NOTE:** This status is set for all integrations in your workspace connected to the same external app until the validation process is complete. After validation is completed, subsequent integrations for the same app will not enter this status.

     * **Under review by Cerby:** Cerby is currently reviewing and addressing known issues or failed automations identified during validation.
     * **Validating:** Cerby is executing an automated validation check to verify that the integration setup and connection to the external app are working correctly.
     * **Validated:** The automated validation check completed successfully.
     * Validation failed: The automated validation check did not complete successfully.
     * **In progress:** A security operation, such as provisioning, updating, deprovisioning, or syncing, is being executed for this integration.
     * **Failed:** The latest security operation did not complete successfully.
     * **Retrying:** The latest failed security operation is being retried.
     * **Up to date:** The integration is working correctly, and the last security operation was completed successfully.
