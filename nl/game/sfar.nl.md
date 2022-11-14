{
  "date" : "2021-10-20",
  "keywords" :[ "sfar file", "sfar file format", "wat is een sfar file", "file", "sfar example", "Mass Effect 3 DLC File extension","extension", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over Mass Effect 3 SFAR-bestandsindeling en API's die SFAR-bestanden kunnen maken en openen.",
  "title" :"SFAR - Mass Effect 3 DLC-bestand",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Wat is een SFAR-bestand?

Een bestand met de extensie .sfar is een gamegegevensbestand dat door Mass Effect 3 wordt gebruikt om zijn DLC (downloadbare inhoud) op te slaan in een gecomprimeerd, eigen archief. Mass Effect 3 is een game gemaakt door Electronic Arts, een vooraanstaand game-ontwikkelingsbedrijf. De DLC-inhoud die is opgeslagen in een SFAR-bestand wordt gebruikt om het spel uit te breiden met extra inhoud en functies.

## SFAR-bestandsindeling - Meer informatie

SFAR-bestanden worden opgeslagen/opgeslagen als gecomprimeerde archiefbestanden in binaire bestandsindeling. Deze gebruiken zowel LZX- als LZMA-compressie-algoritmen voor het comprimeren van de inhoud. SFAR-bestanden kunnen worden geopend met behulp van de DLC-editor die bij ME3 Explorer wordt geleverd. Naast SFAR kan DLC Editor andere gamebestanden extraheren, zoals [PCC](/nl/game/pcc/).

## Specificaties SFAR-bestandsindeling

Een SFAR-bestand is onderverdeeld in de volgende vier hoofdblokken.

### SFAR-koptekst

SFF Header bevat informatie over de verschillende chunks waaruit het bestand bestaat.

### SFAR-bestandstabel

De SFAR-bestandstabel bevat een lijst met bestandsitems waarbij elk item 30 bytes lang is.

### Blokmaattabel

De Block-Size bevat meerdere items, waarbij elk item 2 byes lang is. Deze waarde specificeert de blokgrootte die overeenkomt met een item in de bestandstabel.

### Blokken

Blokblokken in een SFAR-bestand bevatten de gegevens in het SFAR-bestand.

## Referenties

* [DLC SFAR-bestandsindeling - Onderzoek](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

