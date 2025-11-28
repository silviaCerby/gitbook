# Release Notes - March 12, 2025

**Description:** This article describes the latest enhancements and bug fixes to improve your experience using Cerby.

# **New features**

The following are the new features and improvements we released across the
Cerby platform:

## **Revolutionizing enterprise security with Universal Logout**

Cerby continues to deliver robust protection, keeping users one step ahead of
cyber threats. We have partnered with Okta to extend the reach of its
Universal Logout feature to nonfederated or disconnected apps secured with
Cerby.

With a unified approach, Cerby enables a one-to-many **Universal Logout** ,
immediately revoking user sessions and rotating passwords across a wider range
of applications, including those lacking global token revocation. This feature
significantly improves incident response times and minimizes potential
security damage.

Want to hear something better? Cerby’s Universal Logout is also available as a
standalone feature. It lets you safeguard all your apps and devices, whether
they’re connected through Okta or not.

If you want to learn more, read the blog [Extending Okta's Universal Logout:
Cerby Boosts Security Across
Applications](https://www.cerby.com/resources/blog/extending-oktas-universal-
logout) or the article [Explore Universal
Logout](https://help.cerby.com/en/articles/10495600-explore-universal-logout).

## **Shhh, Cerby is making login magic behind the scenes**

Get a significant boost to your team’s productivity without compromising
security. We have released background **auto sign in** to authenticate the
Cerby browser extension right after accessing your identity provider (IdP).

By leveraging existing, secure IdP sessions, say goodbye to manual
interactions with our browser extension and hello to a more streamlined login
to your accounts from your IdP’s dashboard.

This feature is available in Okta-based workspaces with [extended account
access](https://help.cerby.com/en/articles/9616265-explore-extended-account-
access) turned on, and we are working to support other IdPs in future
releases. Contact your Customer Success representative for more information.

## **Flexibility meets security: Use your AWS KMS environment in Cerby**

Following the success of our [Azure Key
Vault](https://help.cerby.com/en/articles/9189942-set-up-an-azure-key-vault-
integration) integration, we are excited to announce the addition of **AWS Key
Management Service (KMS) support**! Integrate your AWS KMS environment with
Cerby to protect your accounts and secrets and take full control of data
encryption and decryption.

Leverage Cerby's Zero Knowledge architecture while maintaining full ownership
and control over your keys. We provide the tools, and you retain absolute
sovereignty. In essence, your data, your keys, your platform.

Ready to set it up or want more information? Take a look at the article [Set
up an AWS KMS vault
integration](https://help.cerby.com/en/articles/10085037-set-up-an-aws-kms-
vault-integration?q=azure+key). **Figure 1** shows how an AWS KMS vault is
displayed in the Cerby web app.

![](images/AD_4nXeRRWjW5xR8qFArOpn1pbJO2VyS8R36dSFRjRcMa466YDOF6T1S56D4u17FLFTEIBhv2686s2-2ASAYOXlLC-0NBkI4hiL5FKXfDIwugkpNvl5DWCF6Yi9i7-1H-3n8rE8YhVNc)

**Figure 1.** **Privacy and security** tab in the **Workspace Configuration**
page of the Cerby web app dashboard

## **Say goodbye to unauthorized changes in your app settings**

Cerby has been your silent guardian in the complex world of shared accounts,
and now we're expanding our vigilance. With the new **App settings
restrictions** feature, you can prevent unauthorized changes to your app
settings, a task that seemed impossible until now.

Powered by the Cerby browser extension, we detect when users attempt to modify
the password or member settings in your app and take action based on your
preferences. We can fully block the user interface or guide users make changes
through Cerby.

For more information on how this feature works, read the article [Explore App
settings restrictions](https://help.cerby.com/en/articles/10276184-explore-
app-settings-restrictions). Explore the extension settings, as shown in
**Figure 2** , where you can manage this feature.

![](images/AD_4nXcvYNMvd9KUMGLmEhGGOpWR8YOAYZb1P9oxhnn5Bl_SpavzhiiNUGZFHL6KU_rUAC5tu8WKxtgDIirYFy-
rE23qg_aRsjOmlcRLcV9b1fI5VhNzWt-hr2gIDdDdnfEfcW4AfWAHKQ)

**Figure 2. Extension settings** tab in the **Workspace Configuration** page
of the Cerby web app dashboard

## **Fast track to Cerby from your password manager**

We've been keeping a secret, but you guessed it: our **CSV File Importer** is
live!

In addition to our importers for
[LastPass](https://help.cerby.com/en/articles/7175132-migrate-from-lastpass-
to-cerby) and [1Password](https://help.cerby.com/en/articles/9613378-migrate-
from-1password-to-cerby), we’ve designed a universal and flexible method for
migrating your items from your enterprise password manager (EPM). You just
need to upload a CSV file to Cerby, and we’ll do the rest.

So, prepare your file and take control of your data migration. Check out the
instructions and template in our article [Import your items from a CSV file to
Cerby](https://help.cerby.com/en/articles/10290203-import-your-items-from-a-
csv-file-to-cerby).

## **Proactive security starts here**

Here’s another long-awaited release: the **Security Hub** , a comprehensive
view of the health of all the accounts saved in your workspace. The goal is to
help you spot and address proactively potential vulnerabilities before they
escalate.

In the first version of this feature, we are providing you with a report of
orphaned accounts. Now, you can quickly identify any accounts that should be
assigned to one or more **Owners** so that account management capabilities are
not lost.

If you want to learn more about the Security Hub and orphaned accounts, take a
look at the articles [Explore Security
Hub](https://help.cerby.com/en/articles/10492095-explore-security-hub) and
[Assign Owners to orphan accounts in your
workspace](https://help.cerby.com/en/articles/10580392-assign-owners-to-
orphan-accounts-in-your-workspace?q=security+hub).

## **Cerby web app**

Check out what’s new in our Cerby web app:

  * The wait is over! After much anticipation and multiple requests, we’re thrilled to unveil the support of verification codes in the Cerby web app.   
As shown in **Figure 3** , those who prefer switching tabs and copy-pasting
their login credentials can now find the codes on the account details page
when Cerby manages multi-factor authentication (MFA).

![](images/AD_4nXfSGONjeI-y7uibWiPKa9j-JwRoIh_xk3s5WIVpSOMV0xgkLPR46pOE0Mksjh_YeCploJy3z5Gt9FIVopRGXLY41tlTBjKJ5IcNEBmoZJu-
Ay009OJUM4ILdCFA-la0mXLbYx1w_g)

**Figure 3.** MFA codes in the account details page of the Cerby web app
dashboard

  * Check the new features and improvements in the business hub user experience:

    * The **Business Hubs** page now has a search bar to easily find business hubs when users have multiple integrations connected to Cerby.

    * You can now share access to a business hub with other workspace members without granting a seat or license in the external app. This behavior applies only to business hub **Owners** , whereas **Collaborators** are always granted a seat.

    * When assigning a seat to a user who didn’t have one, you can also select the roles to assign them on assets.

    * The **Unmatched users** tab in the business hub details page is now removed when no user is listed with the unmatched status.

    * You can now disconnect the token of a native partner. Just go to the corresponding tab in the business hub details page and select **Disconnect token** from the **More options** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1417318520/f547cfbf14a000f9eed969c4574a/AD_4nXeUCE5crjTJ-oX0QthVR1jJo4lFlhSzG3Mjs1kgJdhw9NLW3LdHYznfqTmOXLZu1sMyoD0GVys_gQqeZmEFf23LxarPsKsbMk6IBrz9ht_sYd9pi2ezAe0RoKoP-8QHYtMydRIJGw?expires=1755918000&signature=c23808fc9e6c23d1b532302a38009efbbe3ca11f339603188c6256004bafdabe&req=dSQmEcp%2FlYRdWfMW3Hu4gfwq383PqOJjAAjTqnxFq59ump0wSo6wG5PZDHQP%0Aew%3D%3D%0A)) drop-down menu.

    * Team deprovisioning events from the corporate identity provider now trigger password rotations for business hub users. 

  * We now provide more information in the table of the **Automation tasks** page when an automated task is not completed.

  * We now prevent**Super Admins** with the **All-Access Mode** turned on from being able to manage (add or remove) accounts and secrets within a collection. These management actions are available in the **Accounts** and **Secrets** tabs of the collection details page.

