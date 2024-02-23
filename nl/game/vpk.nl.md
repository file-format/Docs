{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over de Unreal Static Meshes VPK-bestandsindeling en API's waarmee VPK-bestanden kunnen worden gemaakt en geopend.",
  "title" : "VPK-bestand - Onwerkelijk statisch meshes-bestand",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk-nl",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## Wat is een VPK-bestand?

Een .vpk-bestand is een bestandsindeling die wordt gebruikt door de **Source Engine**, een game-engine ontwikkeld door Valve Corporation. VPK-bestanden worden gebruikt om game-inhoud te verpakken, zoals modellen, texturen en geluiden, en worden vaak gebruikt in games als Team Fortress 2, Left 4 Dead en Counter-Strike: Global Offensive. De bestanden kunnen worden geopend en uitgepakt met behulp van verschillende tools, zoals GCFScape en VPK Tool.

## VPK-bestandsindeling - Meer informatie

VPK-bestanden worden als binaire bestanden op schijf opgeslagen. Eén enkel vpk-bestand kan deel uitmaken van een VPK-pakket of kan fungeren als een onafhankelijk onbewerkt VPK-bestand. Informatie die in een VPK-bestand kan worden opgeslagen, omvat kaarten, materialen, game-inhoud en choreografiescènes.

### Hoe maak ik een VPK-bestand aan?

Er zijn verschillende manieren om een .vpk-bestand te maken, afhankelijk van de beschikbare tools.

1. `Het VPK-hulpprogramma gebruiken:` Dit is een opdrachtregelprogramma dat kan worden gebruikt om VPK-bestanden te maken en uit te pakken. Een VPK-bestand kan worden gemaakt met behulp van de volgende opdracht:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Hierdoor wordt een VPK-bestand gemaakt vanuit de opgegeven map en wordt dit opgeslagen als het opgegeven uitvoerbestand.

1. `De Hammer Editor gebruiken:` De Hammer Editor is een hulpmiddel dat bij de Source SDK wordt geleverd en kan worden gebruikt om niveaus te maken en te bewerken voor games die de Source-engine gebruiken. Het bevat ook de mogelijkheid om VPK-bestanden te maken door met de rechtermuisknop op een map op het tabblad Bestandssysteem te klikken en VPK maken te selecteren.

1. `Met behulp van de VPK-maker van Valve:` Dit is een tool ontwikkeld door Valve die wordt gebruikt voor het verpakken en distribueren van game-inhoud. Deze tool kan worden gebruikt om VPK-bestanden te maken en het is ook de officiële tool voor het maken van VPK-bestanden.

## Referenties

 * [Klepsoftware](https://www.valvesoftware.com/en/)
 * [VPK-ontwikkelaarsbronnen](https://developer.valvesoftware.com/wiki/GCF)

