{
  "date": "2023-01-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODTTF fájl – Obfuszkált OpenType betűtípusfájl formátum",
  "description": "Ismerje meg az ODTTF fájlformátumot és az API-kat, amelyek ODTTF-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle": "ODTTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-odtt-huf"
}
},
  "lastmod": "2023-01-13"
}

## Mi az ODTTF fájl?

An ODTTF file is a font file format that is utilized by the [.XPS](/page-description-language/xps/) and Microsoft Office 2007 file formats. It contains obfuscated OpenType font that has been modified in order to make it difficult to extract the font's design information or to reverse-engineer the font's source code. ODTTF is based on the fonts used in the original documents but are not in plain format and may not be to read by third-party software to extract font data.

Az ODTTF fájlokat a Pagemark XpsViewer, az Apple Safari a Pagemark XpsPlugin, a Mozilla Firefox a Pagemark XpsPlugin használatával nyithatja meg,
NiXPS View és NiXPS Edit.

## ODTTF fájlformátum

Az ODTTF fájlformátum belső fájlformátum-struktúrája nem ismert, mivel ezek beágyazott obfuszkált formátumként vannak tárolva. Ezek beágyazhatók olyan digitális dokumentumokba, mint a .PDF vagy .DOCX.

## Hivatkozások
 * [A Microsoft OpenType betűtípus-specifikációi](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [TrueType áttekintése](https://learn.microsoft.com/en-us/typography/truetype/)