## **Cerby browser extension**

Explore the latest features in our Cerby browser extension:

  * Here’s one to Cerby adoption, security, and improved user experience. Workspace **Admins** can now turn on the **Enforced account autosave** feature to let the Cerby browser extension automatically save all accounts when users log in or sign up for the domains you specify without displaying a prompt.

You can only turn on and configure this feature using the Cerby web app as
follows:

    1. Select the **Settings** option in the left menu.

    2. Activate the **Extension** **settings** tab.

    3. Select the **Enforced autosave** option in the left panel, as shown in **Figure 4**.

![](images/AD_4nXeOXyU1vrnfzkXLX8CmMwEuFKLmlXRi1llSnOOeiR7KXiBfR3PomwtWZ-
NI0Ui2arFCeH2ZjZc9FsZGTTJvKXiSh_RDcbcnDfoooYNWO6P8whSC0y5NbQrYzgRrfRhd5rsPsSbxWA)

**Figure 4.** **Enforced account autosave** settings in the Cerby web app
dashboard

    4. Activate the **Enforced account autosave** switch to turn on the feature for your workspace.

    5. Add the domains for which you want to enforce account autosave.

## **Cerby mobile app**

Dive into the newest additions to our Cerby mobile app:

  * We released the new account details screen in the mobile app for iOS v1.0.235 and Android v.1.0.130. Additionally, we improved the loading time for account passwords and secrets in iOS and started supporting software license secrets in Android.

  * Cerby is implementing biometric security to prepare for passkeys. From versions 1.0.221 for iOS and 1.0.182 for Android, the Cerby mobile app supports **Biometrics Login** to enable users to unlock and access the app.  
