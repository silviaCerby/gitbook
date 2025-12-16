---
description: This article describes how to turn on the biometrics login feature on your Cerby mobile app.
intercom_id: 10355971
---

# Turn on the Biometrics Login feature

{% hint style="info" %}


**Who can use this feature?**

* Workspace **Owners** , **Super** **Admins** , **Admins** , and **Users**
* Available in the Cerby mobile app


{% endhint %}

The **Biometrics Login** feature enhances the security of your Cerby mobile app by using your biometric information, such as **Face ID** or **Touch ID** on iOS and **Face Lock** or **Fingerprint** **recognition** on Android. Turning on this feature ensures that only the registered user can unlock and access the app.

This feature provides convenience and added protection, making it easier to access your app securely while safeguarding your personal information.

{% hint style="danger" %}


**IMPORTANT:**

* The **Biometrics Login** feature does _not_ replace the app login process. When your session expires, you must log in again using your Identity Provider (IdP) login credentials, such as Okta or Entra ID (formerly Azure AD).
* For the feature to work correctly, the phone’s biometric authentication system on Android and iOS must be enabled. Before using this feature, ensure your device's biometric settings are configured. Check the following resources to learn more about your options:
    * iOS
      * [Use Face ID on your iPhone or iPad Pro](https://support.apple.com/en-us/108411)
      * [Set up Touch ID on iPhone](https://support.apple.com/guide/iphone/set-up-touch-id-iph672384a0b/ios)
    * Android (depends on your device manufacturer)
* The Cerby mobile app uses the biometric information you have enabled by default on your phone: Face ID or Touch ID on iOS or Face Lock or Fingerprint recognition on Android. If you have both options enabled on your phone, the Cerby mobile app uses Face ID on iOS and Fingerprint on Android by default.


{% endhint %}

To turn on the **Biometrics Login** feature, you must complete the following steps:

  1. Open the Cerby mobile app on your phone.
  2. Log in to your Cerby workspace.
  3. Tap the profile icon. The **My Profile** screen appears.
  4. Tap the **Settings** option. The **Settings** screen is displayed.
  5. Activate the **Biometrics Login** switch. The next steps are different depending on your operating system and your default biometric settings:

     * **iOS**
       * If you have **Face ID** enabled, the **Do you want to allow “Cerby” to use Face ID** message box is displayed.

         1. Tap the **Allow** option. The phone’s Face ID is activated.
         2. Look at the phone’s camera. A checkmark is displayed, indicating that the verification has been completed.

       * If you have **Touch ID** enabled, the **Touch ID** message box is displayed with the information of the associated email address.

         1. Tap the **Cancel** button to close the message box.

     * **Android**
       * If you have **Face Lock** enabled, the **Use Face Lock** menu is displayed, and the phone’s face recognition is activated.

         1. Look at the phone’s camera. The **Success** menu is displayed, indicating that the recognition has been successful.
         2. Tap the **Continue** button. The menu closes.

       * If you have **Fingerprint** enabled, the **Use your screen lock** menu is displayed.

         1. Place your finger on the phone’s lock button. The **Success** menu is displayed, indicating that the recognition has been successful.
         2. Tap the **Continue** button. The menu closes.

Now you are done. The next time you log in to the Cerby mobile app, you’ll have to verify your identity with your biometric information to unlock and access the app.
