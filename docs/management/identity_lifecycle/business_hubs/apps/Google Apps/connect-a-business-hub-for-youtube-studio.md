---
description: This article describes how to add your business hub for YouTube Studio to centrally manage access to it and its assets from Cerby.
---

# Connect a business hub for YouTube Studio

Cerby leverages the power of automation to connect your Cerby business hub to YouTube Studio. With this connection, you can import your user data, such as roles, permissions, and members, to centrally and securely manage the access from Cerby.

YouTube Studio manages members’ roles and permissions for YouTube channels. Within YouTube Studio, the channel **Owner** and **Managers** can control access to the channel by adding or removing members and assigning different roles with varying levels of permissions. After importing your YouTube Studio members, you gain visibility on who accesses your YouTube Studio, including the members’ role levels. Users with a Cerby account are automatically matched to their corresponding identity in your corporate directory, which may be managed by an identity provider (IdP), such as Okta or Entra ID (formerly Azure AD).

Matched users are prompted in the Cerby dashboard to connect their IdP and YouTube Studio profiles to Cerby. After connecting them, you can manage and secure their access to your YouTube Studio and its assets and update their role, all from one single interface. External collaborators without a Cerby account are displayed as unmatched users. For these users, you can perform the following actions:

  * Match and invite users to join your channel through YouTube Studio through Cerby
  * Remove unmatched users
  * Exempt unmatched users to keep their user account active in YouTube Studio; however, you cannot manage them through Cerby

This article describes how to add a YouTube Studio integration and import its users to Cerby.

* * *

# Requirements

The following are the requirements to add your YouTube Studio integration to Cerby:

  * A Cerby workspace
  * A Cerby account
  * A collaboration space in your YouTube Studio

