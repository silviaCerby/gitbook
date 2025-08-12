# Update user roles in your app via a business hub

**Description:** This article describes how to update user roles in your external seat-based and paid social apps via a business hub.

{% hint style="info" %} **Who can use this feature?** * Business hub
**Owners** * Only supported using the Cerby web app {% endhint %}

As a business hub **Owner** , you can update user roles in your external seat-
based and paid social apps via an automated task triggered from Cerby.

{% hint style="danger" %} **IMPORTANT:** You cannot update user roles
individually if they have shared access to a business hub integration through
a team. In this case, you must update the role of the corresponding team. The
instructions are different depending on how the teams were created in Cerby: *
Self-managed teams * [Update team roles in your app via a business
hub](https://help.cerby.com/en/articles/11139474-update-team-member-roles-in-
your-app-via-a-business-hub) * IdP-managed teams * [Update user roles in your
apps via an IdP and business
hub](https://help.cerby.com/en/articles/11040590-update-user-roles-in-your-
apps-via-an-idp-and-business-hub) {% endhint %}

To update the role of a user in your external app, you must complete the
following steps:

  1. Log in to your [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Business Hubs** option from the left menu. The **Business Hubs** page is displayed.

  3. Click the **More options** (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1492686690/4fa5fa85b4a0fc88221e2c7ca61d/AD_4nXeU8DgAdiB-iCqwb_6R5lWeyd9fkeiOknG555YrLTsasYPOnUOvGmkW8pSDDFXdYS9XP34jzVYFjBD-ALHVAztnuNQEtVzp7WvKUqlH8bOIxfBsWcoNc9MFKbey0AhMsbUJ6eIeYA?expires=1745658000&signature=9d96ee6003e591a70e941f28795264fafeb45fb1a9fba516c8e57a95cfe98f45&req=dSQuFM92m4dWWfMW3Hu4gaHTdDeZUeO7LkP5bAuPj3BQPxEgGAEwwn0xROLZ%0Aiw%3D%3D%0A)) icon of the corresponding business hub card. A drop-down menu is displayed.

  4. Select the **Settings** option from the menu. The business hub details page is displayed with the **Settings** tab activated.

  5. Activate the **Users** tab. The **User Overview** section is displayed with tables of users who have shared access to the business hub.

  6. Navigate to the table that lists the users whose role you want to change in your external app.

**NOTE:** You can only update user roles after they have accepted the
invitation to the external app.

  7. Click the down arrow icon (![](https://downloads.intercomcdn.com/i/o/pc0ldyqu/1492691508/fce05e2bdb11f137e589613bce86/AD_4nXcV6jb3GgdUDrD4KUE7yRRgS4ZZiHOWQu6qiEpwcYXwu81JK1IlN3kBUyShxV4eOm0K3CeFqVHm5w717w-4ZeDLOd4b0DHW3uvLjeOrY-sLah1RSkVOpGDtytCMjgijjelYOKiRnA?expires=1745658000&signature=d2796a6a1f6d1ffbf097e9459a885abb7402406fc218cec824862607c2212329&req=dSQuFM93nIRfUfMW3Hu4gTdKLeVsuK9pWfba11eucb1XsHgefXjYmViRe5pf%0AgA%3D%3D%0A)) in the **App Access** column of the corresponding user. A drop-down menu is displayed with the available roles in the app.

  8. Select or deselect the role options you want to assign or remove.  
​**NOTE:** The roles you can select are different for each external app. Cerby
imports these native roles and displays them during the process.

  9. Click the **Apply** button. The drop-down list closes, and a success message box is displayed.

Now you are done.

# **Important considerations**

While the instructions above provide a general guide for updating the user
access role, outcomes can vary depending on how access was granted to the
business hub integration. The following are important considerations:

  * The process of updating user roles differs based on whether the external applications support weighted roles or not. Cerby manages these updates in the following ways:

    * If the external app supports weighted roles, Cerby triggers the automated task to update the user’s role when a higher role is assigned or the highest role is removed.

    * If the external app doesn’t support weighted roles, Cerby triggers an automated task to update the user’s role to reflect the latest assignment. 

