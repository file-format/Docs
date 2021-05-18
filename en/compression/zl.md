{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ZL - ZLIP Compressed File Format",
  "description":"Learn about ZL file format and APIs that can create and open ZL files.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-14"
}

## What is a ZL file?

A file with .zl extension is a ZLIP compressed file format that uses a variant of DEFLATE compression algorithm for compressing files. It is independent of CPU type, operating system, file system, and character set, and hence can be used for interchange of information. Technical specifications of ZLIP compression are available on the [IETF site](https://tools.ietf.org/html/rfc1950) and can be referred from developer's perspective.

## ZL File Format

A zlib stream has the following structure:

 * `CMF (Compression Method and flags)` -  This byte is divided into a 4-bit compression method and a 4-bit information field depending on the compression method.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
 * `CM (Compression method)` - It identifies the compression method used in the file. Its values and corresponding compression method are as follow.

 | CM Value| Compression|
 |---|---|
 |CM = 8|DEFLATE wiht a window size up to 32K|
 |CM = 15|Reserved|

 * `CINFO (Compression info)` - For CM = 8, CINFO is the base-2 logarithm of the LZ77 window size, minus eight (CINFO=7 indicates a 32K window size).

 * `FLG (FLaGs)` - This flag byte is divided as follows:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## References ##

* [Zlib File Format Specifications](https://tools.ietf.org/html/rfc1950)
