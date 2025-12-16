---
description: This article describes how to disable a vault.
intercom_id: 10113683
---

# Disable a vault

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super Admins** , and **Admins**
* Only supported using the Cerby web app
* **IMPORTANT:** If you use local vaults, you must have already set up at least one trusted session on your devices. For instructions, read the article [Set up trusted sessions on your devices](https://cerby-test.gitbook.io/cerby-test/management/workspace-configuration/trusted-devices/set-up-trusted-sessions-on-your-devices)


{% endhint %}

To disable a vault, you must complete the following steps:

{% hint style="danger" %}


**IMPORTANT:** You cannot disable AWS KMS vaults.


{% endhint %}

  1. Log in to your [Cerby](https://app.cerby.com/) workspace using the Cerby web app.
  2. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed.
  3. Activate the **Privacy and security** tab. A table with a list of vaults is displayed in the **Vault** **management** section.
  4. Click the **More options** (<figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1248048078/083eeb369ebb4477dcf480f4a793/AD_4nXfjfsmJ5IFnMdV4S4DYV40cLIIQ2pLZ4ffuhose8yIDFAt6MPWWw9NQU9a0dTOTv77HKeS43K2jPKQH-G9OdkzWRgTbYqqPBHag2ZjJkXpq53SzHBNGCdPJvSZALO-afM8B8JmpfB2yM96BjNEVbIx51yR0?expires=1754568000&signature=02b7d80ee208cba044e035635e4f4573443322f270b3058acec402377f6c1f2d&req=dSIjHsl6lYFYUfMW3Hu4gV6JxLpYYw%2FGS4xv89hnbkeFuw3CxxDcgXUO4Bjc%0Afg%3D%3D%0A" alt=""><figcaption></figcaption></figure>) icon of the corresponding vault. A drop-down list is displayed.
  5. Select the **Disable vault** option from the list. The **Disable vault?** dialog box is displayed.
  6. Click the **Disable vault** button. The **Confirm your identity to continue** dialog box is displayed, and a push notification is sent to your Cerby mobile app.
  7. Confirm your identity by using one of[ Cerby's multi-factor authentication methods](https://cerby-test.gitbook.io/cerby-test/management/identity-providers-idps/scim/set-up-your-identity-with-cerby-s-mfa-methods). The vault is displayed in the table with the **Disabled** status.
