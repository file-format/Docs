{
  "date": "2023-09-27",
  "keywords": [
    "cfg",
    "cfg file",
    "cfg mame configuration file",
    "what is a cfg file",
    "how to open cfg file",
    "file",
    "cfg file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "CFG File Format - MAME Configuration File",
  "description": "Learn about CFG MAME Configuration File format and APIs that can create and open CFG files.",
  "linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
      "parent": "settings"
    }
  },
  "lastmod": "2023-09-27"
}

## What is a CFG file?

CFG file is an XML keyboard configuration file used by MAME arcade video game emulators. It is crucial component for customizing keyboard controls and hotkeys to suit player's preferences. These files store mappings and settings that determine how keyboard interacts with emulator while playing game. By editing this file, users can tailor their gaming experience by assigning specific keyboard keys to actions within game, such as coin insertion, start, movement and various other functions.

## MAME Configuration File

MAME, which stands for **Multiple Arcade Machine Emulator**, is software application that allows you to emulate and play arcade games on your computer. MAME uses configuration files to customize its behavior and settings. These configuration files are typically located in `cfg` folder within your MAME directory. 

Here are main configuration files you may encounter when setting up and configuring MAME:

1. **mame.ini:** This is main configuration file for MAME. It contains global settings that apply to all games. You can find this file in root directory of your MAME installation.

1. **default.cfg:** This file stores default settings for all games that do not have their own configuration files. It is used as fallback for game-specific settings.

1. **game-specific.cfg:** These files are used to store settings for individual games. They are typically named after ROM file for game they correspond to. For example if you have game called "pacman.zip", configuration file for it would be "pacman.cfg."

Here are some common settings you might find in MAME configuration file.

1. **rompath:** Specifies directory where your arcade game ROMs are located.

1. **cfg_directory:** Specifies directory where game-specific configuration files are stored.

1. **nvram_directory:** Specifies directory where non-volatile RAM (NVRAM) files are stored. NVRAM stores high scores and other game-specific data.

1. **artwork_directory:** Specifies directory where artwork files (such as bezels, marquees, and flyers) are stored.

1. **samplepath:** Specifies directory where sample sound files are located.

1. **cheatpath:** Specifies directory where cheat files are located.

You can also configure various other settings such as video and audio options, controls, and input devices. To modify these settings, you can open configuration file in text editor and make necessary changes.

## MAME

MAME, which stands for **"Multiple Arcade Machine Emulator,"** is software application designed to emulate and replicate hardware of vintage arcade machines and arcade game consoles. It allows users to play vast library of classic arcade games on modern computers and other compatible devices. MAME is an open-source project and has become go-to emulator for preserving and enjoying rich history of arcade gaming.

1. **Emulation:** MAME's primary purpose is to accurately emulate hardware of arcade machines, including their central processing units (CPUs), sound chips, graphics chips, and input devices. This level of accuracy ensures that games behave as close to original arcade experience as possible.

1. **Compatibility:** MAME supports wide range of arcade game ROMs, making it one of most comprehensive arcade emulators available. It can run games from various arcade platforms including classic games from '70s, '80s, '90s, and even some more recent arcade titles.

1. **Preservation:** One of MAME's primary missions is to preserve history of arcade gaming. By accurately emulating arcade hardware, MAME helps prevent loss of classic games and ensures that future generations can experience them as they were originally intended.

1. **Front-Ends:** Many users utilize front-end applications that provide graphical interface to manage and launch games through MAME. These front-ends make it easier to navigate MAME's extensive library of games.

## How to open CFG file?

Programs that open or reference CFG files

- MAME (Free) (Windows)
- ExtraMAME (Trial)
- MacMAME (MAC)

## Other CFG files

Here are other file types that use the **.cfg** file extension.

**Settings**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Game**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**System & Misc**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## References
* [MAME](https://en.wikipedia.org/wiki/MAME)
