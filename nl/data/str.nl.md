{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "STR-bestand - dBASE-structuurlijstobjectbestand - Wat is een .str-bestand en hoe kunt u het openen?",
  "description" : "Leer meer over het STR dBASE Structuurlijstobjectbestand en hoe u dit kunt openen.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-nl",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Wat is een STR-bestand?

STR-bestandsindeling wordt vaak geassocieerd met dBASE, een databasebeheersysteem. In dBASE vertegenwoordigt een .str-bestand doorgaans een structuurlijstobjectbestand. Dit bestand bevat de structuur van een databasetabel, inclusief informatie over velden (kolommen) en hun eigenschappen.

Het structuurlijstobjectbestand (.str) bevat metagegevens zoals veldnamen, gegevenstypen, veldlengtes en andere eigenschappen die aan elk veld in de databasetabel zijn gekoppeld. Het wordt gebruikt om de structuur van de databasetabel te definiëren zonder daadwerkelijke gegevensrecords te bevatten.

Programma's zoals dBASE of andere tools voor databasebeheer kunnen dit bestand gebruiken om de lay-out van de databasetabel te begrijpen en bewerkingen uit te voeren zoals het opvragen, bijwerken of maken van nieuwe records op basis van deze structuur.

Hier is een eenvoudig voorbeeld van wat een STR-bestand zou kunnen bevatten:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Dit voorbeeld beschrijft een tabel met vier velden: ID, Naam, Leeftijd en Geboortedatum, samen met hun respectieve gegevenstypen en lengtes.

## Hoe open je een STR-bestand?

De belangrijkste manier om .str-bestanden te openen is door dBASE zelf te gebruiken, vooral op Windows-besturingssystemen. dBASE kan de inhoud van deze bestanden lezen en interpreteren, waardoor gebruikers de databasestructuur kunnen bekijken en ermee kunnen werken.

Omdat .str-bestanden in wezen gewone tekstbestanden zijn die informatie bevatten over de structuur van de database, kunt u ze ook openen met een teksteditor. Voorbeelden van teksteditors zijn Microsoft Notepad op Windows en Apple TextEdit op Mac. Wanneer u het in een teksteditor opent, kunt u de inhoud van het bestand bekijken, inclusief veldnamen, gegevenstypen en andere structurele informatie, in een voor mensen leesbaar formaat.

## Referenties
* [dBase](https://en.wikipedia.org/wiki/DBase)


