# hassctl <a href="https://flattr.com/submit/auto?fid=o7dr10&url=https%3A%2F%2Fgithub.com%2Fdale3h%2Fhassctl" target="_blank"><img src="https://button.flattr.com/flattr-badge-large.png" alt="Flattr this" title="Flattr this" border="0"></a>

A command line utility to simplify the management of Home Assistant

## Compatibility

This utility has been tested on the following platforms:

* Raspberry Pi
  * Manual install (with `systemd` service)
  * AIO/One-Step Installer
  * HASSbian Image
* Ubuntu Server 16.04.1
  * Manual install (with `systemd` service)

## Installation

`sudo curl -o /usr/local/bin/hassctl https://raw.githubusercontent.com/dale3h/hassctl/master/hassctl && sudo chmod +x /usr/local/bin/hassctl`

## Updating Home Assistant

The safest way to update Home Assistant in a production environment is to run:

`hassctl update-hass && hassctl config && hassctl restart`

This set of commands will update Home Assistant, run a configuration check, and then restart.
If the update fails, the configuration check will not run.
If the configuration check fails, Home Assistant will not be restarted.

If you would like to install a specific version of Home Assistant, run:

`hassctl update-hass 0.43.1` (replace `0.43.1` with the version you wish to install)

## Updating `hassctl`

To update `hassctl` to the latest stable version, run `hassctl update-hassctl` or `hassctl update-hassctl master`
To update `hassctl` to the latest dev version, run `hassctl update-hassctl dev`

## Usage

You can update Home Assistant using:

**`hassctl update-hass [version]`**

You can control Home Assistant using:

**`hassctl start`**

Start the Home Assistant service

**`hassctl stop`**

Stop the Home Assistant service

**`hassctl restart`**

Restart the Home Assistance service

**`hassctl kill`**

Send a SIGKILL (-9) signal to the Home Assistant service

**`hassctl log`**

Follow the Home Assistant logs (errors are highlighted)

**`hassctl error`**

Follow the Home Assistant error logs

**`hassctl config`**

Run the configuration check script

**`hassctl update-hassctl [branch]`**

Update `hassctl` to the latest version

## Configuration Examples

The configuration file is located at `/etc/hassctl.conf`.

### HASSbian

```
HASSCTL_BRANCH=master

VIRTUAL_ENV=/srv/homeassistant
PIP_EXEC=$VIRTUAL_ENV/bin/pip3
HASS_EXEC=$VIRTUAL_ENV/bin/hass

HASS_CONFIG=/home/homeassistant/.homeassistant
HASS_USER=homeassistant
HASS_SERVICE=home-assistant.service
```

### Current AIO Installer

```
HASSCTL_BRANCH=master

VIRTUAL_ENV=/srv/homeassistant/homeassistant_venv
PIP_EXEC=$VIRTUAL_ENV/bin/pip3
HASS_EXEC=$VIRTUAL_ENV/bin/hass

HASS_CONFIG=/home/homeassistant/.homeassistant
HASS_USER=homeassistant
HASS_SERVICE=home-assistant.service
```

### Pre-December 2016 AIO Installer

```
HASSCTL_BRANCH=master

VIRTUAL_ENV=/srv/hass/hass_venv
PIP_EXEC=$VIRTUAL_ENV/bin/pip3
HASS_EXEC=$VIRTUAL_ENV/bin/hass

HASS_CONFIG=/home/hass/.homeassistant
HASS_USER=hass
HASS_SERVICE=home-assistant.service
```
