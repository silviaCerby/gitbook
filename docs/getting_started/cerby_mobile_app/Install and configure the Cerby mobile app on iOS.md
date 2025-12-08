# Install and configure the Cerby mobile app on iOS

## Install and configure the Cerby mobile app on iOS

**Description:** This article describes the key steps to install and configure the Cerby mobile app on your iPhone.

The Cerby mobile app enables you to access and manage your accounts, secrets, and collections from your iPhone. It also serves as a second device to authenticate sensitive tasks by providing you with verification codes and confirming your identity with push notifications.

This article describes the steps to install and appropriately configure the required settings of the Cerby mobile app.

***

## Requirements

The following are the requirements to install, configure, and use the Cerby mobile app on iOS:

* Cerby requires iOS 16 as the minimum supported OS version due to security updates and performance improvements. If your iPhone has an older operating system (OS) version, refer to the article [Troubleshooting: Older operating systems are no longer supported by the Cerby mobile app](https://help.cerby.com/en/articles/6681521-troubleshooting-older-operating-systems-no-longer-supported-by-the-cerby-mobile-app)
* From **v1.0.261** , the Cerby mobile app also supports installation on iPads (minimum supported OS: iOS 16)
* Access to a Cerby workspace

***

## Install and configure the Cerby mobile app on iOS

To install and configure the Cerby mobile app on your iPhone, you must complete the following steps:

1. Install from the App Store
2. Turn on the Autofill Service on your iPhone
3. Turn on the Allow Notifications feature on your iPhone
4. Log in to your Cerby workspace
5. Turn on the Biometrics Login on your iPhone
6. Set up the Cerby mobile app as a trusted device

The following sections describe each main step.

### **1. Install from the App Store**

To install the Cerby mobile app on your iPhone from the App Store, you must complete the following steps:

1. Open the Cerby mobile app in the [App Store](https://apps.apple.com/us/app/cerby/id1533747684).
2. Tap the **Install** () button. The app is downloaded and installed on your iPhone.

The next step is 2. Turn on the Autofill Service on your iPhone.

### **2. Turn on the Autofill Service on your iPhone**

The **Autofill Service** feature enables Cerby to securely and efficiently manage and fill in usernames and passwords within apps and login pages, saving you the hassle of manually entering your login credentials every time you log in to your corporate account.

To continue the configuration of the Cerby mobile app and turn on the **Autofill Service** , you must complete the following steps:

1. Open the Cerby mobile app on your phone. The **Access your items** screen displayed.
2. Swipe the screen to the left until you see the **Easily AutoFill passwords with Cerby** screen.
3. Activate the **Allow AutoFill from Cerby** switch in the **Easily AutoFill passwords with Cerby** screen. The **Turning on Cerby’s AutoFill** screen is displayed with the instructions you must follow on your device.
4. Tap the **Open iPhone setting** button. The **Autofill & Passwords** screen of your iPhone is displayed.
5. Activate the **AutoFill Passwords and Passkeys** switch if it wasn’t previously activated.
6. Activate the **Cerby** switch in the **AUTOFILL FROM** section. The **Cerby** screen is displayed.
7. Activate the **Auto-Copy One-Time Passwords** switch if it wasn’t previously activated.
8. Tap the **Done** option at the top right corner to return to the previous screen.
9. Return to the Cerby app to continue the app setup.

The next step is 3. Turn on the Allow Notifications feature on your iPhone.

### **3. Turn on the Allow Notifications feature on your iPhone**

The **Allow Notifications** feature enables you to receive real-time alerts and updates from the Cerby mobile app, such as verifying your identity to reveal a secret or other actions.

To continue the configuration and turn on the **Allow Notifications** feature, you must complete the following steps:

1. Swipe the screen to the left. The **Enable notifications to verify your identity** screen is displayed.
2. Activate the **Allow notifications** switch. The **Allow Cerby to send notifications?** dialog box is displayed.
3. Tap the **Allow** option. The **Allow notifications** switch is turned on.
4. Tap the **Continue** button. The **Welcome to Cerby** screen is displayed.

The next step is 4. Log in to your Cerby workspace.

### **4. Log in to your Cerby workspace**

To log in to your Cerby workspace with the Cerby mobile app, you must complete the following steps:

1. Tap the**Log in** button. The **Let’s find your workspace account** screen is displayed.
2. Enter the name of your Cerby workspace in the **Enter your workspace name below** field.
3. Tap the **Next** button. The login page of your identity provider (IdP) is displayed.
4. Log in to your IdP. The **Turn on Face ID to unlock Cerby** screen is displayed.

The next step is 5. Turn on the Biometrics Login on your iPhone.

### **5. Turn on the Biometrics Login on your iPhone**

The Cerby mobile app enables you to use your biometric information, such as your face ID or fingerprint, to unlock the app and add an extra layer of security to your app. To learn more about this feature, refer to the article \[Turn on the Biometrics Login feature]\(https://help.cerby.com/en/articles/10355971-turn-on-the-biometrics- login-feature).

To continue the configuration and turn on the **Biometrics Login** feature, you must complete the following steps:

### **NOTE:** This step is not mandatory. You can set up the **Biometrics Login** later by tapping the **Maybe later** option in the **Turn on Face ID to unlock Cerby** screen and skipping to step 6. Set up the Cerby mobile app as a trusted session.

1. Tap the **Set up Face ID** button. The iPhone’s Face ID is activated.
2. Look at the phone’s camera. A checkmark indicates that the verification has been completed. The **“Cerby” Would Like to Send You Notifications** message box is displayed.
3. Tap the **Allow** button. The **Set up trusted device** screen is displayed.

The next step is 6. Set up the Cerby mobile app as a trusted session.

### **6. Set up the Cerby mobile app as a trusted device**

Trusted sessions and devices provide users with an additional layer of protection by ensuring that all interactions with Cerby come from authorized devices that meet corporate security standards. To learn more about trusted sessions, refer to the article \[Set up trusted sessions on your devices]\(https://help.cerby.com/en/articles/8142370-set-up-trusted-sessions- on-your-devices).

To continue the configuration and set up your Cerby mobile app as a trusted device, you must complete the following steps:

1. Tap the **Set up device** button in the **Let’s set up your mobile device as a trusted device** screen. The **Name your device** screen is displayed.
2. Enter a name for your device in the **Device name** field.

**NOTE:** Cerby creates a name by default for you using the format: `[username] - [operating system]`. If you want to change it, Cerby recommends using a device name you can easily recognize and including the name of your mobile OS. Device names must be unique.

3. Tap the **Next** button. The **Verify your identity** screen is displayed with the following options to approve the device from a trusted session:
   * **Approve from another trusted session**
     1. Log in to Cerby from a trusted session on the Cerby web app.
     2. Select the **My profile** option from the user profile menu located in the top-right corner.
     3. Activate the **My trusted devices** tab in your **Profile** information. The list of your trusted sessions is displayed.
     4. Hover the mouse over the device with the **Pending** approval status. The **Approve** and **Deny** buttons are displayed.
     5. Click the **Approve** button. The Cerby dashboard screen and a success message box are displayed on your mobile app.
   * **Approve using a secure code**
     1. Tap the **I don’t have access to my trusted device** option. The **Verify your device** screen is displayed, and a message with a verification code is sent to your email.
     2. Copy the verification code from the email Cerby sent you. **IMPORTANT:** The verification code expires in 5 minutes.
     3. Enter the code in the **Verification code** field in your mobile app.
     4. Tap the **Verify code** button. The dialog box closes, and a success message box is displayed. The Cerby dashboard screen and a success message box are displayed on your mobile app.
   * **Set up the trusted session later**
     1. Tap the **Continue without a secure session** option. The Cerby dashboard screen and a warning banner indicating that your session is not secured are displayed. You can set up the trusted session by tapping the **Right arrow** () button and following the instructions.

Now you are done. You can start using Cerby on your iPhone.
