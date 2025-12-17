---
description: This article describes how to turn on and manage the Enforced autosave setting at the workspace level, applicable to all workspace users.
intercom_id: 11635871
---

# Turn on and manage enforced account autosave in the workspace

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Super** **Admins** and **Admins**
* Only supported using the Cerby web app


{% endhint %}

As a workspace **Admin** or **Super Admin** , you can configure and specify the domains where you want to apply the enforced account autosave feature.

With the **Enforced autosave** setting, Cerby automatically detects login and signup attempts on specified domains and adds a new account to Cerby using the provided credentials, without prompting the user.

The following are the enforced account autosave settings you can manage:

* [Turn on Enforced autosave in the workspace](turn-on-and-manage-enforced-account-autosave-in-the-workspace.md#id-turn-on-enforced-autosave-in-the-workspace)
* [Add a domain to Enforced autosave](turn-on-and-manage-enforced-account-autosave-in-the-workspace.md#id-add-a-domain-to-enforced-autosave)
* [Remove domains from Enforced autosave](turn-on-and-manage-enforced-account-autosave-in-the-workspace.md#id-remove-domains-from-enforced-autosave)

{% hint style="danger" %}


**IMPORTANT:** To learn how Cerby manages roles with the account autosave feature, refer to the article [Explore Account Autosave](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-account-autosave).


{% endhint %}

* * *

## Turn on Enforced autosave in the workspace

To turn on the **Enforced autosave** setting in the workspace, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using the Cerby web app.
  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed with the **General** tab activated.
  3. Activate the **Extension settings** tab. The **Prompted autosave** left tab is displayed activated.
  4. Activate the **Enforced autosave** tab.
  5. Activate the switch in the **Enforced account autosave** section to turn on the **Enforced account autosave** setting for all workspace users. The following occurs:

     * A success message is displayed.
     * The information about the user who modified the setting, the date, and time is updated.
     * The **Enter a domain for the enforced account autosave** field is displayed. To configure this list, read the following sections:
       * [Add a domain to Enforced autosave](turn-on-and-manage-enforced-account-autosave-in-the-workspace.md#id-add-a-domain-to-enforced-autosave)
       * [Remove domains from Enforced autosave](turn-on-and-manage-enforced-account-autosave-in-the-workspace.md#id-remove-domains-from-enforced-autosave)
     * Depending on whether you have added domains for enforced account autosave, these domains are listed below.
* * *

## Add a domain to Enforced autosave

To add a domain to the **Enforced account autosave** setting, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using the Cerby web app.
  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed with the **General** tab activated.
  3. Activate the **Extension settings** tab. The **Prompted autosave** left tab is displayed activated.
  4. Activate the **Enforced autosave** tab.
  5. Click the **Search for your app or type the domain** field.
  6. Enter the domain you want to add in the field. As you type, the search narrows down the results, updating the list of matches in real time.
  7. Select the domain you want to add. The domain is added to the list below.
  8. Repeat steps 5 to 7 as needed to add multiple domains.

Now you are done. Cerby will automatically add a new account to your workspace the next time any user logs in or signs up for an account in this domain.

* * *

## Remove domains from Enforced autosave

To remove one or multiple domains from the **Enforced autosave** setting, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using the Cerby web app.
  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed with the **General** tab activated.
  3. Activate the **Extension settings** tab. The **Prompted autosave** left tab is displayed activated.
  4. Activate the **Enforced autosave** tab.
  5. (Optional) Narrow down the list of domains to remove by using the following alternatives:

     * Search for the domain you want to remove from the list by clicking the **Search** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1583078273/4d34a5e7f428b64bd2cbc5f543e2/AD_4nXfjiZFFvG6pJgbkYgUBccCS5lSbD56s2AlPwTdKKRrKkJWLEjlrX8uizGceRj5ARbCq9-_lHdkmuQ6mxVAdkiStszpo2jcTgZHL5AbE-Gz-Fp05zjKIGmuB40WcJA1C8EpDgAfxAw?expires=1750734000&signature=95c65f9aa7efc7216664f2f8932c852c3b72142772930ca6d05b8d51cf7247d7&req=dSUvFcl5lYNYWvMW3Hu4gchQQuEsCbCmtzh9DBEfapN83tcfO7SxEIZXncMf%0A%2Bg%3D%3D%0A" alt="">) icon, which displays the search field. As you type, a list of all matches is displayed below in real time.
     * Sort the list by recently added, earlier added, A to Z, or Z to A by clicking the **Sort by** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1583078540/2524d6b90e4c62985846b6602601/AD_4nXeLLEc0F2qubfeOoN-0uNmM2pLasvkfgBiMPwtHn4SOOIQhFgKLVjRYQaI2540K9yemQ4KyOf49XLskRvdUPimU6BENZD23XFelzVhIFCWREfm8YRFTJ7n8N7oKhwUDYTgxmS0yLg?expires=1750734000&signature=67a9af4945fc2f47ad492e8dff36f7fc0c848cb0cf38cca37685d63dc0801f83&req=dSUvFcl5lYRbWfMW3Hu4gSJUR9psE%2FZhIm5xjrhJt4FgJxCQg59tN4gH4mlS%0ACw%3D%3D%0A" alt="">) icon next to the search field.

  6. Remove one or multiple domains as follows:

     * **One domain**

       1. Click the **Remove from list** (<img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1583078711/a7c6fbe2342b710a8e062cfe256b/AD_4nXdwev4haA9bs9GJR2tUDG-jilKafiw0AvIHkRLOsKPRV0Oj_PX8YyDsbiCKGlXRg0WCXadJ2Ztg7GDsXjYNmToPtaNtXF4Op-4QDMdrZaf_akReULyLJuRyZQ4sOEVqc2D4EIzbOA?expires=1750734000&signature=b756832d31d35e9c5171102f713305223e1eab720ab61416db827b36b3ab020b&req=dSUvFcl5lYZeWPMW3Hu4gatddfa2oBLwqFjmVZG6t6ZAs5vll6Bq805YpF4F%0AJg%3D%3D%0A" alt="">) icon on the right side of the domain name. A success message appears, and the domain is removed from the list.

     * **Multiple domains**

       1. Select the domains you want to remove from the list. A menu is displayed at the bottom of the page indicating the number of domains you have selected.

       **TIP:** To deselect all domains, you have two alternatives in the menu at the bottom: the **Deselect all** button and the **Close selection** (<img src="../../../../../.gitbook/assets/AD_4nXfmYlyJH5hoymGxAgNMtuZN17IyS81uXHuExwviaDkbR_TQIZOgt2cDx0Ulc0vNgfd0Og9LaT4RY5Kd1m2EqNn9oE5pPBhcU7Dqk3mqObGLPuaDl7Dl33lJpntwDd-KHuvWTW6h.png" alt="">) button, which also closes the menu.

       2. Click the **Remove from list** option in the menu at the bottom. A success message appears, and the selected domains are removed from the list.

Now you are done.
