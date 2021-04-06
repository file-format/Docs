{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "B6Z - B6ZIP Archive File Format",
  "description":"Learn about B6Z file format and APIs that can create and open B6Z files.",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-05"
}

## What is a B6Z file?

 A file with .b6z extension is a compressed archive file created macOS software application [B6Zip](http://b6zip.com) that is used to compress and decompress files. It is comparatively new archive format that allows higher compression ration. B6Z has open architecture and supports file sizes upto 900000 PB. It supports data compression, error recovery, and file spanning. The B6Zip utility software is available for free on MacOS to open different type of compressed files including B6Z.

## B6Z File Format

The B6Z file format is based on open architecture and provides solid compression with AES-256 encryption algorithm. It uses LZMA2 as default compression method, but also supports other compression methods as follow.

|Method|Description|
---|---|
|LZMA	|Optimized version of LZ77 algorithm|
|LZMA2|	Improved version of LZMA|
|Deflate|	Regular LZ77 algorithm|
|BZip2|	Standard BWT algorithm|
|PPMD|	Dmitry Shkarin's PPMdH|

The B6Zip utility supports all these compression standards and is highly optimized resulting in high speed. It supports working with [ZIP](/compression/zip/), [TAR](/compression/tar/) and [RAR](/compression/rar/) file formats. B6Z files have MIME type application/x-b6z-compressed.

## References ##

* [B6Zip](http://b6zip.com)
