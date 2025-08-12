# Release Notes - May 26, 2025

**Description:** This article describes the latest enhancements and bug fixes to improve your experience using Cerby.

# **New features**

The following are the new features and improvements we released across the
Cerby platform:

## **Start your passwordless journey with Cerby**

Get ready to experience the next evolution of online security and convenience:
passkeys have officially arrived in Cerby!

We're thrilled to introduce this passwordless authentication method for
accessing your accounts. Using a combination of device and biometric
authentication with the Cerby mobile app, your login becomes phishing-
resistant and stronger against common cyber threats, and your experience gets
smoother and effortless.

**Figure 1** shows a sneak peek of the passkeys experience on mobile.

![Screenshots of the Cerby mobile app \(left\) and the Passkey page for
logging in to Amazon. The Cerby mobile app displays a list of saved passkeys
for amazon.com, and the Passkey page displays a button to set up this
authentication
method.](gitbook/imagesAD_4nXf2Eyrg1fPkZSzuHZVbsr9T5QDxILsOPXi6fFLZ6I4jL0MLw3zwnxzuIWIBa62xmNSkWxh1ZKUNnNUwvoqXxYxDq5RFs_g0XnSMN6pGd0AXlsH2vCdpYJ1apJWZOFH3iFoMG_vANg)

**Figure 1.** Passkeys in the Cerby mobile app and the **Passkey** setup page
for Amazon

Want to give it a try? Take a look at the article [Explore passkeys in
Cerby](https://help.cerby.com/en/articles/10875208-explore-passkeys-in-cerby),
where we reference the supported operating systems and apps, as well as the
instructions to create a passkey. This feature was released in the following
versions of the Cerby mobile app: iOS v1.0.241 and Android v1.0.120.

## **Gain more control over your secrets**

The wait is over! Based on your feedback, we've released significant
improvements to the Secrets feature.

Now, you can create secrets with an expiration time between 1 to 30 days. When
they expire, they are automatically deleted. The goal is to reduce manual
cleanup efforts in the Cerby dashboard and enhance protection for your
sensitive information. This feature is available when adding or editing a
secret, as shown in **Figure 2**. For instructions, read the articles [Add a
secret](https://help.cerby.com/en/articles/8705289-add-a-secret) and [Edit a
secret](https://help.cerby.com/en/articles/8705406-edit-a-secret).

![Screenshot of the Add Secret dialog box in the Cerby web app. The “Set
expiration for the secret”  and “Ask users to confirm their identity to view
the secret” options are
selected.](gitbook/imagesAD_4nXc9eKN6poLDx8mQsAAetJxymPq7_3zmYRoE3BOHPVnoVrItl74yG8Xb1Sps5ZIbx4tEEVZiCQF6dZ4uwQ5l8FMXyhnG-
zG-steEyh7-AUwMg3T-ENUO42DMay3Y3u7niWWz7-h4sA)

**Figure 2.** **Add Secret** dialog box in the Cerby web app dashboard

Additionally, as a secret **Owner** , you can turn on or off the identity
confirmation challenge to view a secret anytime. Previously, you could only
set up this configuration when adding a secret; now, you can also do it when
editing a secret.

## **Cerby browser extension**

Explore the latest features in our Cerby browser extension:

  * Our Password Generator is getting more robust. Now, you can generate passphrases and specify the number of words and their complexity using the other password strength selectors.

Give it a try by completing the following steps:

    1. Open the Cerby browser extension popup.

    2. Click the **Password generator** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1542098796/1d957277c3d40c0c5d5b3d6be0e8/AD_4nXeXQn5hz4FHLiyyLXnVpci1DKice9iTxCY2YgyQfbk2Fazqc-x6TKGPHpc5qbvN2zwcLXOYmsg1i_CMuAhlXRELORrH55exbgaBvhwOZZK9bZr9oONaysx3wZJNYPvLvTwAWpcGgA?expires=1748301900&signature=411983d0bc0b55905b6394b07e6d279490fed4a856dc5a677d50329e3459184c&req=dSUjFMl3lYZWX%2FMU3HP0gOwMeXfria8Huon3WiY0Jz68ONuzUGw%3D%0A)) icon. The **Password generator** page is displayed, as shown in **Figure 3**.

