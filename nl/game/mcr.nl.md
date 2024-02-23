{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Meer informatie over de MCR-bestandsindeling en API's waarmee u MCR-bestanden kunt maken en openen.",
  "title": "MCR - Minecraft Regio Bestandsformaat",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-nlr"
}
},
  "lastmod": "2022-12-14"
}

## Wat is een MCR-bestand?

Het Minecraft MCR-bestandsformaat is een gegevensformaat dat door Minecraft wordt gebruikt om terreinbrokken van een Minecraft-wereld op te slaan. Het is gebaseerd op het NBT-formaat (Named Binary Tag), dat is ontwikkeld door de ontwikkelaars van de populaire open-source game-engine Minecraft Forge. Het MCR-bestandstype werd in het allereerste begin geïntroduceerd en werd later vervangen door de [MCA file format](/game/mca/).

## MCR-bestandsindeling

Het MCR-bestandsformaat is gestructureerd als een reeks benoemde binaire tags, die elk een specifiek type gegevens bevatten. De tag op het hoogste niveau is de tag 'Level', die alle gegevens voor een enkel spelniveau bevat. Binnen de Level-tag zijn er verschillende andere benoemde tags die verschillende soorten gegevens opslaan, zoals de 'Data'-tag, die informatie over de spelwereld opslaat, en de 'Entities'- en 'TileEntities'-tags, die gegevens opslaan over de gamewereld. respectievelijk spelobjecten en tegelentiteiten in de wereld.

## Wat zit er in het MCR-bestandsformaat?

In het Minecraft MCR-bestandsformaat is een regio een blokgebied van 32x32 van de gamewereld. Het MCR-formaat verdeelt de spelwereld in regio's om de gegevens efficiënter te beheren en het sneller laden en opslaan van spelniveaus mogelijk te maken. Elke regio wordt opgeslagen in een afzonderlijk bestand en het MCR-bestandsformaat gebruikt een coördinatensysteem om de positie van elke regio binnen de spelwereld te identificeren. De coördinaten van een gebied worden bepaald door de blokcoördinaten van de linkerbenedenhoek van het gebied. Een regio met coördinaten (-1,0) zou zich bijvoorbeeld één regio links en nul regio's lager dan de oorsprong van de spelwereld bevinden.

## Specificaties MCR-bestandsindeling

De specificaties van het MCR-bestandsformaat zijn openbaar beschikbaar. De specificaties voor het NBT-formaat, waarop het MCR-formaat is gebaseerd, zijn beschikbaar op de Minecraft Forge-website. Bovendien bevat de [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) ook gedetailleerde informatie over het MCR-bestandsformaat, inclusief de structuur en de verschillende gegevenstypen die het ondersteunt.

### Gecomprimeerde gegevens in MCR-bestanden

Het Minecraft MCR-bestandsformaat ondersteunt compressie. Het MCR-bestandsformaat is gebaseerd op de [NBT format](https://minecraft.fandom.com/wiki/NBT_format) waarmee gegevens in gecomprimeerde vorm kunnen worden opgeslagen. Dit helpt de grootte van MCR-bestanden te verkleinen en ze efficiënter over te dragen en op te slaan. Dit is een belangrijk kenmerk van het MCR-bestandsformaat, omdat spelers hiermee grote Minecraft World-terreingegevens met anderen kunnen delen.

## Referenties

* [Wereldeditor voor Minecraft](https://www.mcedit.net/)

* [Over Minecraft](https://www.minecraft.net/)

* [Regio bestandsformaat](https://minecraft.fandom.com/wiki/Region_file_format)

* [NBT-formaat](https://minecraft.fandom.com/wiki/NBT_format)


