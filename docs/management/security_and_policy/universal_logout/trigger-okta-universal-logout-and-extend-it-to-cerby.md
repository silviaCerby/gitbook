---
description: This article describes how to trigger Okta Universal Logout from the Okta Dashboard and extend it to Cerby.
intercom_id: 10495624
---

# Trigger Okta Universal Logout and extend it to Cerby

{% hint style="info" %}


**Who can use this feature?**

* Okta **Admins**
* Available from your organization’s Okta Admin Dashboard


{% endhint %}

As an Okta**Admin** , you can trigger Okta Universal Logout for a specific user from the Okta Admin Dashboard. This action can be extended to Cerby, triggering Cerby Universal Logout, which terminates the user’s sessions and tokens in their Cerby-assigned apps.

{% hint style="danger" %}


**IMPORTANT:** Users must be provisioned from Okta for the Universal Logout feature to work.


{% endhint %}

To trigger Cerby’s Universal Logout from Cerby, you must complete the following steps:

  1. Log in to your organization's[ Okta Admin Console](https://developer.okta.com/login/).
  2. Select the **People** option under the **Directory** drop-down from the left navigation drawer. The **People** page is displayed.
  3. Select the user whose session you want to terminate.
  4. Click the **More actions** button. A drop-down menu is displayed.
  5. Select the **Clear User Sessions** option. The **Clear sessions and revoke access** dialog box is displayed, confirming that all of the user’s sessions and tokens will be revoked for the apps assigned to them in Okta.
  6. Select the **Also include logout enabled apps and Okta API tokens** checkbox, as shown in **Figure 1**.
​

​**Figure 1.** **Clear sessions and revoke access** dialog box
**IMPORTANT:** You must select this option to extend Okta’s Universal Logout to Cerby.

<figure><img src="../../../../.gitbook/assets/Screenshot_2025-01-31_at_4.19.13_3Fp.m..png" alt=""><figcaption></figcaption></figure>

  7. Click the **Clear and revoke** button to trigger Okta’s Universal Logout and extend it to Cerby. The user’s sessions and tokens are revoked not only for their assigned apps in Okta but also for their Cerby client apps.

Now you are done.
