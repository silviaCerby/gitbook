---
description: This article describes the latest enhancements and bug fixes to improve your experience using Cerby.
intercom_id: 12455154
---

# Release Notes - September 29, 2025

## New features

The following are the new features and improvements we released across the Cerby platform:

### Cerby web app

Check out what’s new in our Cerby web app:

* We now support sending invite links when executing automation jobs for adding users to an external app. This feature is helpful for apps like JetBrains, where invite URL links are generated in the user interface and must be manually shared, instead of the app sending an email. Role updates in JetBrains go through the same flow of generating the invite URL and having to send the invite manually.
* You can now search for failed automation jobs by app name in the **Automation Log** page. We identify when an automation job requires attention or when Cerby is working to solve the issue.
* We’ve implemented a sorting rule when you view the details of all nested automation jobs in the **Automation Log** page. Now, when you click **View all jobs** for an automation job with the “Not completed” status and a new browser tab is displayed, we now show first the nested jobs with the “Not completed” status so you can take action.

### Cerby browser extension

Explore the latest features in our Cerby browser extension:

* We now detect DevTools and show a message to let our users know that, while DevTools are open, automations through the extension are stopped; additionally, the autofill feature is restricted both from the browser extension popup and the inline menu.
Users with enough context on how to use DevTools could potentially leverage them to access login credentials.

* We’ve improved our detection capabilities of Okta authentication to leverage user sessions for our auto sign-in feature. Some of the login timeout errors that users encountered actually occurred because they needed to re-authenticate or provide additional authentication information to Okta.

### Cerby mobile app

Dive into the newest additions to our Cerby mobile app:

* We’ve released a feature that improves the autofill experience using the Cerby mobile app for iOS v1.0.260 (it was previously released for Android). Now, when logging in to an account using autofill, we display a section with suggested self-managed accounts based on the app domain.
* We've optimized some of our background processes to significantly speed up how the app handles network calls. This means a smoother and faster experience for you using the Cerby mobile app on Android v1.0.215 onwards.
* We’ve enabled basic full-screen support for the Cerby mobile app on iPads and Android tablets. This feature was released in versions v1.0.261 for iOS and v1.0.216 for Android.

### CLI

The Cerby CLI has the following updates:

