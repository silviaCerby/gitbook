---
description: This article describes how to troubleshoot the disconnection between social media apps and management platforms after a password rotation.
intercom_id: 6843921
---

# [UNPUBLISHED] Troubleshooting: Reconnect social media management platforms after a password rotation

This document guides you on how to reconnect your social media management platforms and social media apps after a password rotation in Cerby.

## Cause of the problem

When you automatically rotate the password of a social media app account from Cerby, and the automation workflow does not detect the account is linked to a management platform, the accounts will be disconnected because a password change often invalidates all active sessions.

This disconnection happens whether the password rotation is triggered manually because of a security event such as user deprovisioning or suspicious activity, or automatically because of a security policy configured in Cerby by your **Workspace Admin**.

Currently, Cerby has automation workflows available for some social media apps to automatically reconnect them to management platforms after a password rotation. However, they may fail when the accounts are not properly configured.

**Table 1** shows the social media apps and management platforms that Cerby currently supports with automatic reconnection after a password rotation.

**Social media management platform**| **Twitter**| **Instagram**
---|---|---
Hootsuite| Yes| Yes
Sprinklr| Yes| Yes
Emplifi| Yes| Yes

**Table 1. Social Media Apps and Management Platforms Supported with Automatic Reconnection**

## Solution

To solve the disconnection issue, you have two options:

* [Automatic reconnection for supported apps](unpublished-troubleshooting-reconnect-social-media-management-platforms-after-a-password-rotation.md#id-automatic-reconnection-for-supported-apps)
* [Manual reconnection](unpublished-troubleshooting-reconnect-social-media-management-platforms-after-a-password-rotation.md#id-manual-reconnection)

The following sections describe the steps to complete for each option.

### Automatic reconnection for supported apps

For supported apps, as shown in **Table 1** , the Cerby Support team can help you configure your accounts to automatically reconnect your management platforms and social media apps after a password rotation. For us to do so, you must complete the following steps:

1. Add the supported social media management platform account to Cerby.
2. Contact the Cerby Support team to configure the supported social media app accounts in Cerby. You must provide the following information:

   * The name of your social media accounts in Cerby that are connected to the social media management platform.
   * The name of your social media management platform account in Cerby.

We will contact you when we complete the configuration.

### Manual reconnection

For apps not supported with automatic reconnection, you must perform this task manually.

Use the Cerby browser extension to help you copy and paste the new password of the social media account to update the password stored in the social media management platform.

If you want us to work on a specific automation workflow for reconnection, contact us at [support@cerby.com](mailto:support@cerby.com).
