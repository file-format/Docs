{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "bestand", "extensie", "bestandsindeling", "Pagina-indeling", "Encapsulated PostScript"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over EPS-bestandsindeling en API's die EPS-bestanden kunnen maken en openen.",
  "title" :"EPS-bestandsindeling - ingekapseld PostScript-bestand",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een EPS-bestand?

Een .eps-bestand is een afbeeldingsbestand dat op schijf wordt opgeslagen in de bestandsindeling Encapsulated Postscript. Het kan elke combinatie van tekst, afbeeldingen en afbeeldingen bevatten. EPS-bestanden kunnen ook een voorbeeldafbeelding van een bitmap bevatten die is ingekapseld voor weergave door toepassingen die dergelijke bestanden kunnen openen.

## Korte geschiedenis van het EPS-bestandsformaat

Een snelle blik op het EPS-bestandsformaat vanuit het perspectief van de geschiedenis onthult de volgende informatie:

* De eerste versie van EPS werd ergens tussen 1985 en 1988 door Adobe uitgebracht
* Versie 2.0 van de EPS-specificatie werd gepubliceerd in januari 1989
* De specificatie voor versie 3.0 van EPS is in 1992 als apart document gepubliceerd; dit is de laatst gepubliceerde versie.

EPS, in combinatie met het uitbreidingsmechanisme voor Open Structuring Conventions, beschreven in clausule 9 van Adobe's PostScript Language Document Structuring Conventions Specification, vormde de basis van vroege versies van het Adobe Illustrator Artwork-bestandsformaat.

## EPS-bestandsindeling

EPS is een eigen, maar openbaar gedocumenteerd formaat en de specificaties van het EPS-bestandsformaat zijn openbaar beschikbaar ter referentie van de ontwikkelaar. EPS is een [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Document Structuring Convention) conform bestandsformaat en voldoet aan alle regels die door de DSC zijn opgesteld. De DSC is een speciaal bestandsformaat voor PostScript-documenten van Adobe. Elke toepassing die beweert EPS-bestanden te kunnen lezen, moet DSC-compatibel zijn.

Een EPS-bestand bestaat uit twee hoofdgedeelten, zoals hieronder wordt uitgelegd.

### Voorbeeldafbeelding ###

Een typisch EPS-bestand bevat een voorbeeldafbeelding in een indeling die bedoeld is voor gemakkelijk gebruik in een workflow waarbij meerdere systemen of toepassingen betrokken zijn. De bedoeling van een voorvertoning is om een afbeelding te hebben in een formaat dat de meeste grafische toepassingen kunnen weergeven; een voorbeeld heeft meestal een lagere resolutie, in pixelafmetingen en/of in bitdiepte. Het voorbeeldbestand kan een van een aantal formaten hebben. De specificatie voor EPS_3 vermeldt drie "apparaatspecifieke" voorbeeldindelingen:

* voor de Apple Macintosh, een PICT-afbeelding zoals gebruikt door de QuickDraw-toepassing
* voor DOS-computers, een TIFF-bitmap
* Windows-metabestand.

PICT en Windows Metafile kunnen zowel bitmapgegevens als vectorafbeeldingen bevatten. Bovendien definieert de specificatie een zeer eenvoudige apparaatonafhankelijke weergave voor een ingebedde bitmapvoorbeeldafbeelding. Deze weergave staat bekend als Encapsulated PostScript Interchange Format (EPSI).

Een EPSI-voorbeeld is een bitmap weergegeven als ASCII hexadecimaal, verpakt tussen een paar PostScript-opmerkingen ter identificatie en bedoeld om eenvoudig en gemakkelijk te vervoeren te zijn. Om onderscheid te maken tussen EPS-bestanden met de verschillende voorbeeldformaten, werden in de EPS-specificatie verschillende DOS-bestandsextensies en Macintosh-bestandstypes aanbevolen.

### PostScript-code

Het EPS-bestandsformaat moet minimaal het volgende bevatten:

* een koptekst, %!PS-Adobe-3.0 EPSF-3.0
* en een begrenzingsvakcommentaar, %%BoundingBox: llx lly urx ury, dat de grenzen van de illustratie beschrijft. Deze vier argumenten komen overeen met de linkerbenedenhoek (llx, lly) en de rechterbovenhoek (urx, ury) van het selectiekader.

Een EPS-bestand kan geen van de volgende operatoren gebruiken:

* bandapparaat,
* cleardictstack
* Kopieer pagina
* wispagina
* exitserver
* frameapparaat
* grestoreall
* initclip
* initgraphics
* initmatrix
* ontslag nemen
* renderbanden
* setglobal
* setpage-apparaat
* setshared
* startbaan.

## Conversie van EPS naar andere bestandsformaten

EPS-bestanden kunnen worden geconverteerd naar standaard afbeeldingsformaten zoals [JPG](/nl/image/jpeg/), [PNG](/nl/image/png/), [TIFF](/nl/image/tiff/) en [PDF](/nl/pdf/) met verschillende toepassingen zoals Adobe Illustrator, Photoshop en PaintShop Pro.

Vanwege een [beveiligingskwetsbaarheid](https://support.microsoft.com/en-us/office/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) in EPS-bestanden, hebben Office 2016, Office 2013, Office 2010 en Office 365 de mogelijkheid uitgeschakeld om EPS-bestanden in Office-documenten in te voegen.

## Referenties

* [Encapsulated PostScript - Door Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

