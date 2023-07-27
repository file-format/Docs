{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "Bestand", "Formaat", "Open", "Lezen", "API", "MicroStation", "Intergraph Interactive Graphics Design System"],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - MicroStation CAD-ontwerpbestandsformaat",
  "description" :"Meer informatie over DGN-bestandsindeling en API's die DGN-bestanden kunnen maken en openen.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## Wat is een DGN-bestand?

Een bestand met de extensie .dgn (Design) is een tekenbestand gemaakt door en ondersteund door CAD-toepassingen zoals MicroStation en Intergraph Interactive Graphics Design System. Het wordt gebruikt voor het maken en opslaan van ontwerpen voor bouwprojecten zoals snelwegen, bruggen en gebouwen. Het formaat is vergelijkbaar met het [DWG](/nl/cad/dwg/) bestandsformaat van Autodesk en wordt als zijn concurrent beschouwd. DNG-bestanden kunnen worden opgeslagen als Intergraph Standard File Format of V8 DGN. DGN kan worden geconverteerd naar verschillende andere formaten zoals DWG, [BMP](/nl/image/bmp/), [JPEG](/nl/image/jpeg/), [PDF](/nl/pdf/), [GIF](/nl/image/ gif/) en anderen. Het kan worden geopend met Autodesk AutoCAD, Bentley View en Bentley Systems MicroStation, naast andere softwaretoepassingen zoals Corel PaintShop Photo Pro en IMSI TurboCAD Deluxe-versies.

## V8 DGN-bestandsindeling

Een MicroStation V8 DGN-bestand bestaat uit een of meer modellen. Een model is een container voor elementen. De V8 DGN verwijdert alle op bestandsindelingen gebaseerde beperkingen die aanwezig waren in eerdere versies van MicroStation. Hieronder volgt een lijst met verbeteringen in het DGN-bestandsformaat.

* Limiet op het aantal niveaus in een DGN-bestand is verwijderd en elk niveau wordt benoemd en opgeslagen als een element.
* De maximale fysieke grootte van het DGN-bestand heeft geen beperking en wordt alleen beperkt door het besturingssysteem (zoals de NT-limiet is 4 GB)
* De maximale grootte van een enkel element is 128 KB.
* Er is geen limiet aan de maximale grootte van een cel.
* Celnamen zijn beperkt tot ongeveer 500 tekens.
* Er is geen limiet aan het aantal referenties dat aan een DGN-bestand kan worden toegevoegd.
* Een lijnreeks, vorm of puntcurve kan tot 5000 hoekpunten hebben.
* Er is geen limiet aan het aantal componenten in een complexe ketting of complexe vorm.
* Er is geen limiet aan het aantal grafische groepen in een DGN-bestand.
* Het hekwerk staat evenwijdig aan het aanzicht waarin het is geplaatst.
* Een enkele regel tekst kan 65.535 tekens bevatten.
* Er is geen limiet aan de maximale grootte van een tekstknooppunt.
* Er is geen limiet aan het aantal tekstknooppunten in een DGN-bestand.
* Elk element heeft een unieke 64-bits identifier die niet verandert gedurende de levenscyclus van het element.
* Elk element heeft een tijdstempel die het tijdstip van de meest recente wijziging aangeeft.

## Referenties

* [DNG - Door Wikipedia](https://en.wikipedia.org/wiki/DGN)
* [MicroStation V8 DGN-bestandsindeling](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

