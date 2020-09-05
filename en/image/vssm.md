{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "VSSM - Microsoft Visio Macro Enabled File Format",
  "description":"Learn about VSSM file format and APIs that can create and open VSSM files.",
  "linktitle" : "VSSM",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

Files with .VSSM extension are Microsoft Visio Stencil files that support provide support for macros. A VSSM file when opened allows to run the macros to achieve desired formatting and placement of shapes in a diagram. In general, Microsoft Visio is drawing software that allows to create files that can contain and represent user defined information in different shapes. The most common of these include, but not limited to, UML diagrams, flow charts, visual objects, information flow, organizational charts, software diagrams, network layout, database models, objects mapping and other similar information. Files generated using Visio can also be converted to different file formats such as [PNG](https://wiki.fileformat.com/Image/PNG/), [BMP](https://wiki.fileformat.com/Image/BMP/), [PDF](https://wiki.fileformat.com/page-description-language/pdf/) and others.

# VSSM File Format #

The VSSM file format was introduced with Microsoft Visio 2013 which is based on the OpenOffice XML specifications. Certain other file types that comprise the Visio 2013 file format include:

* .vsdm (Visio macro-enabled drawing)
* .vssx (Visio stencil)
* .vssm (Visio macro-enabled stencil)
* .vstx (Visio template)
* .vstm (Visio macro-enabled template)

Under the hood, the Visio 2013 file format uses a structured means to store application data together with related resources in an archive such as [ZIP](https://wiki.fileformat.com/Compression/ZIP/). The ZIP file can be extracted using any standard extraction utility where it contains other types of files as well.

Each Visio file is termed as package that holds other files or parts. A package part can be an XML file, an image or even a VBA solution.The parts within the package can be devided into "document" and "relationship" parts.

## References ##

* [Introduction to Visio File Format](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)
