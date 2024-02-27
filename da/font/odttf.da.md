{
  "date": "2023-01-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODTTF-fil - sløret OpenType-skrifttypefilformat",
  "description": "Lær om ODTTF filformat og API'er, der kan oprette og åbne ODTTF filer.",
  "linktitle": "ODTTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-odtt-daf"
}
},
  "lastmod": "2023-01-13"
}

## Hvad er ODTTF fil?

An ODTTF file is a font file format that is utilized by the [.XPS](/page-description-language/xps/) and Microsoft Office 2007 file formats. It contains obfuscated OpenType font that has been modified in order to make it difficult to extract the font's design information or to reverse-engineer the font's source code. ODTTF is based on the fonts used in the original documents but are not in plain format and may not be to read by third-party software to extract font data.

Du kan åbne ODTTF-filer ved hjælp af Pagemark XpsViewer, Apple Safari med Pagemark XpsPlugin, Mozilla Firefox med Pagemark XpsPlugin,
NiXPS View og NiXPS Edit.

## ODTTF filformat

Den interne filformatstruktur af ODTTF-filformatet er ikke kendt, da disse er gemt som indlejret sløret format. Disse kan indlejres i digitale dokumenter såsom .PDF eller .DOCX.

## Referencer
 * [OpenType Font Specifications fra Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [TrueType Oversigt](https://learn.microsoft.com/en-us/typography/truetype/)

