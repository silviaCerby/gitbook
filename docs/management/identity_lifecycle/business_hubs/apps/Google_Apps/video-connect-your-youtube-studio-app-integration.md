---
description: "[Article description] This video shows how to add the YouTube app integration to manage access to it and its assets from Cerby centrally."
intercom_id: 9186795
---

# [Video] Connect your YouTube Studio app integration

## Key concepts

* Learn how to connect the YouTube app integration to Cerby to manage user access centrally.
* Understand the prerequisites, including creating a service account in your corporate identity provider (IdP) and ensuring it has the **Owner** or **Manager** role on your YouTube channel.
* Follow step-by-step instructions to configure the integration, including entering channel details and selecting user management methods.

{% hint style="danger" %}


**IMPORTANT:** For a successful onboarding, make sure you meet the following prerequisites before getting started:

* The **Channel ID** of your YouTube channel. You can copy the ID from the [Advanced settings](https://www.youtube.com/account_advanced) of your YouTube Studio account. For more information, read the [Find your YouTube user & channel IDs](https://support.google.com/youtube/answer/3250431?hl=en) official documentation
* A service account in the IdP (Okta, Entra ID, Jumpcloud, Other) with the following characteristics:
  * It must have the Google Suite apps assigned; thus, having access to the Gmail Inbox
  * It must have the **Owner** or **Manager** role on the YouTube channel
  * It must have the multi-factor authentication (MFA) method enabled for the Google account, thus accepting authenticator apps, such as Google Authenticator or Phone MFA. The steps to turn on MFA are referenced in the following videos:

    1. [How to add a Cerby-managed email or phone number to your account](https://cerby-test.gitbook.io/cerby-test/management/identity-lifecycle/business-hubs/apps/google-apps/video-connect-your-youtube-studio-app-integration)
    2. [How to turn on MFA for Google manually](https://cerby-test.gitbook.io/cerby-test/how-to-use-cerby/cerby-web-app/accounts/protecting-your-account/video-how-to-turn-on-mfa-for-google-manually)

  * It must be used exclusively to add the YouTube app integration to Cerby; thus, don't assign it to a user
  * It must be added to your channel with the Manager role. For more information, read the [Add or remove access to your YouTube channel with channel permissions](https://support.google.com/youtube/answer/9481328?hl=en#:~:text=Tap%20your%20profile%20picture%20.,you'd%20like%20to%20invite.) official documentation


{% endhint %}

## 1\. Complete the prerequisites before onboarding YouTube Studio to Cerby

Check the video to verify you fulfill the prerequisites before onboarding YouTube Studio to Cerby.

* Verify you are the "Owner" or "Manager" of your YouTube channels: <https://www.youtube.com/account>

{% embed url="https://play.vidyard.com/pjRzcF6EuRYuctkDTXQpSR" %}

## 2\. Connect the YouTube Studio app integration

Complete the instructions in the video to connect the YouTube Studio app integration.

{% embed url="https://play.vidyard.com/sW3cv4rspAnhVgQbou3i9D" %}
