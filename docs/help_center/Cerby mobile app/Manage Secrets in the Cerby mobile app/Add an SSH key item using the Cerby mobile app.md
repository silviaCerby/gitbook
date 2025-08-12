# Add an SSH key item using the Cerby mobile app

**Description:** This article describes how to add Secure Shell (SSH) key pairs to your Cerby workspace using the Cerby mobile app.

{% hint style="info" %} **Who can use this feature?** * Workspace**Owners** ,
**Super Admins** , **Admins** , and **Users** * Only supported using the Cerby
web and mobile apps {% endhint %}

To add an SSH key item using the Cerby mobile app, you must complete the
following steps:

  1. Open the Cerby mobile app on your mobile phone.

  2. Log in to your Cerby workspace.

  3. Tap the **Add** button from the bottom navigation bar. The **Select a category** screen is displayed with a list of options.

  4. Select the **SSH keys** option from the list. The**SSH Key** screen is displayed.

  5. Enter the information in the corresponding fields:

     * **SSH keys label in Cerby:** It is the name of the SSH key item that is always displayed on the secret card.

     * **Bit strength:** It is the cryptographic key length of the SSH key, measured in bits. For example, 2048, 3072, or 4096 bits.

     * **Format:** It is the encoding format of the SSH key, such as RSA or DSA.

     * Passphrase: It is a confidential phrase or password that provides an optional extra layer of security for the SSH key.

     * **Private key:** It is the private part of the SSH key pair, crucial for authenticating the user.

     * **Public key:** It is the non-sensitive, public part of the SSH key pair, shared with remote servers or services for authentication purposes.

     * **Hostname:** It is the domain name or IP address of the server associated with the SSH key.

     * **Date:** It is the date when the SSH key item was created or last modified.

     * **Notes:** It is a space for additional information or personalized notes related to the database.

  6. (Optional) Select the **Ask users to confirm their identity to view the secret** option if you want an identity challenge to be issued when users want to view it.  
​**NOTE:** You can add an identity challenge later via the Cerby web app. For
more information, read the article [Edit a secret or secret item using the
Cerby mobile app](https://help.cerby.com/en/articles/11429620-edit-a-secret-
or-secret-items-to-cerby-using-the-mobile-app).

  7. (Optional) Enter the name of a collection to which you want to add the secret in the **Collection** name.

  8. Select a vault where you want to save the secret from the **Vault** drop-down menu.  
​**NOTE:** If you only have one vault, the Vault drop-down list is not
displayed.

  9. Tap the **Save** button in iOS or **Save item** in Android. A success message box is displayed.

Now you are done. You can start managing access to your secrets securely.

