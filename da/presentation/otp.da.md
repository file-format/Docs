{
  "date": "2021-01-21",
  "keywords": [
"otp fil",
"otp filformat",
"hvad er en otp-fil",
"fil",
"otp eksempel",
"otp filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTP - OpenDocument-præsentationsskabelon",
  "description": "Lær om OTP-filformat og API'er, der kan oprette og åbne OTP-filer.",
  "linktitle": "OTP",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-ot-dap"
}
},
  "lastmod": "2021-01-21"
}

## Hvad er en OTP fil?

Filer med .otp-udvidelse repræsenterer præsentationsskabelonfiler oprettet af applikationer i OASIS OpenDocument-standardformat. Indholdet af en sådan fil omfatter præsentationsinformation i form af dias med tekst, billeder, former, multimedieindhold, overgangseffekter og andre diaselementer. Disse skabelonfiler bruges til hurtigt at skabe nye præsentationer baseret på de stiloplysninger, der er gemt i selve skabelonen. OTP-filer kan oprettes og gemmes med flere forskellige applikationer, såsom Impress, der følger med OpenOffice-pakken og Microsoft PowerPoint. OTP-filformatet ligner Microsoft PowerPoint-skabelonfiler [.pot](/presentation/pot/) og [.potx](/presentation/potx/).

## OTP filformat

OTP-filformatet er baseret på OpenDocument-standarden, der understøtter dokumentrepræsentation som et enkelt XML-dokument samt indsamling af flere underdokumenter i en enkelt zippet pakke i formatet [ZIP](/compression/zip/). Indholdet af filen er distribueret i flere xml-filer pakket sammen. Disse flere [XML](/web/xml/)-filer indeholder oplysninger om stil, indhold, metaoplysninger og indstillinger for dokumentet som nævnt nedenfor.

* `content.xml` – Dokumentindhold og automatiske stilarter, der bruges i indholdet.

* `styles.xml` – Typografier brugt i dokumentindholdet og automatiske typografier brugt i selve typografierne.

* `meta.xml` – Dokument metaoplysninger, såsom forfatteren eller tidspunktet for den sidste gemte handling.

* `settings.xml` – Programspecifikke indstillinger, såsom vinduesstørrelse eller printeroplysninger.


## Referencer

* [OpenDocument - Af Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


