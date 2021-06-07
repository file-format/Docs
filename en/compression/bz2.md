{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "BZ2 - Compressed File Format",
  "description":"Learn to know what is a BZ2 file and APIs that can create and open BZ2 files.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2020-09-05"
}

## What is a BZ2 file?

BZ2 are compressed files generated using the [BZIP2](http://www.bzip.org/) open source compression method, mostly on UNIX or Linux system. It is used for compression of a single file and is not meant for archiving of multiple files. This is in contrast to the TAR file format on the same platforms that archives multiple files into a single file but without compression. Files compressed as BZ2 can be decompressed with applications like [WinZip](https://www.winzip.com/win/en/). BZIP2 uses Run-Length Encoding (RLE) or [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) compression algorithm to achieve high levels of compression.

## BZ2 File Format

There are no formal specifications available for this file format. However, an unofficial [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) show that a .bz2 stream consists of a 4-byte header which is followed by zero or more compressed blocks. It is immediately followed by an end-of-stream marker containing a 32-bit CRC for the plain text whole stream processed. There is no padding between the compressed blocks and all the blocks are bit-aligned.

## Unzip/Extract BZ2 File

You can unzip a BZ2 file on Windows and Mac OS using software such as WinZip. On linux, the following command in terminal.

```
bzip2 -d filename.bz2
```

## References

* [BZIP2 Format Specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)
