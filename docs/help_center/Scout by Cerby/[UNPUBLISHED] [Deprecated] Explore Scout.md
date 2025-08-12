# [UNPUBLISHED] [Deprecated] Explore Scout

**Description:** This article describes the benefits of Scout for workflow scouting and accelerating the workflow-building process.

With Cerby, you can be part of the engine that shapes the automated tasks you
use to manage and protect your accounts and seat-based and paid social apps.

Scout is a browser extension that accelerates and improves the building
process of automated workflows by capturing web interactions. The information
Scout captures can lead to better-designed features, smoother workflows, and
more user-friendly interfaces, directly benefiting you by making the
applications you use more intuitive and efficient.

**Figure 1** shows how the Scout browser extension looks.

![ Screenshot of Scout ](gitbook/imagesAD_4nXdzxvgu-EyfuxDs7oNhK-
VodfaXzRy4aBG8sjaeKgJWY4mFD0FFwzbKZfiLMN79PtAwzM28lx7FnOzWhsvCfRSyuH0mAA6-YHwo-8WuWswglhMbSTzD86DJfXiXRyyToAMlmPeZn9SR3taCoEiO2iikeHUt)

**Figure 1.** Scout browser extension popup on top of a web browser

To start using Scout, you must request it from a Cerby workspace **Admin or
Super Admin** , who must provide you with an API key. Once authorized, you
just need to activate Scout for a specific webpage and complete any of the
following tasks:

  * **Log in:** Navigate to your app’s login page and authenticate.

  * **Invite a user:** Add a new user to an app.

  * **Remove a user:** Remove the access of an existing user from an app (usually performed by an app admin).

  * **Update user roles:** Modify the role of a user or group (usually performed by an app admin).

  * **Manage two-factor authentication (2FA):** Navigate to your account security settings page and enable 2FA using Cerby.

  * **Update your account's password:** Access the account settings page and change your password.

{% hint style="danger" %} **IMPORTANT:** Scout doesn’t capture or store any
input values entered on any field. Only workspace **Admins** can use Scout
after their organization has requested access to this extension to Cerby. For
more information, refer to the How Scout protects your privacy section. {%
endhint %}

* * *

# How Scout works

Scout captures all your user interface (UI) interactions on a web browser,
such as clicks, scrolls, and overall navigation. This information is saved in
a scouting report that you send to Cerby team so the Development team can
build the automated task.

To get started, you must authenticate by providing an API key that you
generate in the Cerby web app with the following scopes:

  * **Read automated jobs:** Enables reading automated job data.

  * **Write automated jobs:** Enables writing automated job data.

After authentication, you can start scouting your workflows in the current
browser tab. All your interactions are captured as they occur, and you can
stop the recording when you are done.

Before sending the scouting report, you can preview it using the following
playback controls:

  * Play and pause

  * Progress bar

  * Full-screen mode

  * Speed selector

* * *

# How Scout protects your privacy

When using Scout to capture your UI interactions, Cerby prioritizes the
protection of your sensitive information at all times. This section explains
how Scout ensures the safety of your data and the details of what we capture
and what not.

## **What information Scout captures**

To provide valuable insights while maintaining your privacy, Scout captures
user interactions on a webpage considering the following:

  * **On-demand and tab-specific capture:** Scout captures user interactions only from the browser tab the user specifies and operates strictly on demand. If a user does not actively start Scout it does not send any data to Cerby's servers.

  * **Interaction paths:** Scout captures user interactions from the browser tab, focusing on elements -such as input fields and buttons where users click. These data points are used to automatically create your app integration workflows.

  * **Playback of web content:** Cerby uses the Scout data to replay the web views and user interactions. Scout _never_ records an actual video of the screen or browser tab.

  * **Masked input data:** Scout masks all input fields –such as usernames, email addresses, and other sensitive information– ensuring that your private data is _not_ captured or made visible to Cerby.

Scout’s approach protects your privacy and security by sharing only what is
necessary to build and maintain the business workflows.

## **What information Scout does _not_ capture**

Cerby understands the critical importance of privacy and security for your
company; protecting your secrets is what we do best! We designed Scout to
gather the only data we require while omitting unnecessary or sensitive
fields.

  * **Application credentials:** Scout does _not_ capture passwords or other credentials. Masked fields are automatically excluded from capture.

  * **User data entry:** Scout does _not_ capture any browser input fields. 

  * **Headers and cookies** : Scout does _not_ capture raw POST data, headers, or cookies.

We recognize that business application administrators have demanding
workloads; therefore, our objective is to alleviate that burden. Scout works
asynchronously with your teams on their schedule, not ours. We believe in
effective collaboration without asking for direct access to your applications
or scheduling support sessions.

* * *

# Best scouting practices and tips

The following are best scouting practices and tips for scouting your
workflows:

  * Think through all of the steps necessary to perform the task so you don’t miss anything.

  * Make sure you have a stable internet connection.

  * Record one task per scouting report, and try to perform only the relevant steps to complete that task. 

  * Avoid scouting reports that are shorter than 15 seconds.

  * Review the scouting report for any mistakes or errors before sending it to Cerby.

  * Select an appropriate task type and enter the name of your application before sending the scouting to the Cerby Integrations team.

* * *

# Related articles

The following articles contain more information about Scout:

  * [Install the Scout browser extension](https://help.cerby.com/en/articles/10046805-install-scout)

  * [Log in to Scout](https://help.cerby.com/en/articles/10046820-log-in-to-scout)

  * [Scout a workflow](https://help.cerby.com/en/articles/10046916-scout-a-workflow)

  * [Log out from Scout](https://help.cerby.com/en/articles/10046948-log-out-from-scout)

