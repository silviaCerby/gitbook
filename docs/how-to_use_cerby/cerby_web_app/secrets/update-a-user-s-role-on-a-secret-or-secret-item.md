---
description: "This article describes how to update the role of other workspace members on your secrets and secret items."
intercom_id: 9483752
---

# Update a user's role on a secret or secret item

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , **Users** , and **Guest Users**
* Secret and secret item **Owners**
* Supported using the Cerby web app and the Cerby mobile app
* **NOTE:** For the Cerby mobile app, read the article [Update a user’s role on a secret using the Cerby mobile app](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-mobile-app/secrets/update-a-user-s-role-on-a-secret-using-the-cerby-mobile-app)


{% endhint %}

As a secret or secret item (such as WiFi, SSH keys, database, server, and custom item) **Owner** , you can update the role of other workspace members on your items using the Cerby web app. To do so, you must complete the following steps:

1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
2. Select the **Secrets** option from the left navigation drawer. The **Secrets** view is displayed.
3. Click the **Settings** (<img src="../../../../.gitbook/assets/unnamed_45.png" alt="">) icon of the corresponding secret card. The secret details page is displayed with the **Settings** tab activated.

**NOTE:** If an identity challenge is configured, the **Confirm your identity to continue** dialog box is displayed, and a push notification is sent to your Cerby mobile app:

   1. Confirm your identity by tapping the**It’s me!** button from the **Confirmation Request** screen of your Cerby mobile app. The **Confirm your identity to continue** dialog box closes in the Cerby web app, and the secret details page is displayed with the **Settings** tab activated.
4. Activate the **Members** tab. The **User Overview** section is displayed with a table of users who have shared access to the secret or secret item.
5. Select the option from the **Cerby role** drop-down list that corresponds to the new role on the secret or secret item:

   * **Owner:** Members can share access, edit, add attachments, and manage the secret settings.
   * **Collaborator:** Members can only view the secret and download the attachments.

   **IMPORTANT:** Users who have received shared access to the same secret or secret item multiple times appear with the **Mixed role** status in the **Cerby role** column. When clicking the drop-down list, the **Share secret** dialog box is displayed with each access grant and role. You can only update the role if shared access is via a direct grant to the secret or a collection to which you have the **Owner** role.

A success message box is displayed.

Now you are done.
