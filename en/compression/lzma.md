{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "LZMA - LZMA Compressed File Format",
  "description":"Learn about LZMA file format and APIs that can create and open LZMA files.",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-18"
}

## What is a LZMA file?

A file with .lzma extension is a compressed archive file created using the LZMA (Lempel-Ziv-Markov chain Algorithm) compression method. These are mainly found/used on Unix operating system and are similar to other compression algorithms such as [ZIP](/compression/zip/) for minimising file size. LZMA is a legacy file format, which is being or has been replaced by the .xz format. The MIME type of the .lzma format is \`application/x-lzma'. This file format was designed by Igor Pavlov for use in LZMA SDK.

## LZMA File Format

The LZMA file consists of two main parts:

 1. Header
 1. Compressed Data


### LZMA Header

The LZMA files has a 13-byte header that is followed by the LZMA compressed data. The LZMA header consists of:

 * Properties
 * Dictionary Size
 * Uncompressed Size

#### LZMA Header Properties

The Properties field contains three properties. An abbreviation is given in parentheses, followed by the value range of the property. The field consists of

1) the number of literal context bits (lc, [0, 8]);
2) the number of literal position bits (lp, [0, 4]); and
3) the number of position bits (pb, [0, 4]).

#### LZMA Dictionary Size

This is stored as an unsigned 32-bit little endian integer with values ranging from 2^n and 2^n + 2^(n-1). LZMA Utils can decompress files with any dictionary size.

#### Uncompressed Size
The Uncompressed Size is stored as unsigned 64-bit little endian integer. A special value of 0xFFFF_FFFF_FFFF_FFFF indicates that Uncompressed Size is unknown. The value is represented by  End of Payload Marker (\*) if and only if Uncompressed Size is unknown.

## How to open LZMA file?

Some of the software applications that can open PKG files include:

 * [7-Zip](https://www.7-zip.org/)
 * [LZMA SDK](https://www.7-zip.org/sdk.html)
 * [p7zip](http://p7zip.sourceforge.net/)

## References

* [LZMA File Format](https://svn.python.org/projects/external/xz-5.0.3/doc/lzma-file-format.txt)
* [Lempel–Ziv–Markov chain algorithm](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)
