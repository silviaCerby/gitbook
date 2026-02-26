---
description: "This article describes how to remove members from a guest workspace."
intercom_id: 9044021
---

# Remove guest workspace members

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Admins**
* Available to Cerby Automate
* Only supported using the Cerby web app


{% endhint %}

As a guest workspace **Admin** who has accepted a host-guest partnership, you can remove users in the following two methods depending on the workspace type and settings:

* [Automatically from your IdP](remove-guest-workspace-members.md#automatically-from-your-idp)
* [Manually from a local user workspace](remove-guest-workspace-members.md#manually-from-a-local-user-workspace)

The following sections describe each method.

* * *

## Automatically from your IdP

When user provisioning is enabled in your Cerby workspace through the System for Cross-domain Identity Management (SCIM) specification from an identity provider (IdP), such as Okta or Entra ID (formerly Azure AD), any change in the corporate directory propagates automatically to your workspace.

IT admins can remove users from the IdP, which causes the corresponding removal in a guest workspace. This action also involves removing all access to accounts shared via a host-guest partnership.

* * *

## Manually from a local user workspace

When you have your Cerby guest workspace configured as a local user workspace, user removal is manual through the **All members** view of the Cerby web app dashboard. Follow the instructions from the [Remove user from workspace](https://help.cerby.com/en/articles/8011381-how-to-create-and-configure-a-local-user-workspace#h_b382e5cb94) section of the article [How to create and configure a local user workspace](https://help.cerby.com/en/articles/8011381-how-to-create-and-configure-a-local-user-workspace).
