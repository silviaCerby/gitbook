---
description: "This article describes how the App setting restrictions feature enables you to enforce security policies directly in users’ web browsers."
intercom_id: 10276184
---

# Explore App setting restrictions

With Cerby, you can achieve more granular tracking and visibility into user, password, and account changes across your apps with our **App setting restrictions** feature.

In shared account scenarios, apps commonly don’t enable admins to restrict or control specific settings according to the users' roles and permissions. The **App setting restrictions** feature helps organizations improve security by encouraging employees to use Cerby rather than the app’s interface to manage users, update passwords, and delete accounts.

This feature enables you to implement either a recommendation-based (thereby reducing user friction) or a full block approach according to your organization's security policies. In any scenario, you can monitor compliance and take action on potential security risks.

As a workspace**Owner** , **Super Admin** , or **Admin** , you can manage and apply restrictions to the following settings directly in users’ web browsers:

* **Password settings:** Control how users configure and change account passwords, including changing, resetting, or updating the password within the app.
* **Member settings:** Control how users manage user access, roles, or permissions within the app.
* **Account deletion:** Control how users delete accounts within the app.

These restrictions give you control over how and where users can modify critical settings, helping to ensure the security and integrity of your accounts.

{% hint style="danger" %}


**IMPORTANT:** Any restriction applies only to workspace **Users** ; workspace **Owners** , **Admins** , and **Super** **Admins** are unaffected.


{% endhint %}

* * *

## How restrictions work

Workspace **Owners** , **Super Admins** , and **Admins** can only configure the app setting restrictions using the Cerby web app. The client app performing the restrictions on the app’s user interface is the Cerby browser extension.

{% hint style="danger" %}


**IMPORTANT:** For the feature to work correctly, users must have the Cerby browser extension installed and logged in. It is not available in the Cerby mobile app.


{% endhint %}

The following are the available restriction options for managing password, user, and account settings:

  * **Fully block:** Users cannot change the settings directly in the app because Cerby restricts interactions with the user interface. Any attempt to change the settings results in a notification informing the user that they do not have permission to make the change. Workspace**Admins** receive an email about blocked attempts, giving them visibility into restricted actions in the **Activity** view.
  * **Prompt to use Cerby:** Users are recommended to make changes through Cerby automation using the account and user management capabilities. However, they can still make updates directly in the app, including account deletion. Workspace **Admins** receive a notification about changes to the app settings.
  * **No restriction:** Users can change the settings directly in the app. Changes are not limited or monitored; users can modify their passwords and members, and delete accounts without intervention.
* * *

## User notifications

The following is the behavior for the different restriction settings when users attempt to make changes in the app:

  * **Full block** : Any modification attempt displays an error message in the app when a setting is fully blocked, as shown in **Figure 1.**

<img src="../.gitbook/assets/AD_4nXcpXX2h0-mX2YAXDEY5rfBM_WooymhgXM-qOqBA13ZhWKmf7wQFAOetVCy9tDIsEvRXaZ3kDjFfCX0TkHqifwgBEEcSdjlXP-ge082Ov8EA_TN8K4fS8Ms8mBep3Yvz8xO9kPYOgQ.png" alt="">

**Figure 1.** Error message displayed in the app when Cerby blocks users

  * **Prompt to use Cerby** : When users are prompted to use Cerby, any attempt to modify settings or delete an account will display an informational window, as shown in **Figure 2** , recommending users to configure the setting through Cerby or to avoid performing the action.

<img src="../.gitbook/assets/AD_4nXfaiXcSIMQMFiRFQitwVVUspwp3t_k5kzBZtLRoHjrlP7KQQm126J-iu_POe71M-8Za0iCmZTPxMHQjYC5tm3R-5Xk3pvgsG4bSq4x2BZQYz_czZph2Sx9OuzWSePQOxHWlzEdKlA.png" alt="">

**Figure 2.** Information message displayed in the app when the app settings are recommended to be modified through Cerby

* * *

## Supported apps

The following are the domains of the apps that support the App setting restrictions feature:

  * google.com
  * appbot.co
  * bitrise.io
  * mailchimp.com
  * make.com
  * ngrok.com
  * paypal.com
  * surveymonkey.com
  * developers.google.com/ads-data-hub
  * cloud.google.com/document-ai
  * acsense.com
  * meraki.com
  * explorium.ai
  * x.com
  * instagram.com
  * facebook.com
  * tiktok.com
  * bsky.app
  * pinterest.com
  * snapchat.com
* * *

## Related articles

The following articles contain more information about the App setting restrictions feature:

  * [Manage access to app settings](https://help.cerby.com/en/articles/10276318-manage-access-to-app-settings)
  * [Add settings restrictions to an app](https://help.cerby.com/en/articles/10276341-add-settings-restrictions-to-an-app)
  * [Edit an app settings restriction](https://help.cerby.com/en/articles/10276378-edit-an-app-settings-restriction)
  * [Customize the user message for setting restrictions](https://help.cerby.com/en/articles/10276389-customize-the-user-message-for-setting-restrictions)
  * [Remove apps from settings restrictions](https://help.cerby.com/en/articles/10276395-remove-apps-from-settings-restrictions)
