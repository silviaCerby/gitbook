# Check for updates in your app and apply report

**Description:** This article describes how to check for updates in your seat-based and paid social apps from Cerby, and apply the report.

{% hint style="info" %} **Who can use this feature?** * App
integration**Owners** * Available to Cerby Automate * Only supported using the
Cerby web app {% endhint %}

As an app integration**Owner** , you can check for updates in your seat-based
and paid social apps to identify and import user, role, and asset changes to
Cerby.

Cerby performs daily checks for updates on your connected Apps via an
automation task, but you can trigger these checks manually from your
dashboard. Whenever you update users and roles manually in the app, Cerby
recommends triggering a check for updates to import the latest information to
your App.

User and role changes are automatically applied to Cerby during a check for
updates unless users are deprovisioned from the IdP. In such a case, Cerby
generates a report and sends you an email to confirm their removal from Cerby
by applying the report.

To check for updates, you and your app members must complete the following
steps from the article [Connect an
App](https://help.cerby.com/en/articles/9046120-connect-an-app):

  1. [Check for updates and import users, roles, and assets to Cerby](https://help.cerby.com/en/articles/9046120-connect-an-app#h_9c6531cf9a)

  2. [Manage unmatched users](https://help.cerby.com/en/articles/9046120-connect-an-app#h_9e56f17ceb)

  3. [Accept invites and connect user accounts to Cerby](https://help.cerby.com/en/articles/9046120-connect-an-app#h_7769f49d7f)

To apply the report after a deprovisioning event from the IdP detected during
a routinary check for updates, you must complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.

  2. Select the **Apps** option from the left navigation drawer. The **Apps** view is displayed.

  3. Click the **Settings** icon of the corresponding app card. The app details page is displayed with the **Settings** tab activated.

  4. Click the **Check for updates** button located at the top-right section of the page. A message box is displayed with information about the process.

**NOTE:** The check and import may take a few minutes, depending on the number
of users. When the process is complete, a success message box and the **View
report** button are displayed.

  5. Click the **View report** button. The **Sync Data** wizard is displayed with the number of new and removed users and updated roles on the **To be updated to Cerby** section

**TIP:** Click the **New Users** , **Removed users** , or **Updated roles**
buttons to display a drop-down list with the details of the users to be added
or removed from Cerby, as well as the role changes.

  6. Click the **Finish Sync** button. The wizard closes, and a success message box is displayed. The corresponding users are removed from Cerby and the app via an automated task, and role changes are applied.

If you invited new users, complete their onboarding by performing the
following steps from the article [Connect an
App](https://help.cerby.com/en/articles/9046120-connect-an-app):

     1. [Manage unmatched users](https://help.cerby.com/en/articles/9046120-connect-an-app#h_9e56f17ceb)

     2. [Accept invites and connect user accounts to Cerby](https://help.cerby.com/en/articles/9046120-connect-an-app#h_7769f49d7f)

{% hint style="info" %} **NOTE:** If you only want to review and apply a
report for a check of updates already performed, complete steps 5 and 6. {%
endhint %}

