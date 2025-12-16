---
description: This article describes how to add Secure Shell (SSH) key pairs to your Cerby workspace.
intercom_id: 8705355
---

# Add an SSH key item

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , and **Users**
* Available to the Cerby Automate and Cerby Protect products. Cerby Protect users must have already set up their [trusted devices](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/trusted-devices/set-up-trusted-sessions-on-your-devices)
* Only supported using the Cerby web app


{% endhint %}

You can add a Secure Shell (SSH) item and attachments to Cerby in the following two ways:

* Add an SSH key item manually
* Import SSH key items from LastPass

The following sections describe each way.

* * *

## Add an SSH key item manually

To add an SSH key item and, optionally, a file attachment, you must complete the following steps using the Cerby web app:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Secrets** option from the left navigation drawer. The **Secrets** view is displayed.
  3. Click the **Add secret** button. A drop-down list is displayed.
  4. Select the **SSH keys** option from the list. The **Add SSH Key** dialog box is displayed.
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

  6. Add an attachment optionally by performing the following actions:
     1. Click the **Add attachment** button. A file dialog box is displayed.
     2. Select the file you want to add as an attachment to the secret. For more information on the size limits and supported file formats, read the [Specifications](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-secrets) section.
     3. Click the **Open** button. The file dialog box closes, and the file is displayed on the **Attachments** section.
     4. Repeat steps a to c as necessary.
  7. Select a vault where you want to save the secret from the **Vault** drop-down list.
**NOTE:** If you only have one vault, the **Vault** drop-down list is not displayed.

  8. Click the **Add Secret** button. The dialog box closes, and the secret details page is displayed.

Now you are done. You can start sharing your SSH key items securely.

* * *

## Import SSH key items from LastPass

To import SSH key items from your password manager, including their file attachments, follow the instructions in the [How to use the Password Manager Importer](https://cerby-test.gitbook.io/cerby-test/management/credential-management/item-importer/migrate-from-lastpass-to-cerby) article.

After importing your SSH key items, you can start managing access to them securely.
