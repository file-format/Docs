{
  "date" : "2019-12-12",
  "keywords" : [ "EPS", "file", "extension", "file format", "Page Layout", "Encapsulated PostScript" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Your file format guide to know what is an EPS file and APIs that can create and open them.",
  "title" : "What is an EPS file?",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
    }
  },
  "lastmod" : "2019-09-10"
}

FIles with EPS extension essentially describe an Encapsulated PostScript language program that describes the appearance of a single page. The name "Encapsulated" because it can be included or encapsulated in another PostScript language page description. This script based file format may contain any combination of text, graphics and images. EPS files may include a bitmap preview image encapsulated inside for display by applications that can open such files. EPS files can be converted to standard image formats such as [JPG](/image/jpeg/), [PNG](/image/png/), [TIFF](/image/tiff/) and [PDF](/pdf/) using different applications e.g. Adobe Illustrator, Photoshop and PaintShop Pro. Because of a [security vulnerability](https://support.office.com/en-us/article/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) in EPS files, Office 2016, Office 2013, Office 2010, and Office 365 have turned off the ability to insert EPS files into Office documents.

## Brief History ##

A quick look at EPS file format from history perspective reveals the following informaiton:

* The first version of EPS was released by Adobe sometime between 1985 and 1988
* Version 2.0 of the EPS specification was published in January 1989
* The specification for version 3.0 of EPS was published as a separate document in 1992; this is the latest published version.

EPS, in combination with the Open Structuring Conventions extension mechanism described in clause 9 of Adobe's PostScript Language Document Structuring Conventions Specification, formed the basis of early versions of the Adobe Illustrator Artwork file format.

## Document Structuring Convention (DSC) ##

The DSC is a special file format for PostScript documents by Adobe. The DSC defines the set of rules that define how to organize PostScript data. EPS is a DSC conforming file format and adheres to all the rules established by the DSC. Any application that claims to be able to read EPS files should be DSC-compliant. 

Every DSC-compliant document is indicated by having the comment %!PS-Adobe-3.0 as the first line. This comment is a flag to indicate that the document is compliant. You should never use this comment unless your document really is DSC compliant. There are many other parts to proper DSC. A document which follows the DSC can be manipulated in many ways. In particular, post-processors can shuffle the pages, print two or more pages on a side, and so on. The printer drivers from some notable companies do not follow the DSC, and their PostScript documents are, therefore, impossible to work with once they’ve been generated.

## EPS File Format ##

EPS is a proprietary but publicly documented format and the file format specifications are available [here](http://www.adobe.com/content/dam/acom/en/devnet/actionscript/articles/5002.EPSF_Spec.pdf). EPS is a DSC (Document Structuring Convention) conforming file format and adheres to all the rules established by the DSC. The DSC is a special file format for PostScript documents by Adobe. Any application that claims to be able to read EPS files should be DSC-compliant. Any EPS file consists of two main sections as explained below.

### Preview Image ###

A typical EPS file contains a preview image in a format intended for convenient use in a workflow that involves several systems or applications. The intent of a preview is to have an image in a format that most graphics applications can render; a preview is usually of lower resolution, in pixel dimensions and/or in bit-depth. The preview file can be in one of a number of formats. The specification for EPS_3 lists three "device-specific" preview formats:

* for the Apple Macintosh, a PICT image as used by the QuickDraw application
* for DOS computers, a TIFF bitmap
* Windows Metafile.

PICT and Windows Metafile can incorporate both bitmap data and vector graphics. In addition, the specification defines a very simple device-independent representation for an embedded bitmapped preview image. This representation is known as Encapsulated PostScript Interchange Format, or EPSI. An EPSI preview is a bitmap represented as ASCII hexadecimal, wrapped between a few PostScript comments for identification and intended to be simple and easily transportable. In order to distinguish EPS files with the different preview formats, different DOS file extensions and Macintosh file types were recommended in the EPS specification.

### PostScript Code ###

At a minimum, the EPS file format must include the following:

* a header comment, //%!PS-Adobe-3.0 EPSF-3.0//
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

These also include operators from statusdict and userdict operators like legal, letter, a4, b5, etc. Some operators that should be carefully used include nulldevice, setgstate, sethalftone, setmatrix, setscreen, settransfer, and undefinefont.

EPS files can be encoded using 7-bits (ASCII, like PostScript data usually are) as well as 8-bits (binary, which is virtually always done on Macintosh because it decreases the size of the file significantly). 8-bit EPS-files cannot be handled properly by all operating systems or applications.

### File Types and Naming ###

EPS files have become a standard format for importing and exporting PostScript language files among applications in a variety of heterogeneous environments. Being scripted file format, different environments allow different file formats to be associated with EPS files. On Mac OS, e.g. application-created PostScript file type is EPSF, though files of TEXT also allowed for creation of such files with standard text editors. Similarly, on MS-DOS file system, the recommended file extension is EPS. In all the cases, the applications must strictly follow the DSC.

## References ##

* [EPS File Format - Adobe](http://www.adobe.com/content/dam/acom/en/devnet/actionscript/articles/5002.EPSF_Spec.pdf)
* [Encapsulated PostScript - By Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)
* [The EPS file format | Prepressure.com](https://www.prepressure.com/library/file-formats/eps)