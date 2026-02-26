---
description: "This article describes the benefits of using Cerby-managed verification methods to enhance the security of your accounts."
intercom_id: 5457562
---

# Explore the Cerby-managed verification methods for your accounts

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* **Account Owners**
* Supported using the Cerby web app and mobile app


{% endhint %}

Cerby helps you protect your shared accounts by centralizing and automating the verification methods used during login. Instead of relying on personal multi-factor authentication (MFA) devices or external email and SMS channels, Cerby can manage, store, and deliver verification codes securely to all authorized users, improving security, privacy, and team collaboration.

* * *

## Why centralized verification matters

Cerby recommends enabling multiple verification methods where possible, prioritizing the authenticator app above other methods.

The following are the key benefits of centralized verification using Cerby:

  * **Streamlined login experience:** After configuration, Cerby can **automatically enter** time-based one-time passwords (TOTPs), SMS one-time passwords (OTPs), and other codes during login flows, reducing manual steps and login friction. Users can also manually copy codes from the Cerby client apps if necessary.
  * **Centralized control and shared access:** Verification codes sent to Cerby-managed email addresses or phone numbers are routed into Cerby’s Shared Inbox. This means codes are accessible to all users who need them, without exposing personal contact details.
  * **Encrypted and private:** Cerby applies a zero-knowledge security model to sensitive time-based codes. Even Cerby’s internal systems cannot read the stored MFA secrets or TOTPs.
  * **Improved collaboration:** All users with shared access to an account can retrieve verification codes without coordination overhead, avoiding bottlenecks when a single person is unavailable.
  * **Reduced exposure of personal info:** Using corporate-managed contact channels reduces the risk of exposing employees’ personal email addresses or phone numbers to external services, thereby lowering privacy and phishing risks.
* * *

## Cerby-managed verification methods

Cerby supports four distinct methods you can configure for your accounts:

  * [Authenticator app](explore-the-cerby-managed-verification-methods-for-your-accounts.md#authenticator-app)
  * [Cerby-managed email address](explore-the-cerby-managed-verification-methods-for-your-accounts.md#cerby-managed-email-address)
  * [Cerby-managed phone number](explore-the-cerby-managed-verification-methods-for-your-accounts.md#cerby-managed-phone-number)
  * [RSA codes](explore-the-cerby-managed-verification-methods-for-your-accounts.md#rsa-codes)

The following sections describe each verification method.

### Authenticator app

Cerby serves as your authenticator app by generating TOTPs that refresh every 30 seconds. These codes can be used for MFA on supported apps and are shared with all authorized users.

**TIP:** This verification method is preferred for the correct functionality among your apps and Cerby. For more information, refer to the article [Turn on MFA with Cerby as an authenticator app](https://help.cerby.com/en/articles/8429534-turn-on-mfa-with-cerby-as-an-authenticator-app-for-your-account-using-the-web-app?utm_source=chatgpt.com).
---

### Cerby-managed email address

Create and configure an email address managed by Cerby and owned by your company to receive MFA verification codes. Cerby then routes these codes into the Shared Inbox for retrieval or automated logins.

**TIP:** Use this verification method when MFA via email is supported or required by the application. For more information, refer to the articles __[Set up and associate a Cerby-managed email address for your account](https://help.cerby.com/en/articles/11888658-set-up-and-associate-a-cerby-managed-email-address-for-your-account) and [Turn on MFA with a Cerby-managed email address for your account](https://help.cerby.com/en/articles/11888742-turn-on-mfa-with-a-cerby-managed-email-address-for-your-account).
---

### Cerby-managed phone number

Similar to managed email, a corporate phone number can be created in Cerby to receive SMS verification codes. These codes are centralized in the Shared Inbox and used for MFA or automated login flows.

**TIP:** Use this verification method when SMS-based MFA is required.__ For more information, refer to the articles [Set up and associate a Cerby-managed phone number for your account](https://help.cerby.com/en/articles/11889035-set-up-and-associate-a-cerby-managed-phone-number-for-your-account) and [Turn on MFA with a Cerby-managed phone number for your account](https://help.cerby.com/en/articles/11889236-turn-on-mfa-with-a-cerby-managed-phone-number-for-your-account).
---

### RSA codes

Cerby can integrate with RSA token-based MFA systems to retrieve and autofill one-time codes generated by RSA. This allows automated logins while preserving strong token security.

**TIP:** Use this verification method when your app uses RSA token MFA. For more information, refer to the articles [Set RSA tokens as your account verification method](https://help.cerby.com/en/articles/10858212-set-rsa-tokens-as-your-account-verification-method) and [Turn on the RSA codes for your account using the Cerby mobile app](https://help.cerby.com/en/articles/11429260-turn-on-the-rsa-codes-for-your-account-using-the-cerby-mobile-app).
---

* * *

## Best practices for enterprise security

The following are some of the best practices we recommend for improving the security of your accounts:

  * **Enable at least two verification methods:** If the primary method fails or is unavailable, having a secondary method improves resilience.
  * **Use corporate-owned channels:** Reduces reliance on personal devices and protects employee privacy.
  * **Centralize for shared access:** Makes MFA codes available to all authorized users, preventing access bottlenecks.
