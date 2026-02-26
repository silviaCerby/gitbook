---
description: "This article describes how to create a password policy for all the accounts belonging to one or multiple managed apps."
intercom_id: 11466694
---

# Create a password policy

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , and **Admins**
* Only supported using the Cerby web app


{% endhint %}

As a workspace **Admin** , you can create a [password policy](https://help.cerby.com/en/articles/11465716-explore-password-policies) to enforce automated password rotations for all the accounts saved in your workspace belonging to one or multiple managed apps. As part of the setup, you can specify the event that triggers the rotations.

{% hint style="info" %}


**NOTE:** You can only configure password rotation policies for managed apps that support the password rotation automated task.


{% endhint %}

To create a password policy for one or multiple apps, you must complete the following steps:

1. Log in to your [Cerby](https://app.cerby.com/) workspace.
2. Select the **Password Policies** option from the left menu. The **Password Policies** page is displayed with a table of policies.
3. Click the **Create policy** button located at the top right of the page. A wizard is displayed on the **Create Policy** page.
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

For example, if you enter **1** and select **week** , the automated password rotations will be executed every week starting on the date you have selected in step a.

**IMPORTANT:** The frequency can only be an interval between one day and one year.

3. Specify a time window to execute the automated password rotations in the **Time window execution** section.
​**IMPORTANT:** The time window consists of a start and an end time, and must be at least 8 hours.

6. Click the **Next** button. The **Add a Policy** page of the wizard is displayed.
7. Select the apps for which you want to implement the password policy.

**TIP:** You can use the search bar to look for specific apps, the drop-down filter to show all apps or only apps with business hubs, or the **Select all** option to select all apps in the list.

8. Click the **Next** button. The **Review data** dialog box is displayed for you to review and confirm the policy.
9. Click the **Done** button. The dialog box closes, and a success message box and the new policy are displayed

{% hint style="info" %}


**NOTE:** Cerby performs only one password rotation every 24 hours after the last successful rotation by policy. You can still perform automated password rotations on demand.


{% endhint %}

Now you are done.
