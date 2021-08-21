{
  "date" : "2021-01-21",
  "keywords" : [ "otp file", "otp file format", "what is a otp file", "file", "otp example", "otp file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "OTP - OpenDocument Presentation Template",
  "description":"Learn about OTP file format and APIs that can create and open OTP files.",
  "linktitle" : "OTP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
    }
  },
  "lastmod" : "2021-01-21"
}

## What is an OTP file?

Files with .otp extension represent presentation template files created by applications in OASIS OpenDocument standard format. The contents of such a file include presentation information in the form of slides with text, images, shapes, multimedia content, transition effects and other slide elements. These template files are used for creating new presentations quickly based on the styling information stored in the template itself. OTP files can be created and saved with several different applications such as Impress that comes with OpenOffice suite and Microsoft PowerPoint. The OTP file format is similar to Microsoft PowerPoint template files [.pot](/presentation/pot/) and [.potx](/presentation/potx/).

## OTP File Format

The OTP file format is based on the OpenDocument standard that supports document representation as a single XML document as well as collection of several sub-documents in a single zipped package in the [ZIP](/compression/zip/) format. The contents of the file are distributed in multiple xml files packaged together. These multiple [XML](/web/xml/) files contain information about the style, content, meta information, and settings of the document  as mentioned below.

* `content.xml` – Document content and automatic styles used in the content.
* `styles.xml` – Styles used in the document content and automatic styles used in the styles themselves.
* `meta.xml` – Document meta information, such as the author or the time of the last save action.
* `settings.xml` – Application-specific settings, such as the window size or printer information.

## References

* [OpenDocument - By Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)
