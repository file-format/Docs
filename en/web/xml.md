{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "XML File Format",
  "description":"Learn about XML file format and APIs that can create and open XML files.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an XML file?

XML stands for Extensible Markup Language that is similar to **[HTML](/web/html/)** but different in using tags for defining objects. The whole idea behind creation of XML file format was to store and transport data without being dependent on software or hardware tools. Its popularity is due to it being both human as well as machine readable. This enables it to create common data protocols in the form of objects to be stored and shared over network such as World Wide Web (WWW). The "X" in XML is for extensible which implies that the language can be extended to any number of symbols as per user requirements. It is for these features that many standard file formats make use of it such as Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/web/xhtml/)** and **[SVG](/page-description-language/svg/)**.

## XML File Format

The XML file format is based on the XML Document Object Model (DOM) that is a programming API for HTML and XML documents. The XML DOM defines a standard method to access and manipulate the XML document elements. It makes a tree-structure view of an XML document that can be used to access all elements through the DOM tree. Existing elements can be modified/deleted as well as new elements can be created in the XML tree. Each element of an XML document is called a node. The XML DOM is as shown in the following image.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### Universal approach of XML

The power of XML makes it a universal language for data communication over the network by making data transport and platform changes simplified. This also makes sure exchange data between incompatible systems possible by storing data in plain text format. HTML is for data representation over the web, whereas XML is for exchange of data. The markup tag pairs used inside XML define the key elements of the structure to be utilized by reading applications.

## XML Example

The following is a simplified example of a CD catalog where each record contains information about CDs such as artist, country, company, price and year of production.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## How to open XML file?

|Operating System| Software|
---|---|
|Windows| Internet Explorer, Adobe Dreamweaver 2020, Notepad++, Microsoft Visual Studio 2019|
|Mac| TextEdit, Microsoft Visual Studio 2019, Adobe Dreamweaver 2020|

## References

* [XML - By Wikipedia](https://en.wikipedia.org/wiki/XML)
* [XML - W3Schools.com](https://www.w3schools.com/xml/xml_whatis.asp)
