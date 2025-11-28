# Add a secret

**Description:** This article describes how to add a secret to Cerby.

{% hint style="info" %} **Who can use this feature?** * Workspace**Owners** ,
**Super Admins** , **Admins** , and **Users** * Supported using the Cerby web
app and mobile app. For information about how to add a secret in the Cerby
mobile app, read the article [Add a secret to Cerby in the mobile
app](https://help.cerby.com/en/articles/11429477-add-a-secret-to-cerby-in-the-
mobile-app) **IMPORTANT:** If you use local vaults, you must have already set
up at least one [trusted
session](https://help.cerby.com/en/articles/8142370-set-up- trusted-sessions-
on-your-devices) on your devices. {% endhint %}

As a user with any workspace role, except the **Login-Only** and **Guest
User** roles, you can add secrets and attachments to Cerby in the following
two ways:

  * Add a secret manually

  * Import secrets from LastPass

The following sections describe each way.

* * *

# **Add a secret manually**

To add a secret and a file attachment manually using the Cerby web app, you
must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Secrets** option from the left menu. The **Secrets** page is displayed.

  3. Click the **Add secret** button. A drop-down menu is displayed.

  4. Select the **Secret** option from the menu. The **Add Secret** dialog box is displayed.

  5. Enter the information in the corresponding fields:

     * **Secret label in Cerby:** It is the name of the secret that is always displayed on the secret card.

     * **Notes:** It is the body of the secret that only users with shared access can view. You can enter up to 45,000 characters.

  6. (Optional) Add an attachment by completing the following steps:

     1. Click the **Add attachment** button. A file dialog box is displayed.

     2. Select the file you want to attach to the secret. For more information on the size limits and supported file formats, read the [Attachment and input specifications](https://help.cerby.com/en/articles/7216784-explore-secrets#h_4d6ff4fb5e) section.

     3. Click the **Open** button. The file dialog box closes, and the file is displayed in the **Attachments** section.

     4. Repeat steps a to c as necessary.

  7. (Optional) Make the secret temporary by completing the following steps:

     1. Select the **Set expiration for this secret** option. The **Expiration time** drop-down menu is displayed.

     2. Select the corresponding option from the **Expiration time** drop-down menu:

        * **1 Day**

        * **2 Days**

        * **7 Days**

        * **14 Days**

        * **Custom  
IMPORTANT: **When selecting the Custom option, a calendar is displayed for you
to choose a specific date and click Apply. Your choice in the calendar is
limited to one month or 30 days. For more information about temporary secrets,
read the article [Explore
Secrets](https://help.cerby.com/en/articles/7216784-explore-
secrets#h_1f4ba25ffc).

  8. (Optional) Enter the name of a collection to which you want to add the secret in the **Collection** name.

  9. Select a vault where you want to save the secret from the **Vault** drop-down menu.

**NOTE:** If you only have one vault, the **Vault** drop-down list is not
displayed.

  10. (Optional) Select the **Ask users to confirm their identity to view the secret** option if you want an identity challenge to be issued when users want to view it.

**NOTE:** To add an identity challenge later, activate the **Request users to
confirm their identity to view the secret** switch in the **Settings** section
of the secret details page. For more information, read the article [Edit a
secret](https://help.cerby.com/en/articles/8705406-edit-a-secret).

  11. Click the **Add Secret** button. The dialog box closes, and the secret details page is displayed with the **Settings** tab activated.

Now you are done. You can start managing access to your secrets securely.

* * *

# **Import secrets from LastPass**

To import secure notes from your password manager as secrets in Cerby,
including their file attachments, follow the instructions in the [How to use
the Password Manager Importer](https://help.cerby.com/en/articles/7175132-how-
to-use-the-password-manager-importer) article.

After importing your secrets, you can start managing access to them securely.

