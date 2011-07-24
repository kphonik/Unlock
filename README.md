Unlock
=========

https://github.com/jridgewell/unlock

## Description

The LaunchDaemon will allow the system to unlock and mount CoreStorage encrypted drives during boot (and before a User logs in). In other words, this allows you to log in as a User whose user directory is on an encrypted secondary disk without any problems.

## Install

- Find the UUID of the CoreStorage Logical Volume you are trying to unlock (run `diskutil cs list` in the terminal and search for the LV UUID; it will be a string like: "497C771B-63FE-461F-AD7B-0BEF9A6BA718").
- Run `bash <(curl -s https://raw.github.com/jridgewell/Unlock/curlinstall/install.sh)` in the terminal
- Enter the UUID when asked.
- Enter the passphrase you used to encrypt the drive when asked.
- Finally, enter your login password when asked.
- Everything should be set up! Restart your computer and log in to test.

## Uninstall

- Run `https://raw.github.com/jridgewell/Unlock/curlinstall/uninstall.sh` in the terminal (you'll be asked for your login password) to remove all traces from the system.

## Limitations

- You're passphrase is stored in plain text. While not the best option, you're boot drive is already encrypted, meaning someone must already have a login password in order to read it.
- You're passphrase __cannot__ contain a '/' (forward slash). 

## Problems?

If have a problem, file a [bug report][issue] or fix it and submit a [pull request][pull].

[issue]: https://github.com/jridgewell/unlock/issues
[pull]: https://github.com/jridgewell/unlock/pulls
