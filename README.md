# hassctl

A command line utility to simplify the management of Home Assistant

## Installation

`sudo wget https://raw.githubusercontent.com/dale3h/hassctl/master/hassctl -O /usr/local/bin/hassctl && sudo chmod +x /usr/local/bin/hassctl`

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
