{
  "date": "2021-08-09",
  "keywords": [
    "cso file",
    "cso file format",
    "what is an cso file",
    "file",
    "cso example",
    "cso file extension",
    "extension",
    "format",
    "iso",
    "DAX compression"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about CSO file format and APIs that can create and open CSO files.",
  "title": "CSO - Compressed ISO Disk Image",
  "linktitle": "CSO",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cso"
    }
  },
  "lastmod": "2021-08-09"
}

## What is a CSO file?

A file with the .cso extension is a compressed ISO image file. The CSO is an alternative to the DAX compression method; also known as CISO; was the first method to compress the [ISO](/compression/iso/) files and is usually a preferred method for archiving PlayStation Portable stuff. This format uses Deflate compression, which can include up to nine compression layers. Software such as Prometheus and YACC are used to create the images.

## CSO file format

The CSO file format was the first compression method for ISO for saving more memory space. The enhancements were made from time to time for better compression. The CSO is using Deflate compression having nine levels of presets, usually, each level can handle 2 KiB blocks individually. While the highest levels of compression can slow and lengthy load-times in software which depends heavily on disc streaming, Also the lower levels can perform substantial compression.

### CSO file structure

The CSO file format contains a 24-byte header, data blocks, and an index table. Little-endian is assumed for fields larger than a byte. The architecture endianness of PlayStation Portable is given below.

#### Header

| Offset (bytes) | Name | Size (bytes) | Purpose |
----------|----------|--------------|---------|
| 0x0 | Magic | 4 | Always CISO, or 0x4F534943 when read as a 32-bit integer. This field is used to identify a CSO file. Note that this field can be different for the other derivatives of CSO, for example, ZSO used the magic code ZISO. |
| 0x4 | Header size | 4 | For the original CSO "v1" file format, this field is ignored and therefore not required to be accurate. However, the "v2" and ZSO format require this field to always be 0x18 (24 bytes). |
| 0x8 | Uncompressed size | 8 | The size of the original uncompressed ISO in bytes. |
| 0x10 | Block size | 4 | The size of each data block in bytes before compression. Usually 2048 bytes, same as the size of each ISO 9660 sector. |
| 0x14 | Version | 1 | The version of the file format in use. For the "v1" format, the value can be either 0 or 1. For the "v2" format, this must be 2. Additionally, the ZSO format requires this to be 1. |
| 0x15 | Index alignment | 1 | The alignment of each index entry, specified in bits. |
| 0x16 | Reserved | 2 | This field is unused. In the "v1" format, this field is ignored and may contain arbitrary values. In the "v2" format, this field must be zero. |

#### Index table

The index table contains several 4-byte entries, which indicate the position of each data block, and an additional, last entry which points to the end of the file.
The content of each entry is as follows:
| Bit | Length | Mask | Name | Purpose |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFF | Position | This field, when shifted left by the index alignment given in the header, gives off the position where the data block starts. |
| 31 | 1 | 0x80000000 | Compression type |  The ZSO format has similar semantics, only that 0 represents LZ4 instead of Deflate. In the "v2" format. The block is implicitly considered to be uncompressed if the block size is equal to or larger than the block size specified in the file header. |

#### Data blocks

The data blocks comprises of the uncompressed or compressed data. The size of a block is calculated by getting its position, and then subtracting it from the position of the following block. If the index alignment is greater than zero, it is likely that the block size is larger than the data it holds.


## References 

* N/A
