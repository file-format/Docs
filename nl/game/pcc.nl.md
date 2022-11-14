{
  "date" : "2021-09-08",
  "keywords" :[ "pcc-bestand", "pcc-bestandsformaat", "wat is een pcc-bestand", "bestand", "pcc-voorbeeld", "pcc-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over Mass Effect PCC-bestandsindeling en API's die PCC-bestanden kunnen maken en openen.",
  "title" :"PCC - Mass Effect-pakketbestand",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Wat is een PCC-bestand?

Een bestand met .pcc is een [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) bestand dat gamegegevens bevat om game-inhoud zoals modellen, texturen en kamers. Mass Effect 2 en 3 zijn de eerste schietspellen gebaseerd op de Unreal Engine 3 gaming-engine. De game is oorspronkelijk ontwikkeld door [Bioware](https://www.bioware.com/about/) die de meeste gamebronnen in hun eigen PCC-bestandsindeling bewaarde. Bioware werd overgenomen door Electronic Arts, een toonaangevende wereldwijde uitgever van interactief entertainment.

## PCC-bestandsindeling - Meer informatie

PCC-bestanden bevatten gecomprimeerde en/of niet-gecomprimeerde structuren die bijdragen aan de algehele bestandsorganisatie.

### Gecomprimeerde PCC-structuur

Een gecomprimeerd PCC-bestand bestaat uit tabellen en gegevens die in brokken zijn gesegmenteerd. Elke chunk bevat een variabel aantal gecomprimeerde blokken.

* `Chunks Header` - Een gemeenschappelijke header van 16 bytes, die informatie over de chunks bevat.
* `Chunk Header` - Een header van 16 bytes die informatie bevat over de onbewerkte gecomprimeerde gegevens in het blokformulier.

### Niet-gecomprimeerde PCC-structuur

Niet-gecomprimeerde PCC-bestanden zijn onderverdeeld in de volgende vijf delen.

* `Header` - bevat basisinformatie over de structuur van het PCC-bestand.
* `Name Table` - bevat de naam die in het pakket wordt gevonden, inclusief importklassen, exports en exporteigenschappen.
* `Import Table` - bevat alle klassen en objecten die door de PCC zijn geïmporteerd.
* `Export Table` - bevat alle objecten die in het pakket zijn opgeslagen. Elke export kan variëren in grootte.

## Referenties

* [Me3Explorer - PCC-bestandsindeling](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Mass Effect-spel](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)

