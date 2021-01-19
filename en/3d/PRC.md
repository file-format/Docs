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
lastmod: 2020-18-01
---

## What is a PRC file?

PRC (Product Representation Compact) is a 3D file format that is optimized to store, load, and display 3D data especially coming from CAD (Computer-Aided Design) systems. It is a sequential binary file, written in a portable way. PRC can be used to embed 3D data in a PDF file. PRC supports most of the mains constructs of CAD such as assemblies and parts, trees of 3D entities, exact geometry representation, triangulated representation, and markup. PRC uses the .prc extension and the internet media type used is *model/prc*.

PRC is a multipurpose file format that based on its usage can either be stored using regular compression to directly represent CAD data or be stored using high compression to reduce the file size. The 3D data stored in a PDF using PRC format is interoperable with CAM and CAE applications.

## PRC File Format

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

## References

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC Format Specification](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
