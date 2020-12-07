{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "GZ - Gnu Zipped Archive File Format",
  "description":"Learn about GZ file format and APIs that can create and open GZ files.",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2019-09-10"
}

Files with .gz extension are compressed files created with gzip compression application. It can contain multiple compressed files and is commonly used on UNIX and Linux systems. GZIP was introduced as a free utility for replacing the Compress program used in Unix systems. Such files can be opened and extracted with a several applications such as WinZip which is available on both Windows and MacOS. While the format is similar to [.ZIP](https://wiki.fileformat.com/Compression/ZIP/) compression in archiving, it differs in terms of compression applied to the archive instead of individual file.

# GZ File Format #

Gzip uses the [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) algorithm for compression of archive and differs from the .ZIP archive format in applying the compression algorithm on complete archive rather than individual files. The GZIP file format specifications version 4.3 published by Internet Engineering Task Force (IETF) contains detailed information about the file format. The file format consists of:

* File Header
* Optional Headers
* Compressed Data
* File Footer

## File Header ##

The file header consists of 10 bytes as follow:


|Offset|Size|Value|Description
---|---|---|---|
|0|2|0x1f 0x8b|Magic number identifying file type
|2|1| |Compression Method * 0-7 (Reserved) * 8 (Deflate)
|3|1| |File Flags
|4|4| |32-bit timestamp
|8|1| |Compression flags
|9|1| |Operating system ID

### File Flags ###


|Value|Identifier|Description
---|---|---|
|0x01|FTEXT|If set the uncompressed data needs to be treated as text instead of binary data. This flag hints end-of-line conversion for cross-platform text files but does not enforce it.
|0x02|FHCRC|The file contains a header checksum (CRC-16)
|0x04|FEXTRA|The file contains extra fields
|0x08|FNAME|The file contains an original file name string
|0x10|FCOMMENT|The file contains comment
|0x20| |Reserved
|0x40| |Reserved
|0x80| |Reserved

### Operating System ###


|Value|Description
---|---|
|0|FAT filesystem (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (or OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari TOS
|6|HPFS filesystem (OS/2, NT)
|7|Macintosh
|8|Z-System
|9|CP/M
|10|TOPS-20
|11|NTFS filesystem (NT)
|12|QDOS
|13|Acorn RISCOS
|255|unknown

## Optional Headers ##

The optional extra headers are those as denoted by the file flags and include information such as the original filename, extra fields, comments and header checksum.

## Compressed Data ##

This section contains the compressed data using the DEFLATE compression algorithm.

## File Footer ##

The file footer is 8 bytes in size and contains following information.


|Offset|Size|Description
---|---|---|
|0|4|Checksum (CRC-32)
|4|4|Uncompressed data size value in bytes

## References ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: GZIP file format specification](http://tools.ietf.org/html/rfc1952), by [IETF](https://forensicswiki.org/index.php?title#IETF&action#edit&redlink#1)
