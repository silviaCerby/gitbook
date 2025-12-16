---
intercom_id: 11642821
description: >-
  This article describes how to retrieve the SCIM gateway details required to
  connect your disconnected apps to your IdP through IdLCM.
---

# Retrieve the SCIM gateway details for an IdLCM integration

{% hint style="info" %}
**Who can use this feature?**

* Workspace **Owners** , **Super** **Admins** , and **Admins**
* Only supported using the Cerby web app
{% endhint %}

Cerby uses unique SCIM gateway tokens for secure identity provider (IdP) integration with each application connected through our**Identity Lifecycle Management**(IdLCM) solution. These tokens are used to authenticate and authorize API requests between a SCIM client and a SCIM server, enabling your identity provider (IdP) to provision users to your Cerby-integrated apps.

When you set up an app integration in your IdP to connect it to your Ceby-integrated app, you must provide the SCIM gateway URL, a SCIM gateway token, and the Bookmark URL. You can retrieve these elements in the following ways:

* Retrieve the SCIM gateway URL
* Generate a SCIM gateway token
* Regenerate a SCIM gateway token
* Retrieve the Bookmark URL

The following sections describe each way.

***

## Retrieve the SCIM gateway URL

To retrieve the SCIM gateway URL of an IdLCM integration, you must complete the following steps:

