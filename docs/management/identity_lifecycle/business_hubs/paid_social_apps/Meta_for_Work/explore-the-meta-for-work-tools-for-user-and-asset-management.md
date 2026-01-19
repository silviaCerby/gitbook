---
description: "This article describes the Meta for Work tools available to manage user access and your business assets and how they relate to Cerby."
intercom_id: 8958757
---

# Explore the Meta for Work tools for user and asset management

The **Meta for Work** tools comprise a suite of online collaboration, knowledge sharing, and communication services and devices for organizations. **Meta Work Accounts** and **Meta Business Manager** are part of these tools, and they enable you to manage user access and business assets in your Meta for Work ecosystem.

With **Meta Work Accounts** , you can provide a **single sign-on (SSO)** authentication solution for your suite of productivity tools, allowing employees to use their work credentials instead of personal Facebook profiles to streamline access to multiple Meta applications. Additionally, you can set up automatic user provisioning from your **identity provider (IdP)** via the **System for Cross-Domain Identity Management (SCIM)** standard.

**Meta Business Manager** is the central hub where you can manage your business activities, external online presence, and assets (ad accounts, pages, and pixels) on Meta platforms like Facebook, Instagram, WhatsApp, Messenger, and Audience Network. Using the Business Manager platform, you can create and run ads, manage business pages, analyze insights, and connect with your audience across the Meta ecosystem.

Cerby customers can leverage both of these tools to improve collaboration and centrally manage user access to a **Meta Business Manager** and their corresponding assets.

Using an **API** and **agent-based integration** , you can connect your **Meta Business Manager** to your Cerby workspace to import your user data (assets, roles and permissions, and members) and perform the following user management tasks from Cerby:

* Identify, sync, and import all users of a Meta Business Manager, including partners, and their roles to Cerby.
* Change the roles of your Meta Business Manager users from Cerby.
* Invite new users to join Meta Business Manager through Cerby.
* Remove Meta Business Manager users from Cerby.

For more information about this integration, read the article [How to add a Meta Business Center integration](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/paid-social-apps/meta-business-manager/connect-a-business-hub-for-meta-business-manager).

When you use **Meta Work Accounts** , you can independently provision and deprovision users from your Meta ecosystem and Cerby because these access management actions are triggered directly from the corporate directory managed by your IdP, such as Oka or Entra ID (formerly Azure AD).

However, you can still connect your **Meta Business Manager** to Cerby to perform the user management tasks mentioned above.

{% hint style="danger" %}


**IMPORTANT:**[Meta for Work](https://forwork.meta.com/), released in July 2023 for beta testing, is being transitioned by some organizations to replace personal Facebook profiles as the default login for Meta Business Manager.

Note that this feature is currently available to **selected customers only**. For more information or to inquire about eligibility, please contact your Meta support representative.


{% endhint %}

The following scenarios apply depending on your decision to transition to Meta Work Accounts or not:

  * **Existing customers transitioning to** **Meta Work Accounts**
    * When you complete the transition, the old personal Facebook profiles will be replaced with Meta Work Accounts, meaning users will now use their work credentials to log in to Meta Business Manager.
    * Whenever you perform a check for updates manually or via a policy check, the Meta Work Accounts will be matched automatically to their corresponding Cerby account.
    * Automatic user provisioning and deprovisioning will happen between the IdP and Meta, decentralized from Cerby. The rest of the user management tasks supported by Cerby’s Meta Business Center integration will remain the same.
  * **Existing customers not transitioning to Meta Work Accounts**
    * Meta Business Manager users will continue logging in with their personal Facebook profiles.
    * The user management tasks supported by Cerby’s Meta Business Center integration will remain the same.
    * Automatic user provisioning and deprovisioning will happen between the IdP and Cerby, and these actions will propagate to Meta.
  * **New customers with Meta Work Accounts already implemented:**
    * When connecting your Meta Business Manager to Cerby and checking for updates, Cerby will sync and import your user data and automatically match the users’ work credentials with their corresponding Cerby account.
    * Automatic user provisioning and deprovisioning will happen between the IdP and Meta, decentralized from Cerby. The rest of the user management tasks supported by Cerby’s Meta Business Center integration will be supported.
* * *

## Related articles

The following articles contain more information about how to use the Meta for Work tools as an admin or end user:

* [Meta for Work tools for admins](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/paid-social-apps/meta-for-work/meta-for-work-tools-for-admins)
* [Meta for Work tools for end users](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/paid-social-apps/meta-for-work/meta-for-work-tools-for-end-users)
