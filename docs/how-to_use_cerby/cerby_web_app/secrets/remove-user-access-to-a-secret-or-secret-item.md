---
description: This article describes how to remove user access to a secret or secret item.
intercom_id: 9483805
---

# Remove user access to a secret or secret item

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , **Users** , and **Guest Users**
* Secret and secret item **Owners**
* Supported using the Cerby web app and mobile app
* **NOTE:** For the Cerby mobile app, read the article [Remove user access to a secret or secret item using the Cerby mobile app](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-mobile-app/secrets/remove-user-access-to-a-secret-or-secret-item-using-the-cerby-mobile-app)


{% endhint %}

As a secret or secret item (such as WiFi, SSH keys, database, server, and custom item) **Owner**.

To remove user access to a secret or secret item, you must complete the following steps using the Cerby web app:

1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
2. Select the **Secrets** option from the left navigation drawer. The **Secrets** view is displayed.
3. Click the **Settings** (<img src="../../../../.gitbook/assets/unnamed_42.png" alt="">) icon of the corresponding secret card. The secret details page is displayed with the **Settings** tab activated.

**NOTE:** If an identity challenge is configured, the **Confirm your identity to continue** dialog box is displayed, and a push notification is sent to your Cerby mobile app:

   1. Confirm your identity by tapping the**It’s me!** button from the **Confirmation Request** screen of your Cerby mobile app. The **Confirm your identity to continue** dialog box closes in the Cerby web app, and the secret details page is displayed with the **Settings** tab activated.
4. Activate the **Members** tab. The **User Overview** section is displayed with a table of users who have shared access to the secret or secret item.

**NOTE:** To remove guest user access from external parties, activate the **Guest users** tab.

5. Click the **More options** (<img src="../../../../.gitbook/assets/unnamed_43.png" alt="">) icon of the corresponding user. A drop-down list is displayed.
6. Select the **Remove access** option. The **Remove access?** dialog box is displayed.
7. Click the **Remove access** button. The dialog box closes, and a success message box is displayed.

Now you are done.
