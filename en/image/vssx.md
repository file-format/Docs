{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "VSSX - Visio Stencil File Format",
  "description":"Learn about VSSX file format and APIs that can create and open VSSX files.",
  "linktitle" : "VSSX",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

Files with .VSSX extension are drawing stencils created with [Microsoft Visio](https://products.office.com/en/visio/flowchart-software) 2013 and above. The VSSX file format can be opened with Visio 2013 and above. Visio files are known for representation of a variety of drawing elements such as collection of shapes, connectors, flowcharts, network layout, UML diagrams, software diagrams, database models, objects mapping and other similar information. Microsoft Visio also provides the capability to convert Visio files to different file formats such as [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) and others. It is available for both Windows and Mac OS.

# VSSX File Format #

The VSSX file format is based on the OpenOffice format adopted by Microsoft since 2007. It is based on the [ZIP](/compression/zip/) archive that represent the overall file format based on XML file format specifications. The binary file format equivalent of VSSX was VSS that was supported till Visio 2007. You can view the contents of VSSX file format by replacing its extension with .ZIP and open in any archiving file format such as WinZIP.

VSDX files are based on the Open Packaging Conventions and XML and developers can benefit from this format by learning how to work with these file programmatically. The format inherits many of the same XML structures as its parts from the Visio XML Drawing file format (.vdx). Interoperability with Visio files is greatly increased since third-party software can manipulate Visio files at a file format level.

Certain other file types that comprise the Visio 2013 file format include:

* .vsdm (Visio macro-enabled drawing)
* .vssx (Visio stencil)
* .vssm (Visio macro-enabled stencil)
* .vstx (Visio template)
* .vstm (Visio macro-enabled template)

Each Visio file is termed as package that holds other files or parts. A package part can be an XML file, an image or even a VBA solution.The parts within the package can be devided into "document" and "relationship" parts.

## References ##

* [Introduction to Visio File Format](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)
* [Schema Map - Visio XML](https://docs.microsoft.com/en-us/office/client-developer/visio/schema-mapvisio-xml)
