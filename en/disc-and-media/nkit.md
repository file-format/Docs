{
  "date" : "2022-04-01",
  "keywords" : [ "nkit file", "nkit file format", "what is an nkit file", "file", "nkit example", "nkit file extension","extension", "format", "nkit footer", "file format of nkit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
   "toc" : true,
  "description" : "Learn about NKIT file format and APIs that can create and open NKIT files.",
  "title" : "NKIT - Disk Image File Format",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
    }
  },
  "lastmod" : "2022-04-01"
}

## What is an NKIT file?

An NKIT file is a disk image of data extracted from NintendoWii and GameCube games. NKIT is for Nintendo Toolkit format. The resultant compression [ISO](/compression/iso/) file utilizes the main data of these games to be run with emulator programs such as Dolphin, Swiss, and Nintendont. NKit comes in raw (iso) adn compressed (gcz) file formats which were both designed keeping in view playability and size.

## NKIT File Format

NKit file format is a non-lossy format and is used for shrinking and restoring Nintendo Wii and GameCube images. The formats are available in ISO and GCZ file formats for each of GameCube and Wii games.

|System	|Format	|Hardware Supported	|Dolphin Supported	|Restorable 1:1	|Notes|
---|---|---|---|---|---|
|GameCube|	nkit.iso|	Yes	|Yes|	Yes	|Same as compacted GameCube iso|
|GameCube|	nkit.gcz|	No|	Yes|	Yes	|GCZ is Dolphin's own block seekable compression format|
|Wii|	nkit.iso|	No	Yes|	Yes|	RVT-H format only playable in Dolphin|
|Wii|	nkit.gcz|	No	Yes|	Yes|	RVT-H in GCZ playable in Dolphin only|

### NKIT Header

The NKIT file format header is as follow.

|Offset	|Length	|Name|
---|---|---|
|0x200	|0x4	|NKit Header 'NKIT'|
|0x204	|0x4	|NKit Version ' v01'|
|0x208	|0x4	|Source image original CRC32|
|0x20C	|0x4	|NKit CRC - makes the NKit file CRC32 equal the source CRC at 0x208 (at 0x4 in GCZ)|
|0x210	|0x4	|Source image length|
|0x214	|0x4	|Forced Junk ID (When Disc ID differs - rare - GameCube only)|
|0x218	|0x4	|Wii Update partition CRC32 if removed when converting|

## References ##

* [NKIT File Format - by gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)
