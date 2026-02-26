---
description: "This article describes how to retrieve a bearer token to use in the Cerby CLI."
intercom_id: 9450993
---

# Retrieve a bearer token

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , and **Admins**
* Only supported using the Cerby web app


{% endhint %}

To retrieve a bearer token, you must complete the following steps:

1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace using the Cerby web app.
2. Click your user profile located at the top right of the page. A drop-down list is displayed.
3. Select the**My Profile** option. The **My Profile** page is displayed with the **General** tab activated.
4. Activate the **Dev Tools** tab. The **Developer tools** section is displayed with the **Copy Bearer Token** information.
5. Click the **Copy token** button. Your bearer token is copied to the clipboard.

{% hint style="danger" %}


**IMPORTANT:** You must never share your bearer token with other users or store it in a visible place. Your bearer token is your unique identifier to perform different activities on Cerby, depending on your role. Be aware that bearer tokens expire after one hour.


{% endhint %}

Now you are done. You can start using the bearer token to [authenticate and log in to the Cerby CLI](https://help.cerby.com/en/articles/9132804-authenticate-with-the-cerby-cli#h_7e37d0e3a8).
