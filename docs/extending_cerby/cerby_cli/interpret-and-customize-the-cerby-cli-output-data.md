---
description: This article describes how the Cerby CLI outputs the results of your commands and how to customize this output.
intercom_id: 9136341
---

# Interpret and customize the Cerby CLI output data

When retrieving your accounts and secrets, the Cerby CLI outputs data in JSON format, providing a structured and machine-readable representation of the information. With the JSON format, you can quickly parse and manipulate the data using any JSON parsing library or tool in your preferred programming language or scripting environment.

This article contains the following aspects of the Cerby CLI output data:

* Default output
* Output customization
* Output parsing and processing
* Output error codes
* Output help commands

The following sections describe each aspect of the output.

* * *

## Default output

By default, when retrieving information about accounts or secrets, the output reflects the first 20 items per page in the response. The specific structure of the JSON response varies depending on the invoked command and any additional parameters used.

* * *

## Output customization

You can customize the output of some of the Cerby CLI commands by adding the following flags to the secrets and accounts list commands:

* **\--page-size** (number): Specifies the number of items displayed per page. 20 items are shown by default per page, but you can limit the results to a desired number.
* **\--start-index** (number): Selects the starting index within the response array from which results are displayed. This is useful for paginating through large datasets.

For example, when you execute the following command:

    secrets list --page-size=5 --start-index=2

The previous command retrieves a list of accounts, displaying only 10 entries starting from the 21st item (index 20). Additionally, it includes the `--totalResults` flag to show the total number of available accounts.

* * *

## Output parsing and processing

After receiving the JSON output, you can use any tool or library to parse and process the output.

* * *

## Output error codes

The following are the error codes per command you might encounter while using the Ceby CLI:

* `register`
    * **`Unauthorized`:** Run the login command or provide a valid token using the --bearer-token option
    * **`Error`:** The device already exists
* `sync`
    * **`Unauthorized`:** Run the login command or provide a valid token using the --bearer-token option
    * **`RemoteDeviceNotFoundError`** : Run the register command to re-onboard your device
* `secrets`
    * **`Unauthorized`:** Run the login command or provide a valid token using the --bearer-token option
    * **`RemoteDeviceNotFoundError`:** Run the register command to re-onboard your device
    * **`VaultNotFoundInDeviceError`:** The vault was not found
    * **`Forbidden`: **You don't have permission to access this resource
* `accounts`
    * **`Unauthorized`:** Run the login command or provide a valid token using the --bearer-token option
    * **`Not found`:** Verify the --id of the resource you're trying to access.
    * **`VaultNotFoundInDeviceError`:** The vault was not found
​**NOTE:** The previous error is returned when you're trying to read a secret, and you have a registered/approved device, but you haven't run sync yet. It is solved by running the `sync` command

* * *

## Output help commands

The Cerby CLI offers the following guidelines that can help you understand how to use the commands effectively:

* Summarize the available command options
* Get help with a command
* Get the version of the Cerby CLI
* Enable the debugging mode

The following sections explain each command in detail.

### Summarize the available command options

To get a summary of the available command options and the basic usage guidelines, you can type the command name without any arguments. You can use this option as a quick way to remember the command's core functionality.

### Get help with a command

To get the information on the arguments and flags for a particular command, you can append the `--help` flag to the commands.

### Get the version of the Cerby CLI

To get the number version of the Cerby CLI you have installed in your Operating System, run the `--version` flag.

### Enable the debugging mode

To deeply understand the underlying process behind executing a command, such as for debugging purposes, you can use the `--verbose` flag. Appending `--verbose` to a command instructs the CLI to generate more detailed output, often including:

* Additional logs and messages detailing the command's execution steps.
* Debugging information that can help troubleshoot unexpected behavior.
