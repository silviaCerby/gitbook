---
intercom_id: 6634083
description: >-
  This article describes how to add a host-guest partnership to share access to
  your accounts with external parties.
---

# Add a host-guest partnership

{% hint style="info" %}
**Who can use this feature?**

* Workspace**Admins** and **Users**
* Available to Cerby Automate
* Only supported using the Cerby web app
{% endhint %}

With Cerby, you have a secure and controlled way to collaborate with external parties through a [host-guest partnership](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-partners).

This feature helps you and your company support sharing access to accounts with members who don't belong to your domain (contractors, agencies, partners, vendors, or clients) while retaining complete control over these accounts and gaining visibility on their usage.

A host-guest partnership is a connection between existing host and guest workspaces managed by their respective **Admins**. This connection is established via a request sent from the host workspace and accepted by the guest workspace **Admin**.

{% hint style="danger" %}
**IMPORTANT:** A host workspace can have multiple host-guest partnerships. However, Cerby supports establishing only one partnership with the same guest workspace.
{% endhint %}

Any user from the host workspace can add this type of partnership, and they automatically become the **Partnership Owners** , a role that enables them to perform management tasks over the partnership.

When sharing an account with the guest workspace, **Partnership Owners** can assign one of two roles:

* **Collaborator:** With this role, guest workspace members can only log in to the shared accounts.
* **Manager:** With this role, guest workspace members can log in to the shared accounts and request access to these accounts for other members.

For more information about roles, read the article [How Cerby manages roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles).

This article describes how to add a host-guest partnership.

***

## Requirements

The following are the requirements to add a host-guest partnership:

* From the host workspace
  * An existing Cerby workspace
  * A Cerby account with any workspace-level role. For more information about roles, read the article [How Cerby manages roles](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/how-cerby-manages-roles).
  * The workspace ID of the guest workspace **TIP:** The workspace ID is located at the top-right corner of the **Partners** view in the dashboard of the guest workspace, as shown in **Figure 1**. The **Workspace Admin** from the guest workspace must share this ID beforehand with the host workspace user who will add the partner.

**Figure 1.** Workspace ID in the **Partners** view of the Cerby web app dashboard

<figure><img src="../../../../.gitbook/assets/X1fHfpu3CtpnBLAnR1H0H1bFKc5JhSRtyKLDbLtXp2JILZnTtBnstaTSfBDgB85Xk0kBZGvGjbJjypyVJpl-vYIgX3YoonLoEATLeOP3J-SOR6WiwwZmJi0dmCsIn5m6DMKq7uu-0vn7Y7tZAMsLd9Q.png" alt="Screenshot of the Cerby web app dashboard. The Partners view is displayed with a workspace ID and the Copy ID button highlighted at the top-right corner of the page"><figcaption></figcaption></figure>

* From the guest workspace
  * An existing Cerby workspace **IMPORTANT:** Contact the Cerby Customer Support team by sending an email to [support@cerby.com](mailto:support@cerby.com) or a message through the help chat of the Cerby dashboard to request the Partners feature and receive assistance in creating the guest workspace. You can also ask for the existing guest workspaces created by your organization
  * A Cerby account with the **Admin** role to accept the partnership request from the host workspace

***

## Add a host-guest partnership

As a user from the host workspace, regardless of your workspace-level role, you can add a host-guest partnership. The process involves sending a partnership request that must be approved and accepted by the corresponding **Admin** in the host and guest workspaces.

To add a host-guest partnership, you and your partners must complete the following main steps:

1. Send the partnership request
2. Approve the partnership request in the host workspace
3. Accept the partnership request in the guest workspace

The following sections describe each main step.

### 1. Send the partnership request

As a user from the host workspace, you must complete the following steps to send the partnership request:

1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
2. Select the **Partners** option from the left navigation drawer. The **Partners** view is displayed, as shown in **Figure 2**.

**Figure 2.** **Partners** view of the Cerby web app dashboard

<figure><img src="../../../../.gitbook/assets/BSheLRNFgj9-Uyga0pErjmwfwTpkLPmRcnosQWX4uH979gvAP1x9BHkn_oSLMUfFGWnVA-ARM7D4s68RVzRJTyyeGSEyjjDJYtqhQbhvFGUjVqbq9rG-MRC68OkQtdWo8Jy4MKvNQc_-RIhCBlTjLeE.png" alt="Screenshot of the Cerby web app dashboard. The Partners view is displayed with a message explaining this feature and the Add partner button"><figcaption></figcaption></figure>

