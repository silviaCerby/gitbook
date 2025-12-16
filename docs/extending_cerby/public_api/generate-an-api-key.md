---
description: This article describes how to generate an API key to use in your requests to the Cerby API.
intercom_id: 9450943
---

# Generate an API key

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , and **Admins**
* Only supported using the Cerby web app


{% endhint %}

To generate an API key, you must complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed.
  3. Activate the **API keys** tab. A table of API keys is displayed.
  4. Click the **Generate API key** button. The **Generate API key** wizard is displayed.
  5. Enter and select the information of your key in the corresponding fields:

     * **API key name:** It is the name of your API key.
     * **Expiration time:** It is the expiration time of your API key. Select the corresponding option from the drop-down list:
       * 1 hour
       * 12 hours
       * 1 day
       * 5 days
       * 1 year
       * Custom

  6. Click the **Next** button. The **Select scopes** page of the wizard is displayed.
  7. Select the options that correspond to the scopes you want to assign to the API key for reading and writing data:

     * **Read activities:** Enables reading activity data.
     * **Read items:** Enables reading account, secret, and collection data.
     * **Read accounts:** Enables reading account data.
     * **Read secrets:** Enables reading secret data.
     * **Read users:** Enables reading user and team data.
     * **Read integrations:** Enables reading integration and entitlement data.
     * **Write integrations:** Enables writing integration and entitlement data.
     * **Read automated jobs:** Enables reading automated job data.
     * **Write automated jobs:** Enables writing automated job data.

  8. Click the **Next** button. The **Store your API key** page of the wizard is displayed with the API key masked.
**IMPORTANT:** This is the only time you can view and copy the API key before it is hashed and stored in the Cerby platform. Make sure you store it in a safe place or save it as a secret in Cerby to use it in your API requests.
To save your API key as a secret in Cerby, complete the following steps:

     1. Select a vault where you want to save the API key from the **Select vault** drop-down list.
**NOTE:** If you only have one vault, the **Select vault** drop-down list is not displayed.

     2. Click the **Save in Cerby** button. The **Save your API key in Cerby?** page of the wizard is displayed.
     3. Click the **Save in Cerby** button. The dialog box closes, and the new key is displayed in the table of API keys with the “Active” status and saved as a secret in Cerby.
  9. Select the “I have stored the key in a safe place” option.
  10. Click the **Done** button. The wizard closes, and the new key is displayed in the table of API keys with the “Active” status.

Now you are done. You can start using the API key to [authenticate your API requests](https://developer.cerby.com/#authentication) by including it in the **X-API-Key** header.
