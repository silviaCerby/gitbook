# Set up the Cerby CLI as a trusted device

**Description:** This article describes how to set up a trusted device using the Cerby CLI commands.

As explained in the [How Cerby protects your data with cloud and local
encryption](https://help.cerby.com/en/articles/8376548-how-cerby-protects-
your-data-with-cloud-and-local-encryption) article, Cerby stores your
sensitive data in encrypted cloud vaults. If your organization leverages the
local encryption scheme, vault data encryption keys (DEKs) are stored
exclusively on trusted devices registered by Cerby's servers, and decryption
happens decentralized on such devices.

Therefore, similar to using the other [Cerby client
apps](https://help.cerby.com/en/articles/8142370-how-to-set-up-and-manage-
your-trusted-devices#h_845ba67337), you must set up the Cerby CLI as a trusted
device using its commands to strengthen the security of your items. This
process is required to access encrypted attributes of items stored in local
vaults.

To set up the Cerby CLI as a trusted device using its commands, you must
complete the following steps:

  1. Execute the following command to verify if the device has already been registered:
         
         cerby-mac{os} register --status

     * If the device is correctly registered, then the following is output:
           
           Device is registered and approved

     * If the registry verification returns the `RemoteDeviceNotFoundError` error (or other), you must register the device correctly. Go to step 2 to continue registering the device. 

  2. Execute the following command to request a verification code to the email you have registered in Cerby:
         
         cerby-mac{os} register --request-code

  3. Copy the verification code from the email Cerby sent you.

**IMPORTANT:** The verification code expires in 5 minutes.

  4. Execute the following command to verify the code:
         
         cerby-mac{os} register --verification-code {code_from_your_email}

**NOTE:** You might encounter the "`Error: Device already exists`" error while
executing this command if your machine has been previously verified. In that
case, ignore the error and continue to step 4.

  5. Execute the following command to sync your account and secret data:
         
         cerby-mac{os} sync

{% hint style="info" %} **NOTES:** * Read the[ Sync your
data](https://help.cerby.com/en/articles/9136331-use-the-cerby-
cli#h_9e0001613c) command documentation to learn more about how Cerby syncs
data to your local machine. * Downloading your data might take some minutes,
especially if it's the first time you execute the sync. The time also depends
on the volume of data you have. {% endhint %}

