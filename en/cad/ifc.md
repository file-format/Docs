{
  "date" : "2020-03-16",
  "keywords" : [ "IFC File", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about IFC file format and APIs that can create and open IFC files.",
  "title" : "IFC File Format",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an IFC file?

Files with IFC extension refer to  Industry Foundation Classes (IFC) file format that establishes international standards to import and export building objects and their properties. This file format provides interoperability between different software applications. Specifications for this file format are developed and maintained by buildingSMART International as its Data Standard. The ultimate objective of IFC file format is to improve communication, productivity, delivery time and quality throughout the life cycle of a building. Due to the established standards for common objects in the building industry, it reduces the loss of information during transmission from one application to another. IFC can hold data for geometry, calculation, quantities, facility management, pricing etc. for many different professions (architect, electrical, HVAC, structural, terrain etc.).

## Brief History ##

IFC initiative was taken in 1994 by Autodesk to support integrated application development and included companies like Honeywell, Butler Manufacturing, and AT&T. In 1995, the membership was opened for opened for anyone and the name was changed to International Alliance for Interoperability. The non-profit's intent was to publish the Industry Foundation Class (IFC) as an AEC product model. In 2005, the name was again changed and buildSMART now maintains it.

## IFC File Format ##

The IFC file format has undergone several changes over the past to reach the file format specifications v4. Several minor changes occurred from time to time as well as that have been made part of the specifications as Addendums. Following is a list of different versions of file specifications that have been made public over the past.

* IFC4 Add2 (2016)IFC4 Add1 (2015)
* IFC4 (March 2013) ifcXML2x3 (June 2007)
* IFC2x3 (February 2006) ifcXML2 for IFC2x2 add1 (RC2)
* IFC2x2 Addendum 1 (July 2004)ifcXML2 for IFC2x2 (RC1)
* IFC 2x2IFC 2x Addendum 1ifcXML1 for IFC2x and
* IFC2x Addendum 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

The latest versions of IFC file format specifications are always available on buildingSMART website and developer should consult these for any type of applications they plan to develop. As of writing this article, the version 4 [Addendum2](http://www.buildingsmart-tech.org/ifc/IFC4/Add2/html/) specifications are the latest ones available online.

### IFC Data File Formats ###

IFF file format supports data exchange between applications using different formats as listed below:

**IFC:**  This is the default IFC exchange format and uses the STEP physical file structure according to ISO 10303-21. This file format has .ifc file extension and is the mostly used IFC format.

**IFC-XML:** It is an XML file format version of IFC that can be generated directly by the sending application as per ISO 10303-28 structure, also called STEP-XML. The IFC-XML file format is considered suitable for interoperability among XML tools. As compared to IFC file format, the IFC-XML is 300-400% larger in size.

**IFC-ZIP:** It is a [ZIP](/compression/zip/) compressed version of IFC or IFC-XML where the one of these files lie the main directory of the zip archive. This format compresses an .ifc down by 60-80% and a .ifc XML file by 90-95%.

### IFC Architecture ###

The IFC specification includes terms, concepts and data specification items that originate from use within disciplines, trades, and professions of the construction and facility management industry sector. Terms and concepts uses the plain English words, the data items within the data specification follow a naming convention.

the data item names for types, entities, rules and functions start with the prefix "Ifc" and continue with the English words in CamelCase naming convention (no underscore, first letter in word in upper case); the attribute names within an entity follow the CamelCase naming convention with no prefix; the property set definitions that are part of this standard start with the prefix "Pset_" and continue with the English words in CamelCase naming convention; the quantity set definitions that are part of this standard start with the prefix "Qto_" and continue with the English words in CamelCase naming convention.

The data schema architecture of IFC defines four conceptual layers, each individual schema is assigned to exactly one conceptual layer.

**Resource layer** — the lowest layer includes all individual schemas containing resource definitions, those definitions do not include an globally unique identifier and shall not be used independently of a definition declared at a higher layer;

**Core layer** — the next layer includes the kernel schema and the core extenstion schemas, containing the most general entity definitions, all entities defined at the core layer, or above carry a globally unique id and optionally owner and history information;

**Interoperability layer** — the next layer includes schemas containing entity definitions that are specific to a general product, process or resource specialization used across several disciplines, those definitions are typically utilized for inter-domain exchange and sharing of construction information;

**Domain layer** — the highest layer includes schemas containing entity definitions that are specializations of products, processes or resources specific to a certain discipline, those definitions are typically utilized for intra-domain exchange and sharing of information.

## References ##

* [IFC Specifications - By buildSmart](http://www.buildingsmart-tech.org/specifications)
* [Industry Foundation Classes - By Wikipedia](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)
