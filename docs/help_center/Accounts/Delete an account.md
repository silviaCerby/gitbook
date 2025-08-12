# Delete an account

**Description:** This article describes how to delete an account from Cerby.

{% hint style="info" %} **Who can use this feature?** * Workspace **Owners** ,
**Super Admins** , **Admins** , **Users** , and **Guest Users** * Account
**Owners** * Supported using the Cerby web app {% endhint %}

As an account **Owner** , you can delete an account when you no longer need to
keep it saved in your Cerby workspace.

To delete an account from Cerby, you must complete the following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.

  2. Click the corresponding account card. The account details page is displayed.

  3. Expand the **Emergency controls** section located at the bottom of the page.

  4. Click the **Remove account** button in the **Remove the account from Cerby** section. 

     * **TIP:** You can also access the **Remove account** option by completing the following steps:

       1. Click the **More options** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1633510499/6028c63bcfcc981dfce075123e3f/AD_4nXdOyjX5VLeggjdNYSerZAO85zLoRuGx-DRYGaBp5CcOE7iipWt7SEaIEbDX4NMoTmVyVtFaiQY2VJIKoi0vTCXg_xzY_zavd1sDBWVm-lXWSlbMpWDQP6k8ukILEFdUFELx3bH4?expires=1754784000&signature=cf938310b0961b557e1a73c0d30823de902259024645396893cba445eb4e5327&req=dSYkFcx%2FnYVWUPMW3Hu4gY8%2BG8zcMZ41tisR3Oe2vXyoZPsFRF5q6GXS12Gk%0Akw%3D%3D%0A)) icon that appears when hovering over the corresponding account card. A drop-down menu is displayed.

       2. Select the **Delete from Cerby** option.

The **Delete <your-account-name> account** page is displayed.

  5. Select the reason why you want to delete the account from the **Why are you deleting your account?** drop-down menu.

  6. Take action on your account before deleting it:

     * Choose what to do with the multi-factor authentication (MFA) setup if it is turned on and managed by Cerby as an authenticator app:

       * Select the **Keep my account secure** option to keep MFA turned on and managed by Cerby.   
Verification codes will be accessible through the account details page of the
deleted account.

       * Select the **Reset account settings** option to turn off and delete the MFA setup from Cerby automatically. **IMPORTANT:** This feature is only available for managed apps with the [supported automated task](https://help.cerby.com/en/articles/6263064-explore-the-supported-automated-tasks-for-your-managed-accounts).

       * Click the **View QR code** button to configure another authenticator app so you don’t lose access to your account. The **Confirm your identity dialog box** is displayed.

         1. Confirm your identity by using one of [Cerby's multi-factor authentication methods](https://help.cerby.com/en/articles/9462605-verify-your-identity-with-cerby-s-mfa-methods). A dialog box is displayed with a QR code.

         2. Set up MFA with another authenticator app by scanning the QR code or copying and pasting the TOTP secret key.

     * You can view the account’s password by completing the following steps:

       * Click the **View Password** button. The **Confirm your identity to continue** dialog box is displayed.

       * Confirm your identity by using one of [Cerby's multi-factor authentication methods](https://help.cerby.com/en/articles/9462605-set-up-your-identity-with-cerby-s-mfa-methods). The **View Password** dialog box is displayed.

         1. Click the **View** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1660892029/1f980cece78492fd5b0707b255dd/AD_4nXckIwWVkC1bp0CbigSzNSxDN7LjEKOE6H_yaZI5zd9oZRYw0cyO667fsE5G-oSvgZl7eUQEWknUxjfi5qnfT3qDyrkbc4B06peba6F6nPlw_jib49xpY6CaHUGan0BMcZubXRV0?expires=1754668800&signature=674f827a90b8a979d63f8a11341792eadd1d1a7fece30623ad017c7f491061f0&req=dSYhFsF3n4FdUPMU3HP0gLbHOhY2VQnCM4CqMbLrBQZgIIA4mn8%3D%0A)) button to show the password.

         2. Click the **Copy** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1660892421/dcf1a271de99c21724c2ec27ce2f/AD_4nXdHwiZbJ24B0y_qU7VZ5ddgxtQNoM29tr02hfQBvnswHFjHq8zhXvVI-aEIJxPfL7K8dhZRR198sfrSArudRzgWm_rPuun-77ZxmbO8LLq0V0_OGsReuPsmQZGBSv8ONjhVM7lE?expires=1754668950&signature=66f6894da9cd68d8b0d51398948b8dd7912e9b4a1d5f4c90d668dcfa0198308b&req=dSYhFsF3n4VdWPMU3HP0gCz5TJ3ZHTW8OzSziMGpKxIiB8AUFL4%3D%0A)) button to copy the password to the clipboard. You can paste it in a safe place.

       * Click the **Done** button to close the dialog box.

  7. Click the **Delete account** button. The page closes, and a success message box and the account details page are displayed.

Now you are done.

* * *

# **Important considerations**

The following are important considerations about this feature:

  * Cerby keeps the account details and activity log stored for security, compliance, and auditing purposes.

  * Account **Owners** can still restore the account. For instructions, read the article [Restore a deleted account](https://help.cerby.com/en/articles/11385391-restore-a-deleted-account).

  * Users, guest users, and team members who had shared access to the account as **Collaborators** lose access.

