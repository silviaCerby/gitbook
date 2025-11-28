# Import users, roles, and entitlements from an IdLCM integration into Okta

**Description:** This article describes how to import the users, roles, and entitlements from an IdLCM integration into Okta.

{% hint style="info" %} **Who can use this feature?** * IT admins with an Okta
tenant * Workspace**Owners, Super Admins,** and**Admins** {% endhint %}

As an IT admin collaborating with a workspace **Owner** , **Super** **Admin**
, or **Admin** , you can import the users, roles, and entitlements of an IdLCM
integration to sync user and group data to Okta.

This process is especially helpful for SCIM-enabled integrations where users
or groups might be created, updated, or deactivated directly in the external
app. You can also detect and reconcile changes between your Cerby-integrated
app and your Okta environment.

To import the users, roles, and entitlements from an IdLCM integration into
Okta, you must complete the following steps:

  1. Log in to the[ Okta Admin Console](https://developer.okta.com/login/) of your organization.

  2. Select the **Applications** option from the **Applications** drop-down list located in the left menu.

  3. Select the app integration you have created for IdLCM.

  4. Activate the **Import** tab. The **Import Results** page is displayed. 

  5. Click the**Import Now** button. A dialog box showing the scanned users and groups is displayed. 

  6. Click the **OK** button. The list of imported users and any detected attribute changes is displayed.

  7. Review the imported users and the matching Okta user assignments, and select the users and changes you want to apply.

  8. Click the **Confirm Assignment** button. The **Confirm Imported User Assignments** dialog box is displayed.

  9. Click the **Confirm** button. Okta applies the selected changes, updating user profiles and assignments as needed. 

Now you are done.

