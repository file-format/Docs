{
  "date" : "2019-12-12",
  "keywords" : [ "EPUB", "file", "extension", "format", "E-Book", "Digital book" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about EPUB file format and APIs that can create and open EPUB files.",
  "title" : "What is an EPUB file?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
    }
  },
  "lastmod" : "2019-12-12"
}

## What is an EPUB file?

Files with .epub extension are an e-book file format that provide a standard digital publication format for publishers and consumers. The format has been so common by now that it is supported by many e-readers and software applications. For example, on Mac OS, the pre-installed **Books** software provides the support for opening such files. In addition, there are a lot of compatible software available for smartphones, tablets and computers. EPUB file standards are maintained by the [International Digital Publishing Forum ](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). The version EPUB 3 is also endorsed by the Book Industry Study Group (BISG), a leading book trade association for standardized best practices, research, information and events, for packaging of content.

## Brief History of EPUB File Format

* **October 2007** - EPUB 2.0 was approved
* **September 2010** - Maintenance update was released
* **October 2011** - EPUB 3.0 specifications became effective
* **June 2014** - Minor maintenance update was released to supersede the 3.0 version
* **January 2017** - EPUB 3.1 became effective

## EPUB File Format

EPUB file format is an archive that can be renamed to [ZIP](/compression/zip/) extension and its contents can be viewed by extracting the archive with any archive extractor. It is an open XML-based format and consists of HTML files, images, CSS style sheets, and other elements. It can also be converted to PDF, Mobi and several other file formats through a number of software applications and APIs.

{{< figure src="../epub.png" alt="EPUB File Format" >}}

**EPUB E-Book opened with Mac OS Books Application**

The EPUB file format is based on following three open standards.

### Open Public Structure (OPS) ###

An EPUB 2.0 file uses XHTML 1.1  to construct the content of a publication. In essence this means that an EPUB file consists of one or more web pages. Even though you could include the entire content of a book or newspaper in a single page, it is better that such a file doesn’t exceed 300K, both for performance and compatibility reasons. Just like with regular web pages, the styling and layout is defined using cascading style sheets (CSS). In EPUB files a subset (limited series of commands) of CSS2 needs to be used. Many of the new features of CSS3, such as rounded boxes or drop shadows, are not available yet. For backwards compatibility, a creator can also use DTBook instead of XHTML to encode the content.

### Open Packaging Format (OPF) ###

This part of the specs deals with structural information such as metadata (who is the author and the publisher, what is the title,..), the manifest (a list of all the files inside an epub file) and the table of contents. These data are all embedded using XML.

### Open Container Format (OCF) ###

As the above descriptions should have made it clear an EPUB document consists of a series of files. The OCF specs define how all those files end up being packaged in one single container file. ZIP compression is used for this.

## Supported Image File Formats ##

The EPUB file format supports the following image file formats.

* [GIF](/image/gif/)
* [JPG](/image/jpeg/)
* [PNG](/image/png/)
* [SVG](/page-description-language/svg/)

## References ##

* [EPUB - By Wikipedia](https://en.wikipedia.org/wiki/EPUB)