![Screenshot of the Cerby browser extension popup on top of a web browser. The
popup displays the “Use passphrase” option selected and a generated
passphrase.](gitbook/imagesAD_4nXco2j6hUjl8QjWAj4gvknbXowVLqQVqmwoLaQ55uWxHPgaC4BfUbMsvfGnppsAt7HI_Ze5jeDjlATSaGCBX9vMezcy804_pGRgVzQlthpzzKfF387_bWvkTJXHSWs6ysqF377CLTA)

**Figure 3.** **Password generator** page in the Cerby browser extension popup

    3. Select the **Use passphrase** option.

    4. Move the **Length (words)** slider to select the number of words in the passphrase.

    5. Select other password strength options to make the passphrase more complex, if necessary.

  * Connecting your existing user accounts to a business hub just got easier, and you don’t even have to use the Cerby web app.   
Whether you log in to your account through the app’s login page or the
dashboard of your identity provider (IdP), such as Okta, the Cerby browser
extension now displays a page where you can select any of your existing
accounts to connect it to the business hub, as shown in **Figure 4**.

![Screenshot of the “Select an account to log in” page in a web browser. The
page displays a list of existing accounts in Cerby for the same external app
so that the user can select
one.](gitbook/imagesAD_4nXdzYqxjbe_XYI8UAE-5_Vk6L2rcWAGbZPBcKZZWtrWib-
_-T7lIAK_4IN88r7dondQj6XY_iG1Hmmz3AnR_3IqriNYK3JaSy2ToQxTEd1RVYrNqUKq-2_tWkpi58gxFLYyDca1n)

**Figure 4.** **Select an account to log in** page

If you don’t have an account for the app, the **No accounts saved for this
business hub** page is displayed or you are redirected to the app’s login
page.

  * To enhance your future logins and avoid errors, autosaving your accounts with the Cerby browser extension is now more granular.

You can now select the corresponding app during an account autosave prompt
when multiple accounts have the same domain, as shown in **Figure 5**. Cerby
will remember your selection the next time you log in.

![Screenshot of the Cerby browser extension popup on top of a web browser. The
popup displays a message saying that the account was saved, and a callout
prompts the user to select the correct app among multiple shared
domains](gitbook/imagesAD_4nXd0SX2kuCxM9LAp6vkgcg02viQKgQXyYGzv3aJpeYSOAw4SRND4-cfSOXJ44Ib7D9yT75LnJh_QMIq13uUMZqdL2Zz4pGcWx-
SxZzmj5aide6dmFsRczTkf-GC1nNDM80XNuHzy)

**Figure 5.** Account autosave prompt in the Cerby browser extension

## **Cerby mobile app**

  * You can now enjoy the following improvements in the Cerby mobile app for iOS v1.0.241 and v1.0.247:

    * Global search navigation

    * Async vault synchronization

    * MFA code autofill during login

    * Hidden secret and time-based one-time password (TOTP)

## **Cerby API**

