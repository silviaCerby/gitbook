---
description: This document describes how to get started with Cerby’s Identity Lifecycle Management (IdLCM) solution to connect your disconnected apps to Okta as your identity provider.
---

# Getting started with IdLCM integrations connected to Okta

Cerby’s IdLCM enables you to automate user provisioning, updates, and deprovisioning across all your Cerby-integrated apps. By acting as an intermediary between your IdP and your disconnected apps, IdLCM extends centralized identity and access governance by managing the joiner-mover-leaver (JML) lifecycle, ensuring that each user has the right access at the right time while maintaining policy compliance and operational efficiency.

This guide provides a step-by-step overview of how to enable and configure IdLCM for your organization:

  * Key concepts
  * How IdLCM works
  * Quick setup checklist
  * Steps to configure your IdLCM integration
  * Next steps
* * *

# Key concepts

**Table 1** contains key concepts that are useful for understanding the IdLCM solution:

**Concept**| **Description**
---|---
**Entitlement**|  It is a specific permission granted to a user or role to perform actions on a resource.  Entitlements dictate what a user can do, for example, read a file, modify a database record, or view customer data. These permissions can be granted or denied.
**External app**|  It is a third-party app or service provider that relies on Cerby to manage the lifecycle of enterprise identities. Access to these apps is governed by users’ licenses or seats.
**Integration**|  It is the entity that represents the SCIM gateway configuration for an external app within Cerby.
**SCIM gateway**|  It is the intermediary that transmits SCIM messages or information between two or more SCIM-enabled systems, facilitating the exchange of user identity and attribute data. It also exposes a SCIM interface consisting of a set of standard endpoints on top of a system that doesn’t natively support the SCIM protocol. Being a gateway implies it performs "protocol translation," not only proxying of messages.
**Service account**|  It is a user account intended for managing the external app or service provider. Service accounts are used for machine-to-machine operations.  These accounts are added to Cerby and associated with an integration to execute automated user management tasks.
**Disconnected app**|  It is an app or service provider that doesn’t integrate with identity management systems or follow standard authentication protocols and security standards. Commonly, these apps lack API integrations for user management.

**Table 1.** IdLCM key concepts

* * *

# How IdLCM works

Cerby’s IdLCM solution enables disconnected apps to function like standard SCIM-compliant apps by automatically creating a SCIM gateway when you set up an integration. This gateway acts as the communication layer between your IdP and the external app, ensuring that provisioning and deprovisioning events are automatically reflected.

Upon receiving a lifecycle event from your IdP, the SCIM gateway reviews the request, verifies that the operation can be performed by the requesting party, and processes the operation. Cerby then triggers the automation job to perform the corresponding provisioning, updating, or deprovisioning actions within the integrated app.

For disconnected apps, it's essential to establish a dedicated **service account or token** so Cerby can securely access the app and perform user and access management automatically.

**Figure 1** shows how Cerby’s IdLCM integration connects your IdP and disconnected apps to enable full lifecycle automation.

<figure><img src="../.gitbook/assets/5baafbb1-30d2-410e-ba43-ab693288c258.png" alt=""><figcaption></figcaption></figure>

**Figure 1.** Sequence diagram of a disconnected app connected to an IdP through an IdLCM integration

The sequence diagram illustrates the following steps:

  1. A lifecycle event (joiner, mover, or leaver) is triggered in Okta, prompting a SCIM event to be sent to Cerby.
  2. Cerby, through the IdLCM integration, receives the event, reviews it, and processes the request.
  3. Cerby then triggers an automation job to apply the corresponding provisioning, update, or deprovisioning changes in the disconnected app.
  4. The result of the automation job is reported back to Cerby for tracking and visibility.

* * *

# Quick setup checklist

Use the checklist in **Table 2** as your guide for setting up and connecting your IdLCM integration.

**Step**| **Action**| **Description**
---|---|---
0| **Prerequisites**|  Verify that you meet all prerequisites for your Cerby workspace, Okta tenant, and disconnected app.
1| **Create a service account**|  Create a service account in your external app with admin privileges and save it in Cerby.
2| **Create an IdLCM integration in Cerby**|  Create an IdLCM integration for your external app in Cerby.
3| **Retrieve the SCIM gateway details**|  Retrieve the following values from Cerby: SCIM gateway URL, SCIM gateway token, and bookmark URL.
4| **Create an Okta app integration**|  Create and set up an app integration in Okta connected to your IdLCM integration.
5| **Sync users, roles, and entitlements from your app to Cerby**|  Identify and sync users, roles, and entitlements from your app to Cerby.
6| **Import users, roles, and entitlements from Cerby into your IdP**|  Import users, roles, and entitlements from an IdLCM integration into Okta.

**Table 2.** Setup checklist for an IdLCM integration

* * *

# Steps to set up your IdLCM integration

Complete the following steps to add, set up, and connect your IdLCM integration using Okta as your identity provider.

## Step 0. Prerequisites

