{
  "date": "2023-01-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Soubor ODTTF – Zmatený formát souboru písem OpenType",
  "description": "Přečtěte si o formátu souboru ODTTF a rozhraních API, která mohou vytvářet a otevírat soubory ODTTF.",
  "linktitle": "ODTTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-odtt-csf"
}
},
  "lastmod": "2023-01-13"
}

## Co je soubor ODTTF?

An ODTTF file is a font file format that is utilized by the [.XPS](/page-description-language/xps/) and Microsoft Office 2007 file formats. It contains obfuscated OpenType font that has been modified in order to make it difficult to extract the font's design information or to reverse-engineer the font's source code. ODTTF is based on the fonts used in the original documents but are not in plain format and may not be to read by third-party software to extract font data.

Soubory ODTTF můžete otevřít pomocí Pagemark XpsViewer, Apple Safari s Pagemark XpsPlugin, Mozilla Firefox s Pagemark XpsPlugin,
NiXPS View a NiXPS Edit.

## Formát souboru ODTTF

Vnitřní struktura formátu souboru ODTTF není známá, protože jsou uloženy jako vložený obfuskovaný formát. Ty lze vložit do digitálních dokumentů, jako jsou .PDF nebo .DOCX.

## Reference
 * [Specifikace písem OpenType od společnosti Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [Přehled TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

