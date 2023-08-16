{
  "date" : "2019-12-12",
  "keywords" : [ "EPS", "file", "extension", "file format", "Page Layout", "Encapsulated PostScript" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about EPS file format and APIs that can create and open EPS files.",
  "title" : "EPS File Format - Encapsulated PostScript File",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an EPS file?

A .eps file is an image file that is saved to disc in Encapsulated Postscript file format. It may contain any combination of text, graphics and images. EPS files may also include a bitmap preview image encapsulated inside for display by applications that can open such files.

## Brief History of EPS File Format

A quick look at EPS file format from history perspective reveals the following information:

* The first version of EPS was released by Adobe sometime between 1985 and 1988
* Version 2.0 of the EPS specification was published in January 1989
* The specification for version 3.0 of EPS was published as a separate document in 1992; this is the latest published version.

EPS, in combination with the Open Structuring Conventions extension mechanism described in clause 9 of Adobe's PostScript Language Document Structuring Conventions Specification, formed the basis of early versions of the Adobe Illustrator Artwork file format.

## EPS File Format

EPS is a proprietary but publicly documented format and EPS file format specifications are available publicly for developer's reference. EPS is a [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Document Structuring Convention) conforming file format and adheres to all the rules established by the DSC. The DSC is a special file format for PostScript documents by Adobe. Any application that claims to be able to read EPS files should be DSC-compliant.

An EPS file consists of two main sections as explained below.

### Preview Image ###

A typical EPS file contains a preview image in a format intended for convenient use in a workflow that involves several systems or applications. The intent of a preview is to have an image in a format that most graphics applications can render; a preview is usually of lower resolution, in pixel dimensions and/or in bit-depth. The preview file can be in one of a number of formats. The specification for EPS_3 lists three "device-specific" preview formats:

* for the Apple Macintosh, a PICT image as used by the QuickDraw application
* for DOS computers, a TIFF bitmap
* Windows Metafile.

PICT and Windows Metafile can incorporate both bitmap data and vector graphics. In addition, the specification defines a very simple device-independent representation for an embedded bitmapped preview image. This representation is known as Encapsulated PostScript Interchange Format (EPSI).

An EPSI preview is a bitmap represented as ASCII hexadecimal, wrapped between a few PostScript comments for identification and intended to be simple and easily transportable. In order to distinguish EPS files with the different preview formats, different DOS file extensions and Macintosh file types were recommended in the EPS specification.

### PostScript Code

At a minimum, the EPS file format must include the following:

* a header comment, %!PS-Adobe-3.0 EPSF-3.0
* and a bounding box comment, %%BoundingBox: llx lly urx ury, that describes the bounds of the illustration. These four arguments correspond to the lower-left (llx, lly) and upper-right (urx, ury) corners of the bounding box.

An EPS file can not use any of the following operators:

* banddevice,
* cleardictstack
* copypage
* erasepage
* exitserver
* framedevice
* grestoreall
* initclip
* initgraphics
* initmatrix
* quit
* renderbands
* setglobal
* setpagedevice
* setshared
* startjob.

## Conversion of EPS to Other File formats

EPS files can be converted to standard image formats such as [JPG](/image/jpeg/), [PNG](/image/png/), [TIFF](/image/tiff/) and [PDF](/pdf/) using different applications e.g. Adobe Illustrator, Photoshop and PaintShop Pro.

Because of a [security vulnerability](https://support.microsoft.com/en-us/office/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) in EPS files, Office 2016, Office 2013, Office 2010, and Office 365 have turned off the ability to insert EPS files into Office documents.

## References

* [Encapsulated PostScript - By Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)
