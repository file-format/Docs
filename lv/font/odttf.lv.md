{
  "date": "2023-01-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODTTF fails — obfuskēts OpenType fonta faila formāts",
  "description": "Uzziniet par ODTTF faila formātu un API, kas var izveidot un atvērt ODTTF failus.",
  "linktitle": "ODTTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-odtt-lvf"
}
},
  "lastmod": "2023-01-13"
}

## Kas ir ODTTF fails?

An ODTTF file is a font file format that is utilized by the [.XPS](/page-description-language/xps/) and Microsoft Office 2007 file formats. It contains obfuscated OpenType font that has been modified in order to make it difficult to extract the font's design information or to reverse-engineer the font's source code. ODTTF is based on the fonts used in the original documents but are not in plain format and may not be to read by third-party software to extract font data.

Varat atvērt ODTTF failus, izmantojot Pagemark XpsViewer, Apple Safari ar Pagemark XpsPlugin, Mozilla Firefox ar Pagemark XPSPlugin,
NiXPS View un NiXPS Edit.

## ODTTF faila formāts

ODTTF faila formāta iekšējā faila formāta struktūra nav zināma, jo tie tiek glabāti kā iegultais obfuscēts formāts. Tos var iegult digitālos dokumentos, piemēram, .PDF vai .DOCX.

## Atsauces
 * [OpenType fontu specifikācijas no Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [TrueType pārskats](https://learn.microsoft.com/en-us/typography/truetype/)

