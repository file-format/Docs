{
  "date": "2021-01-21",
  "keywords": [
"ai fil",
"ai filformat",
"hvad er en ai-fil",
"fil",
"et eksempel",
"ai filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AI - Adobe Illustrator Artwork File",
  "description": "Lær om AI-filformat og API'er, der kan oprette og åbne AI-filer.",
  "linktitle": "AI",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-a-dai"
}
},
  "lastmod": "2021-01-21"
}

## Hvad er en AI fil?

A file with an .ai extension is an Adobe Illustrator Artwork file that contains vector graphics in a single page. it uses points to create paths for displaying the image data, thus making it safe from losing image quality if it is enlarged. AI file format is base don the PGF file format which are similar to AI files. AI format finds its major usage for logos and print media, and its initial versions were considered similar to that of [EPS](/page-description-language/eps/) files. AI files can be opened with Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro, and CorelDraw Graphics tools.

## AI filformat

AI er Adobe Illustrators proprietære filformat og bruger den dobbelte sti-tilgang svarende til PGF til at gemme EPS-kompatible filer. [Adobe Illustrator File Format specifications](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) giver en detaljeret udviklerreference for interne detaljer om dette filformat. Alle dokumenter (filer) oprettet af Adobe Illustrator er PostScript-sprogdokumenter og har to hoveddele, der er i overensstemmelse med dokumentstruktureringskonventionerne: en prolog og et script.

### Prolog

Prolog-afsnittet indkapsler oplysninger, der kræves til fortolkning af filen. Et eksempel kunne være den afgrænsningsramme, der indeholder alle mærkerne på siden. Den indeholder også ressourceoplysninger såsom skrifttyper og proceduredefinitioner. Disse ressourcer er logisk grupperet i sæt kaldet procsets og indeholder eksplicitte metoder til initialisering og afslutning af deres procedurer.

### Manuskript

Grafiske elementer på siden er beskrevet af scriptet. Et script indeholder referencer til operatørerne og procedurerne i prologen sammen med operander og data. De tre logiske sektioner af et script inkluderer:

 * Setup Sequence - der initialiserer og aktiverer de ressourcer, der er defineret i prologen
 * Sekvens af beskrivende operatorer
 * Trailer, der deaktiverer ressourcer

Operatører i scriptet er sekvenser af grafiske elementer skrevet på det sprog, der er defineret af procsets i prologen. Disse sekvenser består af samlinger af dataelementer, grafiske attributdefinitioner og kald til de procedurer, der er defineret i procedurerne.

### Objektmærker

Objektmærker bruges til at vedhæfte tilpassede oplysninger til et Adobe Illustrator-kunstobjekt. Tags består af en:

 * Tag-id
 * Tag type
 * Data

## Referencer
* [Adobe Illustrator filformatspecifikationer](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)

* [AI-filformat af PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)


