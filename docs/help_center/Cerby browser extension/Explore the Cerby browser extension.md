# Explore the Cerby browser extension

**Description:** This article describes the key benefits of the Cerby browser extension to manage your items and log in to your accounts.

The Cerby browser extension is an add-on for your web browser designed to
provide you with the most optimal user experience. While the core
functionalities of the Cerby platform can be accessed via the web app, the
browser extension unlocks the full potential of Cerby, significantly
streamlining your daily activities.

The extension is strategic for performing automated logins to your accounts,
identifying and autosaving your accounts, and restricting changes to account
settings, among other features. Additionally, it enables you to seamlessly
manage your items: accounts, secrets, and collections.

The following are the four underlying services of the Cerby browser extension:

  * **Autofill:** It consists of the services responsible for interacting with the web page’s content based on the background context. With these services, the extension enables auto and manual injection of login credentials (autofill). 

  * **Popup:** It consists of the main user interface (UI) service of the extension displayed when users click the Cerby icon in the web browser’s toolbar or add-ons section. Users interact with the popup to access and perform actions on their items, such as viewing the details of accounts, secrets, and collections.

  * **Inline menu:** It consists of a complementary UI service of the extension displayed in input fields. Users interact with the inline menu to perform actions specific to the context of the input field, such as autofilling login credentials.

  * **App settings restrictions:** It consists of the service responsible for blocking sections of a page in the web browser to prevent users from changing user and password settings.

  * **Login credential capture:** It consists of the service responsible for identifying login and signup attempts and capturing the login credentials for autosaving accounts, either through a prompted or enforced flow.

* * *

# **Supported browsers**

The Cerby browser extension is supported by the following web browsers:

  * [Firefox](https://addons.mozilla.org/en-US/firefox/addon/cerby-s-browser-extension/)

  * [Google Chrome](https://chrome.google.com/webstore/detail/cerbys-browser-extension/clccplmaaeihbagbefjinmclielobnkb)

  * [Microsoft Edge](https://microsoftedge.microsoft.com/addons/detail/cerbys-browser-extension/bbaiiaogfdgpbapebajffliefkfipoif)

  * [Safari](https://apps.apple.com/mx/app/cerby-web-extension/id1581820030?l=en&mt=12)

{% hint style="danger" %} **IMPORTANT:** While you can install the Cerby
browser extension in Opera, being a Chromium-based web browser, you may
experience issues with field detection. We’ll support Opera in the future. {%
endhint %}

It’s worth mentioning that Cerby provides the flexibility for organizations to
decide whether to make the browser extension installation optional or to
deploy it centrally via a Mobile Device Management (MDM) solution. For more
information, read the article [Install the Cerby browser extension via an MDM
service and a configuration
file](https://help.cerby.com/en/articles/8265232-install-the-cerby-browser-
extension-via-an-mdm-service-and-a-configuration-file).

* * *

# **Key benefits**

The following are the key benefits of the Cerby browser extension:

  * **Real-time sync:** Changes made on the Cerby web app, such as adding accounts, updating passwords, or organizing collections, are instantly reflected in the browser extension, ensuring your information is always up-to-date.

  * **Streamlined login:** Experience automated access to your accounts, eliminating the need to manually enter usernames, passwords, and multi-factor authentication (MFA) codes.

  * **Account onboarding:** Identify and autosave new accounts in Cerby as you log in or sign up for services, maintaining a complete record of your digital footprint.

  * **In-app access management:** For specific domains, the Cerby browser extension can enforce access rules, ensuring users only interact with allowed sections of the app settings.

  * **Enterprise-first:** Leverage your MDM service to install the Cerby browser extension across all the endpoints in your organization. You can pre-seed your workspace in the extension for user convenience.

* * *

# **Key operations**

The following are the key operations of the Cerby browser extension:

  * **Logging in to your accounts:** Leverage automated login by having the Cerby browser extension autofill your login credentials, or perform assisted manual logins.

  * **Autosaving your accounts:** Let Cerby identify login and signup attempts so that these accounts are autosaved in your workspace.

  * **Restricting app settings:** Encourage users to use Cerby rather than the app’s interface to manage users and update passwords in your apps.

  * **Generating passwords:** Use our password strength selectors to generate strong passwords that comply with your app requirements.

  * **Receiving in-context alerts:** Let Cerby display important notifications in your web browser as the Cerby browser extension performs automated logins for you.

  * **Suggesting accounts:** Let the inline menu display existing accounts based on the web page you're visiting.

  * **Accessing your items:** Use the Cerby browser extension popup to view your accounts, secrets, and collections.

  * **Auto signing in to the extension:** Leverage the active session of your identity provider to automatically sign in to the Cerby browser extension. Currently, this feature is available for Okta-based workspaces.

* * *

# **Extension permissions and data access**

The Cerby browser extension adheres to the principle of least privilege
access, as recommended by the [National Institute of Standards and Technology
(NIST)](https://csrc.nist.gov/glossary/term/least_privilege), to conduct the
[key
operations](https://docs.google.com/document/d/1ufc0a7s3FJlorZAGdu0qWKh0QSzTm5ReliNytNWR9AY/edit?tab=t.0#heading=h.sydl068g0qtr)
previously referenced.

The following are the specific permissions and data access guidelines required
by the Cerby browser extension:

  * **`contextMenus`:** It enables the extension to be activated from the context menu after right-clicking in login input fields, particularly for fields that are not auto detected.

  * **`cookies`:** It detects existing valid sessions for accounts, enabling a more streamlined login experience by bypassing login forms when session cookies are present.

  * **`https://*/` (all hosts): **It validates that login credential injection only occurs on domains designated as allowed by users within the Cerby web app, preventing unintended autofills.

  * **`scripting`:** It enables displaying buttons and in-context alerts in web pages.

  * **`storage`:** It stores user and workspace preferences.

  * **`tabs`** : It enables opening new browser tabs for executing automated logins.

  * **`unlimitedStorage`:** It ensures the extension can securely store essential configurations and cache data without being restricted by standard browser storage limits.

  * **`webNavigation`:** It detects whether login attempts were successful or failed, enabling the extension to provide real-time feedback.

* * *

# **Related articles**

The following articles contain more information about the Cerby browser
extension:

  * [Install the Cerby browser extension](https://help.cerby.com/en/articles/10755388-install-the-cerby-browser-extension)

  * [Log in to the Cerby browser extension](https://help.cerby.com/en/articles/10755356-log-in-to-the-cerby-browser-extension)

  * [Generate secure passwords using the Cerby browser extension](https://help.cerby.com/en/articles/8377075-how-to-generate-secure-passwords-using-the-cerby-browser-extension)

  * [Explore Account Autosave](https://help.cerby.com/en/articles/9500455-explore-account-autosave)

  * [Explore App settings restrictions](https://help.cerby.com/en/articles/10276184-explore-app-settings-restrictions)

