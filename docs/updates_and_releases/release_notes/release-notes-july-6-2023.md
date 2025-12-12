---
description: 
---

# Release Notes - July 6, 2023

# New Features

  * We know you wanted to save additional information in your Cerby accounts. That’s why the [Account Notes](https://help.cerby.com/en/articles/8076365-how-to-save-and-manage-account-notes) and [Custom Fields](https://help.cerby.com/en/articles/8076378-how-to-add-and-manage-custom-fields-for-your-accounts) features**** are now available on the account details page using the Cerby web app, as shown in **Figure 1**.

<figure><img src="../.gitbook/assets/T4OVgSMwK1R0HaCnP-nPNyUkCvyZ__U1oCENmYSb0od1wdHYAIFrDZEGQd_3chJZkVKd_snYFgeGeDbhaIWdb2V-OQYt-aWqTyd3fe8kxp9moEFlGxV0YouVLYsxrsDU9FNaWAxajAE8GAooaSgsokY.png" alt="Screenshot of the account details page, where you can manage your account and save information via the Notes field or new custom fields."><figcaption></figcaption></figure>

**Figure 1.** Account details page with notes and custom fields

Notes are a fixed space in all accounts where you can save additional information about your account, application, or service provider. Custom Fields are information fields you can create based on your needs and with a category name. In both features, users with shared access to the account can view the information.

Are you wondering what you can save in Account Notes or Custom Fields?

    * Expiration dates for your licenses
    * The point of contact for more information about licenses
    * The tenant to which the account or license belongs
    * Reminders
    * Links for publicly visible accounts
    * References to VPN access requirements
    * Offline account credentials
  * Need to be more thrilled? Cerby's Password Manager Importer can now transfer the notes you have stored in your LastPass passwords as Account Notes.
  * Improvements keep coming to secrets. You can now preview the list of attachments and download them when viewing a secret.
  * We’ve added more clarity on the status of users onboarded to a tenant. Instead of displaying the “Partial connection” status in the **Members** tab of the tenant details page, Cerby now displays the following:
    * “Cerby onboarded”
    * “Missing Cerby MFA onboarding”
    * “Requires Cerby Password Update”
  * We didn’t want to keep you in the dark when an error occurred during a migration using the Password Manager Importer. The**Import report** view now displays an error message with a migration ID that you can share with the Cerby Customer Support team for troubleshooting. We also send you an email with this ID.

Additionally, we included a checklist in our [documentation](https://help.cerby.com/en/articles/7175132-how-to-use-the-password-manager-importer#h_b02c825502) to ensure you have all you need before retrying the import.

  * Talking about the Password Manager Importer, we fine-tuned our instructions to help you identify your multi-factor authentication (MFA) option for LastPass.

We included a tooltip in the **Enter your login credentials** dialog box of the import wizard. Also, we mention what to do when you have push notification MFA configured.

  * Ever wanted to enter a long name for a collection? We removed the 50-character limit, and you can now write names of up to 1,024 characters. Let’s say we did it for you to unleash your creativity, not only to support long folder names imported from LastPass.
  * One more for the Password Manager Importer. Now, it’s related to permissions:
    * When users have access to a folder in LastPass but without a native role assigned, they are now granted the **Account Collaborator** role on the Cerby collection.
    * When users are invited to a folder, password, or secure note in LastPass but haven't accepted the invite, they are not granted permission in Cerby.
    * When importing subfolders from LastPass, they inherit the permissions from the parent folder and are migrated as individual collections.
  * Our Development team is on fire! Enjoy the new [tenants](https://help.cerby.com/en/articles/6831152-how-to-use-tenants) we support:
    * [Android Developer](https://www.google.com/aclk?sa=l&ai=DChcSEwjwjaKF6Pr_AhWCFq0GHRixCz8YABAAGgJwdg&sig=AOD64_2qVvxA5NSxLiQ3ntWemD0xiJYvjw&q&adurl&ved=2ahUKEwjkgZmF6Pr_AhUyJEQIHe09CswQ0Qx6BAgIEAE)
    * [GitHub](https://github.com/)
    * [LinkedIn Sales Manager](https://business.linkedin.com/sales-solutions/sales-navigator)
    * [Smartlead](https://www.smartlead.ai/)

# Fixes

  * The issue with not rotating the time-based one-time password (TOTP) after scanning the QR code with the Cerby mobile app (iOS v1.0.40 and Android v1.0.90) is fixed.
  * The issue with displaying management actions for distribution lists to all users in the **More options** drop-down list is fixed. Management actions are now enabled only for the owners of distribution lists, and they are accessible through the **Distribution Lists** view.
  * The issue with displaying an incorrect number of items in the **Pending review** tab of the **Import report** view is fixed. This issue happened after a migration using the Password Manager Importer.
  * The issue with the “Please enter a valid domain” error message when updating the information for the **Allowed login domains** field on the account details page is fixed.
  * The issue with the broken link to the Partners documentation in the **Enter Your Partner’s Information** dialog box when trying to add a partner is fixed.
  * The issue with users being able to see the **Remove from this Collection** option for other collection members who were granted access via a team is fixed. The removal action is displayed through the **More options** drop-down list in the **Members** tab of the collection details page.
  * The issue with the email notifications for incomplete automation tasks not redirecting users to the corresponding workspace is fixed.
  * The issue with being unable to migrate passwords from LastPass with the same name as an account in Cerby is fixed. The Password Manager Importer validations now only consider the username, password, and service provider or application.
  * The issue with the pagination in the **Matched users** and **Unmatched users** tabs after a migration using the Password Manager Importer is fixed.
