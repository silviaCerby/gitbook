---
description: This article describes how to edit the settings of an existing password policy.
intercom_id: 11466959
---

# Edit a password policy

{% hint style="info" %}


**Who can use this feature?**

* Workspace**Owners** , **Super Admins** , and **Admins**
* Only supported using the Cerby web app


{% endhint %}

As a workspace **Admin** , you can edit the settings of an existing [password policy](https://cerby-test.gitbook.io/cerby-test/support-and-use-cases/explore/explore-password-policies) to change the execution of automated password rotations.

Due to the current implementation of the Password Policies feature, the following rules have been established:

* You cannot change the event type from **User login** to **Schedule** and vice versa. You must delete the policy first and then create a new one with a different event type.
* For scheduled-based policies, you cannot edit the starting date; this setting is only available when creating the policy. You must delete the policy first and then create a new one with a different starting date.
* The updated password policy takes precedence over the old policy. However, if the old policy has started, the automated password rotations are rescheduled as follows:
    * **User login-based policies:** the queued rotations of the old policy are executed as planned and then, the new policy is implemented. The new policy will only start after the next user login event.
    * **Schedule-based policies:** the new policy is implemented after the current scheduled password rotations are executed according to the frequency. For example, if you change the frequency from 2 weeks to 1 month, you must wait until the 2-week rotation is executed, and then, the new policy is implemented.

{% hint style="info" %}


**NOTE:** Take into consideration that Cerby performs only one password rotation every 24 hours after the last successful rotation by policy.


{% endhint %}

To edit a password policy, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Password Policies** option from the left menu. The **Password Policies** page is displayed with a table of policies.
  3. Click the **Edit** (<figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1543943593/bd82b200d5be62e7efa4875637ed/AD_4nXf0XB_65D36ZTZdceVSJWGwYmL7mUDO2Q9zrgoZIiNCOrgU8ofAC6Im0Isz1bsp9yhlE_rByMmg5DKnZm5p3N3JXYCAR_32XDAPBMadkMjLrkuzru6117cN9DMEJIKY8Q2nDFJCLw?expires=1748389350&signature=bb36e879d97aaf585fafa3247f163a3402523893a851cf5c3e6812c433d90a7b&req=dSUjFcB6noRWWvMU3HP0gK7YwZgrLq%2Bp8L5FKgn2t8%2FEROWeapo%3D%0A" alt=""><figcaption></figcaption></figure>) icon of the corresponding policy. The **Edit password policy** dialog box is displayed.
**TIP:** You can also select the **Edit policy** option from the **More options**(<figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1543943914/783ae929911c1b389831811d31b8/AD_4nXeT3knlE0wH2YpVbRA63-2VFqLllGBNGN5SpUNwPQUXio36aYQKc2xR73Rsshzru2iPd6vuBnUTPsDTHRpe-ZAD3ZEt1dkv4LptnA3tVSjjY5spE71WcvrKTN_ad8tMAiFwjAlaDw?expires=1748389350&signature=717a051bda50ce7cac14cd65dab66427ddb7dbb078336bb7d282a0589d49bb75&req=dSUjFcB6noheXfMU3HP0gMlLa2h%2Fu5kqwfaCKM0qFZA6K9sFosE%3D%0A" alt=""><figcaption></figcaption></figure>) drop-down menu.

  4. Enter a new name in the **Policy name** field, if applicable.
  5. Update the policy settings according to the event type:

     * User login

       1. Select the new schedule interval of the automated password rotations from the **Schedule interval** drop-down menu:

          * **1 hour after login**
          * **2 hours after login**
          * **4 hours after login**
          * **8 hours after login**
          * **12 hours after login**
          * **1 day after login**
          * **2 days after login**
     * Schedule

       1. Specify the new frequency of the automated password rotations by entering a number and selecting the corresponding option in the **Frequency** section:
For example, if you enter **1** and select **week** , the password rotations will be executed every week starting after the rotations of the old policy are executed.

          * **days**
          * **weeks**
          * **months**
          * **years**

       2. Specify a new time window to execute the automated password rotations in the **Time window execution** section.
**IMPORTANT:** The time window consists of a start and an end time, and must be at least 8 hours.

  6. Click the **Confirm** button. The dialog box closes, and a success message box is displayed.

Now you are done.
