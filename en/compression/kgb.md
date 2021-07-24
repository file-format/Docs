{
  "date" : "2021-04-08",
  "keywords" : [ "kgb file", "kgb file format", "what is a kgb file", "file", "kgb example", "kgb file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "KGB - KGB Archive File Format",
  "description":"Learn about KGB file format and APIs that can create and open KGB files.",
  "linktitle" : "KGB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-18"
}

## What is a KGB file?

A file with .kgb extension is a compressed archive file created with the KGB archiver software. KGB archiver uses the [PAQ6](https://en.wikipedia.org/wiki/PAQ6) compression algorithm to compress the files into a KGB archive. KGB archiver has been discontinued and is no more used. KGB file format offers higher compression rates but at the cost of its minimum hardware requirements (recommend processor with 1,5GHz clock and 256MB of RAM) and extended compression/decompression time.

## KGB File Format

There are no technical implementation details available about the KGB file format. It offers AES-256 encryption to protect the archived files. The KGB archiver was developed in Visual [C++](/programming/cpp) by Tomasz Pawlak in April 2006 and it was believed to compress a [1 GB file to up to 10 MB](https://web.archive.org/web/20100522074017/http://cshared.com/compress-1-gb-to-10-mb-kgb-archiver/) file.

## References

* [KGB - Wikipedia](https://en.wikipedia.org/wiki/KGB_Archiver)
* [KGB Archiver](https://sourceforge.net/projects/kgbarchiver/)
