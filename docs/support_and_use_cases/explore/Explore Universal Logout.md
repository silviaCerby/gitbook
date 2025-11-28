# Explore Universal Logout

**Description:** This article describes the benefits of Cerby Universal Logout for terminating user sessions and tokens and rotating account passwords.

With Cerby **Universal Logout** , you can immediately prevent unauthorized
access and protect sensitive data from potential threats by logging users out
of their assigned apps across all devices and terminating their sessions and
access tokens.

This action is complemented by password rotations for the affected accounts,
ensuring that compromised login credentials cannot be reused. Additionally,
when a logout is triggered, all Cerby workspace **Admins** are notified,
keeping your team informed and up to date.

In addition to Cerby’s native Universal Logout capabilities, you can extend
Okta [Universal Logout](https://help.okta.com/oie/en-
us/content/topics/itp/universal-logout.htm) functionality to Cerby directly
from the Okta Admin dashboard. This integration streamlines session
termination across both platforms, saving you time on manual user management
and enhancing overall security. By partnering with Okta, Cerby unlocks new
security enhancements and delivers robust protection that keeps our customers
one step ahead of cyber threats.

The following are the main characteristics of Universal Logout:

  * **Cross-platform session and token termination:** When Cerby Universal Logout is triggered, Cerby terminates all sessions and tokens in the Cerby web dashboard, browser extension, and mobile app. 

  * **Log out more than just Cerby sessions:** User’s sessions and tokens are terminated in apps with Universal Logout support. For other apps, Cerby performs automated password rotations on all accounts to which the user has shared access.

  * **Direct integration with Okta:** Cerby integrates with Okta Identity Threat Protection, providing immediate response to security threats.

{% hint style="danger" %} **IMPORTANT:** Users must be created via SCIM for
the Universal Logout feature to work. {% endhint %}

* * *

# How it works

Cerby Universal Logout works at the following two levels:

  * **Cerby’s native Universal Logout:** Sessions, tokens, and session data are terminated directly through Cerby. Automated password rotations are performed on all accounts to which the user has been granted access, terminating user sessions on the corresponding apps.

  * **Okta Universal Logout extended to Cerby:**

    * **Okta only:** Okta Universal Logout enables Admins to terminate user and app sessions, along with tokens, when risks are detected. Refer to [Okta Universal Logout ](https://help.okta.com/oie/en-us/content/topics/itp/universal-logout.htm)official page.

    * **Okta and Cerby:** Okta Universal Logout is available through the Cerby app in the Okta Integration Network (OIN), automating the Cerby Universal Logout capabilities in conjunction with Identity Threat Protection.

* * *

# Related articles

The following articles contain more information about the Universal Logout
feature:

  * [Trigger Cerby Universal Logout](https://help.cerby.com/en/articles/10496392-trigger-cerby-universal-logout)

  * [Enable Okta Universal Logout for Cerby](https://help.cerby.com/en/articles/10495618-enable-okta-universal-logout-for-cerby)

  * [Trigger Okta Universal Logout and extend it to Cerby](https://help.cerby.com/en/articles/10495624-trigger-okta-universal-logout-and-extend-it-to-cerby)

