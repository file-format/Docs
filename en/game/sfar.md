{
  "date": "2021-10-20",
  "keywords": [
    "sfar file",
    "sfar file format",
    "what is an sfar file",
    "file",
    "sfar example",
    "Mass Effect 3 DLC File extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about Mass Effect 3 SFAR file format and APIs that can create and open SFAR files.",
  "title": "SFAR - Mass Effect 3 DLC File",
  "linktitle": "SFAR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-sfar"
    }
  },
  "lastmod": "2021-10-20"
}

## What is an SFAR file?

A file with .sfar extension is a game data file used by Mass Effect 3 to store its DLC (downloadable content) in a compressed, proprietary archive. Mass Effect 3 is a game created by Electronic Arts, a premier game development company. The DLC content stored in an SFAR file is used to extend the game with additional content and features.

## SFAR File Format - More Information

SFAR files are stored/saved as compressed archive files in binary file format. These use both LZX and LZMA compression algorithms for compressing the contents. SFAR files can be opened using the DLC Editor that comes packaged with ME3 Explorer. In addition to SFAR, DLC Editor can extract other game files such as [PCC](/game/pcc/).

## SFAR File Format Specifications

An SFAR file is divided into the following four main chunks.

### SFAR Header

SFF Header contains information about the various chunks that comprise the file.

### SFAR File Table

The SFAR File Table contains a list of file entries where each entry is 30 bytes long.

### Block-Size Table

The Block-Size contains multiple entries, where each entry is 2 byes long. This value specifies the Block-Size corresponding to an entry in the File Table.

### Blocks

Block chunks in an SFAR file contains the data inside the SFAR file.

## References

 * [DLC SFAR File Format - Research](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)
