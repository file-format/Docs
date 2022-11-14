{
  "date" : "2019-10-11",
  "keywords" :[ "gbr-bestand", "gbr-bestandsindeling", "wat is een gbr-bestand", "bestand", "gbr-voorbeeld", "gbr-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GBR-bestandsindeling - Gerber-bestandsindeling voor PCB",
  "description":"Meer informatie over GBR-bestandsindeling en API's die GBR-bestanden kunnen maken en openen.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een GBR-bestand?

Een bestand met de extensie .gbr is een Gerber-beeldbestandsindeling voor de uitwisseling van ontwerpgegevensoverdracht van printplaten (PCB's). Het is ontwikkeld door Ucamco. PCB-ontwerpgegevens zijn het belangrijkste onderdeel dat de fabricage-industrie nodig heeft voor verwerking. Een GRB-bestand bevat PCB-gegevens zoals koperlagen, soldeermasker, legenda en boor- en routegegevens. Het kan worden gebruikt om gegevens, zoals PCB-fabricagekenmerken, inclusief dikte of afwerking, in een gestandaardiseerd formaat over te dragen. Alle PCB-ontwerpsystemen voeren Gerber-bestanden uit die kunnen worden verwerkt door PCB-fabricagesystemen. GBR-bestanden zijn nu de de facto standaard geworden voor de overdracht van ontwerpgegevens van printplaten (PCB's). Ucamco heeft een [gratis online viewer](https://gerber-viewer.ucamco.com/) ter beschikking gesteld om GBR-bestandsindelingen te openen en te bekijken.

## GBR-bestandsindeling

GBR is een UTF-8 door mensen leesbaar formaat dat uit slechts 27 opdrachten bestaat. Vanwege deze korte lijst met opdrachten en de compactheid ervan, is GBR gemakkelijk te debuggen. Gerber is in de kern een open vectorformaat voor 2D binaire afbeeldingen. Meta-informatie wordt via Attributen bij de afbeeldingen overgedragen. Een enkel GRB-bestand specificeert een enkele afbeelding en vereist geen begeleidende bestanden of externe parameters om te worden geïnterpreteerd. Eén afbeelding heeft slechts één bestand nodig. Het gebruikt 7-bits ASCII-tekens voor alle opdrachten en namen die in de specificatie zijn gedefinieerd en die kunnen worden afgedrukt. Dit dekt volledig de volledige beeldgeneratie.

### Voorbeeld GBR-bestand

Hieronder volgt een voorbeeld Gerber-bestand dat een cirkel met een diameter van 1,5 mm maakt, gecentreerd op de oorsprong. Er is één commando per regel.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Referenties

* [Gerber-formaat](https://www.ucamco.com/en/gerber)

