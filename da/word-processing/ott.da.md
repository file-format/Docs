{
  "date": "2019-10-11",
  "keywords": [
"ott fil",
"ott filformat",
"hvad er en ott-fil",
"fil",
"ott eksempel",
"ott filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTT - OpenDocument Template File",
  "description": "Lær om OTT-filformat og API'er, der kan oprette og åbne OTT-filer.",
  "linktitle": "OTT",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-ot-dat"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en OTT fil?

Filer med OTT-udvidelse repræsenterer skabelondokumenter genereret af applikationer i overensstemmelse med OASIS' OpenDocument-standardformat. Disse er oprettet med tekstbehandlingsprogrammer såsom gratis OpenOffice Writer og kan indeholde indstillinger, der kan bruges til at generere nye dokumenter fra disse skabelonfiler. Disse indstillinger omfatter sidemargener, kanter, sidehoveder, sidefødder og andre sideindstillinger. Sådanne skabeloner bruges i officielle dokumenter såsom firmabrevpapir og standardiserede formularer.

## Kort historie ##

ODP-filformatspecifikationer er baseret på standarden udviklet som ODF-specifikationer. Disse specifikationer har udviklet sig over tidligere i form af tre versioner udviklet og udgivet af OASIS som følger:

**2005:** Version 1.0 blev offentliggjort i maj 2005

**2007:** Version 1.1 blev offentliggjort i februar 2007

**2011:** Version 1.2 blev offentliggjort i september 2011

Der var ret små ændringer i overgangen fra ODF 1.0 til 1.1 versioner. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) er den seneste version for ODF-specifikationer og bør konsulteres af udviklere for udvikling af applikationer relateret til ODS-læsning/skrivning.

## Filformatspecifikationer

OpenDocument-formatet understøtter dokumentrepræsentation som et enkelt XML-dokument såvel som en samling af flere underdokumenter i en pakke som [ZIP](/compression/zip/)-arkiv. Hver af filerne fra ZIP-arkivet gemmer en del af det komplette dokument. Hvert underdokument gemmer et bestemt aspekt af dokumentet. For eksempel indeholder et underdokument stilinformationen, og et andet underdokument indeholder indholdet af dokumentet. Et typisk ODF-dokument har følgende komponenter:

* content.xml – Dokumentindhold og automatiske stilarter, der bruges i indholdet.

* styles.xml – Typografier brugt i dokumentindholdet og automatiske typografier brugt i selve typografierne.

* meta.xml – Dokument metaoplysninger, såsom forfatteren eller tidspunktet for den sidste gemte handling.

* settings.xml – Applikationsspecifikke indstillinger, såsom vinduesstørrelse eller printeroplysninger.


Udover disse kan der i pakken være mange andre underdokumenter som dokumentminiaturer, billeder osv. Dokumentfiler er delmængden af ODF-filer, hvor indholdet (arkene) er gemt i //content.xml// underdokument.

## Referencer ##

* [OpenDocument - Af Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


