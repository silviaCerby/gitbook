# Create a password policy

**Description:** This article describes how to create a password policy for all the accounts belonging to a managed app.

{% hint style="info" %} **Who can use this feature?** * Workspace**Owners** ,
**Super Admins** , and **Admins** * Only supported using the Cerby web app {%
endhint %}

As a workspace **Admin** , you can create a [password
policy](https://help.cerby.com/en/articles/11465716-explore-password-policies)
to enforce automated password rotations for all the accounts saved in your
workspace belonging to a managed app. As part of the setup, you can specify
the event that triggers the rotations.

{% hint style="info" %} **NOTE:** You can only configure password rotation
policies for managed apps that support the password rotation automated task.
For more information, read the article [Explore the supported automated task
for your managed accounts](https://help.cerby.com/en/articles/6263064-explore-
the-supported- automated-tasks-for-your-managed-accounts). {% endhint %}

To create a password policy, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Password Policies** option from the left menu. The **Password Policies** page is displayed with a table of policies.

  3. Click the **Create policy** button located at the top right of the page. The **Create Policy** dialog box is displayed.

  4. Enter a name for your policy in the **Policy name** field.

  5. Select the option from the **Event type** drop-down menu that corresponds to the event you want to trigger the automated password rotation:

     * **User login:** Passwords are rotated in a specified time after a user logs in to an account using autofill with the Cerby browser extension or mobile app.

       1. Select the corresponding option from the **Schedule interval** drop-down menu:

          * **1 hour after login**

          * **2 hours after login**

          * **4 hours after login**

          * **8 hours after login**

          * **12 hours after login**

          * **1 day after login**

          * **2 days after login**

     * **Schedule:** Passwords are rotated at a specified recurring date and time.

       1. Select a date to start the password policy from the **Starting date** calendar.

       2. Specify the frequency of the password rotations by entering a number and selecting the corresponding option in the **Frequency** section:

          * **days**

          * **weeks**

          * **months**

          * **years**

For example, if you enter **1** and select **week** , the automated password
rotations will be executed every week starting on the date you have selected
in step a.

**IMPORTANT:** The frequency can only be an interval between one day and one
year.

       3. Specify a time window to execute the automated password rotations in the **Time window execution** section.  
**IMPORTANT:** The time window consists of a start and an end time, and must
be at least 8 hours.

  6. Specify the apps for which you want to implement the password policy by completing the following steps:

     1. Enter the name of the app in the **Search by app** search bar. A list of apps matching the name is displayed below.

     2. Select the app from the list.

     3. Repeat steps a and b as necessary to select multiple apps.

  7. Click the **Confirm** button. The dialog box closes, and a success message box and the new policy are displayed.

{% hint style="info" %} **NOTE:** Cerby performs only one password rotation
every 24 hours after the last successful rotation by policy. You can still
perform automated password rotations on demand. {% endhint %}

Now you are done.

