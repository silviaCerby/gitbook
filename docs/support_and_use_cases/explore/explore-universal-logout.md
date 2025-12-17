---
description: "This article describes the benefits of Cerby Universal Logout and Okta’s Universal Logout through Cerby."
intercom_id: 10495600
---

# Explore Universal Logout

With Cerby Universal Logout, you can rapidly terminate user access when security or operational needs arise. With a single action, workspace administrators can ensure that a user no longer has access to accounts protected and managed through Cerby. This feature protects sensitive information, supports incident response procedures, and helps maintain a clean and compliant access environment.

Universal Logout is designed to work seamlessly across identity providers and Cerby's supported application ecosystem, allowing teams to take decisive action when needed.

* * *

## Key benefits

The following are the main benefits of using Cerby Universal Logout:

  * **Unified access revocation:** End-user access to accounts managed through Cerby is terminated through a single, centralized control.
  * **Consistent security response:** Administrators can take immediate action without needing to manage each application individually when access needs to be removed for operational events.
  * **Integrated with Okta:** Universal Logout can be initiated directly from identity providers (IdPs) or a Cerby workspace, depending on your organization's setup.
  * **Compliance and governance support:** Helps teams maintain strong access hygiene and reduces exposure from accounts that may otherwise remain active unintentionally.
* * *

## How Universal Logout works

Cerby Universal Logout operates across the Cerby platform and connected identity ecosystems to terminate access efficiently and consistently. The following happens when triggered:

  * The user’s active access across Cerby-supported surfaces is terminated.
  * Cerby coordinates secure access changes across the applications that the user can access through the platform.
  * Administrators are informed of the action to support transparency and governance.

Cerby aligns with identity best practices by respecting IdP-initiated logout signals and organizational lifecycle events. Universal Logout can be initiated from Cerby or, when configured, from your IdP’s administrative interface.

* * *

## When to use Universal Logout

Universal Logout is recommended for scenarios such as:

  * **Security risk events:** When organizations have concerns about a compromised or misused user account.
  * **Employee or contractor offboarding:** When users leave the organization or transition out of access roles.
  * **Access hygiene reviews:** During cleanup efforts or compliance activities.
  * **Centralized incident response:** When rapid action is required across multiple applications.
* * *

## Who can trigger Universal Logout

Users with elevated administrative authority, such as the following roles, can trigger universal Logout:

  * Workspace **Owners**
  * Workspace **Super Admins**
  * Workspace **Admins**
  * IdP administrators (when configured)

The goal is to ensure only trusted roles can initiate access revocation actions.

* * *

## Triggering Universal Logout from Cerby

Administrators can initiate Universal Logout directly from the Cerby workspace. The action is available in the workspace’s user management area, allowing teams to select a user and initiate the logout process.

Cerby provides clear confirmation prompts to ensure administrators understand the impact of their actions before they are executed.

* * *

## Triggering Universal Logout from IdPs

For organizations that integrate Cerby with IdPs, Universal Logout can also be initiated from the IdP’s administrative console. This capability enables teams to incorporate Cerby into their identity-centric workflows and lifecycle management processes.

For example, when a logout or access revocation action is triggered from your IdP for a user, Cerby will participate in that workflow and enforce logout for the corresponding accounts managed through Cerby.

* * *

## Visibility and notifications

After Universal Logout is initiated, the following occurs at a high level:

  * Workspace administrators are notified that an access revocation event has occurred.
  * Cerby records the action for visibility and governance.
  * The workspace’s audit and monitoring tools will reflect the change, supporting compliance and reporting needs.
* * *

## Related articles

The following articles contain more information about the Universal Logout feature:

  * [Trigger Cerby Universal Logout](https://cerby-test.gitbook.io/cerby-test/management/security-and-policy/universal-logout/trigger-cerby-universal-logout)
  * [Enable Okta Universal Logout for Cerby](https://cerby-test.gitbook.io/cerby-test/management/security-and-policy/universal-logout/enable-okta-universal-logout-for-cerby)
  * [Trigger Okta Universal Logout and extend it to Cerby](https://cerby-test.gitbook.io/cerby-test/management/security-and-policy/universal-logout/trigger-okta-universal-logout-and-extend-it-to-cerby)