3. Click the **Add partner** button. The **Invite your partners** dialog box is displayed with a description of the Partners feature. **NOTE:** A list of partners is displayed on the main panel of the **Partners** view when you already have access to any partnership. In this case, click the **Add** button.
4. Select the **Connect with another partner** option.
5. Click the **Next** button. The **Enter your partner's information** dialog box is displayed.
6. Enter the corresponding information in the following fields: **NOTE:** When an **Admin** adds a partner, the **Reason for request** field is not displayed.
   * **Workspace ID**
   * **Partner's email address**
   * **Reason for request**
7. Click the **Send request** button. The dialog box closes, a success message box is displayed, and an email is sent to the\*\*\*\* host workspace **Admin**. The details of the new partnership are also displayed on the main panel of the **Partners** view with the **Awaiting admin’s decision** state.

## **TIP:** If the host workspace **Admin** takes a long time to approve the request, you can click the **Send reminder** button to send a reminder. Also, if the guest workspace declines the partner request after the host workspace approval, you can click the **Resend request** button to send a new request.

The next step is 2. Approve the partner request in the host workspace.

{% hint style="info" %}
**NOTE:** When a host workspace **Admin** sends the partnership request, the approval is automatic, and they become the **Partnership Owner**. You can continue in step 3. Accept the partner request in the guest workspace.
{% endhint %}

### 2. Approve the partner request in the host workspace

As a host workspace **Admin** , you must complete the following steps to approve the partner request:

1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
2. Select the **Partners** option from the left navigation drawer. The **Partners** view is displayed with a list of partners in the **Your partners** section.
3. Select the partner from the list. The **Review partnership request** message is displayed in the **Accounts** tab with the **Decline request** and **Approve request** buttons. **TIP:** Click the **Learn more** button to display the partnership request details: the guest workspace id, the partner’s email address, and the reason for the request.
4. Click the **Approve request** button. A success message box is displayed, and an email is sent to the guest workspace **Admin** with the partner request. For the **Partnership Owner** , the details of the new partnership are also displayed on the main panel of the **Partners** view with the **Share accounts** button disabled.

The next step is 3. Accept the partner request in the guest workspace.

### 3. Accept the partner request in the guest workspace

As a guest workspace **Admin** , you must complete the following steps to accept the partner request:

1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
2. Select the **Partners** option from the left navigation drawer. The **Partners** view is displayed with the **Partnership request** message and the **Decline request** and **Accept request** buttons.
3. Click the **Accept request** button. The **Terms of Service** dialog box is displayed.
4. Select the **I confirm that I have read, consent, and agree to Cerby’s Terms of Service** option. The **Accept request** button is enabled.
5. Click the **Accept request** button. The dialog box closes, and a success message box is displayed.

{% hint style="info" %}
**NOTE:** Refresh the page in both the host and guest workspaces to update the host-guest partnership details. The **Share accounts** button in the host workspace is enabled.
{% endhint %}

Now you are done. It’s time to start using all the supported features of the host-guest partnership.

***

## Use the host-guest partnership

The following are the supported features of the host-guest partnership you can use:

* [Remove guest workspace members](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/partners/host-guest/remove-guest-workspace-members)
* [Share an account via a host-guest partnership](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/partners/host-guest/share-an-account-via-a-host-guest-partnership)
* [Manage access to accounts shared via a host-guest partnership](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/partners/host-guest/manage-access-to-accounts-shared-via-a-host-guest-partnership)
* [Log in to accounts shared via a host-guest partnership](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/partners/host-guest/log-in-to-accounts-shared-via-a-host-guest-partnership)
* [Request access to an account shared via a host-guest partnership](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/partners/host-guest/request-access-to-an-account-shared-via-a-host-guest-partnership)
* [Accept or decline an access request for an account shared via a host-guest partnership](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/partners/host-guest/accept-or-decline-an-access-request-for-an-account-shared-via-a-host-guest-partnership)
* [Remove a host-guest partnership](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/partners/host-guest/remove-a-host-guest-partnership)
* [Track activity on accounts shared via a host-guest partnership](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/user-management/partners/host-guest/track-activity-on-accounts-shared-via-a-host-guest-partnership)
