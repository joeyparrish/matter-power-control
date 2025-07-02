# Matter Power Strip Tool

This is a simple tool based on [chip-tool][] which simplifies the command line
setup and control of Matter power strips.

[chip-tool]: https://project-chip.github.io/connectedhomeip-doc/development_controllers/chip-tool/chip_tool_guide.html


## Requirements

Requires python3, a bluetooth adapter, and chip-tool.

Only tested on Ubuntu Linux, but will probably run elsewhere.


## Installation (Ubuntu)

```
sudo apt install bluez snap
sudo snap install chip-tool

sudo systemctl enable bluetooth
sudo systemctl start bluetooth

git clone https://github.com/joeyparrish/matter-power-control
cd matter-power-control
sudo python3 -m pip install -r requirements.txt

sudo cp matter-power-control /usr/local/bin/
```


## Usage

See `matter-power-control --help` for usage.


## Setup

Setup requires a photo of the QR code on the back of the device.  The device
will typically only beacon for setup frequently right after it boots, so if
setup times out, try rebooting the device and running setup again.

Note that chip-tool stores configurations in a user-specific directory, so any
automation should use the same user as the setup process.


## Factory Reset

If you need to move a device to another network or controller, you should clear
its programming.  You can often factory reset a Matter power strip by holding
down a reset or power button until an LED starts blinking.
