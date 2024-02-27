{
  "date": "2019-10-11",
  "keywords": [
"odp fil",
"odp filformat",
"hvad er en odp-fil",
"fil",
"odp eksempel",
"odp filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODP - OpenOffice Presentation File Format",
  "description": "Lær om ODP-filformat og API'er, der kan oprette og åbne ODP-filer.",
  "linktitle": "ODP",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-od-dap"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en ODP fil?

Filer med filtypenavnet .odp repræsenterer præsentationsfilformatet brugt af OpenOffice.org i OASISOpen-standarden. En præsentationsfil er en samling af dias, hvor hvert dias kan bestå af tekst, billeder, formatering, animationer og andre medier. Disse slides præsenteres for publikum i form af slideshows med tilpassede præsentationsindstillinger. ODP-filer kan åbnes af programmer, der er i overensstemmelse med OpenDocument-formatet (såsom OpenOffice eller StarOffice).

## Kort historie

ODP-filformatspecifikationer er baseret på standarden udviklet som ODF-specifikationer. Disse specifikationer har udviklet sig over tidligere i form af tre versioner udviklet og udgivet af OASIS som følger:

`2005` - Version 1.0 blev offentliggjort i maj 2005
`2007` - Version 1.1 blev offentliggjort i februar 2007
`2011` - Version 1.2 blev offentliggjort i september 2011

Der var ret små ændringer i overgangen fra ODF 1.0 til 1.1 versioner. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) er den seneste version for ODF-specifikationer og bør konsulteres af udviklere for udvikling af applikationer relateret til ODS-læsning/skrivning.

## Filformatspecifikationer

OpenDocument-formatet understøtter dokumentrepræsentation som et enkelt XML-dokument såvel som en samling af flere underdokumenter i en pakke som [ZIP](/compression/zip/)-arkiv. Hver af filerne fra ZIP-arkivet gemmer en del af det komplette dokument. Hvert underdokument gemmer et bestemt aspekt af dokumentet. For eksempel indeholder et underdokument stilinformationen, og et andet underdokument indeholder indholdet af dokumentet. Et typisk ODF-dokument har følgende komponenter:

* `content.xml` – Dokumentindhold og automatiske stilarter, der bruges i indholdet.

* `styles.xml` – Typografier brugt i dokumentindholdet og automatiske typografier brugt i selve typografierne.

* `meta.xml` – Dokument metaoplysninger, såsom forfatteren eller tidspunktet for den sidste gemte handling.

* `settings.xml` – Programspecifikke indstillinger, såsom vinduesstørrelse eller printeroplysninger.


Udover disse kan der i pakken være mange andre underdokumenter som dokumentminiature, billeder osv.

Regnearksdokumentfiler er den delmængde af ODF-filer, hvor indholdet (arkene) er gemt i content.xml-underdokumentet.

## Referencer

* [OpenDocument - Af Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


