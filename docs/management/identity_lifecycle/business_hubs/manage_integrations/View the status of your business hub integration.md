# View the status of your business hub integration

**Description:** This article describes how to view the status of your business hub integration in Cerby.

{% hint style="info" %} **Who can use this feature?** * Business hub
**Owners** and **Managers** * Only supported using the Cerby web app {%
endhint %}

As a business hub **Owner** or **Manager** , you can view the status of your
business hub integration directly in the**Business Hubs** page.

When you connect the first business hub in your workspace for an external app,
Cerby schedules a validation process to confirm that the integration is
correctly configured and working in your environment. After validation, the
integration status might change over time due to account misconfigurations or
changes in the external app affecting Cerby automation. In any case, viewing
the status helps you quickly determine if the integration is working
correctly, if it requires your attention, or if Cerby is actively addressing
an issue or failed automation.

To view the status of your business hub integration, you must complete the
following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.

  2. Select the**Business Hubs** option from the left menu. The **Business Hubs** page is displayed with a table of integrations and a column indicating their status, as shown in **Figure 1.**

![](images/b6552736-502e-4f0d-868c-cf94745226b9)

**Figure 1.** The**Business Hubs** page in the Cerby web app dashboard

You can see your integration status under the **Status** column. The following
are the possible statuses:

     * **Under validation:** The business hub has been successfully connected to an external app, and Cerby is currently validating if the integration works correctly in your environment.  
**NOTE:** This status is set for all business hubs in your workspace connected
to the same external app until the validation process is complete. After
validation is completed, subsequent business hubs for the same application
will not enter this status.

     * **Under review by Cerby:** Cerby is currently reviewing and addressing known issues or failed automations identified during validation. 

     * **Review configuration:** Cerby encountered misconfiguration issues in the business hub, such as an incorrect business ID, and couldn't complete automation. The integration **Owner** must address the misconfiguration.

     * **Review service account:** Cerby encountered misconfiguration issues in the service account associated with the business hub, and couldn't complete automation. The integration **Owner** must address the misconfiguration caused by any of the following reasons:

       * The service account’s login credentials are incorrect.

       * Cerby-managed MFA is not turned on for the account.

     * **Requires sync:** Cerby has outdated data for your business hub because the initial sync with the external app hasn't been executed, or subsequent syncs failed or are over 24 hours old. The integration Owner must perform a manual data sync.

     * **Healthy:** The business hub integration is working, and the last sync was completed successfully within the past 24 hours.

Now you are done.

