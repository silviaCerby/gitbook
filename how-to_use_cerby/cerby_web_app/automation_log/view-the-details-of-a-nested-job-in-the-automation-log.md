---
description: "This article describes how to view and understand the details of nested jobs displayed in the Automation log."
intercom_id: 11713623
---

# View the details of a nested job in the Automation Log

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super** **Admins** , and **Admins**
* Only supported using the Cerby web app


{% endhint %}

As a workspace **Owner** , **Super** **Admin** , or **Admin** , you can see the details of all nested jobs run in Cerby and displayed in the [Automation Log](https://help.cerby.com/en/articles/11642287-explore-the-automation-log).

A nested job contains more than one job involved in completing a task. You can identify a nested job in the Automation Log when the **View all jobs** button is displayed to the right of each log, as shown in **Figure 1**.

<img src="../../../../.gitbook/assets/AD_4nXfAIZ6zPscMdkaikwOYUSahElYIx87B23Bn0fFHn0NrMJbKZrVU-Q4QkcQigItWS25ZsJGrZdLYcPMdn5EV2n8kysQuUNRquTojwQwmm5va7xDM71df3tyEDoXrxpx8kZHS3_Czbg.png" alt="">

**Figure 1.** **View all jobs** button of nested logs

To view the details of a nested job in the Automation Log, you must complete the following steps:

1. Log in to your [Cerby](https://app.cerby.com/) workspace.
2. Select the **Automation Log** option from the left menu. The **Automation Log** page is displayed.
3. Click the **View all jobs** button to the right of a nested job log. A new browser tab is displayed with the following automation details:

   * **Status:** The status of the job
   * **Target:** The target of the job
   * **Task:** The task correlated to the job
   * **Created at:** The date and time when the job was triggered
   * **Updated at:** The date and time when the job was last updated

4. Click the **See details** button. The job details side drawer is displayed with the following information, as shown in **Figure 2** :

<img src="../../../../.gitbook/assets/AD_4nXfwVELaIl28YyvZlsdMoAmXL1l43dYjHdGtaTDrdgSrC0Fpu0NShBg0dZCkmuIo36yF6ZDGsAyokU34CGNHZ8dwMu7rPSkHL1-oknNLha1niGmOEwT5jHjP7ys2JYXdkuIlXNLG1w.png" alt="">

**Figure 2.** Automation job details side drawer of the **Automation details** page

The following is the information displayed:

* The current status of the job
* The job ID
* The service account associated with the job, if applicable
* The trigger that initiated the job

Now you are done.
