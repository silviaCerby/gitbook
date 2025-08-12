# Release Notes - December 30, 2024

**Description:** This article describes the latest enhancements and bug fixes to improve your experience using Cerby.

# New features

The following are the new features and improvements we released across the
Cerby platform:

  * Potential partners, external collaborators, and developers brace yourselves! We’ve made one of the first moves toward opening the Cerby platform to you. The **[Cerby developer portal](https://developer.cerby.com/)** is now live, providing you with the tools and resources to build powerful integrations.  
The following are the available collections in our public API, and we’re
aiming for more in 2025:

    * [Accounts](https://developer.cerby.com/#accounts)

    * [Secrets](https://developer.cerby.com/#secrets)

    * [Collections](https://developer.cerby.com/#collections)

    * [Users](https://developer.cerby.com/#users)

    * [Teams](https://developer.cerby.com/#teams)

    * [Integrations](https://developer.cerby.com/#integrations)

    * [Jobs](https://developer.cerby.com/#jobs)

We can’t wait for you to start building innovative and powerful solutions with
our public API and [Cerby
CLI](https://help.cerby.com/en/articles/9118683-explore-the-cerby-cli).

  * You know we’ve been partners with Okta to secure nonstandard applications for more than one year. Well, our collaboration keeps bearing more fruit!  
We’re excited to announce **Extended account access** , a feature that enables
organizations to enjoy a seamless login experience to their disconnected apps
from Okta powered by Cerby's automation. If you want to centralize access in
your identity provider (IdP) instead of using an additional external
dashboard, look no further.  
Just extend your Cerby accounts to your Okta dashboard, and let the Cerby
browser extension do all the heavy lifting of autofilling the login
credentials and verification codes when Cerby manages multi-factor
authentication (MFA).

For more information, read the article [Explore Extended account
access](https://help.cerby.com/en/articles/9616265-explore-extended-account-
access). **Figure 1** shows how your accounts are displayed as chiclets in the
Okta dashboard.

![](gitbook/imagesAD_4nXdkDn3Jkbvsew2WLT0enpCxJdw9l3g-C-0CZTQYVXT9tM2p-FKvFDW0R4BAddB0yiwNbNSVLbsfzdJ4J32XuQDJIyCC-
gQsu6YAQ6TPGXcG13SklkzDXBP9nLOcQ10dGpMfVrcI5g)

**Figure 1.** Chiclets in the Okta dashboard extended from Cerby accounts

  * Do you think you’ve had enough big news? Keep reading and get ready for a mic drop.

We’ve built and released **Scout by Cerby** , a browser extension aiming to
help you expand your app ecosystem quickly. This extension works on demand to
capture your interactions on a web page so that the Cerby development team has
all the information they need to automate your manual user workflows:

    * Log in to your account

    * Update your account's password

    * Turn on MFA

    * Invite a user to your app

    * Remove a user from your app

    * Update a user's role in your app

Currently, Scout is privately listed in the Chrome Web Store. If you want to
take a peek, see how the extension looks in**Figure 2**. For more information,
read the article [Explore
Scout](https://help.cerby.com/en/articles/9774431-explore-scout).

![](gitbook/imagesAD_4nXdbUgbLtrpeipFWVRqV2zrSQui8qQUhRuksXOrXF9mt4Q8fjb-
yu70XGnVYkO1TDx3dd5lNrL_D59aLBOaHMv6dDCyJAgCGdSN0hgTOsswSFQsWIGssrVrdZ79lmE--
S_d7ldPd)

**Figure 2.** Scout by Cerby browser extension

## **Cerby web app**

Check out what’s new in our Cerby web app:

  * Ever heard about forgetting a password? We know it happens, and that’s why workspace **Admins** can now reset the password of a guest user. Here’s how you can do it:

    1. Select the **All members option** in the left navigation drawer.

    2. Activate the **Guest** tab.

    3. Click the More options (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1308724047/e5f834eebdde9e2598aec9e0333b/AD_4nXcy_6y2XtFQJgh891i6fIMq_9zqoNDkoPEXrKJ09R1qMA7y9krLeGKkJY7FdEff9lSYhiuf6XPTSKEPPYa7uWWVjAz8pM2NGzgeh3UxJ8icqoyQ38fAfK3_a0D9guPf9ThQ7hlw4w?expires=1748412000&signature=b3ba3caec5c86a56663fb8d43f4b1f7ef84af38852cb6af3d181f2d0aaf30f35&req=dSMnHs58mYFbXvMW3Hu4gec7k3REcoJmGEoLiRDPZsbJnYnnJbYm%2FOhwsd2K%0ARA%3D%3D%0A)) icon.

    4. Select the **Force Password Reset** option from the drop-down list.

  * If you manage complex and numerous permissions through a Cerby business hub, we have good news! We’ve added a scroll interaction to the list of app roles displayed in the **Members** tab of the business hub details page. That way you can navigate through them seamlessly.

  * Business hub **Owners** can now move users from the **Exempted** table back to **Unmatched users**. This action can be performed from the **Members** tab in the business hub details page as follows:

    1. Activate the **Exempted** table.

    2. Click the **More options** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1308724047/e5f834eebdde9e2598aec9e0333b/AD_4nXcy_6y2XtFQJgh891i6fIMq_9zqoNDkoPEXrKJ09R1qMA7y9krLeGKkJY7FdEff9lSYhiuf6XPTSKEPPYa7uWWVjAz8pM2NGzgeh3UxJ8icqoyQ38fAfK3_a0D9guPf9ThQ7hlw4w?expires=1748412000&signature=b3ba3caec5c86a56663fb8d43f4b1f7ef84af38852cb6af3d181f2d0aaf30f35&req=dSMnHs58mYFbXvMW3Hu4gec7k3REcoJmGEoLiRDPZsbJnYnnJbYm%2FOhwsd2K%0ARA%3D%3D%0A)) icon of the corresponding user.

    3. Select the **Remove exemption** option.

    4. Click the **Confirm** button.

  * All accounts, including business hubs, now have the **Copy bookmark URL** button available on the account details page. With this URL, you can trigger automated logins with the Cerby browser extension from the dashboard of your identity provider (IdP).

## **Cerby browser extension**

Explore the latest features in our Cerby browser extension:

  * We’ve improved the login experience for your accounts with two features:

    * After a successful login to our extension, we now close the browser tab we open for the process. This way, you can get back to what you were doing. If the login is unsuccessful, we keep the browser tab open so you can retry.

    * The account details screen in the Cerby browser extension popup now displays the **MFA Code** section and a **Copy**(![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1308724723/3e2bb4a3531ba7ef421ff0d3a01d/AD_4nXcNEUZ-c1o6eDNJLqnkLnPe9GnO-NMPcf7_IpxuLdAw1vPot9KBOL-cDU8tPrG6nKb5vQgj6HKKpY_9yCdDhJxstx0oNNyh3ceKUp0bg8XHGAlw6fV4wFPFqVX7EnIrb8k60w9KZw?expires=1748412000&signature=841c08e8c5c65b07bdfc34c137653641d439beeea91a10026172f273e225c3a7&req=dSMnHs58mYZdWvMW3Hu4gUsbdtLMHL8%2BvNVUqH0nWUCckE6Vzv9CTWkVstQb%0AGg%3D%3D%0A)) icon so you can copy the verification codes without navigating to an additional screen.

## **Cerby mobile app**

Dive into the newest additions to our Cerby mobile app:

  * We now track the following analytic events according to the operating system (OS):

    * iOS v1.0.221 and v1.0.222

      * Onboarding

      * Login

      * Profile interactions 

      * Secret details

      * Collection details 

    * Android v1.0.180 and v1.0.181, with full coverage in v1.0.182

      * Onboarding

      * Login

      * Home

      * Collection details

      * Secret details

      * Account details

      * Profile

      * Application settings

      * Trusted devices

  * Keychain data is now completely removed on fresh installs of the Cerby mobile app from iOS v1.0.218 onwards. Some user sessions were not terminated when uninstalling the app.

  * The Cerby mobile app no longer validates the workspace name while the user types the name for logging in purposes. Also, lowercase is enforced. These features were released in iOS v1.0.218 and Android v1.0.181.

  * Restricting workspaces for login through a mobile device management (MDM) platform is now supported in Android v1.0.181.

  * The login credentials of the last accessed account are now preselected when launching an app from the account details screen in iOS v1.0.216.

  * From versions iOS v.1.0.215 and Android v1.0.179 onwards, the Cerby mobile app requires Android 11 and iOS 16 as the minimum supported OS due to security updates and performance improvements. For more information, read the article [Troubleshooting: Older operating systems no longer supported by the Cerby mobile app](https://help.cerby.com/en/articles/6681521-troubleshooting-older-operating-systems-no-longer-supported-by-the-cerby-mobile-app).

* * *

# Fixes

Take note of the issues addressed and resolved by the Development team behind
the Cerby platform:

  * The issue with workspace **Super Admins** being unable to see the items shared with a team, even when they are not part of the team, was fixed.

## **Cerby web app**

  * The issue with not displaying the **More options** drop-down list for a guest user invited to a business hub is fixed. Now, you can perform actions such as removing guest users through the **Members** tab of the business hub details page. 

  * The issue with not redirecting users to the corresponding team from the **Teams** tab of the user details page was fixed. Users were redirected to the main **Teams** view after selecting the **View team** option in the **More options** drop-down list. 

  * The issue with not displaying accounts shared via a public link in the **Activity** view was fixed.

  * The issue with not redirecting users to the secret details page when opening a secret from an email message was fixed. Cerby sends an email whenever a user shares a secret, and it contains a button to open the secret. 

  * The issue with not displaying the **More options** drop-down list of a secret within an expanded collection in the **Collections** view was fixed.

  * The issue with being unable to connect a business hub when selecting different vaults for the business hub account and automation account was fixed.

  * The issue with not preserving the text inputs when moving back or forward in the wizard for connecting a business hub was fixed.

  * The issue with being able to update the YouTube Studio Owner role of a user in the **Members** tab of the business hub details page was fixed. This action is now disabled because YouTube Studio doesn’t support updating an Owner role in any scenario.

## **Cerby mobile app**

  * The issue with not filtering business hubs in the app catalog when adding an account via the Cerby mobile app was fixed in iOS v1.0.222.

  * The issue with displaying an account password before the user manually tapped to view it was fixed in Android v1.0.193.

  * The issue with the Cerby mobile app sometimes crashing when navigating to the **Secrets** screen was fixed in Android v1.0.188.

  * The issue with being incorrectly redirected to the latest autofilled app when launching it from the Cerby mobile app was fixed in Android v1.0.181.

  * The issue with not displaying the password of some Cerby accounts for Instagram after deleting the time-based one-time password (TOTP) configuration was fixed in iOS v1.0.215 and Android v1.0.180.

# New supported managed apps

The following are the latest additions to the list of managed apps with
supported automated tasks:

  * [Acsense](http://acsense.com/)

  * [Aha!](http://aha.io/)

  * [Anedot](http://anedot.com/)

  * [Anthropic](http://console.anthropic.com/)

  * [Apollo](http://studio.apollographql.com/)

  * [Appbot](http://app.appbot.co/)

  * [Your App Domain](http://yourappdomain.com/)

  * [BiliBili](http://bilibili.com/)

  * [Bluesky](http://bsky.app/)

  * [BrandBastion](http://app.brandbastion.com/)

  * [Brandly](http://brandly.com/)

  * [Brightspace](http://anahuac.brightspace.com/)

  * [Chaos](http://chaos.com/)

  * [Checkr](http://checkr.com/)

  * [Cloudally](http://cloudally.com/)

  * [DeepL](http://deepl.com/)

  * [Dock](http://dock.us/)

  * [Doordash](http://doordash.com/)

  * [Dovetail](http://dovetail.com/)

  * [Egnyte](http://egnyte.com/)

  * [Embed.ly - API](https://embed.ly/)

  * [Explorium](https://app.explorium.ai/)

  * [FAMIS360](https://www.accruent.com/products/famis-360)

  * [Gitlab](http://gitlab.com/)

  * [Humata](http://app.humata.ai/)

  * [Kinsta](http://kinsta.com/)

  * [Kuaishou](http://kuaishou.com/)

  * [Massive.io](http://massive.io/)

  * [Mi Plan A](http://www.miplana.mx/)

  * [Mixpanel](http://mixpanel.com/)

  * [NJHIN](http://njhin.info/)

  * [PayPal](http://paypal.com/)

  * [Paypal Business Sandbox](http://sandbox.paypal.com/)

  * [Payper](http://dashboard.payper.ca/)

  * [Planview](http://login.leankit.com/login/)

  * [Playable](http://playable.video/)

  * [Readme](http://readme.com/)

  * [Rival IQ](http://app.rivaliq.com/)

  * [Schwab](http://stockplanservices.schwab.com/)

  * [Shippo](http://apps.goshippo.com/)

  * [SIU](http://siu.anahuacmayab.mx/)

  * [Snappy](http://snappy.com/)

  * [Squarespace](http://squarespace.com/)

  * [Stifel Bank](http://stifel.olbanking.com/)

  * [Superwise](http://superwise.ai/)

  * [testapp.io](http://testapp.io/)

  * [Tiktok Shop](https://seller-us-accounts.tiktok.com/account/login)

  * [User Interviews](http://userinterviews.com/)

  * [Vista Social](http://vistasocial.com/)

  * [Voices](http://voices.com/)

  * [Vonage](http://vonage.com/)

For more information about these apps, read the article [Explore the supported
automated tasks for your managed
accounts](https://help.cerby.com/en/articles/6263064-explore-the-supported-
automated-tasks-for-your-managed-accounts).