Check out the new endpoints available in our [developer
portal](https://developer.cerby.com/) to perform the following actions with
the Cerby API:

  * Retrieve the password of an account

  * Create a secret 

  * List vaults

# **Fixes**

Take note of the issues addressed and resolved by the Development team behind
the Cerby platform:

  * The issue with assigning an **Owner** to an account saved in a local vault integrated with AWS KMS was fixed.

  * The issue with being unable to delete Cerby-managed phone numbers from accounts was fixed. Some users with numerous accounts encountered errors when trying to delete an associated Cerby-managed phone number.

## **Cerby web app**

  * The issue with not loading accounts in the **Add accounts to collection** dialog box was fixed. Users encountered an infinite loading state when they had **Owner** access to numerous accounts.

  * The issue with not loading the account details page when a password was last rotated by a user outside a workspace (for example, the Cerby Technical Support team) was fixed. We now display in the account details page that the last password rotation was performed by Cerby.

  * The issue with displaying the email and phone number as required values in the account details page of social media accounts was fixed. Users were blocked from creating Cerby-managed email addresses and phone numbers, so they had to enter dummy values in the fields first.

  * The issue with incorrectly displaying the status of some MFA methods in the account details page was fixed.

  * The issue with searching for a nonexistent workspace member in the **Members** tab of the collection details page was fixed. The **No results found** message is now displayed and it doesn’t get stuck there.

  * The issue with displaying disabled business hubs as duplicates when using the search bar in the **Business Hubs** page was fixed. Now, we identify disabled business hubs with the “Disabled account” status. 

  * The issue with the inconsistent status between business hub integrations in the **Business Hubs** page and the integration details page was fixed. In some cases, the “Up to date” status was displayed despite the value in the **Last updated** field was “Not synced.”

  * The issue with connecting two different service accounts to a business hub integration was fixed. The error occurred when a second integration **Owner** updated the service account. Now, when the service account is updated, the old account is disconnected from the integration automatically.

  * The issue with collection **Collaborators** being able to add subcollections to a collection was fixed.

  * The issue with not displaying an option to remove a host-guest partnership in the**Partners** page was fixed.

  * The issue with the link of an expired verification magic link was fixed. Instead of reloading the page, the link now redirects to an article with more information about the email magic link as MFA identity confirmation method.

  * The issue with displaying collections to which a user has the **Collaborator** role when adding a business hub to a collection was fixed. Only collections a user owns are now displayed.

  * The issue with not updating the role of a user after changing it in the **Members** tab of the collection details page was fixed.

  * The issue with incorrectly displaying the dialog box for sharing an account instead of a business hub was fixed. Users were able to share a business hub as an account if they clicked the **Share** icon right after loading the **All accounts** page or if the internet connection was slow.

  * The issue with a **Team Admin** being able to select the **Remove from team** option from the **More options** drop-down menu to remove themselves from a team was fixed.

  * The issue with the service account being incorrectly displayed in the **Unmatched Users** table of a business hub details page, instead of the **Onboarded Users** table, was fixed. 

  * The issue with not preserving the filters in the **All accounts** page when navigating through other pages and returning to it was fixed.

  * The issue with displaying an empty page of assets in the business hub details page was fixed. We’ve optimized how we retrieve the assets to avoid timeouts.

## **Cerby API**

  * The issue with retrieving custom roles as entitlements of an integration was fixed.

* * *

# **New supported managed apps**

The following are the latest additions to the list of managed apps with
supported automated tasks:

  * [Ada](http://www.ada.cx/login/)

  * [Advanced Web Ranking](http://advancedwebranking.com/)

  * [Amazon Developer](http://developer.amazon.com/)

  * [Aumni](http://aumni.fund/)

  * [Barclays Developer](https://developer.barclays.com/)

  * [Bluesnap](http://bluesnap.com/)

  * [Braze](http://braze.com/)

  * [Builtin](http://builtin.com/)

  * [ChaseLoan](https://chaseloanmanager.chase.com/Chaselock/)

  * [Chilipiper](http://chilipiper.com/)

  * [Cloudflare](http://cloudflare.com/)

  * [Cohesion](http://cohesionib.com/)

  * [Crazy Egg](http://crazyegg.com/)

  * [Crestron XiO](http://crestron.io/)

  * [Disqus](http://disqus.com/)

  * [Echomark](http://echomark.com/)

  * [EfaxCorporate](http://efaxcorporate.com/)

  * [Facebook](http://facebook.com/)

  * [Fairygodboss](http://fairygodboss.com/)

  * [Foursquare](http://foursquare.com/city-guide)

  * [Getty Images](http://gettyimages.com/)

  * [Govly](http://govly.com/)

  * [Grafana](http://grafana.com/)

  * [Handsontable](http://my.handsontable.com/)

  * [Harmonic.ai](http://harmonic.ai/)

  * [Hoppscotch](http://hoppscotch.io/)

  * [Hotel Effectiveness](http://my.hoteleffectiveness.com/)

  * [IHFA](https://lender.ihfa.org/)

  * [Ivy Mobility](http://bimbo-mx-uat.ivycpg.com/)

  * [LinearApp](http://linear.app/)

  * [Livingston](http://livingston.com/)

  * [Lusha](http://lusha.com/)

  * [Miratech Tracker I-9](http://psts.i9complete.com/)

  * [Muck Rack](http://muckrack.com/)

  * [OneSignal](http://onesignal.com/)

  * [PartnerStack](http://dash.partnerstack.com/)

  * [Ping Identity](http://pingone.com/)

  * [Profitsword](https://sage.profitsage.net/PS-Sage/UI/login.aspx)

  * [Qodo](http://app.qodo.ai/signin)

  * [Sendbird](http://sendbird.com/)

  * [smarterqueue](http://smarterqueue.com/)

  * [Smartling](http://smartling.com/)

  * [Starlink](http://starlink.com/)

  * [StatusGator](http://statusgator.com/)

  * [streamyard](http://streamyard.com/)

  * [Testomat](http://app.testomat.io/)

  * [The Muse](http://themuse.com/)

  * [Trustpilot](http://www.trustpilot.com/users/connect)

  * [Unifi](http://unifi.ui.com/)

  * [Upwork](http://upwork.com/)

  * [Venturefizz](http://venturefizz.com/)

  * [Voya](http://voya.com/)

  * [WalletHub](http://wallethub.com/)

  * [Yelp](http://yelp.com/)

For more information about these apps, read the article [Explore the supported
automated tasks for your managed
accounts](https://help.cerby.com/en/articles/6263064-explore-the-supported-
automated-tasks-for-your-managed-accounts).

* * *

# **New supported business hubs**

The following are the latest additions to the list of business hubs with
supported user management automated tasks:

  * [Ada](http://ada.cx/login/)

  * [Amazon Developer](http://developer.amazon.com/)

  * [Aumni Business](http://aumni.fund/)

  * [Autodesk](http://autodesk.com/)

  * [Bluesnap](http://bluesnap_tenant.com/)

  * [Braze](https://www.braze.com/)

  * [Bridger QA](http://bridgerstaging.lexisnexis.com/)

  * [Bridger](http://bridgerstaging.lexisnexis.com/)

  * [Builtin Boston](http://builtinboston.com/)

  * [Builtin](http://builtinnyc.com/)

  * [Canva](http://canva.com/)

  * [Cloudflare](http://cloudflare_tenant.com/)

  * [Cohesion Business](http://cohesionib.com/)

  * [Crazy Egg](http://crazyegg.com/)

  * [Crestron XiO](http://crestron.io/)

  * [Data.AI](http://www.data.ai/)

  * [Disqus Sites](http://disqus.com/)

  * [Disqus](http://disqus.com/)

  * [Echomark Business](http://echomark.com/)

  * [Fairygodboss](http://fairygodboss.com/)

  * [Glassdoor](http://glassdoor.com/)

  * [Govly](http://govly.com/)

  * [Grafana Business](http://grafana.com/)

  * [Grammarly Business](http://grammarly.com/)

  * [Harmonic.ai](http://harmonic.ai/)

  * [Hotel Effectiveness](http://my.hoteleffectiveness.com/)

  * [Hyperbound](http://hyperbound.ai/)

  * [Indeed Business](https://www.indeed.com/)

  * [Just Words](http://justwords.ai/)

  * [Linear Business](http://linear.app/)

  * [Livingston](http://screening.tradesphere.net/)

  * [Lusha](http://lusha.com/)

  * [Meraki Networks](https://meraki.cisco.com/)

  * [MongoDB Cloud](http://cloud.mongodb.com/)

  * [Muck Rack Business](http://muckrack.com/)

  * [Notion](http://notion.so/)

  * [OneSignal](http://onesignal.com/)

  * [PartnerStack](http://dash.partnerstack.com/)

  * [Perception Point](http://perception-point.io/)

  * [Profitsword](https://actabl.com/)

  * [Qodo](http://app.qodo.ai/signin)

  * [Readme Enterprise](http://dash.readme.com/)

  * [Sendbird](http://sendbird.com/)

  * [Site24x7](https://www.site24x7.com/)

  * [Slack](http://slack.com/)

  * [StatusGator](http://statusgator_tenant.com/)

  * [Superwise](http://app.superwise.ai/)

  * [Testomat](http://app.testomat.io/)

  * [The Muse](http://themuse.com/)

  * [Unity](http://unity.com/)

  * [Upwork Business](http://upwork.com/)

  * [Venturefizz Business](http://venturefizz.com/)

  * [Zapier](https://zapier.com/app/login)

For more information about these business hubs, read the article [Explore the
supported business hubs and automated
tasks](https://help.cerby.com/en/articles/11061084-explore-the-supported-
business-hubs-and-automated-tasks).

