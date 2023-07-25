{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PDF/A File Format",
  "description":"Learn about PDF/A file format and APIs that can create and open PDF/A files.",
  "linktitle" : "PDF/A",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
    }
  },
  "lastmod" : "2019-09-10"
}

# What is PDF/A? #

PDF/A is an ISO standard format for archiving of electronic documents in PDF format. Its primary reason for coming into being was to meet the requirements of long term archiving. The standard ensures the opening of archived files even after long time by imposing certain limitations on document integral parts to achieve conformance. The format is now widely adopted across all industries . PDFA/A viewers like Adobe Acrobat Reader, ensure that files saved with this format can be opened even in future in accordance with the information shared by this Standard.

## PDF/A Versions ##

PDF/A was accepted as ISO Standard in October 2005. Since then, it has been under continuous enhancement and several further standards have been developed with the passage of time. Information about PDF/A standards published with the passage of time and their details are as follow:

* **PDF/A-1:** published in Oct 2005 as ISO 19005-1 and is based on PDF 1.4
* **PDF/A-2:** published in Jun 2011 as ISO 19005-2 and is based on PDF 1.7 (ISO 32000-1:2008)
* **PDF/A-3:** published in Oct 2012 as ISO 19005-3 and is based on PDF 1.7 (ISO 32000-1:2008)

## PDF/A-1 ##

The PDF/A-1 standard was based on the original PDF 1.4 version. The PDF/A-1 standard defines two levels of conformance for PDF files.

### PDF/A-1a ###

It is in conformance with Level A and satisfies all requirements in the specifications of PDF/A-1 Standard. PDF/A-1a ensures that text is extractable from the document. It also guarantees that the natural reading process of integrated text material remain intact. PDF/A imposes the requirement for the ability of text representation on reduced screens by being restructured which is known as "tagged PDF". It was intended to increase the accessibility of conforming files for physically impaired users by allowing assistive software.

### PDF/A-1b ###

PDF/A-1b is a lower level of conformance and deals with the with the visual appearance of electronic documents with respect to the ISO 19005 standard. It ensures that text and other content on pages is reproduced uniformly. This Level B conformance indicates minimal compliance to ensure that the rendered visual appearance of a conforming file is preservable over the long term.

## PDF/A-2 ##

PDF/A-2 was released by ISO Standard in July 2011 as a new standard known as ISO 32001-1. This new standard not only benefited from all the features of PDF versions uptil 1.7, but also was introduced as a new standard. PDF/A-2 included the following features as part of this new standard.

* PDF/A-2 comes with the support of [JPEG2000](/image/jp2/) that is helpful in case of scanned documents.
* It supports embedding of PDF/A collections that can be used to created a container PDF having other similar files
* It supports transparency feature of PDF files in totality as compared to PDF/A-1 where it was partially supported.
* PDF/A-2 provides the support for optional content that is useful for mapping applications and engineering drawings. These are also known as layers that can be made visible or hidden as per the requirements of viewing person.
* It specifies the requirements for custom XMP metadata
* Adds some of the newer comment types to the list of prohibited annotation types. In addition, some of the newer comment types such as  text editing comments were added to the list of acceptable items.

## PDF/A-3 ##

 PDF/A-3 includes all the conformance requirements of Level 2 and allows embedding of additional file formats (such as XML, [CSV](/spreadsheet/csv/), [CAD](/cad/), [word-processing](/word-processing/) , [spreadsheet](/spreadsheet/) and others) into the PDF/A conforming documents.

## References ##

* [PDF/A - By Wikipedia](https://en.wikipedia.org/wiki/PDF/A)
* [White Paper: PDF/A – The Basics](https://www.pdf-tools.com/public/downloads/whitepapers/whitepaper-pdfa.pdf)
