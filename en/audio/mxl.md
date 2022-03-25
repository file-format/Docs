---
date: 2022-03-20
keywords: mxl, Musepack file format, .mxl extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Learn about MXL file format and APIs that can create and open MXL files.
title: MXL File Format - Compressed MusicXML File
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## What is an MXL file?

An MXL file is the compressed form of MusicXML file format that is an open standard format for exchange of digital sheet music. Plain text MusicXML files are large in size and the use of such files as a sheet distribution format was affected with the large file size. This issues was treated with [MusicXML](https://www.musicxml.com/) 2.0 by introducing the MXL file format that compresses the files enough to reduce the file size similar to that of original MIDI files. Recommended media type for MXL files is application/vnd.recordare.musicxml.

## MXL File Format

MXL files are stored as [ZIP](/compression/zip/) compressed [XML](/web/xml/) files with .mxl file extension. MXL files are compressed with the DEFLATE algorithm as specified in the [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### MXL File Structure

Each MXL file has a ZIP-based XML format that must have a META-INF/container.xml file which describes the starting point of the MusicXML version of the file. There is no corresponding .xsd file defined for the MXL file format.

A simple container.xml file has contents as follow. This example is taken from Dichterliebe01.mxl file available on the MakeMusic web site.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
In this example, the <container> element is the document element. The <rootfiles> element can contain one or more <rootfile> elements, with the first <rootfile> element describing the MusicXML root. A MusicXML file used as a <rootfile> may have <score-partwise>, <score-timewise>, or <opus> as its document element.

## References

* [Compressed MXL Files](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)
