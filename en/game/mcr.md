{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about MCR file format and APIs that can create and open MCR files.",
  "title": "MCR - Minecraft Region File Format",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mcr"
    }
  },
  "lastmod": "2022-12-14"
}

## What is an MCR file?

The Minecraft MCR file format is a data format used by Minecraft to store terrain chunks of a Minecraft World. It is based on the NBT (Named Binary Tag) format, which was developed by the developers of the popular open-source game engine, Minecraft Forge. MCR file type was introduced in the very beginning and was later replaced by the [MCA file format](/game/mca/).

## MCR File Format

The MCR file format is structured as a series of named binary tags, each of which contains a specific type of data. The top-level tag is the "Level" tag, which contains all of the data for a single game level. Within the Level tag, there are several other named tags that store different types of data, such as the "Data" tag, which stores information about the game world, and the "Entities" and "TileEntities" tags, which store data about the game objects and tile entities in the world, respectively.

## What is inside MCR File Format?

In the Minecraft MCR file format, a region is a 32x32 block area of the game world. The MCR format divides the game world into regions in order to manage the data more efficiently and allow for faster loading and saving of game levels. Each region is stored in a separate file, and the MCR file format uses a system of coordinates to identify the position of each region within the game world. The coordinates of a region are determined by the block coordinates of the lower-left corner of the region. For example, a region with coordinates (-1,0) would be located one region to the left and zero regions down from the origin of the game world.

## MCR File Format Specifications

The MCR file format specifications are publicly available. The specifications for the NBT format, upon which the MCR format is based, are available on the Minecraft Forge website. Additionally, the [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) also has detailed information about the MCR file format, including its structure and the various data types that it supports.

### Compressed Data in MCR Files

The Minecraft MCR file format supports compression. MCR file format is based on the The [NBT format](https://minecraft.fandom.com/wiki/NBT_format) that allows data to be stored in a compressed form. This helps to reduce the size of MCR files and make them more efficient to transfer and store. This is an important feature of the MCR file format, as it allows players to share large Minecraft World terrain data with others.

## References

* [World Editor for Minecraft](https://www.mcedit.net/)
* [About Minecraft](https://www.minecraft.net/)
* [Region File Format](https://minecraft.fandom.com/wiki/Region_file_format)
* [NBT Format](https://minecraft.fandom.com/wiki/NBT_format)
