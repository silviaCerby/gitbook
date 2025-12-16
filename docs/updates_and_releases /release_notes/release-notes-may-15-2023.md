---
description: 
intercom_id: 7903600
---

# Release Notes - May 15, 2023

## New Features

* Love keeps coming to our Cerby mobile app. With the versions [v1.0.89](https://play.google.com/store/apps/details?id=com.cerby&hl=en&gl=US) for Android and [v1.0.39](https://apps.apple.com/us/app/cerby/id1533747684) for iOS, you can now do the following:
    * View secrets configured with an identity challenge. Behind the scenes, Cerby ensures that only the device requesting to view the secret can open it.
    * Know when you reached the end of the list of accounts and secrets when you scroll down. Cerby the dog will let you know, wink.
    * Access secrets inside collections.
    * View the teams with shared access to your secrets. Previously, you could only view the team members individually.
    * Identify easily if an email address or phone number is managed by Cerby. We added a tag in the account details screen.
* A secret without a text body is still a secret. That’s why we support them now.
* Talking about improvements, you can now benefit from the following using the Cerby web app:
    * A **Shared via** column was implemented in the **Members** tab of an account, secret, and collection details page. The goal is to let you know how an item is shared with you.
    * The grid view is available to display the accounts and secrets in their corresponding tab inside the collection details page.
    * A button is available to add accounts or secrets when you are on the account or secret details pages. Just activate the **Accounts** or **Secrets** tab and click the corresponding **Manage accounts** or **Manage secrets** button.
* We take information security seriously. In compliance with the SOC 2 Type II certification, we’ve implemented a **Terms of service agreement** dialog box for all our users. Please take a minute to review and accept it when it appears.
* The remaining pieces of the [Password Manager Importer](https://cerby-test.gitbook.io/cerby-test/management/credential-management/item-importer/migrate-from-lastpass-to-cerby) feature are in their place. Here’s what you can import now:
    * Folders and subfolders of secure notes with and without attachments to collections
    * Missing team members in bulk with a CSV file.
    * Account- and secret-level permissions for users.
* Tenant admins, rest assured. Now, Cerby got you covered with automatic daily checks for updates for Apple and Verizon [tenants](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-business-hubs).

## Fixes

* The issue with being unable to change the role of a team on an account via the **Teams** tab on the account details page is fixed.
* The issue with displaying long account names on the **Add Accounts** page of the **Create a Collection** wizard is fixed.
* The issue with deleting collections and accounts from the **Teams** view is fixed. Now, they disappear immediately.
* The issue with displaying a previously selected team when selecting a different team in the **Teams** view is fixed.
* The issue with matching, removing, or exempting users from a tenant is fixed. Now, the **User Overview** section is refreshed automatically after performing any of these actions.
* The issue with refreshing the list of saved versions of a secret whenever you reach the bottom of the list on the **Secret history** dialog box is fixed.
* The issue with the in-field Cerby icon disappearing from the **Update your password** dialog box for Discord is fixed.
* The issue with the number of billable accounts that involved Meta in the **Billing Report** view is fixed.
* The issue with the button for our LinkedIn profile on the [www.cerby.com](http://www.cerby.com) site redirecting to an incorrect page is fixed. Report credit: Milan Jain.
* The following issues in our newest version of the Cerby mobile app are fixed:
    * The app kept loading when tapping an empty collection.
    * The keyboard blocked the **Message** field when sharing an account and entering a message, making it difficult to know what you were writing.
