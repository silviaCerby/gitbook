# Confirm your identity with Cerby's MFA methods

## This article describes Cerby’s MFA methods for verifying a user’s identity when managing secrets and Apps and performing other actions.

With Cerby's **multi-factor authentication (MFA) methods**, you can choose how users verify their identities through a push notification on the Cerby mobile app or via an email with a magic link. These methods ensure secure access for performing identity-sensitive actions, such as viewing or editing a secret, regardless of any device constraints.

This article describes how each MFA method works and the actions that require identity verification:

* [Push notification on the Cerby mobile app](#push-notification-on-the-cerby-mobile-app)  
* [Email magic link](#email-magic-link)  
* [List of actions that require identity verification](#list-of-actions-that-require-identity-verification)

The following sections contain the steps to verify your identity using each method.

# Push notification on the Cerby mobile app {#push-notification-on-the-cerby-mobile-app}

With the push notification on the Cerby mobile app, you receive a push notification in real time on your registered mobile device whenever you need to verify your identity.  

| IMPORTANT: Cerby is configured to use this method by default to verify users’ identities for the actions listed in the [List of actions that require identity verification](#list-of-actions-that-require-identity-verification) section. |
| :---- |

To verify your identity through the Cerby mobile app, you must complete the following steps:

1. [Install the Cerby mobile app](https://help.cerby.com/en/articles/6395363-getting-started-guide-for-account-owners-and-collaborators#h_116820eaaa) on your phone.  
2. Set up a [trusted session](https://help.cerby.com/en/articles/8142370-set-up-trusted-sessions-on-your-devices) with your mobile device.  
3. Perform any of the actions listed in the [List of actions that require identity verification](#list-of-actions-that-require-identity-verification) section. The **Confirm your identity to continue** dialog box is displayed, and a push notification is sent to the Cerby mobile app.   
4. Tap the **It’s me\!** button in the **Confirmation Request** screen of the Cerby mobile app. The **Confirm your identity to continue** dialog box closes in the Cerby web app, and a success message box is displayed.

# Email magic link {#email-magic-link}

The email magic link is an alternative if you have restrictions or issues with receiving push notifications on your phone or if your company prefers verifying users’ identities through email. When this option is enabled, you receive an email containing a magic link that, when clicked, verifies your identity in the Cerby web app and grants access.

| IMPORTANT: If you are interested in this feature but don't see it available in your workspace, contact our Customer Support team via email at [support@cerby.com](mailto:support@cerby.com). |
| :---- |

To verify your identity through an email magic link, you must complete the following steps:

1. Perform any of the actions listed in the [List of actions that require identity verification](#list-of-actions-that-require-identity-verification) section. The **Confirm your identity to continue** dialog box is displayed.  
   **NOTE:** The actions apply to any of the Cerby clients: web app, browser extension, and mobile app.  
2. Click the **Send email** button. The **Check your inbox** dialog box is displayed, and Cerby sends an email with a magic link to your inbox.  
3. Open the **Action required: Confirm your identity** email in your inbox.   
4. Click or tap the **Confirm my identity** magic link from the email message. The Cerby web app is displayed on a new browser tab:  
   * If the identity verification is correct, then the **Identity is confirmed. Your good to go\!** message is displayed, and you are redirected to the action you previously performed.  
   * If the identity verification fails, an error message is displayed, and you must repeat the identity verification process.

# List of actions that require identity verification {#list-of-actions-that-require-identity-verification}

You must verify your identity when performing the following actions:

* [Managing the attachments of a secret and secret item](https://help.cerby.com/en/articles/8705439-manage-the-attachments-of-a-secret-and-secret-item)  
* [Deleting a secret and secret item](https://help.cerby.com/en/articles/8705456-delete-a-secret-and-secret-item)  
* [Editing a secret](https://help.cerby.com/en/articles/8705406-edit-a-secret)  
* [Viewing a secret](https://help.cerby.com/en/articles/8705383-view-a-secret) (only if the identity verification is configured)  
* [Viewing the secret history and restoring a secret](https://help.cerby.com/en/articles/8705415-view-the-secret-history-and-restore-a-secret)  
* [Share a secret or secret item](https://help.cerby.com/en/articles/8705424-manage-access-to-your-secrets-and-secret-items)  
* [Removing an App](https://help.cerby.com/en/articles/9046230-remove-an-app)  
* [Retrieving the SCIM API authentication token from Cerby](https://help.cerby.com/en/articles/5683294-retrieve-the-scim-api-authentication-token-from-cerby)  
* [Sharing items with external users via a link](https://help.cerby.com/en/articles/8308908-how-to-share-items-with-external-users-via-a-link)  
* [Creating and managing a vault](https://help.cerby.com/en/articles/8376564-how-to-create-and-manage-a-vault)

Notes:

* If you deny access through mobile, the user does not receive any notification  
* In mobile, the decrypting of your secret does not close automatically

Docs to update:

* Manage the attachments of a secret and secret item  
  * [https://help.cerby.com/en/articles/8705439-manage-the-attachments-of-a-secret-and-secret-item](https://help.cerby.com/en/articles/8705439-manage-the-attachments-of-a-secret-and-secret-item)   
* Delete a secret and secret item  
  * [https://help.cerby.com/en/articles/8705456-delete-a-secret-and-secret-item](https://help.cerby.com/en/articles/8705456-delete-a-secret-and-secret-item)   
* Edit a secret  
  * [https://help.cerby.com/en/articles/8705406-edit-a-secret](https://help.cerby.com/en/articles/8705406-edit-a-secret)   
* View a secret  
  * [https://help.cerby.com/en/articles/8705383-view-a-secret](https://help.cerby.com/en/articles/8705383-view-a-secret)   
* View the secret history and restore a secret  
  * [https://help.cerby.com/en/articles/8705415-view-the-secret-history-and-restore-a-secret](https://help.cerby.com/en/articles/8705415-view-the-secret-history-and-restore-a-secret)   
* Manage access to your secrets and secret items  
  * [https://help.cerby.com/en/articles/8705424-manage-access-to-your-secrets-and-secret-items](https://help.cerby.com/en/articles/8705424-manage-access-to-your-secrets-and-secret-items)   
* Remove an App  
  * [https://help.cerby.com/en/articles/9046230-remove-an-app](https://help.cerby.com/en/articles/9046230-remove-an-app)   
* Retrieve the SCIM API authentication token from Cerby  
  * [https://help.cerby.com/en/articles/5683294-retrieve-the-scim-api-authentication-token-from-cerby](https://help.cerby.com/en/articles/5683294-retrieve-the-scim-api-authentication-token-from-cerby)   
* How to share items with external users via a link  
  * [https://help.cerby.com/en/articles/8308908-how-to-share-items-with-external-users-via-a-link](https://help.cerby.com/en/articles/8308908-how-to-share-items-with-external-users-via-a-link)   
* How to create and manage a vault  
  * [https://help.cerby.com/en/articles/8376564-how-to-create-and-manage-a-vault](https://help.cerby.com/en/articles/8376564-how-to-create-and-manage-a-vault) 

