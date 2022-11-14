{
  "date" : "2021-05-25",
  "keywords" :[ "DML","DML-bestand", "DML-bestandsformaat", "DML-bestandstype", "bestand", "type", "wat is een DML-bestand" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML - DynaScript HTML-bestand",
  "description":"Meer informatie over DML-bestandsindelingen en API's die DML-bestanden kunnen maken en openen.",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## Wat is een DML-bestand?

Een bestand met de extensie .dml is een codebestand voor webpagina's dat is gemaakt met DyanScript. DynaScript is een dynamische [HTML](/nl/web/html/) scripttaal die compatibel is met ECMAScript en de meeste van dezelfde functies biedt als andere scripttaal. Het is vergelijkbaar met ColdFusion-code en Microsoft Active Server Pages-code (ASP). DML-bestanden kunnen worden geopend en bekeken in standaard webbrowsers die vergelijkbaar zijn met andere HTML-pagina's.

## DML-bestandsindeling

DML-bestanden worden gemaakt in platte tekstbestandsindeling en kunnen worden geopend met een teksteditor om de code te bekijken. Het schrijven van code met behulp van DML-scripttaal kan worden gebruikt om dynamisch HTML te genereren op door de server gehoste DML-pagina's. DynaScripts zijn opgebouwd uit de volgende taalelementen:


* SCRIPT-tag - Deze worden in documenten ingesloten als HTML-opmerkingen. Een HTML-opmerking wordt gemarkeerd door een \ <!-- tag.
* Literals - Dit zijn vaste waarden in DynaScript-bestanden. Voorbeelden hiervan zijn gehele getallen zoals s 123 , 0x3F , 0123, getallen met drijvende komma zoals 456.789 , 3.2e-8, Boolean zoals waar of onwaar, en string zoals "De regen in Spanje"
* Variabelen - DynaScript-variabelen hoeven niet te worden gedefinieerd of aan een vast datatype toe te wijzen. Een variabele moet een waarde hebben voordat u deze in een expressie gebruikt; anders wordt er een runtime-waarschuwing gegenereerd.
* Uitdrukkingen - Dit zijn combinaties van variabelen, letterlijke waarden, operators en andere uitdrukkingen. De rechterkant van een toewijzingsinstructie is een uitdrukking.
* Operators - Deze werken op een of meer uitdrukkingen die operanden worden genoemd. Deze kunnen ternair, binair of unair zijn: ternaire operatoren werken op drie expressies, binaire operatoren werken op twee expressies en unaire operatoren werken op één.
* Verklaringen - Deze controleren de scriptstroom, manipuleren objecten en algemene programmering. Over het algemeen volgen deze instructies de standaard C- en Java-syntaxis. Voorbeelden zijn if-else, do-while loops, switch, break, continue, etc. zoals elke andere scripttaal.
* Functies - Functies, net als elke andere scripttaal, stellen u in staat om een set instructies één keer in een document in te kapselen als een functie, en deze vervolgens meerdere keren in het document te gebruiken (door de functie aan te roepen). DynaScript ondersteunt ook functies.
* Objecten - DynaScript is objectgeoriënteerd en ondersteunt `objecten' en de fundamentele objectgeoriënteerde concepten van inkapseling, polymorfisme en overerving.

