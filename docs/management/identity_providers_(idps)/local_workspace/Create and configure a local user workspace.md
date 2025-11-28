# Create and configure a local user workspace

**Description:** This article describes how to create and configure a local user workspace in which Cerby manages the identity and authentication of users.

With Cerby, you can configure a local user workspace when you need Cerby to
manage the identity and authentication of users instead of leveraging an
identity provider (IdP) such as Okta or Azure AD.

In local user workspaces, users are added via direct invites from Cerby to
their email addresses, and user management is performed through the **All
members** view. In regular workspaces, the IdP acts as the authoritative
source of user identity, and changes in user accounts, attributes, or
permissions are synchronized downstream to Cerby via the System for Cross-
Domain Identity Management (SCIM) specification.

Regarding authentication, users authenticate directly to Cerby with
credentials (username and password) managed by Cerby in local user workspaces.
In regular workspaces, users are redirected to their IdP's authentication page
to log in to Cerby.

The user who creates and configures a local user workspace becomes the
**Workspace Owner**. They can add users to the workspace and assign them the
**Workspace Admin** or **Workspace User** roles. For more information about
roles, read the article [How Cerby manages
roles](https://help.cerby.com/en/articles/8500649-how-cerby-manages-roles).

In addition to editing the workspace details, **Workspace Admins** can perform
the following user management tasks in local user workspaces:

  * Add new users to the workspace.

  * Remove users from the workspace.

  * Edit the workspace-level role of users.

  * Reset multi-factor authentication and password for users.

Local user workspaces can be used when businesses collaborate with external
parties who don’t belong to their business domain, such as contractors,
agencies, partners, vendors, and clients. With the Partners feature, a regular
workspace can securely share accounts, secrets, and collections with a local
user workspace. For more information about this feature, read the [How to use
Partners](https://help.cerby.com/en/articles/6634083-how-to-use-partners)
article.

This article describes how to configure a local user workspace.

* * *

# **Requirements**

The following are the requirements to create and configure a local user
workspace:

  * An email invite sent by the Cerby team to create a workspace

  * An authentication app installed on your mobile phone, such as Google Authenticator, Okta Verify, Microsoft Authenticator, Duo Mobile, or Authy

**NOTE:** Ask your IT or Security department for the authorized authentication
app.

* * *

# **Create and configure a local user workspace**

To create and configure a local user workspace, you must complete the
following main steps:

  1. Create your Cerby account and workspace

  2. Install the Cerby mobile app and browser extension

  3. Turn on MFA for your Cerby account

The following sections describe each main step.

## **1\. Create your Cerby account and workspace**

To create your Cerby account and the local user workspace, you must complete
the following steps:

  1. Click the **Create your Workspace** button from the invite that Cerby sent to your email address. The **Welcome to Cerby** page is displayed, as shown in **Figure 1**.

![Screenshot of the Welcome to Cerby page, where multiple buttons are
displayed with the different options to sign in to
Cerby.](images/omhnlZhbqMvnuxx_f-dvvdhsjlp1JMAcekC7irwlP173Hpfac-
Mu1hqqhLOFz_EpgazGd9MVNNPTpSgzHmuW4WFi2BaqeRPwx2Ett8WtbKMWnAA73nsc6ZEv2PBJrgclOta2BpwUFq-
VzCet9bdsKsI)

**Figure 1. Welcome to Cerby** page

  2. Click the **Sign in with Cerby** button. The **Let’s create your workspace** page is displayed.

  3. Enter the name of your workspace in the **Workspace name** field.

  4. Click the **Create Workspace** button. The **Create your account** page is displayed.

  5. Create your Cerby account by entering the following information in the corresponding fields:

     * **Name**

     * **Last name**

     * **Email**

     * **Confirm Email**

     * **Password**

     * **Confirm Password**

  6. Click the **Create my account** button. The **Your Workspace** page is displayed with a success message and the domain of your workspace, for example, **contentzilla.cerby.com**.

  7. Click the **Login** button. The authentication page for Cerby is displayed, as shown in **Figure 2**.

![Screenshot of the authentication page for Cerby with the Username and
Password input fields and the Log in
button.](images/fjvDT_e3XX1qG2QG2bIxkfTKz8Z13UZxSXDlWGpJqwmgMsgdw19IUBN4REDa2MKQOgTPeTMn6c1N8x3PaiCM9VXj8phSn90gcFC7xjGWIVTpQBjedILhQ8Y8Crv8_ncC6gYMkeBphHMPMTgZOJHT9v4)

**Figure 2.** Authentication page for Cerby

  8. Enter your Cerby account credentials in the corresponding fields:

     * Your email address in the **Username** field

     * Your password in the **Password** field 

  9. Click the **Sign in** button. The homepage of the Cerby dashboard is displayed, as shown in **Figure 3**.

![Screenshot of the homepage of the Cerby dashboard, comprised by a left
navigation drawer and a main
section.](images/Li9ZMsx_xS6rM_HSQ4bVWCUrD9vdGiArRGMrzzZeZzK7uaHAbOE_gIr4164ewWMhza-
rkm70T4oscjvGA0aYHSNxgSw2p6SWYXCZ9k8w-3Ex8qL3dZZaTBfU12epZ64OBqp9CTQUogZH4LADu6ji3KA)

**Figure 3.** Homepage of the Cerby dashboard

Your local user workspace is now created. The next step is 2\. Install the
Cerby mobile app and browser extension.

## **2\. Install the Cerby mobile app and browser extension**

To install the Cerby mobile app and browser extension, you must complete the
following steps:

  1. Install the Cerby browser extension by following the instructions in the [How to install the Cerby browser extension](https://help.cerby.com/en/articles/5620156-video-how-to-install-cerby-s-browser-extension) video.

  2. Install the Cerby mobile app by following the instructions in the [Install the Cerby mobile app](https://help.cerby.com/en/collections/10147391-install-the-cerby-mobile-app) collection.

The next step is 3\. Turn on MFA for your Cerby account.

## **3\. Turn on MFA for your Cerby account**

To turn on multi-factor authentication (MFA) for your Cerby account with an
authentication app, you must complete the following steps from the homepage of
your Cerby dashboard:

  1. Click the **Turn MFA On** button from the **Add a second layer of protection** section. The **Link your authentication app to your Cerby account** dialog box is displayed with a QR code.

  2. Open the authenticator app on your mobile phone.

  3. Follow the instructions to add an account by scanning the QR code. A time-based authentication code is generated.

  4. Click the **Next** button from the dialog box you left open in the Cerby web app. The **Try the authentication code** dialog box is displayed.

  5. Enter the time-based authentication code generated by your authentication app in the **Authentication Code** field.

  6. Click the **Verify** button. The dialog box closes, and a success message box is displayed.

Now you are done. It’s time to start adding your accounts to Cerby and sharing
them with your colleagues.

* * *

# **Manage users in a local user workspace**

Users with the **Workspace Owner** and **Workspace Admin** roles can perform
the following user management actions in a local user workspace:

  * Add a user

  * Reset MFA

  * Force password reset

  * Export members

  * Remove user from workspace

The following sections describe each action.

## **Add a user**

To add a user to a local user workspace, you must complete the following
steps:

  1. Select the **All members** option from the left navigation drawer. The **All Members** view is displayed, as shown in **Figure 4**.

![Screenshot of the All members view of the Cerby dashboard, which contains a
table of users with their workspace role, accounts, joined date, and
status.](images/GAsXOJLLmi39iFRZjeQsTMzN-
ARMTmPAyH2M-RmzobX9E8vnfVTPIq1fw9vPsnFD_2Fk7lUDpTI-
DJ8EDO-3jZGNrv9dlPbXS5Tf7jtW2GYI0kEgO04m32RPFEUFd0PyjVPjIHwtYC8lnN7jFZOtvCY)

**Figure 4. All members** view of the Cerby dashboard

  2. Click the **Add member** button located at the top right of the page. The **Add a team member** dialog box is displayed.

  3. Enter the email address of the user you want to add.

  4. Click the **Next** button. The user is added to a list in the **MEMBER** section

**NOTE:** To add multiple users, enter each email address individually and
press Enter. Each one is added to the list in the **MEMBER** section.

  5. Select the workspace-level role of the user:

     * **Admin:** They can invite and manage users in the workspace.

     * **User:** They can add and manage permissions per account.

**NOTE:** If you added multiple users, the role you select will be assigned to
all of them.

  6. Click the **Send Invite** button. The dialog box closes, a success message box is displayed, and an email is sent to the user to join Cerby with a temporary password.

**IMPORTANT:** The temporary password expires in 48 hours. After this time,
users need a new invite.

## **Reset MFA**

To reset MFA for a user in a local user workspace, you must complete the
following steps:

  1. Select the **All members** option from the left navigation drawer. The **All Members** view is displayed.

  2. Click the **More options** icon of the corresponding user. A drop-down list is displayed.

  3. Select the **Reset MFA** option from the list. A message box is displayed, and an email is sent to the user to reset their MFA device.

## **Force password reset**

To force a password reset for a user in a local user workspace, you must
complete the following steps:

  1. Select the **All members** option from the left navigation drawer. The **All Members** view is displayed.

  2. Click the **More options** icon of the corresponding user. A drop-down list is displayed.

  3. Select the **Force Password Reset** option from the list. A message box is displayed, and an email is sent to the user to ask them to reset their password with a code.

## **Export members**

You can export a CSV file with the information of all the workspace members or
a specific member. After the export, Cerby sends you an email with a button to
download the file to your computer.

To export the information of all the workspace members, you must complete the
following steps:

  1. Select the **All members** option from the left navigation drawer. The **All Members** view is displayed.

  2. Click the **Export** button located at the top right of the table. A success message box is displayed, and an email is sent to download the report.

To export the information of a specific workspace member, you must complete
the following steps:

  1. Select the **All members** option from the left navigation drawer. The **All Members** view is displayed.

  2. Click the **More options** icon of the corresponding user. A drop-down list is displayed.

  3. Select the **Export** option from the list. A success message box is displayed, and an email is sent to download the report. 

## **Remove user from workspace**

To remove a user from a local user workspace, you must complete the following
steps:

  1. Select the **All members** option from the left navigation drawer. The **All Members** view is displayed.

  2. Click the **More options** icon of the corresponding user. A drop-down list is displayed.

  3. Select the **Remove from Workspace** option from the list. The **Remove <user name>?** dialog box is displayed.

  4. Click the **Remove from Workspace** button. The dialog box closes, and a success message box is displayed.

{% hint style="warning" %} **NOTE:** For reporting purposes, the account of
removed users is disabled; however, they will no longer be able to access
Cerby. {% endhint %}

* * *

# **Join Cerby from an invite**

After being added to a local user workspace by a **Workspace Owner** or
**Workspace Admin** , all users receive an invite through email to join Cerby
and set up their account.

To join Cerby from an invite, you must complete the following steps:

  1. Open the message Cerby sent to your email address. The message contains the following information:

     * Workspace name

     * Username

     * Temporary password

  2. Click the **Join now** button from the message. The Cerby authentication page is displayed.

  3. Enter your username and temporary password in the corresponding fields.

  4. Click the **Sign in** button. The **Change Password** page is displayed.

  5. Enter a new password for your Cerby account and your profile information in the corresponding fields:

     * **New Password**

     * **Enter New Password Again**

     * **Name**

     * **Family name**

  6. Click the **Send** button. The Cerby dashboard is displayed.

To start using Cerby, all users must complete the following steps from the
Create and configure a local user workspace section:

  1. Install the Cerby mobile app and browser extension

  2. Turn on MFA for your Cerby account

* * *

# **Edit the workspace display name**

Users with the **Workspace Owner** and **Workspace Admin** role can only edit
the workspace display name for a local user workspace. To do so, you must
complete the following steps:

  1. Select the **Settings** option from the left navigation drawer. The **Workspace Configuration** page is displayed with the **General** tab activated.

  2. Activate the **IDP Settings** tab.

  3. Click the **Edit IDP Details** button located at the top right of the **Identity Provider Settings** section.

  4. The **Confirm your identity to continue** dialog box is displayed. An identity challenge is issued in your Cerby mobile app.

  5. Click the **It’s me!** button in the **Confirmation Request** screen of the Cerby mobile app to confirm your identity. The dialog box in the Cerby web app closes.

  6. Enter a new name in the **Workspace display name** field. 

  7. Click the **Save Changes** button. A success message box is displayed.

{% hint style="danger" %} **IMPORTANT:** You cannot edit the **Workspace
name** and **Client Id** fields. If you want to edit these fields, contact the
Cerby Customer Support team. {% endhint %}

* * *

# **Troubleshooting: “We couldn’t turn MFA on for your profile” message**

When you try to turn on MFA for a Cerby account that belongs to a local user
workspace, and you haven’t set your mobile phone time as automatic, the “We
couldn’t turn MFA on for your profile” message may appear, as shown in
**Figure 5**.

![Screenshot of the “We couldn’t turn 2FA on for your profile” message when
trying to verify the authentication code in the Try the authentication code
dialog
box.](images/m5vB4WQ4MI4LtMRX_H8dHxvjh4Bj7RFacSUPbM0V_igXrNtPPjrFtsOIPxwNUpGH_LYGRZS2Hhoqvw8_wEjsFScj4SyoEleTpM5GhxBUpEUyzF7KHfVijZQs7J-usgdd6JZpFgfGQwgWuFVQzLRB4bw)

**Figure 5.** “We couldn’t turn MFA on for your profile” message

The error message is displayed when you verify the authentication code that
your authentication app provides after scanning the QR code. This error occurs
because the authentication app generates time-based codes that expire;
therefore, when your mobile phone has a different time, the code could have
expired or is not yet valid.

To solve this problem, set the time settings to automatic on your mobile phone
by following the corresponding instructions:

  * [Set time, date & time zone](https://support.google.com/android/answer/2841106?hl=en) (Android)

  * [Change the date and time on iPhone](https://support.apple.com/guide/iphone/change-the-date-and-time-iph65f82af3e/ios) (iOS)

Now, try to turn on MFA again by following the steps in step 3\. Turn on MFA
for your Cerby account section.

