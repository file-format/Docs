{
  "date": "2019-10-11",
  "keywords": [
"fodg fil",
"fodg filformat",
"hvad er en fodg-fil",
"fil",
"fodg eksempel",
"fodg filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FODG - OpenDocument Drawing File Format",
  "description": "Lær om FODG filformat og API'er, der kan oprette og åbne FODG filer.",
  "linktitle": "FODG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-fod-dag"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er FODG fil?

En fil med filtypenavnet .fodg er et Apache OpenOffice Drawing-filformat til lagring af tegneelementer. Den er baseret på filformatspecifikationerne skitseret af Advancement of Structural Information Standards (OASIS). Et andet lignende filformat til OpenOffice-grafik er [ODG](/image/odg/), der gemmer tegningselementer som et vektorbillede. FODG-filer kan åbnes med OpenOffice såvel som LibreOffice. Andre filformater, der understøttes af OpenOffice, omfatter f.eks. [ODT](/word-processing/odt/), ODF, [ODP](/presentation/odp/) og [ODS](/spreadsheet/ods/).

## FODG filformat

FODG is based on the OpenDocument's XML file format that conforms to OASIS OpenDocument Format ISO/IEC 26300. Den har Internet Media Type application/vnd.oasis.opendocument.graphics og er også i overensstemmelse med org.oasis-open.opendocument public.composite-content. XML-strukturen er fælles for alle dokumenttyper såsom regneark, tegnefiler og tekstdokumenter. OpenOffice-dokumenter drager fordel af adskillelse af bekymringer ved at adskille indhold, typografier, metadata og applikationsindstillinger i fire separate XML-filer.

`<office:document-content> ` - Dokumentindhold og automatiske stilarter, der bruges i indholdet.
`<office:document-styles> ` - Typografier brugt i dokumentindholdet og automatiske typografier brugt i selve typografierne.
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings> ` - Programspecifikke indstillinger, såsom vinduesstørrelse eller printeroplysninger.

## Referencer ##
 * [Future Specifications for v 1.3 Standardization ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
 * [OASIS Open Document Format for Office-applikationer](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
 * [OpenDocument Format - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

