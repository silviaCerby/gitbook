---
description: "This article describes the concept of accounts in Cerby and how they can be used to manage disconnected applications."
---

# Explore Accounts

Disconnected applications that do not support standard security protocols such as security assertion markup language (SAML) or system for cross-domain identity management (SCIM) present significant unmanaged risks in modern enterprises. In Cerby, the Account serves as the central entity to manage these outliers.

Creating an Account in Cerby provides more than secure password storage. It enhances legacy or non-standard logins with enterprise-level security, automation, and visibility.

## Why accounts matter

Standard identity providers (IdPs) such as Okta or Entra IS work well for primary applications but often overlook shadow or legacy apps. Cerby Accounts addresses this gap by providing a unified access layer for all applications, regardless of their native capabilities. This means you can:

* **Centralize access:** Providing a single location to view and manage all team logins.
* **Extend MFA:** Enabling multi-factor authentication (MFA) for applications that do not natively support it.
* **Enable governance:** Offering a clear audit trail of account access and activity.

## Understanding Account management states

Not all applications are created equal. Cerby categorizes accounts based on the level of control and security you wish to enforce.

### Managed Accounts (high security)

Managed accounts represent the highest standard for securing critical disconnected applications. When an account is managed, Cerby assumes responsibility for its security lifecycle.

* **Automated security:** Cerby manages complex security tasks to ensure compliance with corporate policies.
* **Zero-knowledge access:** Users can perform tasks without viewing or knowing the actual password.
* **Lifecycle sync:** These accounts automatically respond to user changes in the primary identity provider.

### Unmanaged Accounts (visibility only)

Unmanaged accounts offer visibility and secure storage but do not include automated security features.

* **Secure vaulting:** Credentials are encrypted and stored in your dedicated vault.
* **Manual control:** Team members can share and access these accounts, while the owner is responsible for manual security updates such as password rotations.

### Self-managed Accounts (personal productivity)

These accounts are intended for individual use, allowing users full control over the lifecycle while benefiting from Cerby’s secure login and MFA capabilities.

### Key capabilities of a Cerby Account

Every account in your workspace, regardless of its state, gains access to these core Cerby strengths:

| **Capability** | **Benefit to the business** |
| -------------- | --- |
| **Edge-based SSO** | Users log in using their corporate identity, even if the app doesn't support it. |
| **MFA orchestration** | Cerby manages the second factor, eliminating the need for shared physical phones or personal emails for verification codes. |
| **Attribute mapping** | Map specific metadata to accounts to ensure they are organized by department, risk level, or project. |
| **Shared access control** | Securely delegate access to a team or an external partner without revealing the root password. |

**Table 1.** Summary of account management states and their key features

## Getting started with Accounts

To achieve identity coverage, we recommend identifying high-risk, high-value disconnected applications, such as local banking portals, core marketing platforms, or legacy administrative tools, and transitioning them to a managed state. By storing and using Accounts in Cerby, you ensure that critical applications are protected with the highest level of security while providing visibility and control over all accounts in your environment.