This feature is compatible with Face ID or Touch ID on iOS and Face Lock or
Fingerprint recognition on Android. For guidance on setting up your
biometrics, read the article [Turn on the Biometrics Login
feature](https://help.cerby.com/en/articles/10355971-turn-on-the-biometrics-
login-feature).

**Figure 5** illustrates the user experience of this feature.

![](images/AD_4nXe_lAYNDyf7b2hJF9_FBIj3tMX7iEzMCJoNIsWYStY9lntvwf2qFls2-l_IytGWymHN5XxO_93reddIEuJZT_ah8_Cp8HFz2-RkxidczkqhHd7jVgn7YcGv-
CWwLh5Vaxz0w7XSsA)

**Figure 5.** Biometrics in the Cerby mobile app

  * If you use shared company phones and devices, keep reading; we have a cool feature for you. You can now access an account's login credentials without having to log in to the Cerby mobile app by simply scanning a QR code with the phone.   
The code is generated in the Cerby web app. After scanning the code and seeing
the login credentials, you can launch the app and use the phone’s autofill
functionality to log in to the account. You can also manually copy and paste
the values.  
For more information on how to use this feature, read the article [Access an
account via a QR code using the Cerby mobile
app](https://help.cerby.com/en/articles/10063312-access-an-account-via-a-qr-
code-using-the-cerby-mobile-app). It is available in iOS v1.0.222 and Android
v1.0.189 onwards.

* * *

# **Fixes**

Take note of the issues addressed and resolved by the Development team behind
the Cerby platform:

  * The issue with users keeping their **Owner** role on items when they are downgraded to the **Login-Only** role was fixed. **Login-Only** users can only have the **Collaborator** role on items.

