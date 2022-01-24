{
  "date" : "2022-01-23",
  "keywords" : [ "xz file", "file format", "what is a xz file", "file", "xz example", "xz file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "XZ File - XZ Compressed Archive",
  "description":"Learn about XZ file format and APIs that can create and open XZ files.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2022-01-23"
}

## What is a XZ file?

XZ is a compressed file format that utilizes the LZMA2 compression algorithm. It was designed as a replacement for the popular gzip and bzip2 formats, and offers a number of advantages over these older standards. XZ files are well-supported across many platforms, and can be decompressed quickly and easily. While they are not as common as [ZIP](/compression/zip/) or [RAR](/compression/rar/) files, XZ archives can be used to store large amounts of data without sacrificing compression quality. If you need to compress or decompress large files, the XZ file extension is worth considering.

## XZ File Format

XZ file are generated and saved as binary files to disc. It uses the LZMA algorithm to compress data, and can achieve a compression ratio of up to 50%. XZ files are typically used for software distributions and backup archives. They can be decompressed using the XZ utility, which is included in most Linux distributions.

## Unzip XZ Files on Linux/Unix

In order to unzip XZ files, install `xz-utils` package first:
```
$ sudo apt-get install xz-utils
```

Use the `unxz` command to extract .xz files:
```
$ unxz compressed_xz_file.xz
```

or using with --decompress option of XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## References

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)
