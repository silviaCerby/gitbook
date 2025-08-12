# Explore Password Policies

**Description:** This article describes the Password Policies feature that enables you to configure password rotation policies per app.

With Cerby, you can implement more granular security controls on your accounts
based on your corporate policies and the sensitivity level of your apps.

The **Password Policies** feature enables workspace **Admins** to set up and
enforce password rotation policies for all the accounts belonging to an app.
Unlike workspace-wide policies enforced to all users and all accounts, you can
balance security best practices and workflow efficiency in your organization
with app-specific policies.

The automation approach of Cerby makes the policy implementation and execution
more seamless and less manual. You just need to create and set up the policy,
specifying the event that will start the policy and trigger the automated
password rotation execution. Currently, the following are the supported
events:

  * **User login:** The policy starts when Cerby identifies a user login event to an account using autofill with the Cerby browser extension or mobile app. You select the schedule interval for the execution of automated password rotations.

  * **Schedule:** The policy starts on the date you select, and you specify the frequency and time window for the execution of automated password rotations.

Nonstandard apps have varied password policies, and some of them, such as
those handling sensitive data (personal information, financial data, or
proprietary information), may require more frequent password rotations. With
Cerby's Password policies, you can schedule rotations to meet the specific
needs of each app.

Additionally, by centralizing access to your accounts in Cerby, you can ensure
uninterrupted access while maintaining a high level of security.

{% hint style="info" %} **NOTE:** You can only configure password policies for
managed apps that support the password rotation automated task. For more
information, read the article [Explore the supported automated task for your
managed accounts](https://help.cerby.com/en/articles/6263064-explore-the-
supported- automated-tasks-for-your-managed-accounts). {% endhint %}

The following are some of the benefits of the Password Policies feature:

  * **Enhanced security:** Cerby generates strong and unique passwords according to the app policies and password strength rules.

  * **Reduced risk of breaches:** Regular password rotations minimize the impact of potential data breaches because they typically terminate all active user sessions.

  * **Compliance adherence:** Password policies can help organizations comply with corporate and industry regulations and standards.

  * **Complementary protection:** On-demand password rotations and rotations based on deprovisioning events in your corporate identity provider (IdP) are not blocked by this feature.

**NOTE:** For any new account belonging to an app with an active policy, Cerby
verifies if the account must be affected by the policy.

  * **Improved visibility:** Cerby has a dedicated user interface to show the status of the policy and the affected accounts: the **Password Policies** page in the Cerby web app dashboard, described in the following section.

* * *

# **The Password Policies page**

The **Password Policies** page displays a table with all the policies you have
created for your apps in Cerby. This view provides a convenient location to
manage your policies and see all the accounts affected by them.

**Figure 1** shows what the **Password Policies** page looks like.

![Screenshot of the Cerby web app. The Password Policies page is displayed
with a table of apps for which a policy has been created
](gitbook/imagesAD_4nXf1RHkWyMBQQ5RVrwdS1Z1iZ05Bnqhir2AY66kgdX__dDDuYr9w7GaR4-J66G54kvOr-
HgI6aEq6sc3mnZBi8exxgptTUJRR7BSWQ4x-la_K2XqJDeetA0qDk2jAf6xljsEMI60IQ)

**Figure 1.** **Password Policies** page in the Cerby web app dashboard

This view provides the following information about your policies in a table:

  * **App provider:** It is the app for which the policy is implemented.

  * **Name:** It is the name of the policy.

  * **Total accounts:** It is the total count of accounts affected by the policy.

  * **Type:** It is the event type that triggers the automated password rotation. Currently, the possible values are the following:

    * **User login:** The automated password rotation is executed in a specified interval after a user logs in to an account using autofill with the Cerby browser extension or mobile app.

    * **Schedule:** The automated password rotation is executed within a time window at a specified recurring date and time.

  * **Schedule interval:** It is the time to wait to execute the automated password rotation after a login event in user login-based policies or the password rotation frequency in schedule-based policies.

  * **More options (**![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1543845897/16fa6c36b3cdd83176d755b1d216/AD_4nXfOu5NKvvOMXjj_lC3EKEEK-81IcTM46voZ4NAffGloRhT0lKUkRx4E9Uj94HLoepC6unWl39YyNRupuhihxFcnXPQR-GRPwrLkAmApGOx4t_9xU_4U19xp_x9aqqEKXkmtKEvexg?expires=1748466000&signature=7a9760d5fd09049405c0aa83881dd3fb71cbe4ba416f118d8bb320cdf1b52a71&req=dSUjFcF6mIlWXvMW3Hu4gS5AlY7eKvgdtjvU65s01ugrZK7BoQV3FoQYLKbh%0A3A%3D%3D%0A)**):** It is a drop-down menu with the following options:

    * **View all accounts**

    * **Edit policy**

    * **Delete policy**