Before setting up your IdLCM integration, verify that the following prerequisites are met:

  * A Cerby workspace
  * A Cerby user account with the workspace **Owner** , **Super Admin** , or **Admin** role
  * A collaboration space (workspace, team, or dashboard) in your external app
  * The user management and login method for your integration identified. Depending on your app, the options might be the following:
    * Username and password
    * Single sign-on (SSO) with your IdP
    * Access token
  * A business or organization ID. Commonly, you can find the ID in the following ways:
    * **From the address bar:** After you log in to your app, sometimes the ID is displayed in the address bar as part of the URL, either in the subdomain, path, or an ID parameter. For example:
      * **`123456890`** in **`https://business.app.com/settings/&business_id=1234567890`**
      * **`contentzilla`** in **`https://contentzilla.app.com/`**
    * **From the business information or settings:** When you are logged in to your app, go to the settings or business information page. The ID is usually displayed in an information section for you to copy.

**NOTE:** Not all IdLCM integrations require a business or organization ID; Cerby displays an input field when applicable to your app. For more information, read the article [Retrieve the Business ID to connect your disconnected apps to Cerby.](https://help.cerby.com/en/articles/12335748-retrieve-the-business-id-to-connect-your-disconnected-apps-to-cerby)****

  * An Okta tenant
  * A user account in Okta with privileges to manage an app integration in your Okta tenant

## Step 1. Create a service account

Create an admin-level service account that Cerby can use to access your apps for identity and access lifecycle management purposes.

For instructions and recommendations on how to create this account, read the article [Create a service account for your IdLCM integration](https://help.cerby.com/en/articles/11641977-create-a-service-account-for-your-idlcm-integration).

## Step 2. Create an IdLCM integration in Cerby

Create an IdLCM integration in Cerby to connect your disconnected app and associate it with your service account.

For instructions on how to create an IdLCM integration, read the article [Create an IdLCM integration for your app](https://help.cerby.com/en/articles/11650659-create-an-idlcm-integration-for-your-app).

## Step 3. Retrieve the SCIM gateway details

Copy the SCIM gateway URL, SCIM gateway token, and bookmark URL from your IdLCM integration. These details are required when configuring your Okta app integration.

For instructions on how to retrieve the SCIM gateway details, read the article [Retrieve the SCIM gateway token and URL for an IdLCM integration](https://help.cerby.com/en/articles/11642821-retrieve-the-scim-gateway-token-and-url-for-an-idlcm-integration).

## Step 4. Create an Okta app integration

In your Okta Admin Console, create a new app integration and configure it using the Cerby SCIM gateway URL, SCIM gateway token, and bookmark URL. With this app integration, Okta can send lifecycle events to Cerby automatically.

For instructions on how to create and set up an app integration in Okta, read the article [Create and set up an app integration in Okta connected to IdLCM](https://help.cerby.com/en/articles/11643251-create-and-set-up-an-app-integration-in-okta-connected-to-idlcm).

## Step 5. Sync users, roles, and entitlements from your app to Cerby

Import users, roles, and entitlements from your app into Cerby to establish an accurate baseline.

For instructions on how to sync the users, roles, and entitlements from your app to Cerby, read the article [Sync users, roles, and entitlements from your external app to Cerby](https://help.cerby.com/en/articles/11648869-sync-users-roles-and-entitlements-from-your-external-app-to-cerby).

## Step 6. Import users, roles, and entitlements from Cerby into your IdP

Sync users, roles, and entitlements data from Cerby into Okta to ensure both systems are aligned.

For instructions on how to import users, roles, and entitlements from an IdLCM integration into Okta, read the article [Import users, roles, and entitlements from an IdLCM integration into Okta](https://help.cerby.com/en/articles/11647808-import-users-roles-and-entitlements-from-an-idlcm-integration-into-okta).

* * *

# Next steps

Your IdLCM integration is now connected to Okta. You can now manage user provisioning, updates, and deprovisioning for your disconnected app directly from Okta.

The following are the supported tasks and features that help you make the most of your integration and maintain efficient, secure user management through Cerby:

  * **Manage user access**
    * [Provision users to your app via an IdP and IdLCM integration](https://help.cerby.com/en/articles/11644874-provision-users-to-your-app-via-an-idp-and-idlcm-integration)
    * [Update user assignments in your app via an IdP and IdLCM integration](https://help.cerby.com/en/articles/11645015-update-user-assignments-in-your-app-via-an-idp-and-idlcm-integration)
    * [Deprovision users from your app via an IdP and IdLCM integration](https://help.cerby.com/en/articles/11645058-deprovision-users-from-your-app-via-an-idp-and-idlcm-integration)
  * **Monitor your users**
    * [Monitor IdLCM integration events in the Activity tab](https://help.cerby.com/en/articles/11649369-monitor-idlcm-integration-events-in-the-activity-tab)
    * [View the users of an IdLCM integration](https://help.cerby.com/en/articles/11644266-view-the-users-of-an-idlcm-integration)
  * **Advanced configuration options**
    * [View the entitlements in your IdLCM integration](https://help.cerby.com/en/articles/12454982-view-the-entitlements-in-your-idlcm-integration)
    * [Export the entitlement assignments of your IdLCM integration](https://help.cerby.com/en/articles/12454975-export-the-entitlement-assignments-of-your-idlcm-integration)
    * [Configure the sync safeguard threshold of your IdLCM Integration](https://help.cerby.com/en/articles/12313222-configure-the-sync-safeguard-threshold-of-your-idlcm-integration)
