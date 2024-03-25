{
  "date" : "2019-10-11",
  "keywords" : [ "xbrl","xbrl file", "xbrl file format", "xbrl file type", "file", "type", "what is an xbrl file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "XBRL - Business and Financial Reporting File Format",
  "description":"Learn about XBRL file format and APIs that can create and open XBRL files.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
    }
  },
  "lastmod" : "2021-02-25"
}

## What is an XBRL file?

A file with .xbrl (eXtensible Business Reporting Language) extension is a freely available and global framework for exchanging business information.	It is now widely used as one of the standards formats that has replaced the older paper-based reports with more useful and accurate digital records. Data exchanged using the XBRL files includes [ledgers](https://docs.familiarize.com/glossary/ledger/), financial details, and [balance sheets](https://docs.familiarize.com/glossary/balance-sheet/). It supports data tags that allows data processing from preparation till analysis stage of business information of all kinds. XBRL files can be opened using software such as Rivet Software Dragon View XBRL Viewer and APIs like [Aspose.Finance](https://products.aspose.com/finance/).

## XBRL File Format

XBRL is an open international standard for digital business reporting that is widely used globally. It is an [XML](/web/xml/) based language that uses XBRL elements, known as tags, to describe each item of business data to formulate data for report sorting and analysis. XBRL file format specifications are developed and published by XBRL International, Inc, with [XBRL version 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) currently available to users.

### XBRL Document Structure

Complete information about the [XBRL 2.1 tags](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) can be referred by programmers to write applications for working this file format. An XBRL consists of an XBRL instance, and a collection of taxonomies.

**`XBRL Instance`** - The XBRL instance begins with the <xbrl> root element. A large XML document can contain more than one XBRL instance embedded in it.

**`XBRL Taxonomy`**  - The [XBRL Taxonomy](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) is defined as an XML schema structures and set of directly referenced external links element. A scalable taxonomy schema showing the linkbase references is as follow.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## References ##

* [XBRL - By Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html)
