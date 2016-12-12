# hassctl

A command line utility to simplify the management of Home Assistant

## Compatibility

This utility has been tested on the following platforms:

* Raspberry Pi
  * Manual install (with `systemd` service)
  * AIO/One-Step Installer
  * Hassbian Image
* Ubuntu Server 16.04.1
  * Manual install (with `systemd` service)

## Installation

`sudo curl -o /usr/local/bin/hassctl https://raw.githubusercontent.com/dale3h/hassctl/master/hassctl && sudo chmod +x /usr/local/bin/hassctl`

## Updating

To update `hassctl` to the latest version, simply run `hassctl update`

## Usage

You can control Home Assistant using:

**`hassctl start`**

Start the Home Assistant service

**`hassctl stop`**

Stop the Home Assistant service

**`hassctl restart`**

Restart the Home Assistance service

**`hassctl kill`**

Send a SIGKILL (-9) signal to the Home Assistant service

**`hassctl log -f`**

Follow the Home Assistant logs (errors are highlighted)

**`hassctl error`**

Follow the Home Assistant error logs

**`hassctl config`**

Run the config validator

**`hassctl update`**

Update `hassctl` to the latest version
