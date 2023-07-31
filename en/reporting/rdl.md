{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "RDL - Report Definition Language File",
  "keywords" : [ "rdl", "report definition language", "XmlTextWriter", "XSD", "RDL element"],
  "description":"Learn about RDL file format which is an XML representation of a SQL Server Reporting Services report definition.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
    }
  },
  "lastmod" : "2021-03-01"
}

## What is an RDL file? ##

The RDL (Report Definition Language) is a benchmark set by the Microsoft for defining reports. An RDL file consists of one or many RDL Element. Whereas an RDL element consists of its data type and cardinality. An element can be simple or complex. The simple element doesn't have any child element or attributes, whereas a complex element does have children and optional attributes.

## RDL XML Schema Definition
An XML Schema Definition (XSD) file validates the RDL file. The schema defines the rules for where RDL elements can occur in an .rdl file. An RDL element can be simple or complex. A simple element does not have child elements or attributes and a complex element does have children and optionally, attributes.

## Creating RDL
Since RDL is open and extensible in nature, many of application and tools can be built that generate RDL files based on its XML schema. One of the simplest ways to create RDL from an application is to use the Microsoft .NET Framework classes of the **System.Xml** namespace and System.Linq namespace. Particularly, the **XmlTextWriter** class, can be used to write RDL.You can generate a complete report definition from start to finish in any .NET Framework application by using **XmlTextWriter**. Developers can also add custom report items with custom properties to extend the RDL.

## RDL Types
The following table lists the types and attributes used in RDL elements.

|Type|Description|
---|---|
|Binary	|A property with a base-64 encoded binary value.|
|Boolean|	A property with true or false as the value of the object. Unless specified otherwise, the value of an omitted optional Boolean object is False.|
|Date	|A property with a fully specified date or datetime value specified in ISO8601 date format: YYYY-MM-DD[THH:MM[:SS[.S]]].|
|Enum	|A property with a string text value that must be one of a list of designated values.|
|Float	|A property with a float value. A period (.) is used as the optional decimal separator.|
|Integer	|A property with an integer (int32) value.|
|Language	|A property with a text value that contains a language and culture code, such as "en-us" for US English. The value must either be a specific language or a neutral language for which a default language is defined in the Microsoft .NET Framework.|
|Name	|A property with a string text value. Names must be unique within the namespace of the item. If not specified, the namespace for an item is the innermost containing object that has a name.|
|NormalizedString	|A property with a string text value that has been normalized.|
|Size	|A size element must contain a number (with a period character used as an optional decimal separator). The number must be followed by a designator for a CSS length unit such as cm, mm, in, pt, or pc. A space between the number and the designator is optional. For more information about size designators, see CSS Values and Units Reference.In RDL, the maximum value for Size is 160 in. The minimum size is 0 in.|
|String	|A property with a string text value.|
|UnsignedInt	|A property with an unsigned integer (uint32) value.|
|Variant	|A property with any simple XML type.|

## RDL Data Types
In RDL, the DataType Enumeration defines the data type of an attribute, expression, or parameter. The following table shows how CLR data types correspond to RDL data types.

|CLR Type(s)	|Corresponding Data Type|
---|---|
|Boolean|	Boolean|
|DateTime, DateTimeOffset	|DateTime|
|Int16, Int32, UInt16, Byte, SByte	|Integer|
|Single, Double	|Float|
|String, Char, GUID, Timespan	|String|


## References ##

- [Report Definition Language (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Report Definition Language (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)
