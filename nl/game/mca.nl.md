{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Meer informatie over de MCA-bestandsindeling en API's waarmee MCA-bestanden kunnen worden gemaakt en geopend.",
  "title": "MCA - Minecraft Anvil Region-bestandsformaat",
  "linktitle": "MCA",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-nla"
}
},
  "lastmod": "2022-12-13"
}

## Wat is een MCA-bestand?

Het Minecraft Anvil-regiobestandsformaat is een gegevensopslagformaat dat wordt gebruikt om terreinbrokken van een Minecraft-wereld op te slaan in de populaire videogame **Minecraft**. De Minecraft-wereld bestaat uit regio's, waarbij elke regio in stukjes is verdeeld. Het MCA-bestandsformaat maakt de efficiënte opslag van grote hoeveelheden spelgegevens mogelijk, zoals de locatie van blokken en entiteiten in een bepaald deel van de spelwereld. MCA-bestanden moeten worden gecombineerd met andere MCA-bestanden om een hele wereld te genereren.

Naast het opslaan van gamegegevens biedt het Anvil Region-bestandsformaat ook ondersteuning voor verschillende andere gegevenstypen, zoals spelersgegevens en metadata. Dit maakt de efficiënte opslag mogelijk van alle informatie die nodig is om een bepaald deel van de spelwereld volledig opnieuw te creëren, inclusief de locatie van blokken, entiteiten en andere spelobjecten.

## MCA-bestandsindeling - Meer informatie

Het bestandsformaat Anvil Region is een variant van het NBT-formaat (Named Binary Tag), een hiërarchische boomachtige structuur voor het opslaan van gegevens in een binair bestand. Dit maakt de efficiënte opslag van complexe datastructuren in een compact en gemakkelijk leesbaar formaat mogelijk.

### Brokken in MCA-bestand

In Minecraft is een chunk een blokgebied van 16x16x16 van de gamewereld dat in het geheugen wordt geladen en op het scherm van de speler wordt weergegeven. Het Anvil-regiobestandsformaat slaat alle gegevens voor een bepaald deel op in één enkel bestand, dat vervolgens indien nodig snel in het geheugen kan worden geladen. Dit zorgt voor efficiënte opslag en snelle toegang tot de gamegegevens, wat belangrijk is voor een soepele en naadloze game-ervaring.

### Kleine MCA-bestandsgrootte

Een van de belangrijkste kenmerken van het bestandsformaat Anvil Region is het gebruik van compressie. Dit maakt de efficiënte opslag van grote hoeveelheden gegevens mogelijk, zonder dat dit ten koste gaat van de kwaliteit van de gegevens of de snelheid waarmee deze toegankelijk zijn. Dit wordt bereikt met behulp van een verscheidenheid aan technieken, zoals gzip-compressie en chunk-datacompressie.

Het gecomprimeerde bestandsformaat van MCA-bestanden maakt het een belangrijk onderdeel van het gegevensopslag- en beheersysteem van de game. Het efficiënte gebruik van compressie en ondersteuning voor verschillende gegevenstypen zorgt voor efficiënte opslag en snelle toegang tot de gamegegevens, waardoor spelers een soepele en naadloze game-ervaring worden gegarandeerd.

## MCA-bestandsformaatstructuur

De interne bestandsformaatstructuur van MCA-bestanden bestaat uit:
 * Koptekst, en een
 * Laadvermogen

### MCA-koptekst

De header van een MCA-regiobestand begint met een 8KiB-header die is opgesplitst in twee 4KiB-tabellen. De eerste tabel bevat de verschuivingen van segmenten in het regiobestand zelf, terwijl de tweede tabel tijdstempels biedt voor de laatste updates van deze segmenten.

### MCA-payload

MCA Payload bestaat uit segmenten, waarbij elke segmentgegevens beginnen met een (big-endian) veld van vier bytes. Dit veld geeft de exacte lengte van de resterende chunkgegevens in bytes aan. De gegevens van het laatste deel zijn opgevuld tot een lengte van een veelvoud van 4096B. Bestanden waarvan het laatste deel niet is opgevuld, worden niet geaccepteerd door Minecraft.

## Hoe MCA-bestanden te openen

U kunt MCA-bestanden openen en bewerken met het MCEdit-programma, een gratis open source-editor voor Minecraft. U kunt [download MCEdit](https://www.mcedit.net/) vanaf de officiële website gebruiken om de inhoud van uw Anvil-regiobestand te openen en te bekijken.

Zodra MCEdit is geïnstalleerd, kunt u uw Anvil-regiobestand openen door deze stappen te volgen:

 1. Start MCEdit en klik op de knop Openen in de linkerbovenhoek van het venster.

 1. Navigeer in het dialoogvenster Open Wereld naar de locatie van uw Anvil-regiobestand en selecteer dit.

 1. Klik op de knop Openen om het bestand in MCEdit te openen.

 1. MCEdit laadt het bestand en geeft de inhoud ervan weer in het hoofdvenster. U kunt vervolgens de tools en functies in MCEdit gebruiken om gegevens uit het Anvil-regiobestand te bekijken, bewerken en extraheren.

## Referenties

* [Wereldeditor voor Minecraft](https://www.mcedit.net/)

* [Over Minecraft](https://www.minecraft.net/)

* [Regio bestandsformaat](https://minecraft.fandom.com/wiki/Region_file_format)


