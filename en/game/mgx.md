{
  "date": "2021-09-08",
  "keywords": [
    "mgx file",
    "mgx file format",
    "what is a mgx file",
    "file",
    "mgx example",
    "mgx file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about Age of Empires 2 Expansion Replay MGX file format and APIs that can create and open MGX files.",
  "title": "MGX - Age of Empires 2 Expansion Replay",
  "linktitle": "MGX",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mgx"
    }
  },
  "lastmod": "2021-09-08"
}

## What is an MGX file?

A file with .mgx extension is a recorded file for Age of Empires II: The Conquerors game that can be replayed within the Age of Empires II program. It contains complete recording of the campaign played by the user. It can be loaded and played back within in the Age of Empires II program. Once replayed, the game shows all the events and scenarios that the user planned for the campaign and played.

## MGX File Format - More Information

The internal file format of the MGX file have been worked out and available as partially validated information on [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format). The specifications outline the details in the following sections.

### Structure Definitions

The structure definitions of GPX file format are believed to be based on the [BinData Ruby Gem declarations](https://github.com/dmendel/bindata/wiki) that provide a way to read and write structured binary data. This lets the programmer specify the format of the binary data which is then read and write by BinData.

### MGX Messaging

The MGX messaging is based on two type of messages.

 * GAMESTART - specifies the game start commands and is not validated to date
 * CHAT - describes the in-game chat messages. Both, players and the game itself (Gaia) can emit in-game messages.

### GAMEPLAY ACTIONS

There are several [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) that have been retrieved and whose details are available.

## References

* [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format)
