---
description: "This article describes Cerby’s best practices for creating, securing, and managing your service accounts."
intercom_id: 9677654
---

# Cerby secure automation: Non-human identity best practices

In Cerby, service accounts are specialized accounts used to perform authorized App integrations that automate tasks on your behalf.

This article provides a guide to optimizing service accounts within Cerby, outlines key best practices for maintaining account security, and explains key tools in the Cerby platform.

## Enforce the principle of least privilege

Service accounts need to be built on the foundation of least privilege. Administrators need the controls and visibility necessary to ensure that each service account has the minimum set of permissions required to perform its designated function and only the right users have access, limiting the potential damage if a compromise occurs. For this principle, Cerby recommends the following:

* **Granular permission control:** Administrators must define the specific permissions required for each service account, granting access only to necessary resources.
* **Regular access reviews:** Administrators should schedule periodic reviews of service account permissions within Cerby to ensure they remain aligned with current business needs and minimize risk.

## Implement sensitivity-based access scopes for SSO-enabled Apps

In managing Non-Human Identities (NHIs), understood as digital credentials for automated authentication, for Single Sign-On (SSO)-enabled apps Cerby’s best practice is to assign SSO-enabled service accounts based on the following criteria:

* **Risk:** Higher-risk applications should have a lower ratio of service accounts, enabling more granular control and resources, contrary to lower-risk applications.
* **Data sensitivity:** Grouping applications with similar data sensitivity levels can simplify your team’s efforts in management while ensuring security.
* **Organizational structure:** Organizing your applications by organizational structure can address each unit’s needs and prevent you from overlapping efforts in performing security hygiene tasks.

By leveraging the above logic, you can ensure that not every application managed by Cerby requires its own service account within an identity provider like Okta or Microsoft Entra ID. Instead, you can group applications based on a strategy that leverages some or all of the above criteria.

## Strengthen security with MFA

Cerby recommends enforcing an extra layer of protection beyond usernames and passwords using Cerby’s Multi-Factor Authentication (MFA) to prevent unauthorized access:

* **Time-based One-Time Passwords (TOTPs):** Cerby generates unique, temporary codes for strong authentication that are known only to the user and the authentication server.
  * Depending on your identity provider policies, you may need to create a policy for your NHI service accounts that enables said SSO-enabled service accounts to leverage TOTP-based multi-factor authentication (MFA) versus a more human-oriented form of MFA, like biometrics.
* **Passkeys** : Cerby is introducing passkeys, a phishing-resistant method using biometric information. This feature is being implemented in Cerby (coming soon).

## Automate credential rotation with Cerby

Cerby's **Rotate Password** feature regularly rotates service account passwords, keys, and tokens, preventing compromised credentials from persisting.

* **Automated security:** Administrators can schedule automatic credential rotation at recommended intervals, such as every 90 days, making stolen credentials far less valuable to attackers.
* **Seamless integration:** Cerby seamlessly integrates with existing systems, minimizing disruption during the rotation process.

## Leverage continuous monitoring and logging

Cerby's [monitoring and logging](https://help.cerby.com/en/collections/5819820-workspace-monitoring) features provide complete visibility into service account activity:

* **Real-time insights:** Cerby's **Activity** view provides you with a clear picture of service account usage and actions, enabling you to quickly identify and address any suspicious activity.
* **Streamlined compliance:** By downloading the **Activity** report and integrating systems such as Sumo Logic and Splunk, your organization can maintain detailed audit trails of your service account actions to simplify compliance reporting and investigations.

## Take control of your service account security!

Cerby provides you with the tools to implement service account best practices and significantly strengthen your security posture. [Explore Cerby's features today](https://www.cerby.com/), or contact our team at [sales@cerby.com](mailto:sales@cerby.com) to discuss how Cerby can help secure automation workflows.
