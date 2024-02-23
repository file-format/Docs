{
  "date": "2023-01-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Plik ODTTF — zaciemniony format pliku czcionek OpenType",
  "description": "Dowiedz się o formacie pliku ODTTF i interfejsach API, które umożliwiają tworzenie i otwieranie plików ODTTF.",
  "linktitle": "ODTTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-odtt-plf"
}
},
  "lastmod": "2023-01-13"
}

## Czym jest plik ODTTF?

An ODTTF file is a font file format that is utilized by the [.XPS](/page-description-language/xps/) and Microsoft Office 2007 file formats. It contains obfuscated OpenType font that has been modified in order to make it difficult to extract the font's design information or to reverse-engineer the font's source code. ODTTF is based on the fonts used in the original documents but are not in plain format and may not be to read by third-party software to extract font data.

Możesz otwierać pliki ODTTF za pomocą Pagemark XpsViewer, Apple Safari z Pagemark XpsPlugin, Mozilla Firefox z Pagemark XpsPlugin,
Widok NiXPS i Edycja NiXPS.

## Format pliku ODTTF

Wewnętrzna struktura formatu pliku ODTTF nie jest znana, ponieważ są one przechowywane w osadzonym, zaciemnionym formacie. Można je osadzić w dokumentach cyfrowych, takich jak .PDF lub .DOCX.

## Bibliografia
 * [Specyfikacje czcionek OpenType firmy Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [Omówienie TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

