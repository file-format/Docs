{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TGZ File - Gzipped Tar File",
  "description":"Learn about TGZ file format and APIs that can create and open TGZ files.",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2022-03-02"
}

## What is a TGZ file?

A file with .tgz extension is a TAR archive file, comprising of multiple files and folders, that has been compressed using the Gnu Zip (gzip) compression software. A [TAR](/compression/tar/) file usually combines multiple files into a single file for backup or distribution over the internet. It is uncompress file until it is compressed using the gzip software after which it becomes the TGZ file. TGZ files, being compressed files, take less space on disc and are easily transferrable using internet via email. Some applications that can open TGZ files include WinZip, Apple Archive Utility, 7-Zip, and WinRAR. TGZ files are mostly used in UNIX and Linux system.

## TGZ File Format

TGZ files are saved as compressed binary files using the [GZ](/compression/gz/) compression algorithm.

## How to unpack .tgz file on Linux

On Linux/Unix OS, the following command can be used to unpack TGZ files from command line.

```
tar zxvf tgzCompressedFile.tgz
```

The above command decompresses the compressed TGZ file and extracts its files the TAR archive to disc.
## References ##

* [TGS](https://core.telegram.org/animated_stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
