# Authenticate with the Cerby CLI

**Description:** This article describes how you can log in to the Cerby platform with the Cerby CLI to start using its available commands.

To completely wield the capabilities of the **Cerby Command Line Interface
(CLI)** and securely manage your sensitive data, you must complete the
authentication process.

This article describes how to log in to the Cerby platform with the Cerby CLI
via the login command. The login command is the first step in interacting with
Cerby via its commands. This command secures your access to the platform's
resources and initiates a session for executing further commands.

Cerby has the following authentication processes to enable you to log in even
in unusual situations where you can't access a web browser:

  * Log in via a web browser

  * Log in via a bearer token

​​The following sections describe each process.

* * *

# Log in via a web browser

To log in via a web browser and start using the CLI commands, you must
complete the following steps:

  1. Access the location where the Cerby CLI is installed using your command line interface, depending on your OS.

  2. Execute the following command in your OS command line interface:

     * **Windows:** `.\cerby-win.exe login`

     * **Linux:** `./cerby-linux login`

     * **MacOS:** `./cerby-macos login`

You are redirected to your identity provider's login page on a browser page.

  3. Enter your credentials to authenticate via single sign-on (SSO). The **All set!** page is displayed, meaning that the authentication has been successful.

  4. Start using the Cerby commands in your command line. 

To learn more about the available commands in the Cerby CLI, refer to the [Use
the Cerby CLI ](https://help.cerby.com/en/articles/9136331-use-the-cerby-
cli)article.

* * *

# Log in via a bearer token

In cases where opening a browser window is not an option, for example, using a
remote server, you can use the `--bearer-token` flag in the login command as
an alternate way of authentication.

{% hint style="danger" %} **IMPORTANT:** You must never share your bearer
token with other users or store it in a visible place. Your bearer token is
your unique identifier for performing different activities on Cerby, depending
on your role. Be aware that bearer tokens expire after 10 minutes before
renewal. {% endhint %}

To obtain your Cerby bearer token and use it to log in to the Cerby platform,
you must complete the following steps:

  1. Log in to your corresponding [Cerby](https://app.cerby.com/) workspace using the Cerby web app.

  2. Click your user profile at the top-right side of the page. A drop-down list is displayed.

  3. Click the **My Profile** option. The **My Profile** page is displayed with the **General** tab activated.

  4. Activate the **Dev Tools** tab. The **Developer tools** section is displayed. You can see the Copy Bearer Token information in this section with the **Copy token** button at the right.

  5. Click the **Copy token** button. Your bearer token is copied to the clipboard.

  6. Reaccess your command line.

  7. Execute the following command, making sure to paste your bearer token to replace the `{your-bearer-token}` value:
         
         login --bearer-token={your-bearer-token}

  8. Start using the Cerby commands, explained in the [Use the Cerby CLI](https://help.cerby.com/en/articles/9136331-use-the-cerby-cli) article, as needed.

{% hint style="info" %} **NOTE:** Due to the short lifespan (10 minutes) of
the `--bearer-token` option, Cerby CLI supports direct bearer token insertion
into commands. For example: secrets list –bearer-token= {your-bearer-token} {%
endhint %}

