{
  "date": "2021-09-08",
  "keywords": [
    "rel file",
    "rel file format",
    "what is a rel file",
    "file",
    "rel example",
    "rel file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about REL file format and APIs that can create and open REL files.",
  "title": "REL - Relocatable Module File",
  "linktitle": "REL",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-rel"
    }
  },
  "lastmod": "2021-09-08"
}

## What is a REL file?
A file with .rel extension can be used for several kind of purposes. Therefore, in terms of game classification it is known as a relocatable module file used by some Nintendo Wii games, such as Brawl, Super Smash Bros and Mario Kart Wii. It comprises the gameplay data, including character models and stages. REL files perform similarly to the .DLL files used by the Microsoft Windows.

## REL file format
In a REL file format, the file is divided into several sections, grouped by like access, e.g. read only data in one section, all executable code is placed in another, etc. The file starts with a header section, followed by the:
- Table containing section info.
- The section data.
- Relocation information.

### File header
The file starts with a header of up to 0x4C bytes:
| Offset | Size | Field Name | Description |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Arbitrary identification number. Must be unique amongst all RELs used by a game. Must not be 0. |
| 0x04 | 4 | next | Pointer to next module, filled at runtime. |
| 0x08 | 4 | prev | Pointer to previous module, filled at runtime. |
| 0x0c | 4 | numSections | Number of sections in the file. |
| 0x10 | 4 | sectionInfoOffset | Offset to the start of the section table. |
| 0x14 | 4 | nameOffset | Offset to ASCII string containing name of module. May be NULL. Relative to start of REL file. |
| 0x18 | 4 | nameSize | Size of the module name in bytes. |
| 0x1c | 4 | version | Version number of the REL file format. |
| 0x20 | 4 | bssSize | Size of the '.bss' section. |
| 0x24 | 4 | relOffset | Offset to the relocation table. |
| 0x28 | 4 | impOffset | Offset to imp table. |
| 0x2c | 4 | impSize | Size of imp table in bytes. |
| 0x30 | 1 | prologSection | Index into section table which prolog is relative to. Skip if this field is 0. |
| 0x31 | 1 | epilogSection | Index into section table which epilog is relative to. Skip if this field is 0. |
| 0x32 | 1 | unresolvedSection | Index into section table which unresolved is relative to. Skip if this field is 0. |
| 0x33 | 1 | bssSection | Index into section table which bss is relative to. Filled at runtime! |
| 0x34 | 4 | prolog | Offset into specified section of the _prolog function. |
| 0x38 | 4 | epilog | Offset into specified section of the _epilog function. |
| 0x3c | 4 | unresolved | Offset into specified section of the _unresolved function. |
| 0x40 | 4 | align | Version ≥ 2 only. Alignment constraint on all sections, expressed as power of 2. |
| 0x44 | 4 | bssAlign | Version ≥ 2 only. Alignment constraint on all '.bss' section, expressed as power of 2. |
| 0x48 | 4 | fixSize | Version ≥ 3 only. If REL is linked with OSLinkFixed (instead of OSLink), the space after this address can be used for other purposes (like BSS). |

### Section Info Table
The section info table contains of **numSections** entries each 0x8 bytes long:
| Offset | Size | Description |
-------|------------|-------------|
| 0x0 | 30 bits | Offset from the beginning of the REL to the section. If this is zero, the section is an uninitialized section (i.e. .bss). |
| 0x3.6 | 1 bit | Unknown. |
| 0x3.7 | 1 bit | Executable flag; if this is 1 the section is executable. |
| 0x4 | 4 | Length in bytes of the section. If this is zero, this entry is skipped. |
| 0x8 | Next entry | Next entry |

### Relocation Data
The relocation data is one or more lists of 0x8 byte structures. The end of each list is marked by the special type code 203:
| Offset | Name | Size | Description |
-------|------------|------------|-----|
| 0x0 | offset | 2 | Offset in bytes from the previous relocation to this one. If this is the first relocation in the section, this is relative to the section start. |
| 0x2 | type | 1 | The relocation type. Described below. |
| 0x3 | section | 1 | The section of the symbol to relocate against. For the special relocation type 202, this is instead the number of the section in this file which the following relocation entries apply to. |
| 0x4 | addend | 4 | Offset in bytes of the symbol to relocate against, relative to the start of its section. This is an absolute address instead for relocations against main.dol. |
| 0x8 | Next entry | Next entry | Next entry |


 



## References 

* [Relocatable Object Module Format](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)

