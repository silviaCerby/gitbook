---
description: This article describes how to configure MFA in Instagram manually using a Cerby-managed phone number and email address.
intercom_id: 5946657
---

# Configure MFA in Instagram manually

The Cerby platform has a central feature that enables users to automatically configure multi-factor authentication (MFA) for their accounts with service providers. This feature adds an extra layer of security to authentication processes.

However, not all service providers support automation for configuring MFA from Cerby. In these cases, users must manually configure MFA on the platforms of their service providers.

## Supported Features

The following are the supported features for configuring MMFA in Instagram:

* **Auto-login from Instagram.** This streamlined process occurs when users log out of Instagram and log in using the Cerby browser extension. The extension automatically fills in the username and password on the login page and the login code on the authentication challenge page.
* **Recovery codes backup.** This feature enables users to save in Cerby the recovery codes provided by Instagram after configuring MFA so that they can retrieve them whenever necessary from their corresponding workspace.

## Requirements

The following are the requirements to configure MFA in Instagram:

* An account in Cerby with an **Account Owner** role.
* An Instagram account onboarded in Cerby.
* An active Instagram account.
* The Instagram mobile application installed on your mobile phone.

## Configure MFA on Instagram

To configure MFA on Instagram, you must complete different steps depending on the platform you use:

* [Turning on MFA with the Browser](configure-mfa-in-instagram-manually.md#id-turn-on-mfa-with-the-browser)
* [Turning on MFA with the Mobile Application](configure-mfa-in-instagram-manually.md#id-turn-on-mfa-with-the-mobile-application)

**NOTE:** When configuring MFA with the browser, Instagram only supports phone numbers as a verification method. However, you can configure both a phone number and an authentication application using the Instagram mobile application.

The following sections describe the steps to configure MFA using each platform.

## Turn on MFA with the browser

To turn on MFA with the browser, you must complete the following main steps from the Instagram website:

1. [Access the MFA settings](configure-mfa-in-instagram-manually.md#id-1.-access-the-mfa-settings)
2. [Select a verification method](configure-mfa-in-instagram-manually.md#id-2.-select-a-verification-method)
3. [Enter the confirmation code](configure-mfa-in-instagram-manually.md#id-3.-enter-the-confirmation-code)

The following sections describe each main step.

### 1\. Access the MFA settings

To access the MFA settings, complete the following steps:

1. Log in to your [Instagram](https://www.instagram.com/) account.
2. Click the **Profile** button with your picture or avatar located at the top right of the screen. A drop-down list is displayed.
3. Select the **Settings** option from the drop-down list. The **Edit Profile** page is displayed.
4. Click the **Privacy and Security** button from the left navigation drawer. The **Privacy and Security** page is displayed.
5. Click the **Edit Two-Factor Authentication Setting** button located in the **Two-Factor Authentication** section. The **Two-Factor Authentication** page is displayed.

**IMPORTANT:** If the checkbox of the **Use Text Message** option is selected, it means you have already turned on MFA and configured a phone number. Part of this phone number is hidden in a message, for example, “We'll send a code to ****1234.” You must turn off MFA before proceeding with the instructions. To turn off MFA, complete the following steps:

1. Select the **Use Text Message** option. The **Turn This Off?** dialog box is displayed.
2. Click the **Turn Off** button. The dialog box closes, the “Settings saved.” message is displayed at the bottom of the **Two-Factor Authentication** page, and the checkbox of the **Use Text Message** option is deselected.

### 2\. Select a verification method

To select a Cerby-managed phone number as a verification method, complete the following steps from the **Two-Factor Authentication** page:

1. Select the **Use Text Message** option. The **Turn This On?** dialog box is displayed.
2. Click the **Turn On** button. The dialog box closes, and a page with a **Phone Number** field is displayed.

**NOTE:** If the **Phone Number** field displays a phone number, it means that number was already configured. You can change it to a Cerby-managed phone number in step 3.

3. Enter the phone number provided by Cerby in the **Phone number** field. Instagram uses this phone number to send a verification code. To create a phone number managed by Cerby, follow the [Creating a Cerby-Managed Phone Number or Email Address](configure-mfa-in-instagram-manually.md#id-create-a-cerby-managed-phone-number-or-email-address) instructions.

**IMPORTANT:** Make sure to enter a plus (+) sign and the country code before the 10-digit phone number.

4. Click the **Next** button. The **Confirmation** page is displayed.

### 3\. Enter the confirmation code

To enter the confirmation code, complete the following steps from the **Confirmation** page.

1. Enter the confirmation code in the **Confirmation Code** field. This code is sent by Instagram to the phone number you have created in Cerby. To retrieve the code, follow the instructions to [Retrieve the verification code from Cerby](configure-mfa-in-instagram-manually.md#id-retrieve-the-verification-code-from-cerby).
2. Click the **Done** button. The “Settings saved.” message box is displayed at the bottom of the screen and automatically closes after several seconds.
3. Refresh the page. The **Two-Factor Authentication** page displays the checkbox for the **Use Text Message** option selected.

Now you have turned on MFA with a Cerby-managed phone number.

## Turn on MFA with the mobile application

To turn on MFA with the Instagram mobile application, you must complete the following main steps:

1. [Access the MFA settings](configure-mfa-in-instagram-manually.md#id-1.-access-the-mfa-settings)
2. [Select a verification method](configure-mfa-in-instagram-manually.md#id-2.-select-a-verification-method)

The following sections describe each main step.

### 1\. Access the MFA Settings

To access the MFA settings, complete the following steps from the Instagram mobile application:

1. Log in to your Instagram account.
2. Tap the **Profile** button with your picture or avatar located on the right in the bottom navigation drawer. The **Edit profile** screen is displayed.
3. Tap the **Home** button located in the top right of the screen. A drop-down list is displayed.
4. Tap the **Settings** button from the drop-down list. The **Settings** page is displayed.
5. Tap the **Security** button. The **Security** page is displayed.
6. Tap the **Two-factor authentication** button located in the **Login security** section. The **Two-Factor Authentication** page is displayed with the **Add extra security to your account** section.

**NOTE:** If you have previously turned on MFA, the **Two-Factor Authentication** screen displays the **Two-factor authentication is on** section with the verification methods options with an “On” status. Follow the corresponding instructions to change the verification methods to an “On” status:

   * [Add an authentication application](configure-mfa-in-instagram-manually.md#id-add-an-authentication-application)
   * [Change the verified phone number](configure-mfa-in-instagram-manually.md#id-change-the-verified-phone-number)

7. Tap the **Get started** button. The **Two-Factor Authentication** page is displayed with the **Choose your security method** section. You are prompted to select at least one of three security methods.

### 2\. Select a Verification Method

To select a verification method, you must complete different steps from the **Two-Factor Authentication** screen with the **Choose your security method** section, depending on the switch you activate:

* **[Authentication app](configure-mfa-in-instagram-manually.md#id-authentication-app)**
* **[Text message](configure-mfa-in-instagram-manually.md#id-text-message)**

**NOTE:** Cerby recommends enabling the **Authentication app** method as your primary verification method for MFA, and **Text message** , as secondary.

The following sections describe the steps to configure each verification method.

### Authentication App

To select Cerby as the **Authentication app** verification method, complete the following steps:

1. Activate the **Authentication app** switch. The **Authentication app** screen is displayed.
2. Click the **Set Up Another Way** button. The **Your Key** screen is displayed with a secret key.

**TIP:** Click the **Copy Key** button to copy the secret key to the clipboard. You need this key to link your Instagram account to Cerby with the mobile application.

3. Link your Instagram account to Cerby using the secret key. To link your account, follow the corresponding instructions depending on the platform you use:

   * [Linking your account with the Cerby mobile application](configure-mfa-in-instagram-manually.md#id-link-your-account-with-the-cerby-mobile-application)
   * [Linking your account with the Cerby web application](configure-mfa-in-instagram-manually.md#id-link-your-account-with-the-cerby-web-application)

4. Click the **Next** button. The **Confirmation code** screen is displayed.
5. Enter the confirmation code provided by Cerby in the **Enter Confirmation Code** field.
6. Click the **Next** button. The **Confirmation** screen is displayed.
7. Click the **Done** button. The **Account Recovery** screen is displayed with a list of recovery codes that you can use if you lose your mobile phone or cannot receive codes via SMS or an authentication app.
8. Save the recovery codes in Cerby to retrieve them from your workspace whenever needed. To save the codes, follow the [Saving Recovery Codes in Cerby](configure-mfa-in-instagram-manually.md#id-save-recovery-codes-in-cerby) instructions.
9. Click the **Back** button. The **Two-Factor Authentication** screen is displayed, and the Authentication app switch is in “On” status.

### Link your account with the Cerby mobile application

To link your Instagram account with the Cerby mobile application, complete the following steps:

1. Log in to your corresponding workspace using the Cerby mobile application.
2. Tap your Instagram account card. A menu is displayed at the bottom of the screen.
3. Tap the **Scan Code** button at the bottom of the menu in the Add a second layer of protection section. Your mobile phone's camera view will be displayed.
4. Tap the **Can’t scan the QR code?** button. The **Scan QR code** screen is displayed.
5. Enter the secret key provided by Instagram in the **Secret Key** field.

**TIP:** Paste the secret key that you copied previously to the clipboard.

**IMPORTANT:** Remove the spaces in the alphanumeric secret key.

6. Click the **Save Secret** button. A screen with a confirmation code is displayed. You need this code to complete the MFA configuration in Instagram.

**TIP:** Click the **Copy** button to copy the confirmation code to the clipboard.

### Link Your Account with the Cerby Web Application

To link your Instagram account with the Cerby web application, complete the following steps:

1. Log in to your corresponding workspace using the Cerby web application in a browser.
2. Click the **All accounts** button in the left-side navigation drawer. The **All accounts** view is displayed.
3. Click the **Settings** button of the corresponding Instagram account card. The **Account Settings** page is displayed with the **General** tab activated.
4. Click the **Save Code** button located in the **TWO-FACTOR AUTHENTICATION** section. The **Save Code** dialog box is displayed.
5. Enter the secret key provided by Instagram in the **Secret Key** field.

**IMPORTANT:** Remove the spaces in the alphanumeric secret key.

6. Click the **Save Code** button. The **Verify your code** dialog box and a success message are displayed. This dialog box contains the verification code you need to complete the MFA configuration in Instagram.

### Add an Authentication Application

To add Cerby as an authentication application when MFA is turned on, complete the following steps from the **Two-Factor Authentication** screen with the **Two-factor authentication is on** section:

1. Tap the **Authentication app** option with the “On” status. The **Authentication app** screen is displayed.
2. Tap the **Add button** in the **Connected devices** section. The **Connect device** screen is displayed.
3. Enter a name for the authentication application in the **Name** field. For example, **Cerby**.
4. Tap the **Next** button. The **Connect device** screen displays the **Instructions for setup** section and the secret key.

**TIP:** Click the **Copy Key** button to copy the secret key to the clipboard. You need this key to link your Instagram account to Cerby with the mobile application.

5. Set up Cerby as an authentication application by following steps 3 to 8 of the [Authentication App](configure-mfa-in-instagram-manually.md#id-authentication-app) instructions.

### Text message

To select a Cerby-managed phone number as the**Text message** verification method, you must complete different steps depending on whether you have previously configured a phone number or not:

* [Register a new phone number](configure-mfa-in-instagram-manually.md#id-register-a-new-phone-number)
* [Change the phone number](configure-mfa-in-instagram-manually.md#id-change-the-phone-number)

### Register a new phone number

To register a new phone number, complete the following steps:

1. Activate the **Text message** switch. The **Phone Number** screen is displayed.
2. Tap the country code field. The **SELECT YOUR COUNTRY** drop-down list is displayed.
3. Select the **United States (+1)** option from the list. The country code field displays the **US +1** value.
4. Enter the phone number provided by Cerby in the **Add Phone Number** field. Instagram uses this phone number to send a confirmation code. To create a phone number managed by Cerby, follow the [Create a Cerby-managed phone number or email address](configure-mfa-in-instagram-manually.md#id-create-a-cerby-managed-phone-number-or-email-address) instructions.
5. Tap the **Next** button. The **Confirmation code** screen is displayed.

### Change the phone number

To change the configured phone number, complete the following steps:

1. Activate the **Text message** switch. The **Confirmation code** screen is displayed with the **Enter confirmation** code section and a message with the last four digits of the configured phone number.
2. Tap the **Change Phone Number** button located at the bottom of the screen. The **Phone Number** screen is displayed with the **Add Phone Number** section.
3. Tap the country code field. The **SELECT YOUR COUNTRY** drop-down list is displayed.
4. Select the **United States (+1)** option from the list. The country code field displays the **US +1** value.
5. Enter the phone number provided by Cerby in the **Add Phone Number** field. Instagram uses this phone number to send a confirmation code. To create a phone number managed by Cerby, follow the [Create a Cerby-managed phone number or email address](configure-mfa-in-instagram-manually.md#id-create-a-cerby-managed-phone-number-or-email-address) instructions.
6. Tap the **Next** button. The **Confirmation code** screen is displayed.

### Change the verified phone number

To change the configured phone number for MFA, complete the following steps:

1. Tap the **Text message** option with the “On” status. The **Text message controls** screen is displayed.
2. Tap the **Change phone number** button. The**Two-Factor Authentication** screen is displayed with the **Update Phone Number** section.
3. Tap the country code field. The **SELECT YOUR COUNTRY** drop-down list is displayed.
4. Select the **United States (+1)** option from the list. The country code field displays the **US +1** value.
5. Enter the phone number provided by Cerby in the **Add Phone Number** field. Instagram uses this phone number to send a confirmation code. To create a phone number managed by Cerby, follow the [Create a Cerby-managed phone number or email address](configure-mfa-in-instagram-manually.md#id-create-a-cerby-managed-phone-number-or-email-address) instructions.
6. Tap the **Next** button. The **Confirmation code** screen is displayed.
7. Enter the confirmation code in the **Enter Confirmation Code** field. This code is sent by Instagram to the phone number you have created in Cerby. To retrieve the code, follow the [Retrieve the verification code from Cerby](configure-mfa-in-instagram-manually.md#id-retrieve-the-verification-code-from-cerby) instructions.
8. Click the **Next** button. The **Confirmation screen** is displayed with the **Phone number updated** section.

### 3\. Enter the Confirmation Code

To enter the confirmation code, complete the following steps from the **Confirmation code** screen.

1. Enter the confirmation code in the **Enter Confirmation Code** field. This code is sent by Instagram to the phone number you have created in Cerby. To retrieve the code, follow the [Retrieve the Verification Code from Cerby](configure-mfa-in-instagram-manually.md#id-retrieve-the-verification-code-from-cerby) instructions.
2. Click the **Next** button. The **Confirmation** screen is displayed with the **Two-factor authentication is on** section.
3. Click the **Done** button. The **Account Recovery** screen is displayed with a list of recovery codes that you can use if you lose your mobile phone or cannot receive codes via SMS or an authentication app.
4. Save the recovery codes in Cerby to retrieve them from your workspace whenever needed. To save the codes, follow the instructions to [Save Recovery Codes in Cerby](configure-mfa-in-instagram-manually.md#id-save-recovery-codes-in-cerby).
5. Click the **Back** button. The **Two-Factor Authentication** page is displayed with the **Text message** switch activated.

Now you are done.

## Create a Cerby-managed phone number or email address

To create a phone number or email address managed by Cerby, complete the following steps from the Cerby web application:

1. Log in to your corresponding Cerby workspace in a browser.
2. Click the **All accounts** button in the left-side navigation drawer. The **All accounts** view is displayed.
3. Click the **Settings** button of the corresponding Instagram account card. The **Account Settings** page is displayed with the **General** tab activated. You must complete different steps depending on the verification method you want Cerby to provide:

   * [Create a phone number](configure-mfa-in-instagram-manually.md#id-create-a-phone-number)
   * [Create an email address](configure-mfa-in-instagram-manually.md#id-create-an-email-address)

The following sections describe the steps for each alternative.

### Create a Phone Number

To create a phone number, complete the following steps from the **General** tab of the **Account Settings** page:

1. Activate the **Create Phone Number** switch located in the **Account Security** section. The **Create Phone Number** dialog box is displayed with a phone number in the **Auto-generated phone number** field.
2. Select the “I have already added the phone number to Instagram account settings.” and “I’m using this phone for MFA.” options. The **Create Phone Number** button is enabled.
3. Click the **Create Phone Number** button. The dialog box closes, and the **Account Settings** page displays a success message.

**IMPORTANT:** Make sure you complete steps 2 and 3 to create the phone number. If you omit these steps, Cerby will not be able to retrieve the verification code to be sent by Instagram.

**TIP:** Keep your Cerby workspace open because you need it to retrieve the verification code.

### Create an Email Address

To create an email address, complete the following steps from the **General** tab of the **Account Settings** page:

1. Activate the **Create Email Address** switch located in the **Account Security** section. The **Create Email Address** dialog box is displayed with an email address in the **Auto-generated email alias** field.
2. Select the “I have already added the email address to Instagram account settings.” option. The **Create Email Address** button is enabled.
3. Click the **Create Email Address** button. The dialog box closes, and the **Account Settings** page displays a success message.

**IMPORTANT:** Make sure you complete steps 2 and 3 to create the email address. If you omit these steps, Cerby will not be able to retrieve the verification code to be sent by Instagram.

**TIP:** Keep your Cerby workspace open because you need it to retrieve the verification code.

## Retrieve the verification code from Cerby

To retrieve the verification code from Cerby, whether it was sent by Instagram via SMS or email, complete the following steps from the Cerby web application:

1. Open your Cerby workspace in the browser.
2. Click the **Shared Inbox** button in the left-side navigation drawer. The **Shared Inbox** view is displayed with a table of messages. The verification code is displayed in the **Message** column of the corresponding Instagram SMS or email message.

**TIP:** Keep your Cerby workspace open because you need it to save your recovery codes.

## Save recovery codes in Cerby

To save your recovery codes in Cerby, complete the following steps from the Cerby web application:

1. Open your Cerby workspace in the browser.
2. Click the **All accounts** button in the left-side navigation drawer. The **All accounts** view is displayed.
3. Click the **Settings** button of the corresponding Instagram account card. The **Account Settings** page is displayed with the **General** tab activated.
4. Click the **Add Codes** button located in the **Emergency Controls** section. The **Add MFA Backup Codes** dialog box is displayed.
5. Enter the recovery codes provided by Instagram in the **MFA Backup Codes** text block.
6. Click the **Save Codes** button. The dialog box closes, the **Account Settings** page displays a success message, and the **Add Codes** button changes to **View Codes**.

**IMPORTANT:** Whenever you need to see the recovery codes, click the **View Codes** button in the **Emergency Controls** section.
