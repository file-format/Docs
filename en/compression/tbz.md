{
  "date": "2019-10-11",
  "keywords": [
    "tbz file",
    "tbz file format",
    "what is a tbz file",
    "file",
    "tbz example",
    "tbz file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "TBZ - Bzip Compressed Tar Archive",
  "description": "Learn about TBZ file format and APIs that can create and open TBZ files.",
  "linktitle": "TBZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tbz"
    }
  },
  "lastmod": "2021-04-05"
}

## What is a TBZ file?

 A file with .tbz extension is a compressed archive that uses BZIP compression for reducing the size of the content files. The TBZ files are actually UNIX [TAR](/compression/tar/) archived files that are compressed with BZIP then. The most recent second level compression is [BZIP2](/compression/bz2/) that replaced BZIP. TBZ file format is suitable for transferring large files. TBZ files can be opened/extracted using software applications such as 7-Zip, PeaZip, and jZip. Linux and macOS users can also open a TBZ with the BZIP2 command from a terminal window.

## TBZ File Format

TBZ files are actually compressed archives created with BZIP/[BZIP2](/compression/bz2/) compression. There are no formal specifications available for this file format. However, an unofficial [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) show that a .bz2 stream consists of a 4-byte header which is followed by zero or more compressed blocks.

## References ##

* [BZIP2 Format Specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)
