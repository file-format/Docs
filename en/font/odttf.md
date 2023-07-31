{
  "date" : "2023-01-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ODTTF File - Obfuscated OpenType Font File Format",
  "description":"Learn about ODTTF file format and APIs that can create and open ODTTF files.",
  "linktitle" : "ODTTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
    }
  },
  "lastmod" : "2023-01-13"
}

## What is a ODTTF file?

An ODTTF file is a font file format that is utilized by the [.XPS](/page-description-language/xps/) and Microsoft Office 2007 file formats. It contains obfuscated OpenType font that has been modified in order to make it difficult to extract the font's design information or to reverse-engineer the font's source code. ODTTF is based on the fonts used in the original documents but are not in plain format and may not be to read by third-party software to extract font data.

You can open ODTTF files using Pagemark XpsViewer, Apple Safari with Pagemark XpsPlugin, Mozilla Firefox with Pagemark XpsPlugin,
NiXPS View, and NiXPS Edit.

## ODTTF File Format

The internal file format structure of ODTTF file format is not known as these are stored as embedded obfuscated format. These can be embedded in digital documents such as .PDF or .DOCX.

## References
 * [OpenType Font Specifications by Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [TrueType Overview](https://learn.microsoft.com/en-us/typography/truetype/)
