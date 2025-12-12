---
description: This article describes the basic concepts and characteristics of Cerby Suggest.
---

# Explore Cerby Suggest

Hi there, welcome to Cerby Suggest!

Thank you for choosing us to discover and manage rogue apps. We are a cybersecurity company focused on empowering you and your organization to manage and secure access to your apps.

Cerby Suggest is our app sprawl detection product, designed to recommend sanctioned apps when end users are about to sign up for a new app or service provider. The goal is to help you gain centralized visibility on the apps your employees need and use, and provide employees with more information at the decision-making point.

Our approach is unique because we address app sprawl at the moment of account creation. In contrast, other SaaS discovery tools detect accounts after they have persisted for some time, using methods such as email mining or financial record reviews.

In the following sections, we walk you through the basic information and characteristics of Cerby Suggest:

  * Learn how Cerby Suggest works
  * Use Cerby Suggest
  * Boost collaboration with Teams
* * *

# Learn how Cerby Suggest works

Cerby Suggest is a product built to help you detect app sprawl. By being connected to your systems and your identity provider (IdP), Cerby Suggest can guide end users into taking advantage of the licenses and seats of your organization’s sanctioned apps, therefore reducing the costs of unnecessary, unused, orphaned, or duplicate resources.

The process to request licenses or seats is guided and managed by Cerby and your IT team via custom-built integrations. For example, employees can raise IT service request tickets from Cerby Suggest through an integration with ServiceNow.

After receiving authorization to sign up for a SaaS app account, employees can add such an account to Cerby to streamline login and secure access with the multi-factor authentication (MFA) managed by Cerby.

The following sections explain how we detect app sprawl, optimize your licenses and seats, and secure access to your accounts:

  * Custom-built integrations
  * Discovery report
  * Cerby client apps

## Custom-built integrations

The Cerby platform is connected to your organization's systems via custom-built integrations. The goal is to retrieve the necessary data to identify app sprawl effectively, suggest users request existing licenses or seats for apps within the same category and keep track of all the IT service request tickets.

Currently, the following integrations are available:

  * Application assignments
  * Application graph
  * ServiceNow
  * Slack

The following sections describe each integration.

### Application assignments

The organization’s IT admins build and maintain an artifact that serves as the source of truth for the apps all users have been assigned to based on their role, department, and information technology service management (ITSM).

Cerby retrieves the information from this artifact to associate it with each user's Cerby account.

### Application graph

Cerby uses an application graph to identify and map the discovered SaaS apps based on their category or taxonomy. The goal is to provide users with accurate app suggestions according to the workspace policies and objectives.

An application graph refers to the apps sanctioned by an organization and the similar apps defined by Cerby and the organization.

The application graphs can be maintained in the following ways:

  * **IT-led:** The organization’s IT admins feed a self-service artifact with new apps and categories or re-categorize the existing ones. With this IT-led maintenance, the Cerby platform improves the default categories displayed to users.
  * **Third-party providers:** Cerby connects to third-party providers to retrieve and maintain the application graph used to identify and map the discovered SaaS apps based on their category or taxonomy.

### ServiceNow

Cerby connects to ServiceNow to create the corresponding tickets to request SaaS licenses or seats from a user action. This integration provides IT admins with some or all of the following information to approve or deny the request:

  * The name of the requester and approver
  * A business justification
  * A description of the request
  * The type of user who requests the license or seat (employee or contractor)

### Slack

Cerby connects to Slack and sends messages to provide IT admins visibility on the following:

  * Service request tickets generated in ServiceNow
  * Account creation events for Okta apps or similar apps within the application graph
  * Account creation events for apps not listed in the application graph
  * Cerby browser extension deactivation events

To request new integrations, contact the Customer Support team by emailing [support@cerby.com](mailto:support@cerby.com) or sending a message through the help chat of the Cerby dashboard.

## Discovery report

Cerby offers the Discovery Report to provide IT admins with greater visibility on where new logins and signups occur. With this information, IT admins can discover apps that may not be in the organization's scope, perform effective license management, and make decisions about security.

