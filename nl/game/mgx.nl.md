{
  "date" : "2021-09-08",
  "keywords" :[ "mgx-bestand", "mgx-bestandsindeling", "wat is een mgx-bestand", "bestand", "mgx-voorbeeld", "mgx-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over Age of Empires 2 Expansion Replay MGX-bestandsindeling en API's die MGX-bestanden kunnen maken en openen.",
  "title" :"MGX - Age of Empires 2 uitbreidingsherhaling",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Wat is een MGX-bestand?

Een bestand met de extensie .mgx is een opgenomen bestand voor Age of Empires II: The Conquerors-spel dat kan worden afgespeeld in het Age of Empires II-programma. Het bevat een volledige opname van de door de gebruiker gespeelde campagne. Het kan worden geladen en afgespeeld in het Age of Empires II-programma. Eenmaal opnieuw gespeeld, toont de game alle gebeurtenissen en scenario's die de gebruiker voor de campagne heeft gepland en gespeeld.

## MGX-bestandsindeling - Meer informatie

Het interne bestandsformaat van het MGX-bestand is uitgewerkt en beschikbaar als gedeeltelijk gevalideerde informatie op [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format). De specificaties beschrijven de details in de volgende secties.

### Structuurdefinities

De structuurdefinities van het GPX-bestandsformaat worden verondersteld te zijn gebaseerd op de [BinData Ruby Gem-declaraties](https://github.com/dmendel/bindata/wiki) die een manier bieden om gestructureerde binaire gegevens te lezen en te schrijven. Hierdoor kan de programmeur het formaat van de binaire gegevens specificeren die vervolgens door BinData worden gelezen en geschreven.

### MGX-berichten

De MGX-berichten zijn gebaseerd op twee soorten berichten.

* GAMESTART - specificeert de startcommando's van het spel en is tot op heden niet gevalideerd
* CHAT - beschrijft de in-game chatberichten. Zowel spelers als het spel zelf (Gaia) kunnen in-game berichten uitzenden.

### GAMEPLAY-ACTIES

Er zijn verschillende [GAMEPLAY-acties](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) die zijn opgehaald en waarvan de details beschikbaar zijn.

## Referenties

* [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format)

