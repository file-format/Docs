{
  "date": "2019-12-03",
  "keywords": [
    "DOCX",
    "file",
    "format",
    "file type",
    "extension",
    "what is an DOCX file?"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "DOCX",
  "description": "Learn about DOCX file format and APIs that can create and open DOCX files.",
  "linktitle": "DOCX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-docx"
    }
  },
  "lastmod": "2019-12-03"
}

## What is a DOCX file? ##

DOCX is a well-known format for Microsoft Word documents. Introduced from 2007 with the release of Microsoft Office 2007, the structure of this new Document format was changed from plain binary to a combination of XML and binary files. Docx files can be opened with Word 2007 and lateral versions but not with the earlier versions of MS Word which support DOC file extensions.

## Brief History ##

After Microsoft opened the specifications for the DOC file format, it was easy for its competitors to reverse engineer the format and provide the same support in their own applications. In addition, the competition from Open Office in the form of its Open Document Format, compelled Microsoft to adopt more open and wide standards. It was in early 2000 when Microsoft decided to go for the change to accommodate the standard for **Office Open XML**. Documents under this new Standard were given [.docx extension](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), the "X" being for XML. By 2007, this new file format became part of Office 2007 and is carried on in the new versions of Microsoft Office as well. The new file type has added advantages of small file sizes, fewer changes of corruption and well-formatted images representation.

## DOCX File Format Specifications - More Information

A Docx file comprises of a collection of XML files that are contained inside a ZIP archive. The contents of a new Word document can be viewed by unzipping its contents. The collection contains a list of XML files that are categorized as:

* MetaData Files - contains information about other files available in the archive
* Document - contains the actual contents of the document

### Metadata Files ###

Microsoft Word uses these files to find the relationship between files and to locate the document contents. When a Word document archive is extracted, it contains a number of such files as detailed below.

#### Relationships - \_rels/.rels ####

This file contains information that tells MS Word where to look for the document contents and other references. Each relationship is identified by a unique relationship id and specifies the referenced XML file as target. A sample relationship file is shown as follow:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### Content Types ####

A document can contain several media types inside like images, themes, word art, etc. The [Content_Types].xml contains information about such media types present in the document. Contents of a such an XML file are shown as follow:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### References To Resources - \_rels/document.xml.rels ####

Information about resources, such as images embedded in the document, are referenced in this XML file.

#### Main Document Contents ####

This refers to the main XML file of the archive that contains the document's text content. This content is represented by variety of nodes as per the OpenOffice XML specifications. Mostly the contents of this file consist of Paragraphs and Tables, though their can be other nodes as well.

### File Format Nodes ###

The main document.xml file is a collection of nodes for representation of the overall contents of a file. Each node has a start and end that encapsulates either further nodes or the contents. A simplified example of such an xml file is as follow:

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

Following is the information about some of the nodes contained in a DOCX file for representation of contents.

`<w:document>` - Represents the root element of the main content of the file.

`<w:body>` -  Represents the body of the document which can comprise of many other element nodes such as paragraphs, tables and sections.

#### Paragraphs ####

A paragraph is the main content holder within a document. It is represented by **<w:p>** element within a document. A paragraph further consists of one or more runs **<w:r>** that contains the actual text of the paragraph. In addition to runs, paragraphs may also contain other document elements such as hyperlinks, comments, etc. An example paragraph structure is as shown below:

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## DOCX FAQs

 * **Is DOCX a File Extension?** - DOCX is used as file extension to represent Microsoft Word 2007 and later file formats used to store Word files. It also tells your OS that this DOCX file requires Microsoft Word 2007 to open it and show its icon.
 * **Is DOCX same as Word** - DOCX is a file format used by Microsoft Word to save documents in Open XML format. Word, on the other hand, is an application software by Microsoft Office that also supports other file formats such as DOC, DOT, DOTM, and others.
 * **What is difference DOC and DOCX** - DOC is word file saved in Word 2007 and earlier file format. DOCX is based on Open XML file format supported by Microsoft 2007 and later versions. Check [Differences between DOC and DOCX](https://blog.fileformat.com/2022/08/11/doc-vs-docx/) for more details.

## References ##

* [MS - DOCX File Format](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)
