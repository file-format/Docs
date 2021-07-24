{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "3MF",
  "description":"Learn about 3MF file format and APIs that can open and create 3MF files.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2019-12-09"
}

## What is a 3MF file?

3MF, 3D Manufacturing Format, is used by applications to render 3D object models to a variety of other applications, platforms, services and printers. It was built to avoid the limitations and issues in other 3D file formats, like [STL](/cad/stl/), for working with the latest versions of 3D printers. 3MF is relatively a new file format that has been developed and published by the 3MF consortium. It is rich enough to fully describe a model, retaining internal information, colour, and other characteristics that makes it extensible for supporting new innovations in 3D printing. The format is extensible, able to be broadly adopted and free of issues besetting other widely used file formats.

## Brief History ##

The existing limitations in available model descriptive file formats, such as STL and others, lead the leading brands to get together and formulate a more extensible file format for 3D printing. An important consideration was to how applications should pass model data to 3D printers. The 3MF consortium, hence, came into being to back a new 3D file format called 3MF with the aim to make it extendible enough to cater the needs of 3D printing. Several companies were part of this consortium including Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP and others. Microsoft donated its 3D file format work-in-progress as the starting point for the 3MF Consortium’s collaborative further development of the specification.

## 3MF File Format - More Information

3MF is an XML-based data format – human-readable compressed XML — that includes definitions for data related to 3D manufacturing, including third-party extensibility for custom data. The 3MF file format was designed keeping in mind the limitations and issues faced by other 3D file formats. This lead to the formulation of 3MF file format that is:

* **Complete:** Containing all of the necessary model, material and property information in a single archive
* **Human readable:** Using common structures such as OPC, [ZIP](/compression/zip/), and XML to ease development
* **Simple:** A short, clear specification, making development easy and validation fast
* **Extensible:** Leveraging XML namespaces allow for both public and private extensions while maintaining compatibility
* **Unambiguous:** Clear language and conformance tests ensure a file is always consistent from digital to physical
* **Free:** Access to and implementation of the 3MF specification is and will always be free of royalties, patents and licensing

The specifications for 3MF file format are hosted over [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) for public access and continuous updates. The current published version is 1.2.3 that describes the set of conventions for the use of XML and other widely available technologies to describe the content and appearance of one or more 3D models. Developers, who want to build systems for processing 3MF file formats, can refer to these specifications for implementation purpose.

## File Format Specifications ##

The 3MF file format uses the Open Packaging specifications in the form of ZIP archive for its physical model. It includes a well-defined set of parts and relationships that fullfill particular purpose in the document. This also makes the format follow the package feature including digital signatures and thumbnails.

### The 3MF Document ###

A typical 3MF document looks as follow:

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

The payload includes the full set of parts required for processing the 3D Model part. All content to be used to manufacture an object described in the 3D payload MUST be contained in the 3MF Document. The description of each document part along with its status as required or option is as given in the following table.


|**Name**|**Description**|**Relationship Source**|**Required/Optional**
--- | --- | --- | ---
|3D Model|Contains the description of one or more 3D objects for manufacturing.|Package|REQUIRED
|Core Properties|The OPC part that contains various document properties.|Package|OPTIONAL
|Digital Signature Origin|The OPC part that is the root of digital signatures in the package.|Package|OPTIONAL
|Digital Signature|OPC parts that each contains a digital signature.|Digital Signature Origin|OPTIONAL
|Digital Signature Certificate|OPC parts that contain a digital signature certificate.|Digital Signature|OPTIONAL
|PrintTicket|Provides settings to be used when outputting the 3D object(s) in the 3D Model part.|3D Model|OPTIONAL
|Thumbnail|Contains a small JPEG or PNG image that represents the 3D objects in the package or the package as a whole.|Package|OPTIONAL
|3D Texture|Contains a texture used to apply color to a 3D object in the 3D Model part (available for extensions)|3D Model|OPTIONAL
|Custom Parts|OPC parts that are associated with metadata|Package|OPTIONAL

 The [Parts and Relationships](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D Models](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Object Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Material Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) and [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) sections of specifications document give detailed information about the 3MF document.

## References ##

* [3MF File Format Specifications](https://github.com/3MFConsortium/spec_core)
* [3MF - By Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)
