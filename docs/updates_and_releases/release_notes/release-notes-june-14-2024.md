---
description: This article describes the latest enhancements and bug fixes to improve your experience using Cerby.
---

# Release Notes - June 14, 2024

# New features

The following are the new features and improvements we released across the Cerby platform:

  * We’re always listening to your feedback and looking for ways to keep your teams focused and efficient while enhancing security and compliance. With our newest **Login-only** workspace role, you have more options to implement the principle of least privilege.
You can now grant these users permission to log in to your accounts and view secrets only, ensuring that account creation is restricted to designated individuals.
For more information about what you can or cannot do with this role, read the article [How Cerby manages roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).
​

  * We took a step forward in your experience with trusted sessions and devices. You can now set up a trusted session on a new device by approving it through an already registered device, as shown in **Figure 1**.

<figure><img src="../.gitbook/assets/AD_4nXfFdLZSa561pTrE8hlfc79d7itr5WO8b8H8lvYsxcV_-y4fEOFOYxCDWKzPN7wsqRulBCUuq-lo9OrzcT_gJ-a71WhfyA04iG1xgDGGlfiHzr4ZZTNna4-wJOGeMB799c0zT3DOjLpBcf7sAPJtiw12DIdv.png" alt="Screenshot of the “Trust this session?” and “My trusted devices” screens of the Cerby mobile app. You can approve a new trusted session through the mobile app and view the list of trusted devices"><figcaption></figcaption></figure>

**Figure 1.** **Trust this session?** screen in the Cerby mobile app

