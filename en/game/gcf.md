{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about GCF file format and APIs that can create and open GCF files.",
  "title" : "GCF File - Nadeo Game GCF Format",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf",
      "parent" : "game"
    }
  },
  "lastmod" : "2023-01-19"
}

## What is a GCF file?

A .gcf file is a game cache file used by the Steam gaming platform. It contains game data such as textures, models, and other files that are used by the game. These files are stored on the user's computer and are used to reduce the amount of data that needs to be downloaded when updating or installing a game. The .gcf files can also be used to create backups of a game's installation or to transfer a game between computers.

GCF files can be read and write by the Open Source C++ programming Library, [HLLib]((https://developer.valvesoftware.com/wiki/HLLib)).

## GCF File Format

GCF files are saved to disc as binary files. GCF was originally used as an acronym for Grid Cache File (Steam's early code name was Grid), but later on it was taken as Game Cache File. A GCF file is an archive file that stores Steam games. All official content is downloaded as GCF files. GCF files can also be shared between games.

NOTE: GCF is the predecessor of [VPK file format](/game/vpk/).
## References

* [Valve Software](https://www.valvesoftware.com/en/)
* [GCF File Format](https://developer.valvesoftware.com/wiki/GCF)
* [HLLib - Open Source C++ Programming Library for Reading GCF Files](https://developer.valvesoftware.com/wiki/HLLib)
