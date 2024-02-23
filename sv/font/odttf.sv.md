{
  "date": "2023-01-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODTTF-fil - Obfuscated OpenType Font File Format",
  "description": "Lär dig om ODTTF-filformat och API:er som kan skapa och öppna ODTTF-filer.",
  "linktitle": "ODTTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-odtt-svf"
}
},
  "lastmod": "2023-01-13"
}

## Vad är ODTTF fil?

An ODTTF file is a font file format that is utilized by the [.XPS](/page-description-language/xps/) and Microsoft Office 2007 file formats. It contains obfuscated OpenType font that has been modified in order to make it difficult to extract the font's design information or to reverse-engineer the font's source code. ODTTF is based on the fonts used in the original documents but are not in plain format and may not be to read by third-party software to extract font data.

Du kan öppna ODTTF-filer med Pagemark XpsViewer, Apple Safari med Pagemark XpsPlugin, Mozilla Firefox med Pagemark XpsPlugin,
NiXPS View och NiXPS Edit.

## ODTTF filformat

Den interna filformatsstrukturen för ODTTF-filformatet är inte känd eftersom dessa lagras som inbäddade obfuscerade format. Dessa kan bäddas in i digitala dokument som .PDF eller .DOCX.

## Referenser
 * [OpenType Font Specifications by Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [TrueType-översikt](https://learn.microsoft.com/en-us/typography/truetype/)

