---
description: "This article describes how to maximize your account security by completing Cerby's configuration milestones."
intercom_id: 6591141
---

# Configure your accounts with the highest security level

Cerby is the identity automation platform purpose-built to secure disconnected apps that fall outside the reach of traditional identity security tools.

By automating manual security tasks, such as rotating passwords and turning on multi-factor authentication (MFA), Cerby extends governance across your entire ecosystem and empowers your organization to implement zero trust principles for every account.

In addition to saving you time by letting you access the apps you use for your work, our automated tasks help you enforce security best practices before misconfigurations become breaches.

This article describes the benefits of fully configuring your accounts in Cerby and the milestones required to reach the highest level of automated security.

A fully configured account in Cerby involves completing the following milestones:

1. [Ensure the account credentials are correct](configure-your-accounts-with-the-highest-security-level.md#id-1.-ensure-the-account-credentials-are-correct)
2. [Configure your account with an email address managed by Cerby](configure-your-accounts-with-the-highest-security-level.md#id-2.-configure-your-account-with-an-email-address-managed-by-cerby)
3. [Turn on MFA managed by Cerby](configure-your-accounts-with-the-highest-security-level.md#id-3.-turn-on-mfa-managed-by-cerby)
4. [Share the account with collaborators](configure-your-accounts-with-the-highest-security-level.md#id-4.-share-the-account-with-collaborators)
5. [Rotate passwords automatically in Cerby](configure-your-accounts-with-the-highest-security-level.md#id-5.-rotate-passwords-automatically-in-cerby)

The following sections describe each milestone.

* * *

## 1\. Ensure the account credentials are correct

The foundation of Cerby’s automation is the accuracy of your stored login credentials. When your username and password are correct, Cerby can execute its primary security feature: automated login.

That is why, from the moment you add or save an account in Cerby, you must always ensure that the login credentials are correct. Any discrepancy will prevent you from accessing your account through any of the Cerby client apps and from using other supported automated tasks to protect your account, such as rotating passwords or enabling MFA.

To verify your account credentials, just log in to your account through any of the following methods available in the Cerby client apps:

  * **Automatic:**
    * [Log in to an account automatically using the Cerby web app](https://help.cerby.com/en/articles/13747818-log-in-to-an-account-automatically-using-the-cerby-web-app)
    * [Log in to an account automatically using the Cerby browser extension](https://help.cerby.com/en/articles/13747959-log-in-to-an-account-automatically-using-the-cerby-browser-extension)
  * **Assisted or manual:**
    * [Log in to an account manually using the Cerby web app](https://help.cerby.com/en/articles/13747835-log-in-to-an-account-manually-using-the-cerby-web-app)
    * [Log in to an account manually using the Cerby browser extension](https://help.cerby.com/en/articles/13748025-log-in-to-an-account-manually-using-the-cerby-browser-extension)
    * [Log in to an account using the Cerby mobile app](https://help.cerby.com/en/articles/11139221-log-in-to-an-account-using-the-cerby-mobile-app)
* * *

## 2\. Configure your account with an email address managed by Cerby

To move beyond unmanageable accounts, Cerby recommends securing the recovery and identity loop. By associating a Cerby-managed email address or phone number with your account, you improve the login process while ensuring compliance with corporate security policies.

The following are the benefits of configuring these contact details in your account:

  * **Centralized verification:** Cerby receives security alerts and recovery codes and makes them available to all users with shared access to the account.
  * **Streamlined secure access:** When used as MFA verification methods, Cerby retrieves verification codes sent to the Cerby-managed email address or phone number and fills them into input fields during automated logins. For more information, read the [3\. Turn on Cerby-managed MFA](https://docs.google.com/document/d/1ycibUgsll-2G1VZ3NSXlmkbgx1GV2MLHL7Ovn8VmqAE/edit?tab=t.0#heading=h.f9q6jqemdxoe) section.
  * **Continuity of access:** Because accounts are tied to the organization rather than an individual, your organization retains control of the account identity even if a team member is unavailable or leaves the company.

For more information, read the articles [Set up and associate a Cerby-managed email address for your account](https://help.cerby.com/en/articles/11888658-set-up-and-associate-a-cerby-managed-email-address-for-your-account) and [Set up and associate a Cerby-managed phone number for your account](https://help.cerby.com/en/articles/11889035-set-up-and-associate-a-cerby-managed-phone-number-for-your-account).

* * *

## 3\. Turn on MFA managed by Cerby

MFA is a critical pillar of zero trust. According to Microsoft, 99.9% of the compromised accounts it tracks daily don’t have MFA enabled.

Cerby transforms MFA from a manual bottleneck into an automated background process, ensuring that security never comes at the cost of productivity.

Whenever supported by your app, Cerby recommends using the authenticator app as the primary MFA method so that Cerby generates and manages time-based one-time passwords (TOTPs) for your accounts. For apps that don’t support TOTP, you can use email- or SMS-based MFA.

The following are the benefits of turning on MFA with Cerby-managed methods:

  * **Secure distribution:** Unlike traditional authenticators tied to a single physical device, Cerby securely distributes MFA access to all authorized users.
  * **Zero-touch MFA handling:** Regardless of the method used, Cerby automatically retrieves and fills in verification codes during automated logins. Therefore, every login is verified and protected without requiring manual code-sharing.
  * **One-click configuration:** For some managed apps, Cerby offers a one-click configuration experience through automation, where Cerby handles all the steps to turn on MFA.

For more information and instructions, read the following articles:

  * **Automatic:**
    * [Turn on MFA automatically for an account using the Cerby web app](https://help.cerby.com/en/articles/13748418-turn-on-mfa-automatically-for-an-account-using-the-cerby-web-app)
  * **Manual:**
    * [Turn on MFA with Cerby authenticator app for an account using the web app](https://help.cerby.com/en/articles/8429534-turn-on-mfa-with-cerby-as-an-authenticator-app-for-your-account-using-the-web-app)
    * [Turn on MFA with Cerby authenticator for an account using the mobile app](https://help.cerby.com/en/articles/12002648-turn-on-mfa-with-cerby-authenticator-for-an-account-using-the-mobile-app)
    * [Turn on MFA with a Cerby-managed phone number for your account](https://help.cerby.com/en/articles/11889236-turn-on-mfa-with-a-cerby-managed-phone-number-for-your-account)
    * [Turn on MFA with a Cerby-managed email address for your account](https://help.cerby.com/en/articles/11888742-turn-on-mfa-with-a-cerby-managed-email-address-for-your-account)
* * *

## 4\. Share the account with collaborators

True governance means providing access without compromising the login credentials themselves. With Cerby, you can share access to your accounts while retaining full control.

When a Cerby workspace is configured with an identity provider (IdP), all users and teams assigned to Cerby are eligible for account sharing. Additionally, you can invite external collaborators (such as individuals, agencies, or contractors) to your workspace as [guest users](https://help.cerby.com/en/articles/8392946-explore-guest-users) or through the [Partners](https://help.cerby.com/en/articles/8980877-explore-partners) feature so that you can also share your accounts with them.

In the moment of account sharing, you must assign any of the following roles to define the level of access to your account:

  * **Owner:** Users can share the account, manage its configuration, and view passwords.
  * **Collaborator:** Users can only use the account for automated or assisted logins, and viewing the actual password through the user interface is restricted.

{% hint style="danger" %}


**IMPORTANT:** For external collaborators and users with the **Login-Only** workspace role, you can only assign them the account **Collaborator** role.


{% endhint %}

For temporary access, you can share your accounts with external parties who do not have a Cerby account by generating a public link. These links are protected by identity verification and can be set to expire or restricted to one-time access.

For more information and instructions, read the following articles:

  * [Share an account](https://help.cerby.com/en/articles/9479388-share-an-account)
  * [Share an account using the Cerby mobile app](https://help.cerby.com/en/articles/9715128-share-an-account-using-the-cerby-mobile-app)
  * [Share an account via a local partner](https://help.cerby.com/en/articles/9039198-share-an-account-via-a-local-partner)
  * [Share an account via a host-guest partnership](https://help.cerby.com/en/articles/9044036-share-an-account-via-a-host-guest-partnership)
  * [Share items with external users via a link](https://help.cerby.com/en/articles/8308908-share-items-with-external-users-via-a-link)
* * *

## 5\. Rotate passwords automatically in Cerby

The final milestone in achieving the highest security level is eliminating static passwords. Cerby’s automated password rotation reduces the window of opportunity for attackers and ensures that credentials remain secure without manual intervention.

The following are the different ways in which you can trigger password rotations automatically:

  * **One-click experience:** As an account **Owner** , you can trigger automated password rotations directly from the account details page in the Cerby web app. Cerby runs the task server-side. For more information, read the article [Rotate an account password automatically](https://help.cerby.com/en/articles/13512602-rotate-an-account-password-automatically).
  * **Password policies:** You can enforce security at scale by creating policies that automatically rotate passwords on a set schedule or after user login events. For more information, read the article: [Create a password policy](https://help.cerby.com/en/articles/11466694-create-a-password-policy).
  * **Universal Logout:** When a security threat is detected, or a session must be terminated immediately, you can trigger a Universal Logout from your IdP—which extends to Cerby—or only from Cerby. For supported apps, Cerby automatically rotates account passwords during this process. For more information, read the articles [Trigger Okta Universal Logout and extend it to Cerby](https://help.cerby.com/en/articles/10495624-trigger-okta-universal-logout-and-extend-it-to-cerby) and [Trigger Cerby Universal Logout](https://help.cerby.com/en/articles/10496392-trigger-cerby-universal-logout).
  * **User deprovisioning:** To ensure former employees do not retain access to sensitive apps, Cerby automatically runs password rotations when users are deprovisioned via SCIM events from your IdP. This feature is available to all workspaces for supported apps.
  * **Locally-vaulted accounts:** For accounts stored in local vaults, you can still execute automated password rotations. To complete the process, you must authorize Cerby to decrypt your data while the automation is running. For more information, read the article [Run automated tasks for accounts in local vaults](https://help.cerby.com/en/articles/11682782-run-automated-tasks-for-accounts-in-local-vaults).
* * *

## Key Takeaways

Cerby is a must-have for technology executives and their teams to protect the brand, stay secure, and increase productivity.

When you have an account fully configured in Cerby, security is automatically enforced and you only have to worry about doing your daily job. Also, you can continue to onboard and manage your preferred solutions freely, with minimal but sufficient involvement from your IT department.
