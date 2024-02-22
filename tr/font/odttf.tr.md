{
  "date": "2023-01-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODTTF Dosyası - Gizlenmiş OpenType Yazı Tipi Dosya Formatı",
  "description": "ODTTF dosya formatı ve ODTTF dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "linktitle": "ODTTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-odtt-trf"
}
},
  "lastmod": "2023-01-13"
}

## .odttf dosyası nedir?

An ODTTF file is a font file format that is utilized by the [.XPS](/page-description-language/xps/) and Microsoft Office 2007 file formats. It contains obfuscated OpenType font that has been modified in order to make it difficult to extract the font's design information or to reverse-engineer the font's source code. ODTTF is based on the fonts used in the original documents but are not in plain format and may not be to read by third-party software to extract font data.

ODTTF dosyalarını Pagemark XpsViewer, Apple Safari ile Pagemark XpsPlugin, Mozilla Firefox ile Pagemark XpsPlugin kullanarak açabilirsiniz.
NiXPS Görünümü ve NiXPS Düzenleme.

## ODTTF Dosya Formatı

ODTTF dosya formatının dahili dosya formatı yapısı, bunlar gömülü gizlenmiş format olarak depolandığından bilinmemektedir. Bunlar .PDF veya .DOCX gibi dijital belgelere gömülebilir.

## Referanslar
 * [Microsoft'tan OpenType Yazı Tipi Teknik Özellikleri](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [TrueType'a Genel Bakış](https://learn.microsoft.com/en-us/typography/truetype/)