* We’ve enabled the `cerby-source` header in all CLI requests to prevent you from being blocked by our web application firewall (WAF) rules. The goal is to ensure a smoother and more reliable connection when you use the [CLI](https://cerby-test.gitbook.io/cerby-test/extending-cerby/cerby-cli/explore-the-cerby-cli).
* * *

## Fixes

Take note of the issues addressed and resolved by the Development team behind the Cerby platform:

### Cerby web app

* The issue with being unable to remove some **Login-Only** users from a workspace was fixed. The error occurred after triggering a Cerby Universal Logout for the users.
* The issues with some daily syncs not completing for business hubs connected to Meta Business Manager and Discord were fixed.
* The issue with not detecting Instagram as a managed app when importing items using a CSV file was fixed.
* The issue with business hub **Owners** not receiving email notifications after failed automation jobs was fixed. The error occurred when users were granted shared access to the business hub through a team.

### Cerby mobile app

* The issue with Android autofill when logging in with a Google account on a web browser was fixed in v1.0.213.
* The issue with workspace **Owners** not being successfully identified was fixed for Android v1.0.214.
* The issue with the Cerby mobile app for Android crashing when fetching user permissions was fixed in v1.0.215.
* * *

## New supported managed apps

The following are the latest additions to the list of managed apps with supported automated tasks:

* [Airwallex](http://airwallex.com/)
* [Alabama - AL - Department of Labor](http://alabama.gov/)
* [Alabama - AL - Department of Revenue](http://alabama.gov/)
* [Arizona AZ PIT](http://efile.aztaxes.gov/)
* [Arizona AZ Unemployment Insurance](http://ftp.azdes.gov/)
* [Arkansas - AR - Division Of Workforce Services](http://arkansas.gov/)
* [Beyond Trust Remote Support](http://support.com/)
* [California - CA - E-Services For Business](http://ca.gov/)
* [Connecticut - CT - ST Web Client PMFL](http://ct.gov/)
* [DataGroomr](http://datagroomr.com/)
* [District of Columbia DC Department of Employment Services](http://essp.does.dc.gov/)
* [DV360 Advertisers Hub](http://displayvideo.google.com/)
* [Florida FL BSWA](http://secure.bswa.net/)
* [Georgia GA Tax Site](http://gtc.dor.ga.gov/)
* [Google Business Profile](http://google.com/)
* [Hallo015](http://015pbx.net/)
* [Hawaii HI Department of Taxation](http://hitax.hawaii.gov/)
* [Hawaii - HI - Unemployment Insurance](http://huiclaims3.hawaii.gov/)
* [Hunter.io](http://hunter.io/)
* [Idaho ID Unemployment Insurance](http://govconnect.iowa.gov/)
* [Idaho ID Tax Payer Access Point TAP](http://dahotap.gentax.com/)
* [Illinois IL My Tax Portal](http://mytax.illinois.gov/)
* [Intermedia](http://cp.intermedia.net/)
* [Kansas KS Labor Portal](http://kansaslabor.gov/)
* [Kansas - KS - Dept of Revenue](http://kdor.ks.gov/)
* [Louisiana LA SUI](http://esweb.revenue.louisiana.gov/)
* [Maine ME Department of Labor](http://pfml.maine.gov/)
* [Maine ME Paid Family Medical Leave PFML](http://pfml.maine.gov/)
* [Maine ME ReEmployME](http://assist.reemployme.maine.gov/)
* [Maine ME Revenue Services](http://revenue.maine.gov/)
* [Minnesota - MN - Department of Labor](http://mndor.state.mn.us/)
* [Minnesota MN Department of Revenue](http://mndor.state.mn.us/)
* [Minnesota MN Unemployment Insurance](http://www1.uimn.org/)
* [Mississippi MS Department of Employment Security](http://accessmstax.mdes.ms.gov/)
* [Mississippi MS Dept of Revenue](http://tap.dor.ms.gov/)
* [Monday Academy](http://monday.com/)
* [Montana MT Withholding](http://tap.dor.mt.gov/)
* [Alaska AK Unemployment Insurance](http://my.alaska.gov/)
* [District of Columbia DC My Tax DC](http://mytax.dc.gov/)
* [N. Dakota ND Tax Payer Access Point TPA](http://apps.nd.gov/)
* [N. Dakota ND Withholding](http://apps.nd.gov/)
* [Nebraska NE Nebfile](http://ndr-efs.ne.gov/)
* [New Mexico NM Unemployment](http://ui.dws.state.nm.us/)
* [New Mexico NM Withholding](http://tap.state.nm.us/)
* [Nebraska NE NEWorks Portal](http://neworks.nebraska.gov/)
* [Oklahoma OK Employment Security Commision](http://ok.gov/)
* [Oklahoma OK Tax Payer Access Point TAP](http://oktap.tax.ok.gov/)
* [Ordway](http://app.ordwaylabs.com/)
* [Otter.ai](http://otter.ai/)
* [Relevance](http://relevanceai.com/)
* [Rhode Island RI Dept of Labor & Training](http://taxportal.ri.gov/)
* [Salto](http://app.salto.io/)
* [Saola](http://saola.com/)
* [SC Unemployment and Tax Portal](http://uitax.dew.sc.gov/)
* [SD Labor and Regulations](http://apps.sd.gov/)
* [signNow](http://signnow.com/)
* [South Carolina - SC - Department of Revenue](http://mydorway.dor.sc.gov/)
* [Puerto Rico PR Dept of Revenue](http://suri.hacienda.pr.gov/)
* [Tennessee - TN - Department Of Labor And Workforce Development](http://jobs4tnui.tn.gov/)
* [Texas - TX - Texas Unemployment Tax Services](http://apps.twc.texas.gov/)
* [Utah - UT - Taxpayer Access Point](http://utah.gov/)
* [Virginia - VA - Virginia Tax](http://virginia.gov/)
* [Wisconsin - WI - Department of Workforce Development Unemployment Insurance](http://wisconsin.gov/)
* [Wyoming - WY - Wyoming's Online Unemployment System](http://wyui.wyo.gov/)
* [XFunnel](http://dash.xfunnel.ai/)
* * *

## New supported business hubs

The following are the latest additions to the list of business hubs with supported user management automated tasks:

* [Bloomerang CRM Database](http://bloomerang.co/)
* [Comparably](http://comparably.com/)
* [DataGroomr](http://datagroomr.com/)
* [Facebook](https://business.facebook.com/)
* [Hallo015](http://015pbx.net/)
* [Highspot](http://app.highspot.com/)
* [Hunter.io](http://hunter.io/)
* [Intermedia](http://cp.intermedia.net/)
* [Luru Business](http://luru.com/)
* [Netlify](http://app.netlify.com/)
* [Nooks](http://app.nooks.in/)
* [Ordway](http://app.ordwaylabs.com/)
* [Otter.ai](http://otter.ai/)
* [Relevance](http://relevanceai.com/)
* [Salto Business](http://app.salto.io/)
* [Saola](http://app.saola.ai/)
* [SignNow Business](http://signnow.com/)
* [UserTesting](http://usertesting.com/)
* [Xappex](http://portal.xappex.com/)
* [XFunnel Business](http://dash.xfunnel.ai/)
