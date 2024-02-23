{
  "date": "2023-01-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODTTF-bestand - Verduisterd OpenType-lettertypebestandsformaat",
  "description": "Meer informatie over de ODTTF-bestandsindeling en API's waarmee ODTTF-bestanden kunnen worden gemaakt en geopend.",
  "linktitle": "ODTTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-odtt-nlf"
}
},
  "lastmod": "2023-01-13"
}

## Wat is een ODTTF-bestand?

An ODTTF file is a font file format that is utilized by the [.XPS](/page-description-language/xps/) and Microsoft Office 2007 file formats. It contains obfuscated OpenType font that has been modified in order to make it difficult to extract the font's design information or to reverse-engineer the font's source code. ODTTF is based on the fonts used in the original documents but are not in plain format and may not be to read by third-party software to extract font data.

U kunt ODTTF-bestanden openen met Pagemark XpsViewer, Apple Safari met Pagemark XpsPlugin, Mozilla Firefox met Pagemark XpsPlugin,
NiXPS-weergave en NiXPS-bewerking.

## ODTTF-bestandsindeling

De interne bestandsindelingsstructuur van het ODTTF-bestandsformaat is niet bekend, omdat deze worden opgeslagen als ingebed, versluierd formaat. Deze kunnen worden ingesloten in digitale documenten zoals .PDF of .DOCX.

## Referenties
 * [OpenType-lettertypespecificaties door Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [TrueType-overzicht](https://learn.microsoft.com/en-us/typography/truetype/)

