---
date: 2019-10-11
keywords: prc, .prc, prc file format, how to open prc files, .prc extension, prc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PRC File Format
linktitle: PRC
description: Learn about PRC file format and APIs that can create and open PRC files.
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## The PRC file formats
The ".prc" extensions are being used for Product Representation Compact 3D file format and an e-book file format by MobiPocket.

## What is a Product Representation Compact (PRC) file?

PRC (Product Representation Compact) is a 3D file format that is optimized to store, load, and display 3D data especially coming from CAD (Computer-Aided Design) systems. It is a sequential binary file, written in a portable way. PRC can be used to embed 3D data in a PDF file. PRC supports most of the mains constructs of CAD such as assemblies and parts, trees of 3D entities, exact geometry representation, triangulated representation, and markup. PRC uses the .prc extension and the internet media type used is *model/prc*.

PRC is a multipurpose file format that based on its usage can either be stored using regular compression to directly represent CAD data or be stored using high compression to reduce the file size. The 3D data stored in a PDF using PRC format is interoperable with CAM and CAE applications.

### Product Representation Compact (PRC) File Format specification

A PRC file has one main header section followed by one or more file structures followed by one model file at the end. A file structure has one header followed by the following data sections:

- **Globals**: It contains the referenced file structures and colors, line styles, and coordinate systems for each tree entity of the file structure.
- **Tree**: It contains a description of the tree of items like product occurrences, part definitions, representation items, and markup.
- **Tessellation**: It contains all the tessellated(triangulated) data in the leaf entities of the tree(representation items and markups).
- **Geometry**: It contains all exact geometry and topology data of the leaf entities of the tree(representation items).
- **Extra geometry**: It contains the summary data of the geometry. This allows the file to be partially loaded without loading the entire geometry.

The following is the structure of a typical PRC file.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## What is a MobiPocket e-book file with PRC extension
An e-book file format which is introduced by a French company called **Mobipocket** is also using the extension ".prc". Initially, the Mobipocket launched a free application for multiple smart devices like, tablet pcs, PDAs and smartphones. The ".prc" extension is actually identical to .mobi but is used particularly for PDAs which only support **.prc** or **.pdb** extensions.

### Mobipocket PRC file format specifications
The MobiPocket PRC file format is based on the Open eBook standard using XHTML and also it can include JavaScript and frames. Support for native SQL queries to be used with embedded databases is also available.

The Mobipocket Reader has a home page library. Readers can insert blank pages in any part of a book and add variable drawings. The objects like Annotations, bookmarks, corrections, notes, and drawings are manageable from a single location. Images are converted to GIF format and have a maximum size of 64K which is sufficient for mobile phones with small screens. Mobipocket Reader has the electronic bookmarks, and a built-in dictionary.

The reader has a full screen mode for reading and support for many PDAs, Communicators, and Smartphones. The Mobipocket products support most Palm operating systems, Windows, Symbian, BlackBerry, but not the Android. The reader works under Linux or Mac OS X using WINE. the applications like Okular and FBReader can also be used under Linux or Mac OS X, but they work only with un-encrypted files.

The Amazon Kindle can read un-protected .mobi files, as can Amazon's Kindle application for Windows and MacOS. Amazon KindleGen is an .epub to .mobi converter, and it supports IDPF 1.0 and IDPF 2.0 EPUB formats.

## References

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC Format Specification](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Comparison of e-book formats - By Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)
