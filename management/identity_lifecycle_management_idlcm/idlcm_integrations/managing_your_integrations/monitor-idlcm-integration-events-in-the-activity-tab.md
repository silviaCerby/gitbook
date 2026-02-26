---
description: "This article describes how to monitor the IdLCM integration events in the Activity tab"
intercom_id: 11649369
hidden: true
noIndex: true
---

# Monitor IdLCM integration events in the Activity tab

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners, Super Admins,** and**Admins**
* Only supported using the Cerby web app


{% endhint %}

As a workspace**Owner, Super Admin,** or**Admin,** you**** can access a comprehensive audit log with full provisioning event details of an IdLCM integration.

The **Activity** tab, as shown in **Figure 1** , is a read-only log that tracks all changes within an integration. It displays events related to user and group management, SCIM gateway operations, and setup tasks to simplify auditing, tracing, and troubleshooting.

<img src="../../../../../.gitbook/assets/image_7.png" alt="">

**Figure 1.** **Activity** tab in the integration details page

The**Activity** tab provides information about integration events in the following columns:

  * **Date:** It is the date and time at which the event was triggered.
  * **Actor:** It is the entity that triggered the event.
  * **Event:** It is the name of the event that was triggered. For the complete list of events and their description, read the [Integration events](monitor-idlcm-integration-events-in-the-activity-tab.md#integration-events) section.
  * **Target:** It is the entity affected by the event.
* * *

## Integration events

The following table lists the events you can view in the **Activity** tab, along with their descriptions

**Event**| **Description**
---|---
**Service account events**|
Service account created| A service account was associated with the integration.
Service account removed| A service account was removed from the integration.
Service account updated| The service account associated with the integration was updated.
**User invite events**|
User invite requested | A request to provision a user in the external app was received.
User invite in progress | An automation job to provision a user in the external app is in progress.
User invited| A user was successfully provisioned in the external app via an automation job.
User invite failed| The automation job to provision a user in the external app failed.
**User update events**|
User update requested| A request to update user attributes in the external app was received.
User update in progress| An automation job to update user attributes in the external app is in progress.
User updated| The user attributes were successfully updated in the external app via an automation job.
User update failed| The automation job to update user attributes in the external app failed.
**User removal events**|
User removal requested| A request to deprovision a user from the external app was received.
User removal in progress| An automation job to deprovision a user from the external app is in progress.
User removed| A user was successfully deprovisioned from the external app via an automation job.
User removal failed| The automation job to deprovision a user from the external app failed.
**SCIM gateway events**|
SCIM integration connected| A SCIM gateway instance was created and associated with an integration.
SCIM integration health check triggered| An automation job to check the health of the SCIM gateway is in progress.
SCIM integration health validated| The SCIM gateway health check was successful.