**IMPORTANT:** If you have a Brand account, you must migrate to YouTube Studio. Read the instructions in the Migrate members’ permissions to YouTube Studio section to learn how to perform the migration

  * A service account with the following characteristics:
    * It must belong to your IdP, such as Okta, Entra ID, or JumpCloud
    * It must use single sign-on (SSO) to log in to the Google Workspace account
    * It must have the Google Suite apps assigned; thus, having access to the Gmail Inbox
    * It must be associated with an active account in YouTube Studio
    * It must have the **Owner** or **Manager** role in YouTube Studio
    * It must have the multi-factor authentication (MFA) method enabled, thus accepting authenticator apps, such as Google Authenticator or Phone MFA. Then, it must be configured to use Cerby as the authentication app by following the instructions in the [[Video] How to turn on MFA manually for your accounts](https://help.cerby.com/en/articles/6393776-video-how-to-turn-on-2fa-manually-for-your-accounts) article
    * It must be an account dedicated to connecting the integration, not associated with a specific user
  * The [Channel ID](https://www.youtube.com/account_advanced) of your YouTube channel
* * *

# Migrate members’ permissions to YouTube Studio

**IMPORTANT:** Complete the steps in this section only if you have a YouTube Brand account. For instructions on verifying your account type, read the official documentation [Check if you have a Brand Account](https://support.google.com/youtube/answer/7286468?hl=en&ref_topic=9267586&sjid=9713402243757791435-NC). If you already use YouTube Studio's permission system, continue to the Connect a business hub for YouTube Studio section.
---

As a **Primary Owner** of a YouTube Brand account, you must migrate the members’ permissions to YouTube Studio. By performing the migration, you’ll get more control over the members through specific roles and permissions. Refer to the [YouTube documentation](https://support.google.com/youtube/answer/9367690?hl=en) to learn more about YouTube Brand account migration to YouTube Studio.

To migrate the members’ permissions to YouTube Studio, you must follow the next main steps:

  1. Prepare for the member migration to YouTube Studio
  2. Migrate from YouTube Brand account to YouTube Studio

The following sections describe each main step.

## 1\. Prepare for the member migration to YouTube Studio

To prepare for the member migration from YouTube Brand account to YouTube Studio, Cerby recommends you review the following considerations:

  * Members must create a YouTube personal channel
  * Each channel must have a permanent owner
  * Your content might be temporarily unavailable

The following sections describe each consideration.

### Members must create a YouTube personal channel

When you manage a Brand account, members access it by logging in with their personal YouTube account. However, to access YouTube Studio, each member must have a **personal channel** linked to their account. This consideration is important because channel permissions are managed exclusively through YouTube Studio. For more information and instructions, read the official documentation [Add or remove access to your YouTube channel with channel permissions](https://support.google.com/youtube/answer/9481328?sjid=16518201040371443454-NC).

During the migration, each member and channel associated with your Brand account must accept an invitation to join YouTube Studio and confirm their assigned role. As part of this process, YouTube prompts members without personal channels to create one before they accept the invitation. To create a new YouTube channel, read the official documentation [Create a YouTube channel](https://support.google.com/youtube/answer/1646861?hl=en&sjid=16518201040371443454-NC).

### Each channel must have a permanent owner

Unlike Brand accounts, YouTube Studio only permits **one permanent Owner per channel**. When designated, this **Owner** cannot be changed or removed. Ensure that the member completing the onboarding process for YouTube Studio is the individual who will remain the permanent **Owner**. For more information, read the official documentation [Change channel owners & managers with a Brand Account](https://support.google.com/youtube/answer/4628007?hl=en&co=GENIE.Platform%3DAndroid).

### Your content might be temporarily unavailable

The content in your channels might be temporarily disconnected during the migration. Schedule**** a time with minimal account activity to complete the transition because all members and channels must reauthorize their access.

## 2\. Migrate from YouTube Brand account to YouTube Studio

To migrate from YouTube Brand account to YouTube Studio, you must complete the following steps:

  1. Open [YouTube Studio](https://studio.youtube.com/).
​**IMPORTANT:** You must sign in as the **Primary Owner** of the Brand account to have the option to opt into permissions.

  2. Click the **Settings** option on the left drawer.
  3. Click the **Permissions** options. A dialog box is displayed.
  4. Click the **MOVE PERMISSIONS** options. A window appears with the list of members and permissions in your channel through YouTube Studio.
  5. Choose a role for each existing user associated with your Brand Account.
  6. Click the **Invite** button. The following occurs:

     * Each invited user receives an email to accept the invite.
     * Each new user is shown in the **Studio Permissions** dialog box.

**IMPORTANT:** If you have already added the service account you are using for the Cerby integration to the brand account, you must accept the invite to YouTube Studio again because all invitations are renewed.
---

* * *

# Connect a business hub for YouTube Studio

To connect a business hub for YouTube Studio and import your members to Cerby, you must complete the following main steps:

  1. Add a business hub and connect it to your YouTube Studio
  2. Check for updates and import users and roles to Cerby
  3. Manage unmatched users

The following sections describe each main step.

## 1\. Add a business hub and connect it to your YouTube Studio

To add a business hub in Cerby and connect it to your YouTube Studio, you must complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
  3. Click the **Connect Business Hub** button located at the top-right corner of the page. The **Connect your Business Hubs to Cerby** dialog box is displayed.
​**TIP:** You can select the **Don’t show this again** option to skip this step the next time you connect a new business hub.

  4. Click the **Get started** button. A wizard is displayed on the **Select app** page.
  5. Select the **Youtube tenant** option from the app catalog. The **Enter app** details page is displayed on the wizard.
  6. Enter and select your app information in the corresponding fields:

     * **Label in Cerby:** It is the name to assign to your business hub in Cerby and will be displayed on the business hub card.
     * **Channel name:** It is the YouTube channel, which you are adding the business hub in Cerby.
​**IMPORTANT:** This field is case sensitive, which means that you must provide the name of the YouTube channel exactly as it is, including any uppercase and lowercase letters. For example, if the channel name is "TechTutorials," it must be entered as "TechTutorials," not "techtutorials" or "TECHTUTORIALS".

     * **Business ID:** It is your YouTube Channel ID. To find it, access your [YouTube Studio advanced settings](https://www.youtube.com/account_advanced) page.
     * **User management and login method:** It is how your users log in to YouTube Studio and determine if they must save their credentials in Cerby. You must select the **Single sign-on (SSO)** method for the Cerby integration with YouTube. With the **Single sign-on (SSO)** method, access is managed via your identity provider (IdP), and users log in via SSO authentication. They are not asked to save their credentials in Cerby.

  7. Click the **Next** button. The **Select automation account** page is displayed. One of the following scenarios occurs:

     * If you already have an automation account for the business hub to your IdP, a list of accounts is displayed, as shown in the example of **Figure 1** for Okta.

<figure><img src="../.gitbook/assets/qudaeJJ6hCet5Du5--f-jqbvvLWNzNhizAvulKePYKKgNBW75acgeWGV7L5QdqzmsItU-hp3M0Id7cWgmAwZIEJB3sDLMPpsV8IUxo6yiCUzs7MIRyv1TqogPV7CiBAAvYB8GU0DVpjLfDumSmErj7E.png" alt=""><figcaption></figcaption></figure>

**Figure 1.** IdP automation account

       1. Select the corresponding automation account to your IdP provider.
       2. Click the **Connect app** button.

     * If you don’t have an automation account, you are prompted to add it, as shown in **Figure 2** :

<figure><img src="../.gitbook/assets/lj5D8SIIGSh28fk1SUMlGeEtsb9eFAdHXld1RSSQb1DkbGIRdUSqJbA8ePi33lFcfkdrZPQyIl-7U29IBZV6roFX6zBmoOZ7At7_j5JxHmCUNdQMMO3O5EvYyw5ftvQ9AoWqOpq222s6Kej5iTjTVmg.png" alt=""><figcaption></figcaption></figure>

**Figure 2.** Add an automation account for YouTube

       1. Enter your account information in the corresponding fields:

          * **Account label in Cerby:** It is the name to assign to your account in Cerby and will be displayed on the account card.
          * **App:** It is the name of the app or service provider to which the account belongs or the login URL.
            * **Okta**
              * **Username:** It is the username to log in to the Okta account. Sometimes, the username is an email address
              * **Current password:** It is the password to log in to the Okta account
              * **Phone Number Linked to Account:** It is the phone number associated with the Okta account
              * **Workspace URL:** It is the Okta workspace URL corresponding to your company
            * **Entra**
              * **Username:** It is the username to log in to the Entra account. Sometimes, the username is an email address
              * **Password:** It is the password to log in to the Entra account

       2. Click the **Add account** button. The wizard closes, and a success message box is displayed. The corresponding YouTube Studio App integration is also displayed on the **Business Hubs** view.

{% hint style="danger" %}


**IMPORTANT:** If your IdP requires the two-factor authentication method enabled, you must use Cerby as your authentication app. Follow the instructions in the [How to turn on MFA managed by Cerby](https://help.cerby.com/en/articles/8429534-how-to-turn-on-2fa-managed-by-cerby) article to learn how to use Cerby as your authenticator app.


{% endhint %}

The next step is 2\. Check for updates and import users and roles to Cerby.

## 2\. Check for updates and import users and roles to Cerby

To check for updates in YouTube Studio to identify and import users and roles to Cerby, you must complete the following steps:

  1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
  2. Click the YouTube app card. The business hub details page is displayed with the **Settings** tab activated.
  3. Click the **Check for updates** button located at the top-right section of the page. A message box is displayed with information about the process.
​**NOTE** : The check and import process may take a few minutes depending on the number of users and because Cerby automatically matches users to their corresponding Cerby accounts. When the process is complete, a success message box is displayed.

  4. Activate the **Members** tab to review the list of imported users in the following two tabs of the **User Overview** section:

     * The **Onboarded users** tab displays the users matched to their Cerby account. Cerby automatically sends them an invite to join the app.
     * The **Unmatched users** tab displays the users who were not automatically matched because they use an email address that couldn’t be identified or is not in the corporate directory.

{% hint style="info" %}


**NOTE:** After adding the YouTube Studio integration, Cerby automatically performs daily checks for updates, but you can do it manually. When a user is deprovisioned from the IdP, and a check for updates is performed, Cerby generates a report and sends you an email to confirm their removal from Cerby. Follow the instructions in the article[ Check for updates in your app and apply report](https://help.cerby.com/en/articles/9046205-check-for-updates-in-your-app-and-apply-report) to apply the report, and remove deprovisioned users.


{% endhint %}

The next step is 3\. Manage unmatched users, which you must complete from the Cerby dashboard.

## 3\. Manage unmatched users

After a check for updates, Cerby automatically matches users to their corresponding Cerby accounts. Users who couldn’t be identified during the check or who are not in the corporate directory are categorized as unmatched. For these users, you can perform one of the following three actions:

  * Match and invite users
  * Remove unmatched users
  * Exempt unmatched users

These actions are performed from the **Unmatched Users** tab of the **User Overview** section inside the app details page.

**IMPORTANT:** The actions you perform for unmatched users propagate to the corresponding roles and permissions on assets.
---

## Match and invite users

To match and invite users to join your YouTube Studio through Cerby, you must perform the following steps:

  1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
  2. Click the **More options** (...) icon of the YouTube card. A drop-down list is displayed.
  3. Select the **View Members** option from the list. The business hub details page is displayed with the **Members** tab activated and a table of users in the **User Overview** section.
  4. Activate the **Unmatched users** tab from the **User Overview** section.
  5. Click the **Match user** button of the corresponding user. The **Match user** dialog box is displayed.
  6. Enter the username or email address of the user in the **Match with** search bar. A list of users that match your search is displayed.
  7. Select the corresponding option from the list.
  8. Click the **Next** button. The **Select Cerby role** dialog box is displayed.
  9. Select the corresponding role of the user from the **Role** drop-down list:

     * **Owner:** This role enables sharing access and managing the tenant configuration.
     * **Collaborator:** This role enables only logging in to YouTube Studio.

  10. Click the **Match user** button. The dialog box closes, a success message box is displayed, and the user is moved to the **Onboarded users** tab.
The YouTube account and app cards are displayed in the **All accounts** and **Apps** views, respectively, of each matched user.

{% hint style="danger" %}


**IMPORTANT:** If you want to manually add guest users or other Cerby members, you must ensure their emails belong to a Google Suite; otherwise, Cerby shows an error to provide access. A Google account is necessary for accessing YouTube's features, such as uploading videos, subscribing to channels, leaving comments, and creating playlists.


{% endhint %}

## Remove unmatched users

To remove unmatched users, you must perform the following steps:

  1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
  2. Click the **More options** icon of the YouTube card. A drop-down list is displayed.
  3. Select the **View Members** option from the list. The business hub details page is displayed with the **Members** tab activated and a table of users in the **User Overview** section.
  4. Activate the **Unmatched users** tab from the **User Overview** section.
  5. Click the **More options** icon of the corresponding user. A drop-down list is displayed.
  6. Select the **Remove user** option from the list. The **Remove user?** dialog box is displayed.
  7. Click the **Remove user** button. The dialog box closes, and a success message box is displayed. The user is removed from YouTube Studio.

## Exempt unmatched users

Exempted users keep their user accounts active for your YouTube Studio, but you cannot manage them through Cerby. To exempt unmatched users, you must perform the following steps:

  1. Select the **Business Hubs** option from the left navigation drawer. The **Business Hubs** view is displayed.
  2. Click the **More options** icon on the YouTube card. A drop-down list is displayed.
  3. Select the **View Members** option from the list. The app details page is displayed with the **Members** tab activated and a table of users in the **User Overview** section.
  4. Activate the **Unmatched users** tab from the **User Overview** section.
  5. Click the **More options** icon of the corresponding user. A drop-down list is displayed.
  6. Select the **Exempt user** option from the list. The **exempt user** dialog box is displayed.
  7. Enter a reason for exempting the user in the **Provide a reason** field.
  8. Click the **Exempt member** button. The dialog box closes, and a success message box is displayed. The user is moved to the **Exempted users** tab.

Now you are done. You can start managing and securing access to your YouTube Studio from Cerby.

* * *

# Troubleshooting the YouTube Studio integration

This section contains some of the common errors you might encounter while integrating YouTube Studio with Cerby.

## “Oops, you don't have permission to view this page” error

If you encounter the "Oops, you don't have permission to view this page" error message, as shown in **Figure 3**.

<figure><img src="../.gitbook/assets/AD_4nXcv5yMMc2iZThDArIF3oJDogEtiPrAhQLdJW_WV-iwZIzU-3KqLDYZJRaUGsxow2uQMCw6kbnTaUYvbgXTkHpxWySA1ger-RfuHB2EeBkLzyzqMhDIyGLLvCHgoIQxbYgyzRLcj.png" alt=""><figcaption></figcaption></figure>

**Figure 3. “Oops, you don't have permission to view this page”** error message

The following are the possible causes and solutions:

  * Ensure the YouTube user permissions have been migrated from Brand account to YouTube Studio. For instructions, read the Migrate members’ permissions to YouTube Studio section.
  * Verify that the service account has been invited to the YouTube Studio account with a **Manager** role. This role is essential because it has permission to access the account. You must check the invitation status and ensure it has been accepted by the service account.
  * Confirm that the service account has accepted the invitation to join YouTube Studio with the **Manager** role. Without acceptance, access to YouTube Studio is restricted.
  * Confirm that the YouTube Studio Business ID is correct. Review the Requirements section to learn how to correctly find this ID.

## “Only Google accounts can be invited” error while adding a member to YouTube Studio

If you encounter the “Only email addresses with Google accounts can be invited” error message while adding members to the YouTube Studio account, it is because YouTube Studio only allows email addresses associated with Google accounts to be invited. Thus, you must ensure that users have a Google account to join YouTube Studio.

* * *

# Related articles

The following are the supported features of the YouTube Studio app integration you can use:

  * [Invite new app members](https://help.cerby.com/en/articles/9045790-invite-new-app-members)
  * [Remove app members](https://help.cerby.com/en/articles/9046186-remove-app-members)
  * [Manage app members from your IdP](https://help.cerby.com/en/articles/9046188-manage-app-members-from-your-idp)
  * [Update the app members’ roles](https://help.cerby.com/en/articles/9046201-update-the-app-members-roles)
  * [Check for updates in your app and apply report](https://help.cerby.com/en/articles/9046205-check-for-updates-in-your-app-and-apply-report)
  * [Re-assign the app members’ user accounts](https://help.cerby.com/en/articles/9046211-re-assign-the-app-members-user-accounts)
  * [Manage the security of app members’ user accounts](https://help.cerby.com/en/articles/9046212-manage-the-security-of-app-members-user-accounts)
  * [Log in to your app](https://help.cerby.com/en/articles/9046222-log-in-to-your-app)
  * [Track activity on app members’ user accounts](https://help.cerby.com/en/articles/9046226-track-activity-on-app-members-user-accounts)
  * [Remove an App](https://help.cerby.com/en/articles/9046230-remove-an-app)
