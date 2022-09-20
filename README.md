# SNES for Analogue Pocket

Ported from the original core developed by [srg320](https://github.com/srg320) ([Patreon](https://www.patreon.com/srg320)). Latest upstream available at https://github.com/MiSTer-devel/SNES_MiSTer.

Please report any issues encountered to this repo. Most likely any problems are a result of my port, not the original core. Issues will be upstreamed as necessary.

## Usage

**NOTE:** ROM files must not contain a SMC header. If a ROM isn't loading and you think it should, check if it has a header with a tool like [Advanced SNES ROM Utility](https://www.romhacking.net/utilities/1638/) and remove it if so.

ROMs should be placed in `/Assets/snes/common`

PAL ROMs should boot, but there may be timing issues as the core currently doesn't properly support PAL (proper support coming soon).

## Features

### Dock Support

Core supports four players/controllers via the Analogue Dock. To enable four player mode, turn on "Use Multitap" setting.

### Expansion Chips

The currently supported expansion chips are SA-1 (Super Mario RPG), Super FX (GSU-1/2; Star Fox), DSP (Super Mario Kart), and CX4 (Mega Man X 2). Additional chip support will come in the future once several new firmware features are released.

**NOTE:** The SDD1 chip was dropped in release 0.2.0 due to sizing and popularity issues. Support will resume in a future release.

### Video Modes

The Analogue Pocket framework doesn't currently allow for customizing video modes directly, so if you dislike the default 8:7 aspect ratio/want to change to 4:3, you can change it by modifying `Cores/agg23.SNES/video.json` and rearranging the config objects.

Proper PAL support also requires editing these files to have an expanded vertical pixel height.