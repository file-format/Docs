{
  "date": "2019-10-11",
  "keywords": [
    "u3d file",
    "u3d file format",
    "what is an u3d file",
    "file",
    "u3d example",
    "u3d file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "U3D - Universal 3D File Format",
  "description": "Learn about U3D file format and APIs that can open and create U3D files.",
  "linktitle": "U3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-u3d"
    }
  },
  "lastmod": "2019-09-10"
}

## What is a U3D file?

**U3D** (Universal 3D) is a compressed file format and data structure for 3D computer graphics. It contains 3D model information such as triangle meshes, lighting, shading, motion data, lines and points with color and structure. The format was accepted as[ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) standard in August 2005. 3D [PDF](/pdf/) documents support U3D objects embedding and can be viewed in Adobe Reader (version 7 and onwards).

U3D format was developed keeping in view the aim to establish a universal standard for three-dimensional data storage and exchange. However, the format finds its main utilization in encoding for 3D PDF rather than being used as an interchange format. Acrobat 3D converts a supported 3D file type to either U3D or PRC upon conversion into the PDF.

## U3D File Format

U3D files are in binary file format that underwent four editions as described by the [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) reference document, resulting in specifications update with each edition. The PDF file standard ISO-32000 accepts U3D as allowed annotation and multimedia type.

The first edition of U3D was focused on the key representations of 3D graphics properties such as geometry, color, textures, lighting, bones and transform-based animation. The second and third editions corrected some errata in the first edition, with third version being the most commonly used type in industry software. The fourth edition provides definitions for higher-order primitives (curved surfaces). [U3D specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) are available online for user reference on ECMA website.

### Data Types in U3D files

The binary file will contain the following types: U8, U16, U32, U64, I16, I32, F32, F64, and String.

 * U8 : An unsigned 8 bit integer
 * U16 : An unsigned 16 bit integer
 * U32 : An unsigned 32 bit integer
 * U64 : An unsigned 64 bit integer
 * I16 : A signed 16 bit integer
 * F32: An IEEE single precision float.
 * F64: An IEEE double precision float.
 * String: Strings in a U3D file start with an unsigned 16-bit integer that defines the total length of the characters in the string. Strings are always processed as case sensitive.

## U3D File Structure

A U3D file contains a sequence of blocks. There are 3 different types of a block in each U3D file.

 * File Header Block
 * Declaration Block
 * Continuation Block

The loader determines the end of a block if the data in that block is not required or if a decoder for that block type is not available.

{{< figure src="../u3d.png" alt="U3D File Format" >}}

### File Header block
A file header block contains file information that is used by the loaded to determine how to read the file.

### Declaration Block

The declaration blocks contain information about the objects in the file. The objects in a declaration block must be define.

### Continuation Block

Additional information for objects declared in a Declaration block are provided in the continuation block. Each Continuation Block must be associated with a Declaration Block.


## References ##

* [U3D File Format - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [ECMA U3D File Format Specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/)
