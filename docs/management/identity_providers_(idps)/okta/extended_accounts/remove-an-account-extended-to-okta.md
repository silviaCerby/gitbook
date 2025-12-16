---
intercom_id: 9759128
description: >-
  This article describes how to remove an account previously synced and extended
  to your Okta dashboard.
---

# Remove an account extended to Okta

{% hint style="info" %}
**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* Account**Owners**
* Only supported using the Cerby web app
{% endhint %}

As an account **Owner** who has synced and [extended an account to Okta](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-extended-account-access), you can remove it.

{% hint style="danger" %}
**IMPORTANT:** You must have the **Owner** role on the extended account you want to remove. By removing an extended account, the following happens:

* The corresponding chiclet is removed from the Okta dashboard for all workspace members and teams with shared access as **Owners** or **Collaborators** to the Cerby account.
* The account and its access permissions are not affected in Cerby.
{% endhint %}

To remove an account synced and extended to Okta, you must complete the following steps:

1. Log in to your [Cerby](https://app.cerby.com/) workspace using your web browser.
2. Click the corresponding account card. The account details page is displayed.
3. Expand the**Connected services and apps** section.
4.  Click the **More options** (

    <figure><img src="../../../.gitbook/assets/unnamed_13.png" alt=""><figcaption></figcaption></figure>

    ) icon. A drop-down list is displayed.
5. Select the **Remove from Okta** option from the list. The **Remove extended account?** dialog box is displayed.
6. Click the **Yes, remove extended account** button. The dialog box closes, and Cerby starts removing your account from Okta.

Now you are done.