1. Log in to your [Cerby](https://app.cerby.com/) workspace.
2. Select the **Integrations** option from the left menu. The **Integrations** page is displayed.
3. Select the integration you want to connect to your IdP. The integration details page is displayed with the **Settings** tab activated.
4. Activate the **Connected services** left tab.
5.  Click the **Copy** icon (

    <figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1588179532/5fef6ea13834c0f43f9ef66837b4/AD_4nXd_XKaMX07-MLc2p41ZsnNZEz1uoWBvjdhXtTD5jc-hG-fIBaIgDSgPivddZFiEzqr6oB11iZL08RAwNm_pXXS-6kqgxCvIGuCNZzUrDaVefR-eJWv8N7oRyp94nKdg3tf51yukIw?expires=1764126000&#x26;signature=87c2a99a80d0db5c506ea36209d5b07c7971c3963a0fe021e82213ea9139e820&#x26;req=dSUvHsh5lIRcW%2FMW3Hu4gYSHisTCo4%2FdzUNCnvF%2BJFTF1rqJEy%2Fh4tSaVm0b%0ANA%3D%3D%0A" alt=""><figcaption></figcaption></figure>

    ) in the **SCIM Gateway URL** field.

Now you are done. You can paste the SCIM gateway URL when required by your IdP.

***

## Generate a SCIM gateway token

To generate the SCIM gateway token for the first time for a new IdLCM integration, you must complete the following steps:

1. Log in to your [Cerby](https://app.cerby.com/) workspace.
2. Select the **Integrations** option from the left menu. The **Integrations** page is displayed.
3. Select the integration you want to connect to your IdP. The integration details page is displayed with the **Settings** tab activated.
4. Activate the **Connected services** left\*\*\*\* tab.
5. Click the **Generate token** button in the **SCIM Gateway** section. The **Generate token** dialog box is displayed, as shown in **Figure 1**. ​ **Figure 1.** **Generate token** dialog box

<figure><img src="../../../.gitbook/assets/AD_4nXc-GwvMAonKXdcTwsqAzdpaj5gGei337HZ9FVIFYlQ2l5-ELbiAUcY84B0C0ggAb42I1hSEzwctR3cNj3riiSM1ner5dZ7DzqtH7ce7g0wRej9nB2weDOw19pmyFfTpHzHCDoUw.png" alt=""><figcaption></figcaption></figure>

6.  Click the **Copy** icon (

    <figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1588180442/4ce97d6cd5978f65cbc07f7b9543/AD_4nXd_XKaMX07-MLc2p41ZsnNZEz1uoWBvjdhXtTD5jc-hG-fIBaIgDSgPivddZFiEzqr6oB11iZL08RAwNm_pXXS-6kqgxCvIGuCNZzUrDaVefR-eJWv8N7oRyp94nKdg3tf51yukIw?expires=1764126000&#x26;signature=3001622c203e1cacb875ddd0a5e9a346c03d7df6cef8e96cdfcfaab3420a9546&#x26;req=dSUvHsh2nYVbW%2FMW3Hu4gfwHxEX53%2B5XQLWYCRaZARcYUTUExEX2qHi8S%2Fdh%0ATw%3D%3D%0A" alt=""><figcaption></figcaption></figure>

    <figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1584660574/c38bf035fafcd3eec82700fe8f18/AD_4nXdC8FzycgYlwfvcVwFQMXImb5XYFdhIo3nGHLM8hi1KBzlSfub9XXSlsDyrfGMiOFjy15n-0sQGFWQbE-X6X-XEVwFM8gClRM1PO1kfbR-FniCu9k2R9HkbegoY3FadqKF9LG6DlQ?expires=1764126000&#x26;signature=b69349a9e1db96a0507c43f0968275fb6106c832c55ff28877d4af9038a6c053&#x26;req=dSUvEs94nYRYXfMW3Hu4gbC0nWjf6fQWCzyYlw3aobW1Tu91KN4uPjeU010V%0AHA%3D%3D%0A" alt=""><figcaption></figcaption></figure>

    ) to copy the authentication token to the clipboard. ​**TIP:** Keep the **Generate token** dialog box open as the generated token is only displayed once. If you lose the token, you must generate a new one.

Now you are done. You can paste the SCIM gateway token when required by your IdP.

***

## Regenerate a SCIM gateway token

To regenerate the SCIM gateway token of your IdLCM integration when you need to replace an existing token, you must complete the following steps:

1. Log in to your [Cerby](https://app.cerby.com/) workspace.
2. Select the **Integrations** option from the left menu. The **Integrations** page is displayed.
3. Select the integration you want to connect to your IdP. The integration details page is displayed with the **Settings** tab activated.
4. Activate the **Connected services** left tab.
5.  Click the **More options** (

    <figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1588180830/fc9ce04aa8509287eb01b0e74d36/AD_4nXc0zppwqIQiOEARNuT-h0vyxilm5zKN5ar1dqDpgV4CTt2LDg0mYLB3VcY1RB8rtAxj8_Ta4FHIKkb51C3VMB7tHANq2INWT_KuD-KsZiQ3GNq0_F118yFx2raZnXnHogNK_bvLwA?expires=1764126000&#x26;signature=c8509139d2584ae44669d2902ecd8bd15902c05913f7304a8e9cbbc3dbaeccef&#x26;req=dSUvHsh2nYlcWfMW3Hu4geXoWvPneHVS4XtJvNViTbTm%2BMKJL4m5UYCVchSH%0AIQ%3D%3D%0A" alt=""><figcaption></figcaption></figure>

    ) icon in the **SCIM Gateway** section. A drop-down menu is displayed.
6. Select the**Generate new token** option from the menu. The **New token** dialog box is displayed.
7. Click the**Generate new token** button. The **Generate token** dialog box is displayed.
8.  Click the **Copy** icon (

    <figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1588179940/019e49c3b272f2eaa72b6ece2eb0/AD_4nXd_XKaMX07-MLc2p41ZsnNZEz1uoWBvjdhXtTD5jc-hG-fIBaIgDSgPivddZFiEzqr6oB11iZL08RAwNm_pXXS-6kqgxCvIGuCNZzUrDaVefR-eJWv8N7oRyp94nKdg3tf51yukIw?expires=1764126000&#x26;signature=afb915f15f10d5317ed629447eb1b845eca09e8bbb8b01ae51e5116c28b173c9&#x26;req=dSUvHsh5lIhbWfMW3Hu4gTaBeCofVVYGfnU1Dd5drp2r490qBOS4S3kt7fWD%0AIg%3D%3D%0A" alt=""><figcaption></figcaption></figure>

    <figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1584661443/3e731847d8c1d38ad303c5fc6550/AD_4nXdC8FzycgYlwfvcVwFQMXImb5XYFdhIo3nGHLM8hi1KBzlSfub9XXSlsDyrfGMiOFjy15n-0sQGFWQbE-X6X-XEVwFM8gClRM1PO1kfbR-FniCu9k2R9HkbegoY3FadqKF9LG6DlQ?expires=1764126000&#x26;signature=7855c1296193920b00aa7acb6842bae74ce5155e71ae93605e70e06d09343e90&#x26;req=dSUvEs94nIVbWvMW3Hu4gUup9CZCj0VYnfmHuIG8wN1XImlFMfbiv%2BPlAYIi%0AbQ%3D%3D%0A" alt=""><figcaption></figcaption></figure>

    ) to copy the authentication token to the clipboard. ​**TIP:** Keep the **Generate token** dialog box open as the generated token is only displayed once. If you lose the token, you must regenerate a new one.

Now you are done. You can paste the SCIM gateway token when required by your IdP.

***

## Retrieve the Bookmark URL

To retrieve the Bookmark URL of an IdLCM integration, you must complete the following steps:

1. Log in to your [Cerby](https://app.cerby.com/) workspace.
2. Select the **Integrations** option from the left menu. The **Integrations** page is displayed.
3. Select the integration you want to connect to your IdP. The integration details page is displayed with the **Settings** tab activated.
4. Activate the **Connected services** left tab.
5.  Click the **Copy** icon (

    <figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1847597677/ee19ee4549736015996be130dd20/4708d0a8-d21d-4759-a4e5-fa8462da0eef?expires=1764021000&#x26;signature=bd2988e9eb56628dba8b5c71cb0a07b563d53b8087d38e6e538379287ad5d318&#x26;req=dSgjEcx3modYXvMU3HP0gCt19DJYq9IGPInXLCFlNaDJCLhOSnU%3D%0A" alt=""><figcaption></figcaption></figure>

    ) in the **Bookmark URL** field located in the **Quick access shortcut** section.
