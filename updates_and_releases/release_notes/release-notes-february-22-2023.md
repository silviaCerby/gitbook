---
intercom_id: 7020161
---

# Release Notes - February 22, 2023

## New Features

* The new look of the account details page is now available. It’s easier to identify the recommended security actions for your accounts. Also, we condensed and improved the information and actions of every section.
* The following apps are now supported as tenants:
  * Atlassian
  * Calendly
  * Meta Business Suite
  * Mailchimp
* NetComponents and Calendly are now supported with automatic login and password rotation.
* Office 365 is now supported with the following automation:
  * Login
  * Turning on and off MFA
  * Password rotation
* All users, no matter their role, can now see the existing teams and team members within a workspace through the **Teams** view.

## Fixes

* The issue with the **Inbox** in the account details page of the Cerby web app only displaying emails and not SMS is fixed.
* The following issues related to Partners in the Cerby web app are fixed:
  * **Workspace Admins** being unable to see the shared accounts via a partnership, even when the accounts were shared with them.
  * **Workspace Admins** not receiving a partnership request via email.
  * The same**Workspace Admin** creating a partnership and approving the partnership request.
  * The guest contact partner information displaying an unrelated email address.
  * **Workspace Admins** being unable to share accounts into the partnership.
* The issue with the "Connect your account" status in the Cerby web app not changing on the account card for a tenant after connecting an account is fixed.
* The alert issues for Atlassian and Fortinet are fixed by catching TOTP form submissions and sleeps.

## Security Fixes

* Potential click-jacking vulnerabilities in the <https://www.cerby.com/> site and [Contact us](https://www.cerby.com/about-us/contact-us) page are fixed. Report credit: Pavan Vyas and Milan Jain.
