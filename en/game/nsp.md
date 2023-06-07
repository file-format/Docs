{
  "date": "2023-06-05",
  "keywords": [
    "nsp file",
    "what is a nsp file",
    "how to open nsp file",
    "what does nsp file contain",
    "what is the format of nsp file",
    "file",
    "nsp file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "NSP File Format - Nintendo Submission Package",
  "description": "Learn about NSP format and APIs that can create and open NSP files.",
  "linktitle": "NSP",
  "menu": {
    "docs": {
      "identifier": "game-nsp",
      "parent": "game"
    }
  },
  "lastmod": "2023-06-05"
}

## What is a NSP file?

NSP file format is primarily associated with Nintendo Switch console. NSP stands for "Nintendo Submission Package." It is file format used by Nintendo for distributing and installing games, updates and DLC (Downloadable Content) on Nintendo Switch system.

NSP files are essentially containers that contain all necessary data and assets for particular game or content. This includes game executable, graphics, audio and any additional files required for game to run. NSP files can be installed on Nintendo Switch through various means including official Nintendo eShop or custom homebrew software.

NSP files are typically encrypted or signed with digital signature to prevent unauthorized distribution or tampering. This ensures that only legitimate copies of games or content can be installed and run on Nintendo Switch console.

## How to open NSP file?

NSP files are designed to be installed and run on Nintendo Switch console, so they cannot be directly opened or executed on computer or other devices without appropriate software or hardware emulation.

However, there are few software tools and utilities available that can handle NSP files for various purposes, such as extracting or manipulating content within files. Here are few examples:

- **Hactool:** Hactool is command-line utility that allows you to view contents of NSP files, extract individual files, or decrypt/encrypt files. It is primarily used for homebrew development or research purposes.
- **NUT:** NUT is graphical user interface (GUI) tool built on top of Hactool. It provides more user-friendly interface for managing NSP files, including the ability to extract files, display metadata and manage updates and DLC.
- **Tinfoil:** Tinfoil is homebrew application for Nintendo Switch that can install NSP files from various sources, including USB, SD card or network. It also has features like title management, firmware updates and more.

## What does NSP file contain?

The NSP file (Nintendo Submission Package) typically contains following components:

- **Game Executable:** The NSP file contains main executable file for game, which is responsible for running game on Nintendo Switch console.
- **Game Assets:** This includes various files such as graphics, audio, videos and other media assets required for game's visuals and audio effects.
- **Metadata:** The NSP file contains metadata information about game such as its title, version number, publisher, release date, supported languages and other relevant details.
- **Game Data:** NSP files also store game data, including saved game files, configuration settings and any additional files required for game to function properly.
- **DLC (Downloadable Content):** If NSP file includes DLC, it will contain additional content that can be added to base game. This can include new levels, characters, items or other features that expand gameplay experience.
- **Updates and Patches:** NSP files may include updates or patches to game, which can provide bug fixes, performance improvements, new features or other enhancements to original game.

## What is the format of NSP file?

The NSP file format used by Nintendo for Nintendo Switch console is a container format. It is essentially a package that holds multiple files and data related to game or content. The NSP file format follows specific structure and organization to ensure compatibility and proper installation on Nintendo Switch system.

The NSP file format is not publicly documented by Nintendo, as it is proprietary and intended for use with their official software and hardware. However, through reverse engineering and analysis by the homebrew community, some details about the NSP format have been discovered.

The structure of NSP file typically includes:

- **Header:** The NSP file begins with a header section that contains information about file such as file format version, size and encryption details (if applicable).
- **Filesystem Metadata:** This section holds metadata related to file system structure within NSP file. It defines directory structure, file names and attributes.
- **Content Files:** The main portion of NSP file contains actual content files, including game executable, assets, data files, DLC and updates. These files are typically compressed or encrypted to prevent unauthorized access or tampering.
- **Ticket:** The NSP file may include a ticket, which is a digital certificate that verifies legitimacy of content and authorizes its installation on Nintendo Switch console.

## References
* [Nintendo Switch](https://en.wikipedia.org/wiki/Nintendo_Switch)
