---
date: 2022-01-31
keywords: stp, .stp, stp file format, how to open stp files, .stp extension, stp extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: STP File Format
linktitle: STP
description: Learn about STP file format and APIs that can create and open STP files.
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## What is an STP file?

An STP file is a 3D CAD file used for exchange of product data between CAD and CAM applications. It contains information about 3D objects and is saved similar to the **STEP** file format. STP files facilitate the exchange of data between applications as per the [STEP](/3d/step/) Application Protocols ISO 10303-2xx. This ISO defines the encoding mechanism for data representation in EXPRESS data modeling language. STP files can be opened in applications such as such as **Autodesk Fusion 360**.

## STP File Format - More Information

STP files are saved to disc in plain ASCII file format. These contain 3D models information as plain text that can be read by CAD/CAM applications for loading these models.

STP files are also saved with .step extension and consists of a sequence of records. Salient features about these files include:

 * The character set is defined as code points of ISO 10646.
 * "ISO-10303-21;" are the first characters in the first record.
 * Comments are surrounded by "/*" and "*/" characters.
 * The last record contains "END-ISO-10303-21;" if the STEP-file is conforming to the 2002 version.
 * In case it conforms to the 2016 version, there may be one or more digital signatures after the "END-ISO-10303-21;" terminator.
 * Line breaks are denoted by "\N\" and page breaks are denoted by "\F\".

## Open STP Files

STP files can be opened in STP Viewers as well as Text Editors.

### Open STP Files with STP Viewers

Various CAD applications can open STP files for viewing on Windows, MacOS and Linux. These include:

 * Autodesk Fusion 360 (cross-platform)
 * FreeCAD (cross-platform)
 * IMSI TurboCAD (Windows, Mac)
 * Dassault Systems CATIA (WIndows, Linux)

### Open STP Files with Text Editors

STP files are saved as plain text files. This makes it possible to open STP files with text editors. Popular text editors such as Notepad and Notepad++ on Windows OS, and Apple TextEdit on MacOS can open STP files. Once opened in a text editor, user can edit the properties of STP file. However, it can lead to corruption of file in case of updating the properties incorrectly.

## How to convert STP files

There are several applications that can convert STP files to other file formats. CAD applications that can convert STP files include:

 * Autodesk Fusion 360
 * IMSI TurboCAD
 * Siemens Solid Edge

In addition to these, there are several online apps that can convert STP files to other file formats. These online apps lets you upload your STP file to cloud servers where they are converted to your desired format and returned back for downloading.

The Autodesk Fusion 360 can convert STP files to the following 3D and CAD file formats.

 * [OBJ](/3d/obj/)
 * [3MF](/3d/3mf/)
 * [DWG](/cad/dwg/)
 * [DXF](/cad/dxf/)
 * [ASM](/cad/asm/)
 * [IGES](/cad/iges/)
 * [STL](/cad/stl/)
 * [FBX](/3d/fbx/)
 * F3D
 * [USD](/3d/usd/)

## References

 * [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
 * [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)
