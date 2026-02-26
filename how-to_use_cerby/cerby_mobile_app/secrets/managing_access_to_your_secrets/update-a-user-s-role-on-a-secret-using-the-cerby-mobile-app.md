---
description: "This article describes how to update a user’s role on a secret using the Cerby mobile app."
intercom_id: 9742174
---

# Update a user’s role on a secret using the Cerby mobile app

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , **Admins** , **Users** , and **Guest Users**
* Secret and secret item **Owners**
* Supported using the Cerby web app and mobile app. For the web app instructions, read the article [Update a user's role on a secret or secret item](https://help.cerby.com/en/articles/9483752-update-a-user-s-role-on-a-secret-or-secret-item)


{% endhint %}

As a secret or secret item (such as WiFi, SSH keys, database, server, and custom item) **Owner** , you can update the role of other workspace members on your items using the Cerby mobile app.

To update a user’s role on a secret, you must complete the following steps using the Cerby mobile app:

1. Open the Cerby mobile app on your phone.
2. Log in to your Cerby workspace.
3. Activate the **Secrets** tab located at the top on iOS or Android. The **Secrets** screen is displayed.
4. Tap the corresponding secret card. The secret details screen is displayed.
5. Tap the right arrow icon from the **Members** list within the **Sharing** section. The **View members** screen is displayed.
​**NOTE:** To update guest users’ role access from external parties, tap the right arrow from the **Guest users** list.

6. Select the corresponding member from the list. A menu is displayed at the bottom.
7. Tap the **Update role** button from the menu. The list of roles is displayed.
8. Select the user’s new role on the secret:

   * **Owner:** Users can share access and manage the secret configuration.
   * **Collaborator:** Users can only view the secret or secret item content.

9. Tap the **Save** button.

Now you are done.

{% hint style="danger" %}


**IMPORTANT:** Users who have received shared access to the same secret or secret item multiple times appear with the **Mixed role** status in the **Cerby role** column. When clicking the drop-down list, the **Share secret** dialog box is displayed with each access grant and role. You can only update the role if shared access is via a direct grant to the secret or a collection to which you have the **Owner** role.


{% endhint %}
