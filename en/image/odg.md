{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ODG File Format",
  "description":"Learn about ODG file format and APIs that can create and open ODG files.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

The ODG file format is used by Apache OpenOffice's Draw application to store drawing elements as a vector image. It follows the XML based file format specifications outlined by Advancement of Structural Information Standards (OASIS). ODG represents drawings as vector images using points, lines and curves. Besides OpenOffice, LibreOffice and other applications also provide support for working with ODG file format. Other formats supported by OpenOffice, for example, include [ODT](/word-processing/odt/), ODF, [ODP](/presentation/odp/) and [ODS](/spreadsheet/ods/).


### ODG File Format Specifications ###

ODG file format is based on OpenDocument format that is structured XML document format with well defined schema.
Each structural component of an OpenDocument format is represented by an element that has associated attributes. The XML based structure is common for all document types such as text document, spreadsheet or a drawing file. A document can contain different styles. An OpenDocument file strucutre consists of the following elements.
  * Document Root
  * Document MetaData
  * Body Element and Document types
  * Application Settings
  * Scripts
  * Font Face Declarations
  * Styles
  * Page Styles and Layouts

##  Document Roots ##

A document root element contains the entire document and is the primary element of a file in OpenDocument format. The same types of document root elements are applicable to to all types of document such as text, documents, spreadsheets and drawing documents.

### Root Elements ###
A single XML document is represented by its own root element. The five different supported root elements are as follow.

`<office:document>` - Complete office document in a singleXML document.
`<office:document-content>` - Document content and automatic styles used in the content.
`<office:document-styles>` - Styles used in the document content and automatic styles used in the styles themselves.
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings>` - Application-specific settings, such as the window size or printer information.

### Document MetatData ###
The OpenDocument contains all metadata elements in the <office:meta> element. This general information about a document is contained at the start of the document and applications can update multiple instances of the same elements.

### Body Element and Document Types ###
The document body indicates the type of content contained in the document using the document type element. These document types are:
  * text documents
  * drawing documents
  * presentation documents
  * spreadsheet documents
  * chart documents
  * image documents

### Application Settings ###
The settings for office applications represent different settings that are related to the document configuration or visual appearance of the document. Each category is represented by a `<config:config-item-set>`. Examples of such setting categories include:
  * Document settings e.g. default printer
  * View Settings e.g. zoom level

### Scripts ###
It is common for a document to contain several scripts. Each script in an OpenDocument file is represented by an `<office:script>` element. These script elements are contained in a single `<office:scripts>` element. Scripts do not update a document while the document is loading.
### Font Face Declarations ###

A font face declaration contains information about the fonts used by the author of a document. This information helps locate these fonts on other systems.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Styles ###
Following styles are supported by the OpenDocument format.

`Common Styles` - The XML representations of such styles are referred to as styles
`Automatic Styles` - Contains formatting properties that, in the user interface view of a document, are assigned to an object such as a paragraph.
`Mater Styles` - a common style that contains formatting information and additional content that is displayed with the document content when the style is applied. An example of a master style are master pages.

## References ##
  * [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
  * [OpenDocument Format - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)
