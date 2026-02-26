---
description: "This article describes how you can obtain the executable files for Windows, MacOS, and Linux to install the Cerby CLI."
intercom_id: 9118688
---

# Install the Cerby CLI

The **Cerby Command Line Interface (CLI)** executables are available for Windows, MacOS, and Linux through the **Dev Tools** in your Cerby workspace.

{% hint style="danger" %}


**IMPORTANT:** Cerby strongly recommends verifying the authenticity of any downloaded file by using only the executable files downloaded from the Cerby platform. With this verification, you ensure the file originates from a trusted source.


{% endhint %}

To install the Cerby CLI executable, you must complete the following steps:

1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace.
2. Click the user profile menu located at the top right of the dashboard. A drop-down menu is displayed.
3. Select the **My Profile** option. The **My Profile** page is displayed.
4. Activate the **Dev Tools** tab.
5. Click the **Download files** button that appears in the **Download the Cerby CLI** card. The **Download file** dialog box is displayed.
6. Select the executable file corresponding to your operating system. The executable file is downloaded to your system with the following names:

   * **Windows:** Cerby CLI Installer.msi
   * **Linux:** cerby-linux
   * **MacOS:** cerby-macos

7. Install the Cerby CLI following the instructions below corresponding to your OS:

   * Windows

     1. Access the folder where the Cerby CLI installation file was downloaded.
     2. Double-click the installation file. The **User Account Control** dialog box is displayed, asking if you want the CLI app to make changes to your device.
     3. Select the **Yes** button. A dialog box with the progress of the installation is displayed.
     4. Open your command line interface, such as Windows PowerShell.
     5. Access the installation location of the Cerby CLI by executing the following command:

                      cd ‘C:\Program Files (x86)\Cerby\Cli\’

     6. Verify that Cerby CLI is running correctly by executing the following command:

                      .\cerby-win.exe --version

The response must be the Cerby CLI version number.

* Linux

  1. Open your terminal.
  2. Access the folder where the Cerby CLI installation file was downloaded.
  3. Grant the execute permission to the installation file by executing the following command:

                   chmod +x cerby-linux

  4. Access the Cerby CLI prompt by executing the following command:

                   ./cerby-linux --version

The response must be the Cerby CLI version number.

* MacOS

  1. Open your terminal.
  2. Access the folder where the Cerby CLI installation file was downloaded.
  3. Grant the execute permission to the installation file by executing the following command:

                   xattr -cr cerby-macos && chmod +x cerby-macos

  4. Access the Cerby CLI prompt by executing the following command:

                   ./cerby-macos --version

The response must be the Cerby CLI version number.

8. (Optional) Adjust your environment path to enable direct execution from the command line. Refer to your OS documentation for specific instructions.
