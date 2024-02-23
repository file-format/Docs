{
  "date": "2023-01-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Arquivo ODTTF - Formato de arquivo de fonte OpenType ofuscado",
  "description": "Saiba mais sobre o formato de arquivo ODTTF e APIs que podem criar e abrir arquivos ODTTF.",
  "linktitle": "ODTTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-odtt-ptf"
}
},
  "lastmod": "2023-01-13"
}

## O que é um arquivo .ODTTF?

An ODTTF file is a font file format that is utilized by the [.XPS](/page-description-language/xps/) and Microsoft Office 2007 file formats. It contains obfuscated OpenType font that has been modified in order to make it difficult to extract the font's design information or to reverse-engineer the font's source code. ODTTF is based on the fonts used in the original documents but are not in plain format and may not be to read by third-party software to extract font data.

Você pode abrir arquivos ODTTF usando Pagemark XpsViewer, Apple Safari com Pagemark XpsPlugin, Mozilla Firefox com Pagemark XpsPlugin,
Visualização NiXPS e Edição NiXPS.

## Formato de arquivo ODTTF

A estrutura interna do formato de arquivo do formato de arquivo ODTTF não é conhecida, pois são armazenados como formato ofuscado incorporado. Eles podem ser incorporados em documentos digitais como .PDF ou .DOCX.

## Referências
 * [Especificações de fonte OpenType da Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [Visão geral do TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

