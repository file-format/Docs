{
  "date": "2019-12-12",
  "keywords": [
"EPS",
"fil",
"udvidelse",
"filformat",
"Sidelayout",
"Indkapslet PostScript"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om EPS-filformat og API'er, der kan oprette og åbne EPS-filer.",
  "title": "EPS-filformat - indkapslet PostScript-fil",
  "linktitle": "EPS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-ep-das"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en EPS fil?

En .eps-fil er en billedfil, der gemmes på disk i Encapsulated Postscript-filformat. Det kan indeholde enhver kombination af tekst, grafik og billeder. EPS-filer kan også indeholde et bitmap-eksempelbillede indkapslet indeni til visning af programmer, der kan åbne sådanne filer.

## Kort historie om EPS-filformat

Et hurtigt kig på EPS-filformat fra historieperspektiv afslører følgende oplysninger:

* Den første version af EPS blev udgivet af Adobe engang mellem 1985 og 1988

* Version 2.0 af EPS-specifikationen blev offentliggjort i januar 1989

* Specifikationen for version 3.0 af EPS blev offentliggjort som et separat dokument i 1992; dette er den seneste offentliggjorte version.


EPS, i kombination med Open Structuring Conventions-udvidelsesmekanismen beskrevet i paragraf 9 i Adobes specifikationer for PostScript Language Document Structurering Conventions, dannede grundlaget for tidlige versioner af Adobe Illustrator Artwork-filformatet.

## EPS filformat

EPS er et proprietært, men offentligt dokumenteret format, og EPS-filformatspecifikationer er tilgængelige offentligt til udviklerens reference. EPS er et [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Document Structuring Convention) i overensstemmelse med filformatet og overholder alle reglerne fastsat af DSC. DSC er et specielt filformat til PostScript-dokumenter fra Adobe. Ethvert program, der hævder at kunne læse EPS-filer, skal være DSC-kompatibelt.

En EPS-fil består af to hovedsektioner som forklaret nedenfor.

### Eksempelbillede ###

En typisk EPS-fil indeholder et eksempelbillede i et format, der er beregnet til praktisk brug i en arbejdsgang, der involverer flere systemer eller applikationer. Hensigten med en forhåndsvisning er at have et billede i et format, som de fleste grafikprogrammer kan gengive; en forhåndsvisning er normalt af lavere opløsning, i pixeldimensioner og/eller i bitdybde. Eksempelfilen kan være i et af en række formater. Specifikationen for EPS_3 viser tre enhedsspecifikke forhåndsvisningsformater:

* til Apple Macintosh, et PICT-billede, som bruges af QuickDraw-applikationen

* for DOS-computere, en TIFF-bitmap

* Windows Metafil.


PICT og Windows Metafile kan inkorporere både bitmapdata og vektorgrafik. Derudover definerer specifikationen en meget enkel enhedsuafhængig repræsentation for et indlejret bitmap-preview-billede. Denne repræsentation er kendt som Encapsulated PostScript Interchange Format (EPSI).

En EPSI preview er en bitmap repræsenteret som ASCII hexadecimal, pakket ind mellem et par PostScript-kommentarer til identifikation og beregnet til at være enkel og let at transportere. For at skelne mellem EPS-filer med de forskellige forhåndsvisningsformater, blev forskellige DOS-filtypenavne og Macintosh-filtyper anbefalet i EPS-specifikationen.

### PostScript-kode

EPS-filformatet skal som minimum indeholde følgende:

* en overskriftskommentar, %!PS-Adobe-3.0 EPSF-3.0

* og en afgrænsningsbokskommentar, %%BoundingBox: llx lly urx ury, der beskriver illustrationens grænser. Disse fire argumenter svarer til de nederste venstre (llx, lly) og øverste højre (urx, ury) hjørner af afgrænsningsrammen.


En EPS-fil kan ikke bruge nogen af følgende operatorer:

* båndenhed,

* cleardictstack

* kopiside

* slette side

* exitserver

*rammeanordning

*grestoreall

*initclip

* initgrafik

* initmatrix

* Afslut

* renderbånd

*setglobal

* sæt sideenhed

* sætdelt

*startjob.


## Konvertering af EPS til andre filformater

EPS-filer kan konverteres til standard billedformater såsom [JPG](/image/jpeg/), [PNG](/image/png/), [TIFF](/image/tiff/) og [PDF](/pdf/) ved hjælp af forskellige programmer, f.eks. Adobe Illustrator, Photoshop og PaintShop Pro.

På grund af en [security vulnerability](https://support.microsoft.com/en-us/office/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) i EPS-filer har Office 2016, Office 2013, Office 2010 og Office 365 deaktiveret muligheden for at indsætte EPS-filer i Office-dokumenter.

## Referencer

* [Encapsulated PostScript - Af Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)


