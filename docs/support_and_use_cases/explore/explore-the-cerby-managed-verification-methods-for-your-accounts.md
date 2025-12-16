---
description: This article describes the benefits of using Cerby-managed verification methods to enhance the security of your accounts.
intercom_id: 5457562
---

# Explore the Cerby-managed verification methods for your accounts

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* **Account Owners**
* Supported using the Cerby web app and mobile app


{% endhint %}

With Cerby, you can add an extra layer of security to your accounts by turning on Cerby-managed verification methods.

By centralizing these access control mechanisms, Cerby helps you improve, secure, and streamline the login process for you and all the users with shared access to your accounts without affecting collaboration.

Cerby recommends always turning on more than one verification method, such as multi-factor authentication (MFA) for the accounts that support it, prioritizing the authenticator app above other methods when applicable. The following are some of the benefits of trusting Cerby to manage the verification methods of your accounts:

* **Streamlined login:** When these verification methods are configured for MFA, Cerby can fill in the time-based one-time passwords (TOTPs), one-time passwords (OTPs), and verification codes you need to log in automatically. If needed, you can also copy them from the Cerby client apps to log in to your accounts manually.
* **Centralized control:** You can manage the verification codes sent via email or SMS to Cerby-managed email addresses and phone numbers from one place: the Shared Inbox. These codes are distributed to all users with shared access to an account.
* **Encrypted data:** Cerby uses a Zero Knowledge architecture to encrypt TOTPs, meaning that even Cerby cannot access or read your MFA codes.
* **Improved collaboration:** TOTPs and verification codes are distributed through the Cerby platform to all users with shared access to the account whenever they need to log in.
* **Enhanced security and privacy:** By using Cerby-managed email addresses and phone numbers for corporate accounts, you reduce exposure of personal emails and phone numbers to third-party services, enhancing your privacy and mitigating direct spam or phishing attempts to your primary contact details.

MFA is one of the most impactful cybersecurity best practices. [According to Microsoft](https://www.windowscentral.com/microsoft-999-people-get-hacked-one-ridiculous-reason), 99.9% of the compromised accounts they track daily don’t have an MFA method turned on.

* * *

## Cerby-managed verification methods

The following are the Cerby-managed verification methods you can set up for your accounts:

* Authenticator app
* Email address
* Phone number
* RSA codes

The following sections briefly explain each method.

### Authentication app

When configured as your authenticator app, Cerby generates TOTPs for secure MFA. These passcodes are typically valid for 30 seconds, ensuring that each login attempt is protected with dynamic, time-sensitive credentials.

For more information about how to set Cerby as your authenticator app, read the article [Turn on MFA with Cerby as an authenticator app for your account](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/turn-on-mfa-with-cerby-as-an-authenticator-app-for-your-account-using-the-web-app).

### Email address

You can create and set up a dedicated email address managed by Cerby to receive verification codes sent by your apps via email. This method centralizes MFA processes, allowing you to easily manage and retrieve codes from your Shared Inbox in Cerby, streamlining the authentication process for your team.

For more information about how to create and set up a Cerby-managed email address, read the article Set up and associate a Cerby-managed email address for your account.

### Phone number

You can create and set up a phone number managed by Cerby to receive verification codes via SMS from your apps. Like Cerby-managed email addresses, you can centralize MFA processes and manage and retrieve codes from your Shared Inbox in Cerby.

For more information about how to create and set up a Cerby-managed phone number, read the article Create and associate a Cerby-managed phone number with your account.

### RSA codes

When integrating RSA tokens with Cerby, the platform can retrieve and autofill RSA-generated OTPs for logging into accounts. By linking your RSA token, Cerby securely manages the authentication process, enabling seamless login experiences while maintaining high security through time-sensitive, token-based credentials.

For more information about how to create and set up RSA codes with Cerby for MFA, read the article [Set RSA tokens as your account MFA method](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/set-rsa-tokens-as-your-account-verification-method).
