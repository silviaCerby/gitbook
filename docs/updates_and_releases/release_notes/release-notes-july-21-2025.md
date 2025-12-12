---
description: This article describes the latest enhancements and bug fixes to improve your experience using Cerby.
---

# Release Notes - July 21, 2025

# New features

The following are the new features and improvements we released across the Cerby platform:

## Keeping it fresh and secure with password policies

We’re rolling out a powerful feature designed to boost your security posture: Password Policies powered by Cerby automation.

With this feature, you can now set policies to enforce password rotations for all the accounts saved in your workspace belonging to an app. You can choose to start the policy after a user login event or schedule rotations on a date you select, specifying the frequency and time window for execution.

The new Password Policies feature is now your go-to solution for protecting your accounts, replacing the existing Policies experience. If you are interested in trying it out, contact your Customer Success Manager.

**Figure 1** shows how the **Password Policies** page looks, with policies for multiple apps.

<figure><img src="../.gitbook/assets/AD_4nXciRV6HdVHFMq_ixs0u0ZzrNjLTmOZlVcVgJPr3WhlufsB5jOKIeACZ-eGK9Rp03TR5rqgIuAskO-F_RdduvKaRP-dRjRsoRciqPhYN3xnYsiyL6XmfQgVwHQSR4IjpfQN7kCaDkQ.png" alt="Screenshot of the Cerby web app dashboard. The Password Policies page is displayed with a list of apps that already have a policy in place."><figcaption></figcaption></figure>

**Figure 1. Password Policies** page in the Cerby web app dashboard

