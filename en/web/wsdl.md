{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "WSDL File Format - Web Services Description Language File",
  "description":"Learn about what is a WSDL file and APIs that can create and open WSDL files.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2022-02-03"
}

## What is a WSDL file?

A WSDL file is a Web Services Description Language file that is written in XML language for describing Web services. It contains information about the endpoints or interfaces for connectivity to the outside world in a universally accepted format. [WSDL file format specifications](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (maintained by W3C.org) define the terms for publishing data feeds for exchange of data in order to have remote application access over ports and endpoints.

## WSDL File Format - More Information

WSDL files are saved as XML files that are human readable and can be opened in any text editor to view the contents.

## WSDL Service Description

The WSDL 2.0 file format specifications describes the WSDL service as comprising of two stages:

 - Abstract stage
 - Concrete stage

The reusability of the description and independent concern designs is governed by a Web service. This is achieved using several different type of elements including types (data type definitions), messages (the data communicated), operations (actions), and protocols used by the service. These are all managed at abstract level. The binding of transport and wire format details are specified by the binding, that groups the endpoints together to implement a common interface.

### What technologies can be used for interfacing with WSDL services?

Several different technologies can be used for interfacing with WSDL services including ASP.NET, C/C++, and Java applications.

## WSDL Example

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

In this example, the portType "glossaryTerms" defines a one-way operation called "setTerm".

## References

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [WSDL file format specifications](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)
