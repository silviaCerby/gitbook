---
description: "This article describes how to install the Cerby mobile app for iOS using an MDM platform and configuration files."
intercom_id: 13575427
---

# Install the Cerby mobile app for iOS via an MDM service and configuration files

With Cerby, you can deploy the Cerby mobile app for iOS across all of your company endpoints using the Jamf Pro Mobile Device Management (MDM) platform and configuration files.

Cerby suggests always using the latest version of the Cerby mobile app to perform this configuration.

To set up the configuration file, payload, deployment, and roll out the installation, you must complete the following steps:

1. Log in to your [Jamf Pro](https://www.jamf.com/login/) account on a browser window.
2. Click the **Devices** <img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/2010864602/0e60bc86d6d9a36c8db01ec298ad/51ed38c3-2242-45b0-a7ef-5e0f08b14918?expires=1769904000&signature=a32a6a01a56577b81eaf7b03590a1a595706b6edc4c0872ff1082ea88f3f34f8&req=diAmFsF4mYdfW%2FMW3Hu4gRYDNC131q%2BQ8RnJrI0BNsxaSyI%2FBtYCEUM6QEqr%0AQA%3D%3D%0A" alt=""> button located at the top of the left navigation drawer.
3. Select the **Mobile Device Apps** <img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/2010866376/7dae877f6d36d3a2730b01798cd7/4d62c722-2fd5-4694-88e5-a710e5cb6672?expires=1769904000&signature=0db7a6874df120fe459f4ca27a7959009a8db34e8c061eb53a21bae118969ae3&req=diAmFsF4m4JYX%2FMW3Hu4gbzA68ZKq4jFbLlOKR87bzzqQbBfBNWMi8qp1qq%2F%0AAw%3D%3D%0A" alt=""> option from the **CONTENT MANAGEMENT** section in the left navigation drawer. The **Mobile Device Apps** page is displayed.
4. Create a new mobile app configuration profile by performing the following actions:
  1. Click the **New** <img src="https://downloads.intercomcdn.com/i/o/pc0ldyqu/2010868089/012395f4e91278d923b32d42c309/a57f31b1-6faf-4755-bdf3-c0386153974e?expires=1769904000&signature=833ca001d9bbb09ad0253ee7f0b89e594624b7c369a409d34416c82bd553f9d1&req=diAmFsF4lYFXUPMW3Hu4gZAJL7J15ckIX9%2FLAt0p%2FUWsQuQN7x4OYbdPotzD%0Aww%3D%3D%0A" alt=""> button. The **General** section of the **Options** tab is displayed on the **Choose an App** page.
  2. Select the **App Store app or apps purchased in volume** option.
  3. Click the **Next** button.
  4. Enter “Cerby” in the search field.
  5. Click the **Next** button.
  6. Click the **Add** button next to the Cerby item.
  7. Select the **App Configuration** option.
5. Enter the **XML Property Lists** to populate the configuration properties by performing the following actions:
  1. Copy the following XML snippet and paste it in the **Property List** field:

              <?xml version="1.0" encoding="UTF-8"?>
      <!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
      <plist version="1.0">
      <dict>
        <key>com.cerby.managed.workspaces</key>
        <string>cerby,okta,....</string> // the maximum ammount of workspaces is five. If more than five workspaces are added, the first five workspaces in the list are used.
      </dict>
      </plist>

6. Click the **Save** button.
7. Activate the **Scope** tab to add your deployment targets. For more information, read the [Scope](https://learn.jamf.com/bundle/jamf-pro-documentation-current/page/Scope.html) official documentation.
8. Click the **Save** button located at the bottom right of the page.

Now you are done.
