---
intercom_id: 8054798
---

# Release Notes - June 26, 2023

## New Features

* We keep improving our automation to make your work easier. The checks for updates and data syncs for tenants and business centers now automatically match users with their Cerby accounts.
* Talking about improvements, we continue refining our roles to provide you with the best experience and control. Now, users with the **Account Collaborator** role on an account can only see the **Log in** button on the account details page.
* We don’t want to annoy you with never-ending prompts. The feature to save your credentials at login via the Cerby browser extension now only asks three times if you want to add an account to Cerby.
* We’ve given a makeover to the table of users in the **Members** tab of a tenant. Enjoy the improved user experience!
* The pagination in the **Activity** view is now collapsed. So, forget about seeing multiple pages listed.
* The auto-generated user profile avatars for teams no longer support special characters. Get ready to see only letters.
* An improvement for collections to provide visibility about teams. The **Teams** tab is now available on the collection details page, where you can share or remove collections from teams, as well as change the role of the team on the collections.

## Fixes

* The issue with being unable to request access to an account after an import from LastPass is fixed.
* The issue with the business ID of a Meta Business Manager account not being updated on the account details page after editing it is fixed.
* The issue with displaying “Never” in the **Last Used** column of the **Members** tab inside the collection details page is fixed.
* The issue with being unable to enter URLs longer than 50 characters when adding an account through the **Add account** wizard is fixed.
* The issue with entering an incorrect secret key when setting up multi-factor authentication (MFA) for an account and still seeing a success message box is fixed.
* The issue with displaying a loading skeleton for empty teams through the **Teams** view is fixed.
* The issue with editing the body of a secret and not updating the text is fixed.
* The issue with the Cerby web app breaking when a migration error occurs is fixed. We also extended the waiting time for an import to be performed to avoid timeout errors.
* The issue with not identifying by domain the non-supported accounts after an import from LastPass is fixed. We now display the domain.