When clicking the **View all accounts** (![](gitbook/imagesAD_4nXdicSor-
pm2J7BAyqhytQsyte2b6KYldyM6JtYzisJgjQ9-uUPz7HhkkkoHH-c-
foI4FZ2nGoCMSAquDlEsUi5B8f_S9XMsvW0vUGL9P4DI_AVWHIzuhuR22aCSIk72NOLGKMHaKg))
icon or selecting the **View all accounts** option from the **More options**
drop-down menu, the policy details page is displayed, as shown in **Figure
2**.

![Screenshot of the Cerby web app. The policy details page is displayed with a
table of accounts that belong to the same app for which a policy has been
created](gitbook/imagesAD_4nXdOqoaKxB0_LItH5LZtY7Al0PmYcr28rK75bmAhPsXD9qrMTpDpIqSCr6NvUDdNX-
wIadzUg5JxjWYTxNNi6IU3DDhVSHbOfpOsLifUM7kIgJ4yo-sq7maS8fnAFOHl4WzXBhHAdA)

**Figure 2.** Policy details page in the Cerby web app dashboard

This page lists the following information about the accounts affected by the
policy:

  * **Account:** It contains the account name and username associated with the account.

  * **Last attempt:** It is the date and time of the last password rotation attempt.

  * **Last status:** It is the status of the last automated password rotation attempt. The possible values are the following:

    * **Scheduled:** The event has started the policy, but the automated password rotation execution is waiting for the specified time to elapse. 

    * **Queued:** The automated password rotation is in the queue, waiting to be executed.

    * **Excluded:** The account was excluded from the password policy.

    * **Started:** The password policy has started based on the specified event.

    * **Not started:** The password policy is waiting for the event to start.

    * **Running:** The automated password rotation is being executed.

    * **Completed:** The automated password rotation was completed successfully.

    * **Not completed:** The last automated password rotation attempt was not completed.

  * **Next attempt:** It is the date and time of the next automated password rotation attempt. For user login-based policies, this column is only populated after the event triggered the rotation execution.

  * **More options (**![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1543845897/16fa6c36b3cdd83176d755b1d216/AD_4nXfOu5NKvvOMXjj_lC3EKEEK-81IcTM46voZ4NAffGloRhT0lKUkRx4E9Uj94HLoepC6unWl39YyNRupuhihxFcnXPQR-GRPwrLkAmApGOx4t_9xU_4U19xp_x9aqqEKXkmtKEvexg?expires=1748466000&signature=7a9760d5fd09049405c0aa83881dd3fb71cbe4ba416f118d8bb320cdf1b52a71&req=dSUjFcF6mIlWXvMW3Hu4gS5AlY7eKvgdtjvU65s01ugrZK7BoQV3FoQYLKbh%0A3A%3D%3D%0A)**):** It is a drop-down menu with the following options:

    * **Include in policy:** This option is displayed for accounts with the **Excluded** status to include them in the policy.

    * **Exclude from policy:** This option excludes an account from the policy; therefore, the account status changes to **Excluded**.

* * *

# **Related articles**

The following articles contain more information about the Password Policies
feature:

  * [Create a password policy](https://help.cerby.com/en/articles/11466694-create-a-password-policy)

  * [View all accounts with a password policy](https://help.cerby.com/en/articles/11466954-view-all-accounts-with-a-password-policy)

  * [Edit a password policy](https://help.cerby.com/en/articles/11466959-edit-a-password-policy)

  * [Exclude an account from a password policy](https://help.cerby.com/en/articles/11466979-exclude-an-account-from-a-password-policy)

  * [Include an account in a password policy](https://help.cerby.com/en/articles/11466985-include-an-account-in-a-password-policy)

  * [Delete a password policy](https://help.cerby.com/en/articles/11466995-delete-a-password-policy)

