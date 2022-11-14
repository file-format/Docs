{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/X-bestandsindeling",
  "description":"Meer informatie over PDF/X-bestandsindelingen en API's die PDF/X-bestanden kunnen maken en openen.",
  "linktitle" : "PDF/X",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Wat is een PDF/X-bestand? #

PDF/X is een ISO 15930-standaard die in 2001 is gepubliceerd met een subset van PDF-functionaliteit. De norm is opgesteld en gepubliceerd op basis van specifieke vereisten van de drukkerij- en uitgeverijsector. De vereisten voor deze norm zijn allemaal opgesteld volgens de uiteenlopende behoeften van de drukkerij- en uitgeverijsector. PDF/X vereist dat de conforme bestanden volledig zijn, dwz op zichzelf staand. Dit vereist dat elementen zoals lettertypen die op de pagina worden gebruikt, deel moeten uitmaken van het document. Inhoud zoals 3D of video kan geen deel uitmaken van een PDF/X-document. De informatie in het PDF/X-document vereist dat deze nauwkeurig is.

## PDF/X-normen en revisies ##

De PDF/X-familie van standaarden bestaat uit verschillende versies, elk ontworpen voor een gespecialiseerd resultaat. De ontwikkeling van deze normen was bedoeld om tegemoet te komen aan de vele uiteenlopende behoeften van de drukkerij- en uitgeverijsector.

* `PDF/X-1a` - Ook bekend als de eerste standaard van de PDF/X-familie, vereist PDF/X-1a dat alle inhoud deel uitmaakt van het PDF-document om te kunnen worden afgedrukt. Documentelementen zoals lettertypen, formulieren, wachtwoordbeveiliging en zichtbare annotaties zijn niet toegestaan. PDF/X-1a heeft zijn eigen specifieke eisen, zoals die met betrekking tot transparantie en lagen zijn toegestaan. Deze vereisen ook dat printelementen alleen CMYK-, grijswaarden- of steunkleuren gebruiken, wat resulteert in geen gebruik van RGB of apparaatonafhankelijke kleurruimten. is voor uitwisselingen waarbij alle bestanden in CMYK (en/of steunkleuren) moeten worden aangeleverd, zonder RGB of kleurbeheerde gegevens. PDF/X-1a wordt ook wel Complete Exchange genoemd vanwege de volledigheid van de informatie die vereist is door:
* `PDF/X-3` - werd geïntroduceerd in 2002 en heft veel beperkingen van PDF/X-1a op. Hierdoor konden afbeeldingen in een PDF/X-3 op CMYK, grescale, RGB, Lab en ICC gebaseerde kleurruimten gebruiken. Het is eigenlijk gebaseerd op PDF-standaarden 1.3 met [ICC-profiel](https://en.wikipedia.org/wiki/ICC_Profile). Het wordt ook wel Kleurbeheer genoemd vanwege de flexibiliteit en regels die het introduceert met betrekking tot kleuren in een PDF-document.
* `PDF/X-4` - ondersteunt transparanten, dus PDF-X/4 bevat alle gegevens die nodig zijn voor uitvoer zonder afvlakking.
* `PDF/X-5` - is gebaseerd op PDF/X-4 en voegt ondersteuning toe voor externe afbeeldingen via referentie XObjects, evenals externe n-kleurprofielen voor weergave-intentie. Gebruik het voor gedeeltelijke uitwisseling van afdrukgegevens met behulp van PDF-versie 1.6

## Referenties ##

* [PDF/X - Door Wikipedia](https://en.wikipedia.org/wiki/PDF/X)

