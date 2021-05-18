{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PKG - Extensible Archive File Format",
  "description":"Learn about PKG file format and APIs that can create and open PKG files.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-13"
}

## What is a PKG file?

A file with .pkg extension is an installer package file that is used to install software on the macOS. In addition to to Macintosh computers, it is used on the iPhone as well. The builtin Apple installer application can be used to install the contents of a PKG file. A PKG file is similar to an MSI file used on Windows Operating System for installation of software. During installation, these package files can log messages that gives you an idea what extra things are installed by this package.

## PKG File Format

PKR are binary files that are compressed to reduce the overall file size. Since OSX 10.5, flat packages with single installer files have been introduced by Apple. These are different than the earlier packaging formats that came as a bundles rather than single files. These bundled packages contained a structured directory hierarchy that stored files in a way that facilitates their retrieval via some index file. The flat PKG file format is actually a [XAR](/compression/xar/) archive that has a:

 * Header - Defines the size, checksum, and version information
 * Table of Contents - An XML document that is (and must) be encoded as UTF-8 and is stored in the beginning of the file, making it easy to scan through the archive to extract individual file
 * Heap - unstructured heap of data referenced by the TOC

## References

* [Flat Package File Format](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)
