{
  "date" : "2020-11-11",
  "keywords" : [ "ACCDT", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about ACCDT file format and APIs that can create and open ACCDT files.",
  "title" : "ACCDT - Microsoft Access 2007 Template Database File Format",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2020-11-12"
}

## What is an ACCDT file?

A file with .accdt extension is a Microsoft Access database template file that contains pre-defined database elements. These elements are a collection of structures that define a database applications such as database schemas for storing data, layout description for views of the data, and metadata describing the database. Being template files, ACCDT files can be used to create databases based on the template settings available in these. Resultant database files are saved as [ACCDB](/database/accdb/) files and populated with data in tables. Microsoft Access 2007 and onwards can open ACCDT files.

## ACCDT File Format

ACCDT template files are based on the Office Open XML specifications and all the data is contained in the a ZIP package. Structure and contents information of the database is contained in the [XML](/web/xml/) files and text files and linked to each other via relationships. You can rename an ACCDT file to [.zip](/compression/zip/) extension and use any compression software to extract the contents of the ZIP archive.

### File structure

ACCDT files are packages that contain a collection of related parts. Each **part** stores information about the contents of a database application using XML, text and binary formats, that includes:

 * Database objects
 * Associated metadata
 * Structure of the package

#### Package

A Package is a [ZIP](/compression/zip/) archive that contains multiple parts and conforms to the Open Packaging Conventions specified in [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html). ACCDT files must contain atleast one Template metadaa part which should be the target of a relationship. This Template Metadata is the starting part of an ACCDT file.

#### Part

A part is a stream of bytes that has an associated type for specifying the nature and type of content stored in it. Parts enumeration specify valid parts, valid content types, and required relationships between all parts in a package.

#### Relationship

`Package Relationship` - where target is a part and the source is the package as a whole.

`Part-to-Part Relationship` - where the target is a part and the source is a part in the package.

`Explicit Relationship` - where a resource is referenced from the contents of a source part by referencing a relationship element by the value of its ID attribute.

`Implicit Relationship` - a relationship that is not explicit.

`Internal relationship` - where the target is a part in the package.

`External relationship` - where the target is an external resource not in the package.

## References ##

* [Access Template File Format](https://learn.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)
