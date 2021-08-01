{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MXF - Material Exchange Format",
  "keywords" : [ "MXF", "matroska video", "mkv format", "how to play MXF files", "SMPTE", "multimedia", "video" ],
  "description":"Learn about MXF file format and APIs that can create and open MXF files.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2021-03-01"
}

## What is an MXF File?

A file with .mxf extension is a multimedia container format that contains digital video and audio media along with metadata information about the file. It follows the SMPTE (Society of Motion Picture and Television Engineers) standard that is a global association of professionals from engineering, technology, and executives working in the media and entertainment industry. MXF files can be converted to other file formats such as [AVI](/video/avi/) or [MOV](/video/mov/).

## MXF File Format

MXF files are in fact binary files that consist of a sequence of bytes in a definite format. Decoding applications must compliant with this format in order to understand it and extract information from it. The format allows adding new items without breaking backward compatibility using the KLV coding which is described below.

 * Key – the identifier of the element, an SMPTE Universal Label (UL)
 * Length – the length of the data which is the variable-length encoding used in order to reduce the amount of space required for this item
 * Value – the actual value of the element.

### SMPTE Format Specifications

MXF file format has been defined by the following SMPTE specifications.

* SMPTE ST 377-1:2011. Television — Material Exchange Format (MXF) — File Format Specification
* SMPTE ST 377-2 (work in progress as of January 2012). KLV Encoded Extension Syntax for MXF.
* SMPTE ST 378:2004 (Archived 2010). Television — Material Exchange Format (MXF) — Operational Pattern 1a (Single Item, Single Package)
* SMPTE ST 379-1:2009. Material Exchange Format (MXF) — MXF Generic Container
* SMPTE ST 379-2:2010. Material Exchange Format (MXF) -- MXF Constrained Generic Container
* SMPTE ST 380:2004. Television — Material Exchange Format (MXF) — Descriptive Metadata Scheme-1 (Standard, Dynamic)
* SMPTE ST 381-1:2005. Television — Material Exchange Format (MXF) — Mapping MPEG Streams into the MXF Generic Container (Dynamic)
* SMPTE ST 381-2:2011. Material Exchange Format (MXF) — Mapping MPEG Streams into the MXF Constrained Generic Container
* SMPTE ST 382:2007. Material Exchange Format (MXF) — Mapping AES3 Streams and Broadcast Wave Audio to the MXF Generic Container
* SMPTE ST 383:2008. Television — Material Exchange Format (MXF) — Mapping DV-DIF Data to the MXF Generic Container
* SMPTE ST 384:2005. Television — Material Exchange Format (MXF) — Mapping of Uncompressed Pictures into the MXF Generic Container
* SMPTE ST 385:2004. Television — Material Exchange Format (MXF) — Mapping SDTI-CP Essence and Metadata into the MXF Generic Container
* SMPTE ST 386:2004 (Archived 2010). Television — Material Exchange Format (MXF) — Mapping Type D-10 Essence Data to the MXF Generic Container
* SMPTE ST 387:2004 (Archived 2010). Television — Material Exchange Format (MXF) — Mapping Type D-11 Essence Data to the MXF Generic Container
* SMPTE ST 388:2004 (Archived 2010). Television — Material Exchange Format (MXF) — Mapping A-law Coded Audio into the MXF Generic Container
* SMPTE ST 389:2005. Television — Material Exchange Format (MXF) — MXF Generic Container Reverse Play System Element
* SMPTE ST 390:2011. Television — Material Exchange Format (MXF) — Specialized Operational Pattern "Atom" (Simplified Representation of a Single Item)
* SMPTE ST 391:2004 (Archived 2010). Television — Material Exchange Format (MXF) — Operational Pattern 1b (Single Item, Ganged Packages)
* SMPTE ST 392:2004. Television — Material Exchange Format (MXF) — Operational Pattern 2a (Play-List Items, Single Package)
* SMPTE ST 393:2004. Television — Material Exchange Format (MXF) — Operational Pattern 2b (Play-List Items, Ganged Packages)
* SMPTE ST 394:2006. Television — Material Exchange Format (MXF) — System Scheme 1 for the MXF Generic Container
* SMPTE ST 405:2006. Television — Material Exchange Format (MXF) — Elements and Individual Data Items for the MXF Generic Container System Scheme 1
* SMPTE ST 407:2006. Television — MXF — Operational Patterns 3a and 3b
* SMPTE ST 408:2006. Television — MXF — Operational Patterns 1c, 2c, and 3c
* SMPTE ST 410: 2008. Material Exchange Format - Generic Stream Partition.
* SMPTE ST 422:2006. Material Exchange Format — Mapping JPEG2000 Codestreams into the MXF Generic Container
* SMPTE ST 429.4:2006. D-Cinema Packaging — MXF JPEG 2000 Application
* SMPTE ST 429.5:2006. D-Cinema Packaging — Timed Text Track File
* SMPTE ST 429.6:2006. D-Cinema Packaging — MXF Track File Essence Encryption
* SMPTE ST 434:2006. Material Exchange Format — XML Encoding for Metadata and File Structure Information
* SMPTE ST 436:2006. Television — MXF Mappings for VBI Lines and Ancillary Data Packets
* SMPTE ST 2019-4:2009. Mapping VC-3 Coding Units into the MXF Generic Container
* SMPTE ST 2037:2009. Mapping VC-1 into the MXF Generic Container
* SMPTE RP 2008:2008. Material Exchange Format — Mapping AVC Streams into the MXF Generic Container
* SMPTE RP 2057:2011. Text-Based Metadata Carriage in MXF
* SMPTE EG 41:2004. Material Exchange Format (MXF) — Engineering Guideline. Note: This document was no longer listed on the SMPTE Web site when consulted in January 2012.
* SMPTE EG 42:2004. Material Exchange Format (MXF) — MXF Descriptive Metadata
* SMPTE RDD 3:2008. e-VTR MXF Interoperability Specification
* SMPTE RDD 9-2009. MXF Interoperability Specification of Sony MPEG Long GOP Products
* SMPTE metadata registry spreadsheet menu (http://www.smpte-ra.org/mdd/).

### MXF Structural Metadata

Structural metadata is fundamental in an MXF file as it contains useful information about the contents of the file. MXF metadata contains information such as frame rate, frame size, file creation date, and custom modification date. The structural metadata describes the structure and capabilities of an MXF file that includes technically describing the various essential components and conveying how the output timeline is composed.

## References

 * [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
 * [MXF - Progress Report](http://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
 * [OpenSource C++ Library for MXF](http://www.freemxf.org/)
