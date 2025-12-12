---
description: This article describes how to remove users of your seat-based and paid social apps via a business hub.
---

# Remove users from your app via a business hub

{% hint style="info" %}


**Who can use this feature?**

  * Business hub **Owners**
  * Only supported using the Cerby web app


{% endhint %}

As a business hub **Owner** , you can remove the users of your external seat-based and paid social apps through Cerby.

This process involves removing user access to the business hub integration and choosing to remove or keep the user’s seat in the external app.

{% hint style="danger" %}


**IMPORTANT:** You cannot remove users individually if they have shared access to a business hub integration through a team. In this case, you must remove the users from the corresponding team. The instructions are different depending on how the teams were created in Cerby:

  * Self-managed teams
    * [Add or remove members from teams manually](https://help.cerby.com/en/articles/6624225-how-to-use-teams#h_4e263e9165)
  * IdP-managed teams
    * **Okta:** [Remove people from a group](https://help.okta.com/en-us/content/topics/users-groups-profiles/usgp-remove-group-people.htm)
    * **Entra ID:**[Remove members or owners of a group](https://docs.azure.cn/en-us/entra/fundamentals/how-to-manage-groups#remove-members-or-owners-of-a-group)


{% endhint %}

To remove a user from your external app via a business hub, you must complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
  2. Select the **Business Hub** option from the left menu. The **Business Hub** page is displayed.
  3. Click the **More options** (<figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1459426962/3a92e9b609b0a48302efbe8e7718/AD_4nXf_iipjK0DNaXh6iPZGpoBtZww8BvSGW5pn6G-dsBoV3kNHCIktwXQqj5kyWA4ebWu4ehUKBf5lP1u73VKpD-1GYd9S9yqGK2gbNAx22nQZO8Kjwt56vibgfcZo_tLnDuw6Nr7p?expires=1764450000&signature=0aff472e812479b10446d2190d4b8072a0518c6b04c64173dc3a318799efb3d4&req=dSQiH818m4hZW%2FMW3Hu4getyg%2FpqN3Kuk60mfEwY0BZhwIhsHlVPx7WeVcXr%0ASQ%3D%3D%0A" alt=""><figcaption></figcaption></figure>) icon of the corresponding business hub card. A drop-down menu is displayed.
  4. Select the **Settings** option from the menu. The business hub details page is displayed with the **Settings** tab activated.
  5. Activate the **Users** tab.
  6. Click the **More options** (<figure><img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/1459426962/3a92e9b609b0a48302efbe8e7718/AD_4nXf_iipjK0DNaXh6iPZGpoBtZww8BvSGW5pn6G-dsBoV3kNHCIktwXQqj5kyWA4ebWu4ehUKBf5lP1u73VKpD-1GYd9S9yqGK2gbNAx22nQZO8Kjwt56vibgfcZo_tLnDuw6Nr7p?expires=1764450000&signature=0aff472e812479b10446d2190d4b8072a0518c6b04c64173dc3a318799efb3d4&req=dSQiH818m4hZW%2FMW3Hu4getyg%2FpqN3Kuk60mfEwY0BZhwIhsHlVPx7WeVcXr%0ASQ%3D%3D%0A" alt=""><figcaption></figcaption></figure>) icon of the corresponding user. A drop-down menu is displayed.
  7. Select the**Remove user** option. The**Remove user?** dialog box is displayed.
  8. Select the corresponding options to specify the access to remove from the user.

     * **Remove the user's seat and permissions in <app name> Hub: **This option removes the user from the business hub and the external app.
     * **Remove the business hub from the user's Cerby dashboard: T** his option removes the user from the business hub while keeping their user account active in the external app.
​**NOTE:** This option is only available for users who have accepted the invite and joined the external app.

  9. Click the **Remove access** button. A dialog box requesting to confirm the removal option is displayed.
  10. Click the **Confirm** button. The dialog box closes, and a success message box is displayed. Depending on your selection, the user is removed from the business hub integration, the external app, or both.

Now you are done.

# Important considerations

While the instructions above provide a general guide for removing users, outcomes can vary depending on how access was granted to the business hub integration. The following are important considerations:

  * Users who keep shared access to the integration, whether individually or through another team, will not be removed from the external app. Cerby ensures that their role in the external app is updated to reflect their remaining access.
  * To fully remove users’ access, make sure you review and remove all existing user and team access grants to the business hub integration.
  * Removals from the external app or the business hub _don’t_ affect user access to their Cerby workspace.