## **Cerby web app**

  * Business hub fixes:

    * The issue with letting users update the role of a YouTube channel **Owner** from a Cerby business hub integration was fixed. YouTube doesn’t support updating such a role in any scenario.

    * The issue with not displaying custom roles when inviting users to a business hub or updating their roles was fixed.

    * The issue with sending invites for unmatched users provisioned via a group assignment in the identity provider (IdP) was fixed. Because these users already existed in the app, now Cerby only matches the users with their identity in the business hub integration. 

    * The issue with sharing a business hub and its assets with a team and not granting access to the assets was fixed. This scenario is now handled via the claim access flow.

    * The issue with incorrectly displaying the security status of business hub members was fixed. When configuring the user management and login method for your business hub, the following are the possible combinations:

      * With the **Username and password** option selected and the **Request users to save their username and password in Cerby** switch activated, the status is “Pending Cerby onboarding.” 

      * With the **Username and password** option selected and the **Request users to save their username and password in Cerby** switch deactivated, the status is “Managed outside Cerby.”

      * With the **Single sign-on (SSO)** option selected, the status is “Single sign-on.”

    * The issue with displaying the overview dialog box of the wizard to connect a business hub, even when users select the **Don’t show this again** option, was fixed.

    * The issue with being unable to remove local partners, onboarded users, and unmatched users from a business hub was fixed.

    * The issue with sharing a business with a team to which some users already had access was fixed. The security status of these users changed incorrectly to **Cerby only** and the**Log in** button was disabled for them. 

    * The issue with being unable to share the automation or service account with a team that already has shared access as an **Owner** to a business hub was fixed.

    * The issue with removing a team from a business hub and granting individual access to it was fixed as follows:

      * If the user who removed the team selects to revoke only access in the business hub but not in the external app, the team grant becomes an individual grant for all team members. However, the users who have not claimed access to the business hub and the app will be removed from both. 

      * If the user who removed the team selects to revoke access in the business hub and the external app, all team members lose access to both. However, if they already had individual access to the business hub, the team removal doesn't affect them and they keep access.

  * The issue with being unable to update the role of a user on an item when they have a **Mixed role** was fixed. The role update is done in the **Members** tab of the secret and account details pages.

  * The issue with the infinite loading after filtering by collection in the **Accounts** view was fixed. This error only occurred when no collections exist.

## **Cerby browser extension**

  * The issue with being unable to detect the password update field in the account settings of Instagram was fixed in the Cerby browser extension v1.0.426.

## **Cerby mobile app**

  * Issues with the global search were fixed on iOS v.1.0.229 and Android v1.0.199.

  * The issue with the **Add custom fields** bottom menu not working after tapping it in the account details screen was fixed on iOS v1.0.227 and Android v1.0.195.

  * The issue with successful identity confirmations not redirecting to editing a secret was fixed on iOS v1.0.227 and Android v1.0.195.

* * *

# **New supported managed apps**

The following are the latest additions to the list of managed apps with
supported automated tasks:

  * [AllRegs](http://allregs.com/)

  * [Bigleaf](http://bigleaf.net/)

  * [Built In](http://builtin.com/)

  * [BuyMe Business](http://buyme.co.il/)

  * [Canditech](http://canditech.io/)

  * [Clearsurance](http://clearsurance.com/)

  * [Cloudinary](http://cloudinary.com/)

  * [Cursor](http://cursor.com/)

  * [Dash Social](http://www.dashsocial.com/)

  * [Deliveroo](http://deliveroo.ie/login)

  * [Eight](http://8card.net/en/login)

  * [Epidemic Sound](http://epidemicsound.com/)

  * [Fannie Mae](http://fanniemae.com/)

  * [G2](http://my.g2.com/)

  * [G2 Track](http://trackapp.bettercloud.com/users/sign_in)

  * [Geckoboard](http://app.geckoboard.com/login)

  * [Genially](http://genially.com/)

  * [Gridly](http://gridly.com/)

  * [Insided/Gainsight](http://gainsightcloud.com/)

  * [Josys](http://josys.com/)

  * [PageFlows](http://pageflows.com/)

  * [Password Link](http://password.link/)

  * [Paymetric](http://merchantportal.paymetric.com/Authentication/Login)

  * [Spotify for Creators](http://creators.spotify.com/)

  * [Reduct Video](http://app.reduct.video/)

  * [RiskLedger](http://riskledger.com/)

  * [Riverside](http://riverside.fm/)

  * [Rollbar](http://rollbar.com/)

  * [Simple MDM](http://simplemdm.com/)

  * [Stack Exchange (Stack Overflow Talent)](http://talent.stackoverflow.com/)

  * [Stagetimer](http://stagetimer.io/)

  * [Superwise App](http://app.superwise.ai/)

  * [Superwise Portal](http://portal.superwise.ai/)

  * [TextExpander](http://textexpander.com/)

  * [Tower](http://tower.com/)

  * [Trullion](http://trullion.com/)

  * [TrustRadius](http://trustradius.com/)

  * [Truthsocial](http://truthsocial.com/)

  * [Usersnap](http://usersnap.com/)

  * [VidTao](http://app.vidtao.com/)

  * [Workwize](http://app.goworkwize.com/)

  * [Yext](http://yext.com/)

