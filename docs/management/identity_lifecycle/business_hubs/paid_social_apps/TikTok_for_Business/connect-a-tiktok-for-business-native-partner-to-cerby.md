---
description: "This article describes how to connect a TikTok for Business partner to gain visibility on the users with shared access to your assets."
intercom_id: 9082765
---

# Connect a TikTok for Business native partner to Cerby

With Cerby, you can connect a TikTok for Business [native partner](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-partners) to your workspace to gain visibility on the partner’s users with shared access to your assets.

This connection is established via a monitor account with admin access to your partner’s TikTok Business Center and connected to the Cerby Asset Manager app.

{% hint style="info" %}


**NOTE:** Cerby recommends creating a dedicated account in TikTok for Business (not assigned to a specific user) to monitor the partner’s business center from Cerby. Preferably, set it up with a Cerby-managed email address and phone number.


{% endhint %}

It’s worth noticing that the Cerby Asset Manager app has only read-access permissions to your partner’s TikTok Business Center. Therefore, after you add the native partner to Cerby, you can use our API and agent-based integration to sync and import your partner’s user data.

{% hint style="danger" %}


**IMPORTANT:** You can only add a native partner in Cerby if you have shared at least one asset with a partner in your paid social app or vice versa.

For security purposes, Cerby recommends that you invite the admin who will create the monitor account as a **Guest User** of your workspace. That way, they can securely share the credentials with you via a Cerby account.


{% endhint %}

This article describes how to connect a TikTok for Business native partner to Cerby.

* * *

## Requirements

The following are the requirements to add a TikTok for Business native partner to Cerby:

  * A Cerby account
  * A TikTok Business Center integration in Cerby. For more information and instructions, read the article [Add a TikTok Business Center integration](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/paid-social-apps/tiktok-for-business/connect-a-business-hub-for-tiktok-business-center)
  * A partner in TikTok for Business with shared access to your assets
  * An admin from your partner’s side must have already joined your Cerby workspace as a **Guest User**. For more information and instructions, read the article [How to invite a guest user to your workspace ](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-guest-users)
  * Your assets isolated into a single TikTok Business Center (optional)

  **NOTE:** Cerby recommends your partner isolate your shared assets to avoid syncing and importing information from other organizations or customers

  * An active TikTok for Business account with the **Admin** role on your partner’s TikTok Business Center
* * *

## Connect a TikTok for Business native partner to Cerby

To connect a TikTok for Business native partner to Cerby, you and your partner must complete the following main steps:

  1. [Partner setup in TikTok for Business](connect-a-tiktok-for-business-native-partner-to-cerby.md#id-1.-partner-setup-in-tiktok-for-business)
  2. [Native partner connection in Cerby](connect-a-tiktok-for-business-native-partner-to-cerby.md#id-2.-native-partner-connection-in-cerby)

The following sections describe each main step.

### 1\. Partner setup in TikTok for Business

Your partner must complete the following steps in TikTok for Business to set up the connection to Cerby:

  1. Create an account with **Admin** access settings to the TikTok Business Center with the isolated shared asset. For instructions, read the article [Add Users to TikTok Business Center](https://ads.tiktok.com/help/article/add-users-tiktok-business-center?lang=en#anchor-3).

  **NOTE:** Preferably, set this account up with a Cerby-managed email address and phone number, as well as a secure password provided by your partner.

  2. Add the account to Cerby and share it with your partner.

Now, your partner is done. The next step is [2. Native partner connection in Cerby](connect-a-tiktok-for-business-native-partner-to-cerby.md#id-2.-native-partner-connection-in-cerby) that you must complete using the Cerby web app.

### 2\. Native partner connection in Cerby

You must complete the following steps in Cerby to connect with your TikTok for Business native partner:

  1. [Connect the native partner to Cerby](connect-a-tiktok-for-business-native-partner-to-cerby.md#id-1.-connect-the-native-partner-to-cerby)
  2. [Sync and review your partner’s users](connect-a-tiktok-for-business-native-partner-to-cerby.md#id-2.-sync-and-review-your-partners-users)

The following sections describe each step.

#### 1\. Connect the native partner to Cerby

To connect the native partner to Cerby, you must complete the following steps:

  1. Log in to your [Cerby](http://app.cerby.com) workspace.
  2. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.
  3. Click the corresponding app card. The app details page is displayed.
  4. Activate the **Partners** tab.
  5. Activate the **TikTok Business Partners** tab from the **Partners** section. A list of partners with shared access to your assets is displayed.

  **NOTE:** If your partner exists in your TikTok Business Center but is not displayed in the **TikTok Business Partners tab** in Cerby, perform a check for updates to sync and import their user data.

  6. Click the **More options** icon from the corresponding partner, which has a “Pending Cerby onboarding” status. A drop-down list is displayed.
  7. Select the **Connect to Cerby** button. The **Connect your partner token** dialog box is displayed.
  8. Click the **Get started** button. The **Grant access to the Cerby app** dialog box is displayed.
  9. Click the **Next** button. One of the following scenarios occurs depending on whether you have an active session or not in TikTok for Business with your web browser:

     * If you have an active session, the **App Authorization | TikTok For Business** pop-up window is displayed.

       1. Continue in step 10.

     * If you don’t have an active session, the TikTok for Business login page is displayed.

       1. Log in to TikTok for Business by entering the credentials of the monitor account. The **App Authorization | TikTok For Business** pop-up window is displayed.
       2. Continue in step 10.
  10. Click the **Confirm** button. The pop-up window closes, and the app details page and a success message box are displayed.

The next step is [2. Sync and review your partner’s users](connect-a-tiktok-for-business-native-partner-to-cerby.md#id-2.-sync-and-review-your-partners-users), which you must complete from the app details page in Cerby.

#### 2\. Sync and review your partner’s users

To sync and review your partner’s users, you must complete the following steps from the app details page in Cerby:

  1. Click the **Check for updates** button located at the top right of the app details page. The process to sync and import to Cerby the partner’s user data may take a few seconds.

  **NOTE:** You can review the progress of the check for updates through the **Automation** view. When the corresponding automation task has the “Complete” status, you can continue to step 2.

  2. Activate the **Members** tab from the app details page.
  3. Activate the **TikTok Business guest users** tab from the **User Overview** section. A table with the partner’s users is displayed.

Now you’re done. In subsequent checks for updates, you can retrieve the updated information from your partner’s users.