Learn more about this feature in the article [Explore Password Policies](https://help.cerby.com/en/articles/11465716-explore-password-policies).

## Level up your login with RSA token MFA

If you are a user in high-security environments, such as financial institutions, we have something special for you. We’re excited to announce a significant upgrade to our multi-factor authentication (MFA) capabilities.

We now support RSA tokens as the MFA method of your accounts. With this feature, Cerby can streamline the retrieval of codes, enabling you to access your apps faster. Additionally, you can set RSA tokens as your MFA method in two ways: using an activation link in the Cerby web app or scanning a QR code with the Cerby mobile app (iOS and Android).

**Figure 2** shows a sneak peek of the RSA token experience.

<figure><img src="../.gitbook/assets/AD_4nXe-Z22iJWy9A7deOfrieJkRnR4eL4oACv-lW_TF0EigVRXFzM6EQTG-QbPcVrYU2g4xlu1fFN6o1C1vGzJawlNtSIrJd1n-KnPI1tzXlcY62RfgxPgSL-Arnuvbe9m6DaU7jtDmsg.png" alt="Screenshot of the Cerby web app dashboard \(left\) and the mobile app \(right\). The account details page is displayed in the web app with an RSA code, and a QR code being scanned is displayed in the mobile app."><figcaption></figcaption></figure>

**Figure 2.** RSA code in the account details page of the Cerby web app (left) and QR code for setup in the Cerby mobile app (right)

For more information, read the article [Set RSA tokens as your account MFA method](https://help.cerby.com/en/articles/10858212-set-rsa-tokens-as-your-account-mfa-method).

## Your data privacy, our priority

We heard and addressed your concerns about data privacy.

To enhance security and reduce the risk of sensitive information being exposed on screen unintendedly, we now hide by default the following data: the body of a secret and multi-factor authentication (MFA) codes. Now, users must click to show these values in the Cerby web app, browser extension, and mobile app.

This added layer of protection means you can navigate your secrets and account details with confidence.

## Expanding the identity management horizon

Our commitment to providing a versatile and comprehensive solution for your organization's unique needs continues! We're excited to announce a powerful addition to our robust suite of identity provider (IdP) integrations.

Now, you can enjoy seamless user provisioning via SCIM with OneLogin! This means you can easily set up a Cerby workspace where user accounts are automatically created and removed based on user assignments directly within your OneLogin instance, streamlining your user lifecycle management.

Check out our IdP documentation in the [Creating and setting up your workspace](https://help.cerby.com/en/collections/5819419-creating-and-setting-up-your-workspace) collection.

## Cerby web app

Check out what’s new in our Cerby web app:

  * Based on user feedback, push notifications are now removed as the identity confirmation method when creating a public link with the Cerby web app for sharing an account or secret.
  * We’ve made improvements to the performance of the **Members** table so that results now load faster.
  * A new pagination feature now enables our users to customize the number of items to display per page. The available options are 20, 50, and 100 items per page, aiming to improve the user experience and efficiency. Currently, this feature is only released for business hub tables.

## Cerby mobile app

Dive into the newest additions to our Cerby mobile app:

  * You can now use biometric challenges instead of magic links sent via email when you access secrets that require identity confirmation with the Cerby mobile app. This feature aims for a more secure and user-friendly experience and is available from versions iOS v1.0.242 and Android v1.0.201 onwards.
  * You can now create passkeys when adding an account to Cerby. This feature was initially supported in iOS, but was released for Android in version v1.0.207. For more information about passkeys, read the article [Create a passkey for an account using the Cerby mobile app](https://help.cerby.com/en/articles/10875236-create-a-passkey-for-an-account-using-the-cerby-mobile-app).
  * Passkeys with Cerby are now supported by Canva and Shopify.

## Cerby API

Check out the new endpoints available in our [developer portal](https://developer.cerby.com/) to perform the following actions with the Cerby API:

  * Retrieve users or teams of a secret
  * Share a secret with a user or team
  * Retrieve a list of vaults

Additionally, we added the `lastLoginDate` attribute in the account schema. This optional value contains the date when a user last logged in to the account, which means they retrieved the account password for login.

* * *

# Fixes

Take note of the issues addressed and resolved by the Development team behind the Cerby platform:

  * The issue with failed syncs after connecting a Discord business hub was fixed.
  * The issue with the initial sync to extend accounts to Okta and not syncing teams was fixed.

## Cerby web app

  * The issue with not updating the role of a user in the **Members** tab of the collection details page was fixed. In some cases, the drop-down menu was not displayed; in others, the update was not applied.
  * The issue with not loading the vault settings page for an Azure key vault was fixed.
  * The issue with users being able to add self-managed accounts to Cerby even when this functionality has the blocked status was fixed. Users were able to add the account by pasting the app URL in the **App name or URL** field of the **Add account details** dialog box.
  * The issue with users being unable to add self-managed accounts to Cerby was fixed. In this case, self-managed accounts were not blocked.
  * The following issues with the local partner experience were fixed:
    * **Guest Admins** of a local partner with the **Manager** role on shared accounts couldn’t share these accounts with **Guest Users**.
    * The local partner details section couldn’t be loaded.

## Cerby browser extension

  * The issue with the account autosave experience not working correctly for the Livingston app was fixed.

## Cerby mobile app

  * The issue with the Cerby mobile attempting to open previews for unsupported secret file attachments was fixed. Now, we display a message indicating when the preview is not supported.

## Cerby API

  * The issue with retrieving users who have shared access to a secret via a collection was fixed.
  * The issue with requests failing when not including the optional message when sharing a secret with a user was fixed.
* * *

# Security fixes

  * A potential HTML injection vulnerability in auto-generated emails was fixed. User-controllable content, such as usernames or custom messages when completing automation jobs or sharing collections with other users, is now properly sanitized to prevent malicious HTML from being rendered.
  * A potential security bypass on iOS devices was fixed. We've expanded and improved our detection methods for jailbroken or rooted devices, automatically blocking access to Cerby if a device is identified as potentially compromised.
* * *

# New supported managed apps

The following are the latest additions to the list of managed apps with supported automated tasks:

  * [Ad Age](http://adage.com/)
  * [Advantage Credit](http://credit.advcredit.com/)
  * [Adyen](http://ca-live.adyen.com/)
  * [AM Best](http://web.ambest.com/)
  * [Amazon Vendor](http://vendorcentral.amazon..com/)
  * [Arizona PIT](https://efile.aztaxes.gov/AZFSETPortal)
  * [Arizona SUI](http://ftp.azdes.gov/)
  * [AudiTech](https://audit-tech.io/)
  * [AZTaxes](http://aztaxes.com/)
  * [BaptistHealth](http://baptisthealth.avizia.com/)
  * [Barclays](http://developer.barclays.com/)
  * [Bayview/Lakeview](https://www.bayviewtpo.com/)
  * [Better Business Bureau](http://bbb.org/chicago/login)
  * [Bloomberg Tax](http://bloombergtax.com/)
  * [Builder IO](http://builder.io/login)
  * [Chase Loan Manager](http://chaseloanmanager.chase.com/Chaselock/)
  * [Chicago Sun-Times](http://chicago.suntimes.com/)
  * [CIC Mortgage Credit](http://cic.meridianlink.com/)
  * [CNBC](http://cnbc.com/)
  * [Complaints Board](http://complaintsboard.com/)
  * [Cursive](http://cursive-ide.com/)
  * [Dailymotion](http://dailymotion.com/)
  * [Dale Connect Evident](https://dale.connect.evident.com/)
  * [Dane](http://emmet.dane.gov.co/)
  * [Government of the District of Columbia](http://essp.does.dc.gov/TPSPA/Account/Login)
  * [Dun & Bradstreet](http://dnb.com/)
  * [eGoldFax](http://my.egoldfax.com/)
  * [FL BSWA Website](https://secure.bswa.net/BSWALogIn.aspx)
  * [Forbes](http://forbes.com/)
  * [Fortune](https://fortune.com/)
  * [Georgia Tax Center](http://gtc.dor.ga.gov/)
  * [Cabal](http://getcabal.com/)
  * [GrowthSpace](http://app.growthspace.com/)
  * [Hawaii PIT](https://hitax.hawaii.gov/_/#1)
  * [IBISWorld](http://ibisworld.com/)
  * [ID UI](https://govconnect.iowa.gov/)
  * [Idaho PIT](http://dahotap.gentax.com/TAP)
  * [Illinois My Tax Portal](https://mytax.illinois.gov/_/)
  * [Impact](http://impact.com/)
  * [Kansas New Wage and Tax Reporting System](http://kansaslabor.gov/accessks/faces/login/login_local.xhtml)
  * [Kansas Portal Labor](http://kansaslabor.gov/accessks/faces/login/login_local.xhtml)
  * [Kansas Department Of Revenue Customer Service Center](http://kdor.ks.gov/Apps/kcsc/Login.aspx)
  * [Los Angeles Business Journal](http://labusinessjournal.com/)
  * [LoopsAI](http://app.getloops.ai/)
  * [Louisiana SUI](http://esweb.revenue.louisiana.gov/)
  * [Mailmodo](http://mailmodo.com/)
  * [Mailosaur](http://mailosaur.com/)
  * [Maine PFML](https://pfml.maine.gov/contributions/_/)
  * [Maine ReEmployME](https://assist.reemployme.maine.gov/)
  * [Maine Revenue](http://revenue.maine.gov/)
  * [Minnesota Department of Revenue](http://www.mndor.state.mn.us/)
  * [Minnesota UI](http://www1.uimn.org/)
  * [Mississippi Department of Employment Security](http://accessmstax.mdes.ms.gov/accessmstax/faces/login/login.xhtml)
  * [Montana State Withholding](https://tap.dor.mt.gov/_/)
  * [MS Department of Revenue](https://tap.dor.ms.gov/)
  * [My Alaska](http://my.alaska.gov/portal/login)
  * [My Tax Dc](https://mytax.dc.gov/)
  * [MyDisney](http://my.disney.com/)
  * [North Dakota State Government](http://apps.nd.gov/)
  * [North Dakota Taxpayer Access Point](https://apps.nd.gov/tax/tap)
  * [Nebraska Business Electronic Filing System](http://ndr-efs.ne.gov/revefs/allPages/login.faces)
  * [NEWorks Portal](https://neworks.nebraska.gov/vosnet/loginintro.aspx?plang=E)
  * [Oklahoma ESC](https://www.ok.gov/oesc/newhire/app/index.php)
  * [Oklahoma TAP](http://oktap.tax.ok.gov/)
  * [Pickcel](http://pickcel.com/)
  * [Pissed Consumer](http://www.pissedconsumer.com/)
  * [PitchBook](http://pitchbook.com/)
  * [PolyLens](http://polylens.com/)
  * [Posthog](http://posthog.com/)
  * [PR Week](https://www.prweek.com/login?returnUrl=https://www.prweek.com/us)
  * [The Predictive Index](http://app.predictiveindex.com/)
  * [PyPI](http://pypi.org/)
  * [Quantum](http://quantum.com/)
  * [Saas Grid](http://app.saasgrid.com/login)
  * [San Francisco Chronicle](http://subscription.sfchronicle.com/)
  * [Scappman](http://portal.scappman.com/)
  * [SiteJabber](https://www.sitejabber.com/login)
  * [Spectral Ops](http://app.spectralops.io/)
  * [Splunk Cloud](http://splunkcloud.com/)
  * [Sports Business Journal](http://sportsbusinessjournal.com/Member/Login/)
  * [Success Coaching](http://learn.successcoaching.co/)
  * [Talenox](http://talenox.com/)
  * [Taobao](http://login.taobao.com/)
  * [Tesorio](http://dashboard.tesorio.com/login)
  * [The Atlantic](http://accounts.theatlantic.com/login)
  * [The Economist](http://economist.com/)
  * [The Muse Employer](http://employers.themuse.com/)
  * [The Information](http://theinformation.com/)
  * [Thought Industries](http://thoughtindustries.com/)
  * [Time](https://www.time.com/)
  * [Trendemon](http://trendemon.com/)
  * [Triller](http://triller.com/)
  * [Unit](http://app.unit.co/)
  * [US Bank Lender Portal](http://usb-welcome.api.digitals.dmattercloud.com/)
  * [Washington Corporations](http://washington_corporations.com/)
  * [Washington Secure Access](http://washington_secure_access.com/)
  * [Wiz](https://www.wiz.io/)
* * *

# New supported business hubs

The following are the latest additions to the list of business hubs with supported user management automated tasks:

  * [1Password](http://1password.com/)
  * [Adobe Creative Cloud](http://adobe.com/)
  * [Adwords](http://ads.google.com/)
  * [Adyen Business](http://ca-live.adyen.com/)
  * [Affinity](http://affinity.co/)
  * [Apple App Store](https://business.apple.com/)
  * [AudiTech](https://audit-tech.io/)
  * [Auvik](http://my.auvik.com/)
  * [Barclays](http://developer.barclays.com/)
  * [Bitly](https://bitly.com/)
  * [Blinkops](http://app.blinkops.com/)
  * [Bloomberg Tax](http://bloombergtax.com/)
  * [Brandsight Business](http://brandisght.com/)
  * [Builder IO](http://builder.io/)
  * [Bullhorn Staffing](http://mychg.okta.com/)
  * [Chilipiper](http://chilipiper.com/)
  * [Combtas](http://app.combtas.com/)
  * [Crunchbase](http://crunchbase.com/)
  * [Cursive](http://cursive-ide.com/)
  * [Docker](https://www.docker.com/)
  * [Drata](http://drata.com/)
  * [Dun & Bradstreet Business](http://dnb.com/)
  * [eGoldFax](http://my.egoldfax.com/)
  * [FirefliesAI](http://app.fireflies.ai/)
  * [Genially](http://app.genially.com/)
  * [Cabal Business](http://getcabal.com/)
  * [GrowthSpace](http://app.growthspace.com/)
  * [Hoppscotch](http://placeholder.com/)
  * [IBISWorld](http://ibisworld.com/)
  * [Impact](http://impact.com/)
  * [LoopsAI](http://app.getloops.ai/)
  * [Mailmodo](http://mailmodo.com/)
  * [Mailosaur](http://mailosaur.com/)
  * [Mesh Payments](https://app.meshpayments.com/)
  * [Meta Business Manager](https://business.facebook.com/)
  * [Miro](http://miro.com/)
  * [Muck Rack](http://muckrack.com/)
  * [Pageflows](http://pageflows.com/)
  * [PagerDuty](http://pagerduty.com/)
  * [Pickcel](http://pickcel.com/)
  * [PolyLens Business](http://lens.poly.com/)
  * [Posthog](http://posthog.com/)
  * [Quantum](http://quantum.com/)
  * [Reco](http://reco.ai/)
  * [Saas Grid](http://app.saasgrid.com/login)
  * [Sentry Business](https://sentry.io/)
  * [Spectral Ops](http://app.spectralops.io/)
  * [Splunk Cloud](http://splunkcloud.com/)
  * [Success Coaching Business](http://learn.successcoaching.co/)
  * [Superwise App](http://app.superwise.ai/)
  * [Talenox](http://talenox.com/)
  * [Tesorio](http://dashboard.tesorio.com/login)
  * [The Muse Employers](http://employers.themuse.com/)
  * [Thought Industries](http://thoughtindustries.com/)
  * [Trendemon](http://trendemon.com/)
  * [TrustRadius](https://www.trustradius.com/vendoradmin)
  * [Unit](http://app.unit.co/)
  * [Wiz](https://www.wiz.io/)
