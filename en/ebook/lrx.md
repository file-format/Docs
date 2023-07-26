{
  "date" : "2019-12-12",
  "keywords" : [ "LRX", "file", "extension", "format", "E-Book", "Digital book" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about LRX file format and APIs that can create and open LRX files.",
  "title" : "LRX - Librie Reader Source File Format",
  "linktitle" : "LRX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
    }
  },
  "lastmod" : "2020-11-04"
}

## What is an LRX file?

A file with .lrx extension is an associated file for Sony Broadband eBook (BBeB). It contains data such as images, text, and pagination information. The BBeB format is used by the Sony Portable Reader which is a mobile device allowing users to read eBooks. But as of July 2010, it has become obsolete and Sony now uses the [EPUB](/ebook/epub/) file format for ebooks. Applications that can open LRX files include Sony Reader which is available for both Windows and Mac OS.

## LRX File Format

LRX files are in binary file format and all the contents in the file are encrypted unlike [LRS](/ebook/lrs/), which is a non-encrypted format. Another associated BBeB file format is LRS which is XML based and is human-readable in any text editor. The header of LRX files contains information such as:

* Version
* Root object identification
* The type of thumbnail image
* Deflated data values
* Obfuscation key
* Direction flag binding
* Size of the data after deflation

## References

* [BBeB - By Wikipedia](https://en.wikipedia.org/wiki/BBeB)
