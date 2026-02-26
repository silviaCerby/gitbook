---
intercom_id: 8167922
---

# Release Notes - July 24, 2023

## New Features

* Remember how excited you were in April with the beta release of the [Save credentials at login](https://help.cerby.com/en/articles/7239387-beta-how-to-save-your-credentials-at-login-via-the-cerby-browser-extension) feature? Guess what!? We improved the experience, and now you can add accounts to Cerby whether you have an active session with the Cerby browser extension or not.

Just go to the login page of your application using your web browser and log in by entering your credentials, and the Cerby browser extension will do its magic.

If you don’t have an active session, you’ll be asked to log in to the Cerby browser extension before adding the account, as shown in **Figure 1**.

<img src="../../../.gitbook/assets/Zey9D-HOXwa_VgE0kfRN4_gHd43Ssof9oyiQG5X_AE8-gy8mJXOrKAU8DgYhCd_gQF4j2zy6T5mSjBKhso_XtBHJnFR_DLHex5XY0ZgSUmPOTjB6V4hLGsEY6PMHsT3K5S8dyIR-_7q4Umu_sknPM5s.png" alt="Screenshot of the Sign in to Cerby to save your credentials for this account dialog box, where you are asked to sign in before adding an account to Cerby">

**Figure 1.** **Sign in to Cerby to save your credentials for this account** dialog box

After logging in, the experience is the same: Cerby will prefill the account details, and you just have to click the **Add account** button. Make sure you have the latest version of the Cerby browser extension installed ([Firefox](https://addons.mozilla.org/en-US/firefox/addon/cerby-s-browser-extension/),[ Google Chrome](https://chrome.google.com/webstore/detail/cerbys-browser-extension/clccplmaaeihbagbefjinmclielobnkb),[ Microsoft Edge](https://microsoftedge.microsoft.com/addons/detail/cerbys-browser-extension/bbaiiaogfdgpbapebajffliefkfipoif), and[ Safari](https://apps.apple.com/mx/app/cerby-web-extension/id1581820030?l=en&mt=12)).

* Bulk actions to remove users from a tenant are now supported in the **Members** tab of the tenant details page. Just select the checkbox of the corresponding users in the table, and a selector will be displayed, as shown in **Figure 2**.

<img src="../../../.gitbook/assets/FnZ2Tn737jxrAJdSh7qW_ze54UMyvXdkk224MKLMK1HTDf2rnhRXyX_LO30N9cm0lQhyDAmEC7vfMI-BPSNMWhIrle9oJ1HLGF_FAYaTPRDXSRMzQ1v9uoSg3kBQbavGSisJhJ67mUbHea9dH_fA7xA.png" alt="Screenshot of the Members tab in the tenant details page, where you can remove multiple users from a tenant by selecting their corresponding checkboxes. A selector box is displayed at the bottom for bulk actions">

**Figure 2.** **Members** tab of the tenant details page

* Forget about those annoying messages from applications blocking the automation tasks you trigger for your accounts. We now run our automation engine in the locations you regularly access.

## Fixes

* The issue with **Account Collaborators** being able to remove accounts from collections after a migration via the Password Manager Importer is fixed.
* The issue with saving the information when editing the **Account label in Cerby** field in the account details page is fixed.
* The issue with the in-context alerts being cleared by some applications, like upLynk, is fixed.
