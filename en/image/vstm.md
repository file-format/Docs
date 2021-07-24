{
  "date" : "2019-10-11",
  "keywords" : [ "vstm file", "vstm file format", "what is a vstm file", "file", "vstm example", "vstm file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "VSTM - Microsoft Visio Template File Format",
  "description":"Learn about VSTM file format and APIs that can create and open VSTM files.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a VSTM file?

Files with VSTM extension are template files created with Microsoft Visio that support macros. Unlike VSDX files, files created from VSTM templates can run macros that are developed in Visual Basic for Applications (VBA)  code. A template file can be created in order to provide basic settings of the document that can be utilized to generate further documents with these settings. Visio files are used to create drawings that contain visual objects, flow charts, UML diagram, information flow, organizational charts, software diagrams, network layout, database models, objects mapping and other similar information. Files generated using Visio can also be exported to different file formats such as PNG, BMP, PDF and others.

## File Format ##

VSTM files are based on the Open Packaging Conventions and XML and developers can benefit from this format by learning how to work with these file programmatically. The format inherits many of the same XML structures as its parts from the Visio XML Drawing file format (.vdx). Interoperability with Visio files is greatly increased since third-party software can manipulate Visio files at a file format level.

Each Visio file is termed as package that holds other files or parts. A package part can be an XML file, an image or even a VBA solution.The parts within the package can be devided into "document" and "relationship" parts.

### Document ###

The document parts contain the actual content and metadata of the Visio file, like the name of the file, the first page and all of the shapes that it contains, and even the data connections for the shapes. Images and text files within the package are considered document parts.

### Relationships ###

The relationship parts of a Visio file are stored in "_rels" folder and describe how the parts within the package are related to each. It also provides the structure of the file. A standalone XML document uses the parent/child relationship of elements to determine the relationship of entities to each other. A valid Visio 2013 file format contains the correct set of parts and the package contains the relationships between the parts.

Relationship parts are XML documents that describe the relationships between different document parts within the package. They define an association between two items: a specified source (defined by the name and location of the relationship file) and a specified target document part. For example, relationship parts are used to describe which shape masters are associated with the file, how pages relate to the file and to each other, or how images and objects relate to a specific page.

## References ##

* [Introduction to Visio File Format](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)
