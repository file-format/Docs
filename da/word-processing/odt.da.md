{
  "date": "2019-10-11",
  "keywords": [
"odt fil",
"odt filformat",
"hvad er en odt-fil",
"file",
"ulige eksempel",
"odt filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODT - OpenDocument Text File",
  "description": "Lær om ODT-filformat og API'er, der kan oprette og åbne ODT-filer.",
  "linktitle": "ODT",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-od-dat"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er ODT fil?

ODT-filer er en type dokumenter, der er oprettet med tekstbehandlingsprogrammer, der er baseret på OpenDocument Text File-format. Disse er skabt med tekstbehandlingsprogrammer såsom gratis OpenOffice Writer og kan indeholde indhold som tekst, billeder, objekter og stilarter. ODT-filen er for Writer-tekstbehandleren, hvad [DOCX](/word-processing/docx/) er for Microsoft Word. Adskillige applikationer, herunder Google Docs og Googles webbaserede tekstbehandlingsprogram, der følger med Google Drev, kan åbne ODT-filerne til redigering. Microsoft Word kan også åbne ODT-filer og gemme dem i andre formater såsom [DOC](/word-processing/doc/) og DOCX.

## Kort historie ##

ODP-filformatspecifikationer er baseret på standarden udviklet som ODF-specifikationer. Disse specifikationer har udviklet sig over tidligere i form af tre versioner udviklet og udgivet af OASIS som følger:

**2005** Version 1.0 blev offentliggjort i maj 2005

**2007:** Version 1.1 blev offentliggjort i februar 2007

**2011:** Version 1.2 blev offentliggjort i september 2011

Der var ret små ændringer i overgangen fra ODF 1.0 til 1.1 versioner. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) er den seneste version for ODF-specifikationer og bør konsulteres af udviklere for udvikling af applikationer relateret til ODS-læsning/skrivning.

## Filformatspecifikationer ##

OpenDocument-formatet understøtter dokumentrepræsentation som et enkelt XML-dokument såvel som en samling af flere underdokumenter i en pakke som [ZIP](/compression/zip/)-arkiv. Hver af filerne fra ZIP-arkivet gemmer en del af det komplette dokument. Hvert underdokument gemmer et bestemt aspekt af dokumentet. For eksempel indeholder et underdokument stilinformationen, og et andet underdokument indeholder indholdet af dokumentet. Et typisk ODF-dokument har følgende komponenter:

* content.xml – Dokumentindhold og automatiske stilarter, der bruges i indholdet.

* styles.xml – Typografier brugt i dokumentindholdet og automatiske typografier brugt i selve typografierne.

* meta.xml – Dokument metaoplysninger, såsom forfatteren eller tidspunktet for den sidste gemte handling.

* settings.xml – Applikationsspecifikke indstillinger, såsom vinduesstørrelse eller printeroplysninger.


Udover disse kan der i pakken være mange andre underdokumenter som dokumentminiaturer, billeder osv. Dokumentfiler er delmængden af ODF-filer, hvor indholdet (arkene) er gemt i //content.xml// underdokument.

## Referencer ##

* [OpenDocument - Af Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


