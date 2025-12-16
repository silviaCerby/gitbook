---
intercom_id: 9768866
description: >-
  This article describes how to integrate Cerby with Devolutions to view and
  manage your accounts using Remote Desktop Manager (RDM) on MacOS.
---

# Extend your Cerby accounts to Devolutions RDM

Cerby provides a seamless and secure solution for extending your accounts to the Devolutions Remote Desktop Manager (RDM) dashboard.

With Cerby’s RDM integration, you can manage your Cerby accounts directly within RDM while maintaining Cerby’s security practices. This integration is achieved using the Cerby CLI, which must be installed and running locally on your MacOS system. The CLI ensures that Cerby can verify your device's trusted session, retrieve your locally encrypted accounts, and securely decrypt them.

RDM is a platform that centralizes and simplifies the management of remote connections, credentials, and sensitive information because it supports a wide range of connection types, including RDP, VPN, SSH, and more. After integrating RDM with Cerby, you can sync your Cerby accounts through RDM entries and manage them through the RDM dashboard.

After you have extended a Cerby account to RDM, you can perform the following actions:

* View password
* Copy username and password
* Copy account details
* Log in to your account

This document describes how to integrate Cerby with Devolutions RDM.

***

## Requirements

The following are the requirements to integrate RDM with Cerby:

1. An active Cerby account
2. The Devolutions [Remote Desktop Manager](https://devolutions.net/remote-desktop-manager/home/download/) package for MacOs installed with an active account
3. The Cerby CLI installed on your MacOs system. Read the [Install the Cerby CLI on MacOs](https://docs.google.com/document/d/153dIEJ3EH0O6PiBX6ClmN0VGa3nTUBiMYRg500FMuOE/edit#heading=h.tqg9tqd9r86g) section to learn more about the installation.

***

## Install the Cerby CLI on MacOs

To install the Cerby CLI executable, you must complete the following steps:

1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
2. Click the user profile menu located at the top right of the dashboard. A drop-down menu is displayed.
3. Select the **My Profile** option. The **My Profile** page is displayed.
4. Activate the**Dev Tools** tab.
5. Click the **Download** files button that appears in the **Download the Cerby CLI** card. The**Download file** window opens.
6. Select the executable file corresponding to MacOs. The executable file is downloaded to your system with the following name: `cerby-macos`.
7. Move the installation file to the `/usr/local/bin/` folder:
   1. Open your terminal.
   2. Access the folder where the Cerby CLI installation file was downloaded using the `cd` command.
   3. Move the `cerby-macos` file to the `/usr/local/bin/` folder using the following command: `sudo mv cerby-macos /usr/local/bin/` **IMPORTANT:** Cerby CLI must remain in this location at all times for the extended accounts to function correctly.
8. Install the Cerby CLI using the terminal:
   1. Access the `/usr/local/bin/` folder using the command: `cd /usr/local/bin/`
   2. Grant the execute permission to the installation file using the command: `xattr -cr cerby-macos && chmod +x cerby-macos`
   3. Access the Cerby CLI prompt using the command: `./cerby-macos --version` The response must be the Cerby CLI version number.

**IMPORTANT:** If you receive a warning that your MacOs does not trust the application, complete the following steps:

1. Access the MacOs **Settings**.
2. Navigate to the **Privacy & Security** option in the left panel.
3. Scroll to the bottom and locate the **Cerby MacOS** option.
4. Select the **Allow** option to allow the application to run on your MacOs.

***

## **NOTE:** To learn more about the Cerby CLI, refer to the [Cerby CLI](https://help.cerby.com/en/collections/9016503-cerby-cli) documentation.

***

## Extend a Cerby account to your RDM dashboard

To create a new entry in Devolutions to extend your account, you must complete the following steps using RDM:

1. Open the Devolutions RDM dashboard.
2. Click the **New entry** button in the **Edit** section of the **HOME** pane. A window with the category of entry types opens.
3. Search for “Cerby” in the search field at the top of the window.
4.  Select the **Cerby**

    <figure><img src="../../.gitbook/assets/unnamed_10.png" alt=""><figcaption></figcaption></figure>

    option. The **Credentials** window opens.
5. Select the **Cerby** option in the left panel under the **General** folder. The **Workspace** and **Account** fields are displayed in the main pane.
6. Log in to Cerby by completing the following steps:
   1. Enter your Cerby workspace URL in the **Workspace** field using the following format: `https://<workspace-name>.cerby.com`.
   2.  Click the three-dots (

       <figure><img src="../../.gitbook/assets/unnamed_11.png" alt=""><figcaption></figcaption></figure>

       ) icon on the right side of the **Account** field. The Cerby login page is displayed.
   3. Log in to Cerby using your credentials. RDM verifies that the current device is trusted by Cerby, and the **Cerby** window opens with the list of all your accounts.
7. Select the Cerby account you want to retrieve by double-clicking it.
8. Click the**Ok** button. The window closes, and the account name is displayed in the **Account** field. **TIP:** You can use the search function to find and select the account entry you want to retrieve from Cerby.
9. Select the **General** option in the left panel.
10. Enter the name you want your Cerby account to have within the RDM dashboard in the **Name** field.
11. (Optional) Select the RDM folder where you want to locate the Cerby account: 1. Click the three-dots (

    <figure><img src="../../.gitbook/assets/unnamed_12.png" alt=""><figcaption></figcaption></figure>

    ) icon on the right side of the **Folder** field. The **Folder** window opens. 2. Select the folder where you want to locate the Cerby account. 3. Click the **Select** button. The window closes, and the folder name is displayed in the **Folder** field.
12. Click the **Create** button. The Cerby account is displayed on the RDM dashboard with the name you entered in step 10.

## **NOTE:** You won’t see the account name you see in Cerby because you assigned it a Devolutions name. The account keeps its name in Cerby.
