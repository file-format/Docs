{
  "date": "2019-10-11",
  "keywords": [
    "rar file",
    "rar file format",
    "what is a rar file",
    "file",
    "rar example",
    "rar file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "RAR",
  "description": "What is a RAR file extension and APIs that can create and open RAR files.",
  "linktitle": "RAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-rar"
    }
  },
  "lastmod": "2019-09-10"
}

## What is a RAR file?

Files with .rar extension are archive files that are created for storing information in compressed or normal form. RAR, which stands for Roshal ARchive file format, is a proprietary file format created by Eugene Roshal in 1995 who was a Russian software engineer. The format is used to archive files with different methods including various compression techniques. There are several application software available for Windows, Linux and MacOS for extraction of RAR files. WinRAR software, by RARLab, is the shareware file archiving utility (free for 40 days) for Microsoft Windows platform; the software was ported to Linux (only as extractor) by the same Author, Eugene Roshal.

## Versions History of RAR File Format

* v1.3 (original, does not have "Rar!" signature)
* v1.5
* v2.0 - released with WinRAR 2.0 and Rar for MS-DOS 2.0
* v2.9 - released in WinRAR version 3.00
* v5.0 - supported by WinRAR 5.0 and later

## Key Features of RAR Format

RAR has been in the field for quite long time and has been one of the favourite archiving file formats. Key features about the RAR format are:

**`High compression ratio:`** Superior as compared to [ZIP](/compression/zip/), comparable with 7z and zipx format.

**`Strong file encryption by design:`** Encrypted RAR4 archives rely on AES-128 based encryption while encrypted RAR5 archives rely on AES-256 encryption with improved key scheduling

**`Advanced error correction and data recovery capabilities:`** optional recovery records during archive creation

**`File Size:`** Minimum 20 bytes and maximum 2^63 bytes in size (8 exabytes of total size of the archive)

**`Multi-volume RAR Archives:`** Possibility to split large archives into several smaller files to facilitate transfer over the network. In such case, the the file extensions are incremented by 1 to represent split volumes

## RAR File Format

Complete specifications of RAR format are not available publicly and that is why details about the format can not be formulated in a concise manner.

### General Archive Layout

The general layout of a RAR file format introduced in version 5.0 is as follow:

|File Format
---|
|Self-extracting module (optional)
|RAR 5.0 Signature
|Archive Encryption Header (optional)
|Main Archive Header
|Archive comment service header (optional)
File Header 1
|Service Headers (NTFS ACL, streams, etc.) for preceding file (optional)
|...
|File Header N
|Service Headers (NTFS ACL, streams, etc.) for preceding file (optional)
|Recovery Record (optional)
|End of archive header

Information about each section of RAR file mentioned above can be found in the [RAR 5.0 File Format specifications](https://www.rarlab.com/technote.htm#arcstruct) document.

#### Self Extracting RAR Archives

If the RAR file itself is self extracting, the self extracting information is contained at the start of the file preceding the archive signature. Its size and contents are not defined.

#### RAR 5.0 Signature

The RAR signature is an 8-bytes header that consists of following magic number:

0x 52 61 72 21 1A 07 00

where

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## References

* [RAR 5.0 Archive Format](https://www.rarlab.com/technote.htm)
* [RAR - By Wikipedia](https://en.wikipedia.org/wiki/RAR_(file_format))
