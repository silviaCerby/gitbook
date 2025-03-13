# Explore Cerby

## This document describes how Cerby helps businesses secure access to all their applications, including disconnected or nonfederated apps. 

Welcome to Cerby\!

First, thank you for choosing us. We are an identity security company dedicated to protecting businesses and users from digital threats. We’ve built a comprehensive cloud-based platform aiming to secure access to your applications, including those that don’t natively support security standards and protocols–also known as disconnected or nonfederated apps.

With our automation approach, we eliminate the biggest risk in cybersecurity: human error. Cerby enables organizations to automate common security hygiene tasks often overlooked by business users, such as password rotations and multi-factor authentication (MFA). Additionally, with automation, we can extend identity lifecycle management from corporate identity providers (IdPs) such as Okta or Entra ID to any app, reducing manual work while closing security gaps.

The following are some of the benefits and characteristics of our solution:

* Centralize access to all your apps from a single user interface (UI).  
* Share access to your business accounts securely.   
* Safeguard your accounts and sensitive information.  
* Streamline identity lifecycle management for apps without APIs (application programming interfaces) or SCIM (System for Cross-domain Identity Management) support.  
* Discover and audit all behavior in your apps.

This document describes how Cerby helps businesses and users to secure access to their applications.

# **How Cerby works**

The following basic concepts and features describe how Cerby works:

* [Client apps](#client-apps)  
* [Workspace](#workspace)  
* [Roles](#roles)  
* [Dashboard](#dashboard)

The following sections describe each concept and feature.

## **Client apps** {#client-apps}

Cerby is a platform that combines the following three client apps to provide you with the best user experience:

* **Web application:** It enables you to manage all your accounts, grant shared access to them across your organization, and log in to your accounts, all from a single UI.  
  The Cerby web app is available for any browser.  
* **Browser extension:** It enables you to log in to your accounts by automatically filling the credentials you store in Cerby in the corresponding fields of your apps.   
  The Cerby browser extension is available for the following browsers:  
  * Firefox  
  * Google Chrome  
  * Microsoft Edge  
  * Safari  
* **Mobile application:** It enables you to manage and access your accounts from your mobile phone using the operating system native autofill feature. It also serves as an authentication device for sensitive tasks and to set up multi-factor authentication (MFA) managed by Cerby.  
  The Cerby mobile app is available for the following operating systems:  
  * Android  
  * iOS

## **Workspace** {#workspace}

A workspace is an isolated environment in the Cerby platform that enables users to manage access and protect their business accounts. Commonly, each organization has a Cerby workspace and a default cloud vault in which users can save their accounts and sensitive information. The following are some of the account management actions users can perform:

* Manage user access and permissions.  
* Manage account security:  
  * Turn on MFA managed by Cerby  
  * Rotate passwords  
* Retrieve analytics on account usage and user activity

Workspaces are typically connected to a corporate IdP such as Okta or Entra ID and configured with single sign-on (SSO) authentication and user provisioning via SCIM. With this configuration, users in the corporate directory are automatically and continuously synced with Cerby, and they can leverage single sign-on (SSO) to authenticate to Cerby. 

Currently, you can only create a workspace from an invitation sent by the Cerby team from our official email address, [help@cerby.com](mailto:help@cerby.com). After creating your workspace, its name is displayed and identified as follows **\<workspace name\>.cerby.com**.

## **Roles** {#roles}

Roles are sets of permissions that represent the tasks, activities, or functions that users can perform in the Cerby platform. Cerby manages the following roles at a workspace and account level:

* Workspace-level roles  
  * Owner  
  * Super Admin  
  * Admin  
  * User  
* Account-level roles  
  * Owner  
  * Collaborator

For more information about roles, read the article “How Cerby manages roles.”

## **Dashboard** {#dashboard}

The dashboard is the graphical interface of the Cerby web app that integrates information about users, accounts, configuration, services, and applications. 

Every time you log in to the Cerby web app, you land on the homepage, which corresponds to the **Accounts** view, as shown in **Figure 1**.

**Figure 1\.** Homepage of the Cerby web app dashboard

To navigate through the different features of Cerby, the dashboard contains a left navigation drawer, a top navigation bar, and the main section that contains the different views, pages, information, and account cards. Depending on your role, you can access different features of the dashboard.

Account cards consist of card-type buttons displayed on the dashboard homepage representing the accounts you can access and manage through Cerby. Account cards redirect you to log in and authenticate automatically into your apps.

Every time you add an account to Cerby, the corresponding account card is created in the dashboard.