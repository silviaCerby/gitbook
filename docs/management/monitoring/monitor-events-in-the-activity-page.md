---
description: This article describes all the events in the platform that you can monitor in the Activity page.
---

# Monitor events in the Activity page

In Cerby, the **[Activity](https://help.cerby.com/en/articles/10128402-explore-activity)** page is your centralized dashboard for tracking workspace events, changes, and interactions. It enables you to monitor various components across your workspace closely, making it easier to detect unusual patterns, analyze user behavior, and ensure compliance with security protocols.

The following table contains the list of events you can see in the **Activity** page and their description.

**Event name**| **Description**
---|---
**Account events**|
MFA Remains On| An automated task to verify if MFA is still on and with the correct secret key was performed.
MFA Turned Off| MFA was turned off for an account via an automated task.
MFA Turned Off Attempt| An automated task to turn off MFA for an account was triggered.
MFA Turned On| MFA was turned on for an account via an automated task.
MFA Turned On Attempt| An automated task to turn on MFA for an account was triggered.
Account Access Removed| Shared access to an account was removed for one or multiple users.
Account Added To Collection| An account was added to a collection.
Account Deleted| An account was deleted.
Account Disabled| An account was disabled.
Account Fields Created| An account's custom field was created via the account details page.
Account Fields Requested| An account's custom fields were retrieved to display them on the account details page.
Account Fields Updated| An account's custom field was updated via the account details page.
Account Removed From Collection| An account was removed from a collection.
Account Updated| The details of an account were updated.
Captcha Resolution Required| User intervention is required during an automated task to solve a CAPTCHA.
Code Received| A verification code was received in a Cerby-managed email address or phone number.
Email Address Added To The Account| A Cerby-managed email address was created and associated with an account.
Email Forward Messages| A message was forwarded from a Cerby-managed email address via the Shared Inbox.
​
Email Address Removed From The Account| A Cerby-managed email address was removed from an account.
Existing Account Added| A new account was added to the workspace via the **Add account** wizard.
Log in| An automated task to log in to an account was performed.
Login Attempt| An automated task to log in to an account was initiated.
Login To Account Attempt By Account Id| An automated task to log in to an account was initiated, and Cerby has identified this account by its ID.
Login Failed| An automated task to log in to an account was unsuccessful.
Manual MFA Fill| A user filled in the MFA code field manually for an account using the Cerby browser extension.
Manual Login Attempt| A user attempted to log in to an account manually using the Cerby browser extension.
Manual Password Fill| A user filled in the password field manually for an account using the Cerby browser extension.
Manual Username Fill| A user filled in the username field manually for an account using the Cerby browser extension.
New Account Added| A new account was added to the workspace via a password manager import.
Password Retrieved| An account's password was retrieved to display it on the account details page.
Password Rotated| An automated task to rotate the password of an account was performed.
Password Rotated Application| A new password was stored in Cerby after successfully rotating the password via an automated task.
Phone Number Added To The Account| A Cerby-managed phone number was created and associated with an account.
Phone Number Removed From The Account| A Cerby-managed phone number was removed from an account.
Sharing Of Account| An account was shared with one or multiple users.
**Secret events**|
Secret Attachment Created| An attachment was added to a secret.
Secret Attachment Deleted| The attachment of a secret was deleted.
Secret Attachment Requested for Download| The attachment of a secret was downloaded.
Secret Attachment Uploaded| An attachment was uploaded to a secret.
Secret Created| A secret was added to the workspace.
Secret Deleted| A secret was deleted from the workspace.
Secure Secret Requested| The details of a secret were viewed by a user.
Secret Shared| A secret was shared with one or multiple users.
Secret Unshared| Shared access to a secret was removed for one or multiple users.
Secret Updated| The details of a secret were updated.
Vault Secret Created| A secret was created in a vault.
Vault Secret Deleted| A secret was deleted from a vault.
**Collection events**|
Collection Created| A collection was created.
Collection Deleted| A collection was deleted.
Collection Modified| The details of the collection were updated.
Secret Added To Collection| A secret was added to a collection.
Collection Shared| A collection was shared with one or multiple users.
Collection Sub Collection Added| A subcollection was added to the collection.
Collection Sub Collection Removed| A subcollection was removed from a collection.
**Partnership events**|
Account Removed From Partnership| Shared access to an account in a host-guest partnership was removed.
Account Shared Via Partnership| An account was shared via a host-guest partnership.
Partnership Accepted| A host-guest partnership request was accepted by the workspace **Admin** of a guest workspace.
Partnership Declined| The host-guest partnership request was declined by the workspace **Admin** of a guest workspace.
Partnership Requested| A host-guest partnership request was sent to a guest workspace.
Partnership Updated| The details of a partnership request were updated.
Partnership Removed| The host-guest partnership was removed by the host workspace.
**Team events**|
Team Created| A team was created in Cerby either manually or automatically from an IdP group assignment.
Team Deleted| A team was deleted in Cerby either manually or automatically from the IDP.
Team Members Changed| One or multiple team members were added or removed from a team either manually or automatically from an IdP group assignment.
Team Resources Changed| A team's shared access to one or multiple items (accounts, collections, and secrets) was granted or removed.
Team Updated| The information details of the team were updated.
**Business hub events**|
Provide Access| An automated task to invite a business hub member to an app hub was performed.
Received Tenant Access| An invite to access a business hub through Cerby was sent and received.
Member Removed From Tenant| A business hub member was removed from the app via an automated task.
Removing Account Access| Shared access to a business hub account is being removed for one or multiple users in Cerby as part of an automated task to remove app members.
Removing Member From Tenant| An automated task to remove a business hub member from an app was performed.
Removed Tenant Access| Shared access to a business hub was removed.
Sharing Of Tenant| A business hub was shared with one or multiple users.
Tenant role update| An app member's role was updated via an automated task.
Tenant Credentials Connected| A profile account was connected to a business hub.
Tenant Check For Updates| An automated task to check for updates on a business hub was performed.
Tenant user matched| The profile account of a matched user was associated with their corresponding Cerby user account.
User Account Permission Change| The Cerby role of a user on a business hub was updated.
**Workspace events**|
MFA Challenge Issued| An identity confirmation request was sent to the Cerby mobile app.
MFA Offboarded| MFA was turned off to authenticate to a local user workspace.
MFA Onboarded| MFA was turned on to authenticate to a local user workspace.
All Access Mode Disabled| All-Access Mode was disabled for a user with the workspace **Super Admin** role.
All Access Mode Enabled| All-Access Mode was enabled for a user with the workspace **Super Admin** role.
Login To Cerby| A user logged in to their Cerby workspace with credentials provided by Cerby or their IdP.
Logout of Cerby| A user logged out of their Cerby workspace.
SCIM API token retrieved| The SCIM API token was retrieved to configure user provisioning with an IDP for a Cerby workspace.
Secure Device Created| A trusted session was set up on a user's device.
User Activated| A user was activated in a local user workspace.
User added| A user was created in a workspace either manually or automatically through user provisioning from the IDP.
User Created| A user was created in a local user workspace.
User Deactivated| A user was deactivated in a local user workspace.
User Updated| The workspace role of a user was updated in a local user workspace.
App settings restrictions|
App Restriction Warning Cancelled| The user has selected the "No, thanks" option on the prompt to modify the password or member settings within an app.
App Restriction Form Submitted| The user has submitted a form of interest with the settings of an app.
