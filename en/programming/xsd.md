{
  "date" : "2022-02-06",
  "keywords" : [ "xsd", ".xsd","what is a xsd file","how to open xsd file", "extension", "file", "xsd file","xsd file format",  ".xsd extension" ,"xsd file example"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : " Learn about XSD file format and APIs that can create and open a XSD file.",
  "title" : "XSD File Format - XML Schema Definition File",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2022-02-06"
}

## What is an XSD Schema file?

An XSD file is a definition file specifying the elements and attributes that can be part of an XML document. This ensures that data is properly interpreted, and errors are caught, resulting in appropriate XML validation. XSD files ensure that the data entered follows the same structure as defined in the file. XSD files are stored in [XML](/web/xml/) file format and can be opened or edited in any text editor such as Microsoft Notepad, Notepad++, or [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/).

## XSD File Format

XSD files are stored to disc in plain text file format that is human readable. An XSD defines the elements that can be used in the documents, relating to the actual data with which it is to be encoded.

## Example of XSD File

A simple XSD file having a purchase order schema defines the elements using tags as shown in following [XSD example by Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022).

```
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"
           xmlns:tns="http://tempuri.org/PurchaseOrderSchema.xsd"
           targetNamespace="http://tempuri.org/PurchaseOrderSchema.xsd"
           elementFormDefault="qualified">
 <xsd:element name="PurchaseOrder" type="tns:PurchaseOrderType"/>
 <xsd:complexType name="PurchaseOrderType">
  <xsd:sequence>
   <xsd:element name="ShipTo" type="tns:USAddress" maxOccurs="2"/>
   <xsd:element name="BillTo" type="tns:USAddress"/>
  </xsd:sequence>
  <xsd:attribute name="OrderDate" type="xsd:date"/>
 </xsd:complexType>

 <xsd:complexType name="USAddress">
  <xsd:sequence>
   <xsd:element name="name"   type="xsd:string"/>
   <xsd:element name="street" type="xsd:string"/>
   <xsd:element name="city"   type="xsd:string"/>
   <xsd:element name="state"  type="xsd:string"/>
   <xsd:element name="zip"    type="xsd:integer"/>
  </xsd:sequence>
  <xsd:attribute name="country" type="xsd:NMTOKEN" fixed="US"/>
 </xsd:complexType>
</xsd:schema>
```

Here, the following tags are used.

 * `xs:element` - Defines an element.
 * `xs:sequence` - Denotes child elements only appear in the order mentioned.
 * `xs:complexType` - Denotes it contains other elements.
 * `xs:simpleType` - Denotes they do not contain other elements.
 * `type` - string, decimal, integer, boolean, date, time,

## References ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [XSD Sample Example](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)
