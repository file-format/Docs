{
  "date" : "2021-01-20",
  "keywords" : ["xslt", "File", "Extension", "File Format", "File Extension", "Extensible Stylesheet Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "XSLT File Format",
  "description":"Learn about XSLT file format and APIs that can create and open XSLT files.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-01-20"
}

## What is an XSLT file?

A file with a .xslt extension is an Extensible Stylesheet Language Transformation file that is used to transform and style an XML file using XSL instructions. The format is used to transform XML documents into standard output formats such as a text document or .html web page. This transformation creates a new document based on the content of the existing XML document. XSLT is making it theoretically capable of arbitrary computations.

## XSLT File Format

The XLST file format contains transformation instructions in plain text format that can be viewed in any text editor. There have been three revisions to the language.

* `XSLT 1.0` - XSLT 1.0 was published as a W3C recommendation in November 1999.
* `XSLT 2.0` - It includes modifications such as String manipulation using regular expressions, functions and operators for manipulating dates, times, and durations, multiple output documents, grouping, and a richer type system and strong type checking.
* `XSLT 3.0` - It became part of W3C Recommendation on 8 June 2017 and the main new features include streaming transformation, Packages to improve the modularity of large stylesheets, improved handling of dynamic errors with, for example, an xsl:try instruction, and support for maps and arrays, enabling XSLT to handle JSON as well as XML.

### XSLT Example

The following example is taken from [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## References ##

* [XSLT - By Wikipedia](https://en.wikipedia.org/wiki/XSLT)
* [XSLT Elements](https://en.wikipedia.org/wiki/XSLT_elements)
