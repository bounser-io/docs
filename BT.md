# BT tool documentation

## Intro to Bounser CLI Tool (aka "bt")

The bt tool is a wrapper with access control to your other commandline tools like aws. It helps you secure your access without leaving long-lived credentials on your file system.

## Installation
### Prerequisite

Make sure you have the following installed:

* [aws cli](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)


### Installation
Download [bt](https://bounser.io/app/bt_tool) binary. Make sure you choose the right binary for your platform.


### Check installation

Run the following commands to make sure the previous installation was successful:

Check `aws`
```bash
aws --version
```

Check `bt`
```bash
bt version
```

If you see a system popup saying: `"bt" can't be opened because Apple cannot check it for malicious software.`, then go to System Preferences -> Security & Privacy -> General, and click the "Allow" button at the bottom to allow the `bt` binary to execute.

## Usage
### Commands Overview

Here are the available commands of the `bt` tool:

* `bt --help`: shows all the commands and how to use them.
* `bt <command> --help`: describes in detail how to use a specific command.
* `bt verion`: shows the version of the `bt` tool
* `bt run <target-command>`: run a specific target command (e.g., `aws s3 ls`). You can pass in a `--role` flag to specify the role you want to run the target command as (e.g., `bt run --role <role-name> <target-command>`). The `--role` flag takes precedence over the role you assume with `bt assume <role-name>`.
* `bt assume <role-name>`: assume a (default) role so that you don't have to specify a role each time you run `bt run`.
* `bt login`: log in to Bounser to get your token. You need a token to assume a role or run a target command.
* `bt ls`: list all available AWS roles to which you have permission.


## Issues or Questions

If you find an issue with bt tool or have a question, please contact us at onbounser@gmail.com. For live support, click "Contact Us" on the Bounser dashboard [https://bounser.io/app](https://bounser.io/app).
