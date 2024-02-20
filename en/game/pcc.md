{
  "date": "2021-09-08",
  "keywords": [
    "pcc file",
    "pcc file format",
    "what is a pcc file",
    "file",
    "pcc example",
    "pcc file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about Mass Effect PCC file format and APIs that can create and open PCC files.",
  "title": "PCC - Mass Effect Package File",
  "linktitle": "PCC",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-pcc"
    }
  },
  "lastmod": "2021-09-08"
}

## What is a PCC file?

A file with .pcc is a [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) file that contains game data to modify game content such as models, textures and rooms. Mass Effect 2 and 3 are first shooter games based on the Unreal Engine 3 gaming engine. The game was initially developed by [Bioware](https://www.bioware.com/about/) who kept the majority of game resources in their proprietary PCC file format. Bioware was acquired by Electronic Arts, a leading global interactive entertainment publisher.

## PCC File Format - More Information

PCC files contain compressed and/or uncompressed structures that contribute to the overall file organization.

### Compressed PCC Structure

A compressed PCC file comprises of tables and data that is segmented into chunks. Each chunk contains a variable number of compressed blocks.

 * `Chunks Header` - A 16 bytes common header, containing information about the chunks.
 * `Chunk Header` - A 16 byte header containing information about the raw compressed data contained in the block form.

### UnCompressed PCC Structure

UnCompressed PCC files are divided into following five parts.

 * `Header` - contains basic information about the structure of the PCC file.
 * `Name Table` - contains name found inside the package including import classes, exports, and export properties.
 * `Import Table` - contains all classes and objects imported by the PCC.
 * `Export Table` - contains all objects stored in the package. Each export can vary in size.

## References

 * [Me3Explorer - PCC File Format](https://me3explorer.fandom.com/wiki/PCC_File_Format)
 * [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3)
 * [Bioware](https://www.bioware.com/about/)
