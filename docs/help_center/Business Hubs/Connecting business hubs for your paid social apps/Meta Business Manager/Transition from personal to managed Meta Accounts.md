# Transition from personal to managed Meta Accounts

**Description:** This article describes how to transition access to your Meta business tools from using personal accounts to managed Meta Accounts.

With the release of managed Meta Accounts, you can now enable users to access
your Meta Business tools without the need for a personal Facebook profile.  
  
Managed Meta Accounts are designed for business use, offering features like
single sign-on (SSO) and automatic account provisioning. These accounts enable
users to access Meta business tools, such as Business Manager and Meta for
Work, using their work credentials instead of their personal Facebook
accounts.

As an administrator of Business Manager or Meta for Work, you must follow the
official steps provided by Meta to transition users to managed Meta Accounts.
For end users, after the transition, they must simply log in using their
existing identity provider (IdP), such as Okta or Entra ID (formerly Azure
AD). One key benefit of this transition is that users can access everything
through a single interface using Cerby.

Users do need to store their credentials within Cerby; instead, they can
authenticate and access the Meta services with their corporate account. This
approach simplifies the transition and ensures a streamlined experience for
managing Meta Accounts alongside other tools.

**IMPORTANT:** [Meta for Work](https://forwork.meta.com/) was released in July
2023 for beta testing, and some organizations have been transitioning to
replace personal Facebook profiles as the default login for Meta Business
Manager. Note that this feature is currently available to selected customers
only. For more information or to ask about eligibility, please contact your
Meta support representative.  
---  
  
* * *

# **Transition from personal to managed Meta Accounts**

The following are the main steps you must follow to migrate from your personal
account to managed Meta Accounts:

  1. Complete your migration to managed Meta Accounts

  2. Update the login method in Cerby

The following sections describe each main step.

## **1\. Complete your migration to managed Meta Accounts**

The Meta transition from Facebook personal accounts to managed Meta Accounts
is designed to improve security and streamline user access to business
resources without relying on personal Facebook profiles. This change means
more efficient administrative features, such as SSO and automatic account
provisioning.

To learn, prepare, and perform the migration process from personal to managed
Meta Accounts, ensure to review the following official Meta articles:

  * [Managed Meta Accounts & Third-party Integrations](https://developers.facebook.com/docs/facebook-login/managed-accounts)

  * [About migrating to managed Meta accounts in Business Manager](https://www.facebook.com/business/help/967992801216784?helpref=faq_content)

## **2\. Update the users’ login method in Cerby**

To update the users’ login method in Cerby, you must complete the next
substeps:

2.1. Update the login method of the Meta business hub

2.2. Sync the user information in the Meta business hub

The following sections describe each substep.

## **2.1. Update the login method of the Meta business hub**

To update the login method of the Meta business hub, you must complete the
next steps:

  1. Log in to your corresponding[ Cerby](https://app.cerby.com/) workspace.

  2. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.

  3. Click the **Settings** () icon of the corresponding Meta business hub card. The business hub details page is displayed with the **Settings** tab activated.

  4. Click the **Edit** button in the **User management and login** field of the **Settings** section. The **Update user management and login method** dialog box is displayed.

  5. Select the **Single sign on (SSO)** option in the drop-down field in the dialog box.

  6. Click the **Done** button. A success message is displayed.

## **2.2. Sync the user information in the Meta business hub**

To sync the user information in the Meta business hub, you must complete the
next steps:

  1. Log in to your corresponding[ Cerby](https://app.cerby.com/) workspace.

  2. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.

  3. Click the **Settings** () icon of the corresponding Meta business hub card. The business hub details page is displayed with the **Settings** tab activated.

  4. Click the **Check for updates** button located at the top-right section of the page. A message box is displayed with information about the process. 

**NOTE:** The check and import process may take a few minutes depending on the
number of users and assets, and because Cerby automatically matches users to
their corresponding Cerby account. You can review the progress of the
automation task through the **Automation** view; when the process is complete,
a success message box is displayed.

  5. Activate the **Members** tab to review the list of synced users in the **User Overview** section.

Now you are done. The next time users log in to Meta, they must use their
corporate SSO.