For more information about this report, read the article [Explore the Cerby Suggest Discovery Report](https://help.cerby.com/en/articles/10629361-explore-the-cerby-suggest-discovery-report).

## Cerby client apps

The Cerby platform comprises two client apps that work together to provide you with the best experience as a Cerby Suggest user:

  * Cerby web app
  * Cerby browser extension

### Cerby web app

The Cerby web app is the interface that enables you to perform all the management actions on the accounts you save in Cerby and the users who belong to your workspace.

The following are the actions you can perform with the Cerby web app:

  * Add an account, edit the account details, manage access to the account, and start the automatic login via the Cerby browser extension.
  * Store the backup codes manually when configuring MFA for your accounts.
  * Create a collection of accounts and manage access to it.
  * Search through your items.
  * View and export the list of workspace members.
  * View your billing information.
  * View the user activity on your workspace and items.

You can use any web browser to access the Cerby web app, and all of your interactions are through a dashboard displayed after logging in to your workspace, as shown in **Figure 2**.

<figure><img src="../.gitbook/assets/gwfP4-Pfa0yJmqGu2jd7GG6B8gqZ392I8ENCz3a0VygjAy6YPjcbGffWjljj2sk3TKfsXZT3eD7FZd2d304Hvw4ZJ6vUHwLUQF6Jlgs8AngcIwWGjTWfgPaq6gwATRp9VN0ygpPcQn_qmE_VU0QOXBY.png" alt="Screenshot of the Cerby web app dashboard. The All accounts view is displayed with multiple account cards and a button at the top right to add an account or collection."><figcaption></figcaption></figure>

**Figure 2.** Cerby web app dashboard for Cerby Suggest users

Our Development team constantly updates our Cerby web app, meaning you always access the latest features and improvements.

### Cerby browser extension

The Cerby browser extension is an add-on for web browsers vital to the user experience of Cerby Suggest users. The extension is our app sprawl detection tool with the following features:

  * Detects when users navigate to login and signup pages
  * Detects account creation events
  * Suggests users request existing licenses or seats by filling out a form

{% hint style="danger" %}


**IMPORTANT:** End users must be logged in to their corresponding workspace through the Cerby browser extension to use Cerby Suggest.


{% endhint %}

The following are the actions you can perform with the Cerby browser extension:

  * Log in to your accounts automatically by leveraging the autofill feature on login pages. Automatic login is guided by in-context alerts for visibility on what happens in every step and what to do if the process fails or needs your intervention.
  * Log in to your accounts manually by leveraging the inline menu.
  * Generate secure passwords based on custom policies to sign up for applications or rotate your passwords manually.
  * View and copy your account details to manually log in to your apps.
  * View and copy verification codes when MFA is turned on using Cerby as an authenticator app.
  * Search through your items.
  * Save your credentials when logging in or signing up for an app.

After logging in to your workspace with the Cerby browser extension, your interactions are through a popup and an inline menu, as shown in **Figure 3** and **Figure 4**.

<figure><img src="../.gitbook/assets/v-Pe9Lhvx6iX8nBfqD63PRk5MYVnz4cZu-MGyEhpLsDjEdSZeYYDPsilu0BTNp3PCSMVg4zVDtmm292c5M92E4yKRUjowqC7M0Sb6rSYi_q5W3j_y0iXDM5jeDoBxByl6S50lQY-IBP2j7eTWh_DAq8.png" alt="Screenshot of the Cerby browser extension popup on top of a login page. The Accounts tab is activated with a list of account cards."><figcaption></figcaption></figure>

**Figure 3.** Cerby browser extension popup for Cerby Suggest users

<figure><img src="../.gitbook/assets/PSWgJJHhpCMj5kfkMyFYU4VvkWvn1OfwkABnuR23exV_ul3JhCwLHswEWt0xGXW9xHdjT6pVYnnYJguD_Jct4yrEIm8XQ1rgO1KcwCosmN0PzOAchMtAaFbzwdSmgT5ecu-0lpGM53v3f8AkcR3SOd4.png" alt="Screenshot of the Cerby browser extension inline menu on top of the input fields of a login page. A list of account cards is displayed."><figcaption></figcaption></figure>

**Figure 4.** Cerby browser extension inline menu for Cerby Suggest users

The Cerby browser extension can be installed from the browsers’ stores or distributed to all corporate computers via a Mobile Device Management (MDM) solution. You receive the latest version automatically each time the Development team pushes a new version.

The following web browsers are supported for MacOS and Windows computers:

  * Safari
  * Microsoft Edge
  * Mozilla Firefox
  * Google Chrome
  * Island
* * *

# Use Cerby Suggest

Now that you know the basic concepts of Cerby Suggest, get to know more of the actions end users can perform with Cerby Suggest in the [Get started as a Cerby Suggest user](https://help.cerby.com/en/articles/8843620-get-started-as-a-cerby-suggest-user) article.

* * *

# Boost collaboration with Teams

With Teams, you can simplify user and access management through Cerby. This feature helps you and your company support groups of users assigned to items and automatically change the Cerby role and user account provisioning to all group members.

The following are the options to create teams in Cerby:

  * Create a group of users in the corporate directory managed by your IdP, such as Okta and Azure AD, and replicate it automatically as a team in Cerby.
  * Create a self-managed team selecting users from your workspace.

You can manage all your teams through the **Teams** view, as shown in **Figure 6**.

<figure><img src="../.gitbook/assets/3-Zil3qdaOhf7pLa_s-y_E4P0aRdTHAe-XYt63Vzl1Nh1lJdo1RFepG5pT146Y0lH3d_lgbEABm1D9X-67zrFvhJlFQQh0veXjIQqsP_X-BIHD2IQs5g0OijeaZJz20c0KjgMfe4bw0tN1kuWuCEOYk.png" alt="Screenshot of the Teams view in the Cerby dashboard. The Members tab of a specific team is displayed with a list of team members."><figcaption></figcaption></figure>

**Figure 6.** **Teams** view in the Cerby dashboard

To add and manage a team, follow the instructions in the article [How to use Teams](https://help.cerby.com/en/articles/6624225-how-to-use-teams). You can also see the video [How to add a self-managed team](https://help.cerby.com/en/articles/8325134-video-how-to-add-a-self-managed-team).
