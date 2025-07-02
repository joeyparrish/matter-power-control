# Matter Power Strip Tool

This is a simple tool based on [chip-tool][] which simplifies the command line
setup and control of Matter power strips.

[chip-tool]: https://project-chip.github.io/connectedhomeip-doc/development_controllers/chip-tool/chip_tool_guide.html


## Installation

```
sudo snap install chip-tool
git clone https://github.com/joeyparrish/matter-power-control
cd matter-power-control
python3 -m pip install -r requirements.txt
sudo cp matter-power-control /usr/local/bin/
```


## Usage

See `matter-power-control --help` for usage.
