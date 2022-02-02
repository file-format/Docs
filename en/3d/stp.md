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

An STP file is a 3D CAD file used for exchange of product data between different CAD and CAM applications. It contains information about 3D objects and is saved similar to the STEP file format. STP files facilitate the exchange of data between different application as per the [STEP](/3d/step/) Application Protocols ISO 10303-2xx. This ISO defines the encoding mechanism for data representation in EXPRESS data modeling language. STP files can be opened in applications such as such as Autodesk Fusion 360.

## STP File Format - More Information

STP files are saved to disc in plain ASCII file format. These contain 3D models information as plain text that can be read by CAD/CAM applications for loading these models.

STP files are also saved with .step extension and consists of a sequence of records. Salient features about these files include:

 * The character set is defined as code points of ISO 10646.
 * "ISO-10303-21;" are the first characters in the first record.
 * Comments are surrounded by "/*" and "*/" characters.
 * The last record contains "END-ISO-10303-21;" if the STEP-file is conforming to the 2002 version.
 * In case it conforms to the 2016 version, there may be one or more digital signatures after the "END-ISO-10303-21;" terminator.
 * Line breaks are denoted by "\N\" and page breaks are denoted by "\F\".


## References

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
