---
description: This article describes how to view the history and restore the secrets you've added or that you were granted shared access as Owner in Cerby
intercom_id: 8705415
---

# View the secret history and restore a secret

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* Secret **Owners**
* Available to the Cerby Automate and Cerby Protect products. Cerby Protect users must have already set up their [trusted devices](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/trusted-devices/set-up-trusted-sessions-on-your-devices)


{% endhint %}

To view the secret history and restore a secret to a previous version, you must complete the following steps using the Cerby web app:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Secrets** option from the left navigation drawer. The **Secrets** view is displayed.
  3. Click the **Settings** icon of the corresponding secret card. The secret details page is displayed with the **Settings** tab activated.
**NOTE:** If an identity challenge is configured, the **Confirm your identity to continue** dialog box is displayed. To confirm your identity, use one of [Cerby's multi-factor authentication methods](https://cerby-test.gitbook.io/cerby-test/management/identity-providers-idps/scim/set-up-your-identity-with-cerby-s-mfa-methods).

  4. Click the **Secret history** icon. The **Secret history** dialog box displays the history of the secret on the left pane.
​**NOTE:** Cerby registers the date and time when the secret details are modified and the user who edited the information.

  5. Select the date and time that corresponds to the version you want to restore. The secret details of the version are displayed on the right pane.
**IMPORTANT:** Attachment history is not supported.

  6. Click the **Restore** button. The dialog box closes, a success message box is displayed, and the secret details on the **Settings** tab are restored.