Additionally, if you use the Cerby browser extension on a new device but have already set up the Cerby web app with the same browser, your session will be automatically registered as trusted. Pretty neat, right? If you want more information and instructions, read the article [Set up trusted sessions on your devices](https://help.cerby.com/en/articles/8142370-set-up-trusted-sessions-on-your-devices).

By the way, we also doubled your capacity for secure access. You can now register trusted sessions on up to 20 devices.

  * Who says you have to wait for Halloween to experience a good resurrection? You can now restore an account you previously deleted from your workspace, as shown in **Figure 2**.

<figure><img src="../.gitbook/assets/AD_4nXcjy-Fkrbpo2hcEEC-zA1ZNMQSWYyrztb9TNuzVvclOZTvkY9VpkCZILSsutul-vMyh1sbXK1Hj35Jg_vEKlkEJtT5FwqacXQs9cAteWayrADLp5Ey1jAELdoENWmYzIl7MLQsesYpEjek1nVsScFKsbqMG.png" alt="Screenshot of the Cerby web app dashboard with multiple deleted account cards. You can select the “Restore account” option from the “More options” drop-down list."><figcaption></figcaption></figure>

**Figure 2.** Deleted accounts in the **All accounts** view of the Cerby web app dashboard

You just have to complete the following ritual in the Cerby web app to make your account rise from the ashes:

    1. Look for the account using the **Deleted accounts** filter in the **All accounts** view.
    2. Click the **More options** icon of the ghost account card.
    3. Select the **Restore account** option.

  * We’re about to dive into some detailed information but bear with us. It'll be worth it, especially if you're an admin of a Meta Business Manager or a TikTok Business Center connected to Cerby.
We now support sharing app integrations with Cerby teams for these paid social apps. You may have already used this feature in other app integrations to invite multiple users simultaneously. However, Meta and TikTok differ because our integrations work with them based on data requests through application programming interfaces (API) instead of automated tasks.
Our Development team worked hard to make that feature a reality through APIs.

  * Now that we’re talking about Meta Business Manager, we have good news. When using **All-Access Mode** , you can now view all of the Meta Business assets that were synchronized in Cerby. Full visibility mode on!
  * Keep the welcome mat rolled out a bit longer for your guest users. The invitations you send for external collaborators to join your Cerby workspace now expire after three days instead of 24 hours.
Give your guests plenty of time to accept and get in on the action!

  * We’ve enhanced our [Local Partners](https://help.cerby.com/en/articles/8980877-explore-partners#h_7e4add33a2) feature to help you with the management of **Guest Users** :
    * Guest admins can now resend invites, reset multi-factor authentication (MFA), and force password resets for guest users from the **Members** tab of the **Partners** view.
    * Workspace members cannot invite other employees from the same organization as **Guest Users**. We’ve introduced an email verification to filter out invitations sent to users with your corporate domain. If you want them to access your workspace, ask your IT admin to assign them to Cerby.
  * Stop holding back when saving important information in Cerby. You can now enter up to 40,000 characters in the**Notes** field of a new [custom item](https://help.cerby.com/en/articles/8860242-add-a-custom-item). Say goodbye to the 255 characters that might have been limiting your documentation needs.

## Cerby web app

Check out what’s new in our Cerby web app:

  * You know we’re in when it comes to transparency, auditability, and compliance. We now provide workspace **Admins** more information in the downloadable CSV report of the **All members** view, such as:
    * The user ID of all workspace users.
    * The role of all users on all the accounts and collections they have saved or to which they have shared access.
    * The status of multi-factor authentication (MFA) that is managed by Cerby.
  * We revamped the experience of viewing a secret. Whether you click the secret card or the **View** button, now you are redirected to the secret details page instead of a dialog box.
In addition to being consistent with the behavior of accounts, we wanted to accommodate long secrets, including a **View more** button, and reduce the number of clicks in case you want to make edits. Moreover, we added a **Copy** button for the secret name and body.
​

  * As an app integration Owner who shares access to Pinterest Business and triggers an invite from Cerby, you can now select the assets to share with the users and their corresponding permissions.
​

  * Talking about accessibility and other ways to interact with the Cerby web app, you can now navigate through the drop-down list of the **Add item** button using your keyboard. Also, you can keep using the keyboard to move through the input fields of the dialog boxes to add accounts and secrets.

## Cerby browser extension

Explore the latest features in our Cerby browser extension:

  * Now, you can view your collections and subcollections and navigate through them by clicking the **Collections** icon located next to the new global search bar. **Figure 4** shows how the **Collections** screen looks.

<figure><img src="../.gitbook/assets/AD_4nXdg8g82Olzmbpb5NPFwEvT6yjFqipifAN9lYHBb7bAYqz6Rc5qj8461rLcaafspDT4jbaImf6k0LDs_p22bkXTHFoHyg08Idqt45bOd7oSuH4T1OyjX93UI8-Je426_NwDT5dZ2tPYk1HeNn9QpwCanyFAO.png" alt="Screenshot of the “Collections” screen in the Cerby browser extension popup. You can navigate through your collections and subcollections."><figcaption></figcaption></figure>

**Figure 3. Collections** screen in the Cerby browser extension popup

And yes, you read it correctly. We’ve also released a global search bar that enables you to look for any item. But don’t worry, you can still filter the items in the extension popup by accounts and secrets.

Take a look at the global search in **Figure 4**.

<figure><img src="../.gitbook/assets/AD_4nXeZE3mVVfAFHxJdHcxE32AnuP7qlMTP4JoGI0_aAthfw4I1pkmdmtCeTlKZw3ZiT1QP9mMC3fPmLcz9ursBq6eW9lRSy6JMx3zp5ZI_wpd9v3dajbODLATgbkY92c-PvqUbhjmlH9-Jp0oFcwwYVc970Uw.png" alt="Screenshot of the global search bar in the Cerby browser extension popup. You can filter your search by all items, accounts, and secrets."><figcaption></figcaption></figure>

**Figure 4.** Global search bar in the Cerby browser extension popup

  * Feel like a celebrity when using the Cerby browser extension. When you have saved accounts or secrets with long names, you can now view the entire name when hovering over the cards on the extension popup. Almost instantly, the name will start to scroll from right to left, just as billboards do. This feature is available from version v1.0.297 onwards.
  * We know you love Cerby the Dog but want a more streamlined login process. That's why we made a few changes to the process. Now, after you log in to the Cerby browser extension by entering your credentials on a new browser tab, a revamped success page is displayed, and you are automatically redirected to the Cerby web app dashboard instead of staying on the **All set** page.

## Cerby mobile app

Dive into the newest additions to our Cerby mobile app:

  * Another one is about feature parity between client apps. Now, you can do the following with the Cerby mobile app:
    * Add an account and edit account details
    * Add secrets and secret items (such as WiFi, SSH keys, database, server, and custom item) and edit secret details
    * Share accounts, secrets, and collections with other workspace members, guest users, and teams
  * Your time is valuable, and that’s why we always look for ways you can save it. In iOS v1.0.168, we released improvements to the AutoFill suggestions. Now, the Cerby mobile app suggests the last used accounts when you attempt to log in to your apps using AutoFill.
  * To save you one tap when copying a value from the account details screen, we implemented the tap and hold interaction. Before versions 1.0.156 for Android and v1.0.159 for iOS, you had to tap the **More options** icon to select the **Copy** option.
  * Don’t worry if you dismiss the prompt to set up a trusted session with your Cerby mobile app. We now display a banner on top of the screen for you to set up the session whenever you want.
* * *

# Fixes

Take note of the issues addressed and resolved by the Development team behind the Cerby platform.

## Cerby web app

  * The issue with being unable to attach KEY and CERT files when creating a secret was fixed.
  * The issue with collection **Collaborators** being able to view other collections to which they have not been granted access when searching for a subcollection was fixed.
  * The issue with displaying the “Unable to load” error message when checking for updates for a TikTok Business Center app integration was fixed.
  * The issue with not displaying Pinterest Business assets synchronized with Cerby after a check for updates was fixed.
  * The issue with not displaying line breaks in the content of a secret when sharing it via a public link was fixed. The original formatting is now preserved, including line breaks.
  * The issue with not filtering results when searching for a team through the search bar of the **Teams** view was fixed.
  * The issue with displaying the incorrect number of teams a user can access via the **Teams** view was fixed.
  * The issue with the **Shared Inbox** falling into a loading loop when the inbox is empty was fixed.
  * The issue with sharing an account with two workspace members as **Collaborators** even when users select the **Owner** role, was fixed.

## Cerby browser extension

  * The issue with displaying the save accounts at login feature even when the account was already saved in Cerby was fixed in v1.0.285.
  * The issue with being unable to auto-login to an account due to not having a trusted session was fixed in v1.0.306. The extension was not clearing out the state of a disabled device; therefore, it was not asking users to set it up again.
  * The issue with displaying the Cerby browser extension icon with a logged-out status even when users have an active session was fixed in v1.0.288.
  * The issue with not detecting signup activity when the user is logged out of the Cerby browser extension was fixed in v1.0.284.

## Cerby mobile app

  * The issue with being unable to clear the input field of the login URL when adding an account was fixed in Android v1.0.156. Users had to tap outside the field and tap again the field to be able to delete the inputted text.
The issue with being unable to view Instagram accounts as Autofill options due to changes in the internal app identifier of Instagram was fixed in iOS v1.0.172.

* * *

# Security fixes

  * The issue with only rotating the passwords of accounts when they were shared directly with a deprovisioned user, not the ones shared via a collection, was fixed.
* * *

# New supported managed apps

The following are the latest additions to the list of apps with supported automation tasks:

  * [Aetna Vision](http://aetnavision.com/)
  * [Allied Telecom](http://connection.alliedtelecom.net/)
  * [Amazon Ads](http://amazon.com/)
  * [American Strategic](http://americanstrategic.com/)
  * [AnyBill](http://secure-platform.anybill.com/)
  * [Apple Search Ads](http://app.searchads.apple.com/)
  * [Arin](http://arin.net/)
  * [Atkins](http://atkins.com/)
  * [AWS IAM User Account](https://signin.aws.amazon.com/)
  * [Axis](http://axiswg.com/)
  * [Axis Background](http://axis.chyron.com/)
  * [BH Photo Video](http://bhphotovideo.com/)
  * [Brainstorm Force](http://brainstormforce.com/)
  * [BRiweb](http://participant.briweb.com/)
  * [California Fair Plan](http://cfpnet.com/)
  * [CapitalOne](http://capitalone.com/)
  * [CBS Sports](http://cbssports.com/)
  * [Citi](http://citi.com/)
  * [CityVU](http://cityvu.co/)
  * [Claris](http://my.claris.com/)
  * [Claris FileMaker](http://community.claris.com/)
  * [CNET](http://cnet.com/)
  * [Coda](http://coda.io/)
  * [Comic Con Portal](http://comic-con.configio.com/)
  * [Connection](http://connection.com/)
  * [Consumer Affairs](http://consumeraffairs.com/)
  * [CSC Global](http://weblogin.cscglobal.com/)
  * [Cultivate Learning](http://cultivatelearning.ca/)
  * [CVS](http://cvs.com/)
  * [Cyber Source](http://businesscenter.cybersource.com/)
  * [Datorama](http://platform.datorama.com/)
  * [Dell](http://dell.com/)
  * [Delta](http://delta.com/)
  * [Delta Dental](http://deltadentalins.com/)
  * [Disney Plus](http://disneyplus.com/)
  * [Dmarcian](http://dmarcian.com/)
  * [DMV](http://dmv.ca.gov/)
  * [eBay](http://ebay.com/)
  * [Eeg Cloud TV](http://eegcloud.tv/)
  * [Elementor](http://elementor.com/)
  * [Empower Teams](http://portal.empowerteams.io/)
  * [Etrade](http://us.etrade.com/)
  * [Evercast](http://app.evercast.us/)
  * [Fantastapack](http://fantastapack.com/)
  * [Flat](http://flat.io/)
  * [Fox Affiliate](http://foxaffiliateportal.com/)
  * [Geico](http://ecams.geico.com/)
  * [Google Ads](http://google.com/)
  * [ID.me](http://id.me/)
  * [Imagn](http://imagn.com/)
  * [Inspira Financial](http://inspirafinancial.com/)
  * [Larkin](http://thelarkincompany.com/)
  * [Learning Bridge](http://learningbridge.com/)
  * [Little Caesar - Call of Duty Sweepstakes](http://r09513callofdutylittlecaesars-reviewtool-prod.azurewebsites.net/)
  * [LiveRamp](http://liveramp.com/)
  * [LiveU central](http://lu-central.liveu.tv/)
  * [MediaCloud](http://mediacloud.fox/)
  * [Megaphone TV](http://megaphonetv.com/)
  * [Merkle](http://eprize.net/)
  * [Microsoft Live](http://login.live.com/)
  * [Microsoft Partner Hub](http://partnerhub.msn.com/)
  * [Midco Sports Plus](http://midcosportsplus.com/)
  * [Mobbin](http://mobbin.com/)
  * [MorganStanley AtWork](http://atwork.morganstanley.com/)
  * [Motortrend](http://motortrend.com/plus/)
  * [National General Agency](http://natgenagency.com/)
  * [Neptune Agent Portal](http://neptuneflood.com/)
  * [NGP VAN](http://ngpvan.com/)
  * [OneTrust](http://onetrust.com/)
  * [Pacific specialty](http://pacificspecialty.com/)
  * [Pandora](http://pandora.com/)
  * [Pendo](http://pendo.io/)
  * [PL Rating](http://rating.vertafore.com/)
  * [Progressive](http://progressive.com/)
  * [Quickbase](http://quickbase.com/)
  * [Quickbooks](http://quickbooks.intuit.com/)
  * [Rebrandly](http://rebrandly.com/)
  * [Resources For Living](http://resourcesforliving.com/)
  * [RunZero](http://runzero.com/)
  * [S&S Active Wear](http://ssactivewear.com/)
  * [SageSure](http://agents.sagesure.com/)
  * [Santander Empresas](http://empresas3.gruposantander.es/)
  * [SkillJar](http://skilljar.com/)
  * [Small Improvements](http://app.small-improvements.com/)
  * [Southwest](http://southwest.com/)
  * [State Auto](http://stateauto.com/)
  * [Tealium](http://my.tealiumiq.com/)
  * [TicketsAtWork](http://ticketsatwork.com/)
  * [Travel Tracker Security](http://tracker.travelsecurity.com/)
  * [Tripsource](http://mytrips.tripsource.com/)
  * [Trustwave](http://trustwave.com/)
  * [UScellular](http://uscellular.com/)
  * [Vanity Fair](http://vanityfair.com/)
  * [WhenToWork](http://whentowork.com/)
  * [Workmatters](http://workmatters.workcare.com/)
  * [Zoho](http://zoho.com/)
  * [ZoomShift](http://zoomshift.com/)
