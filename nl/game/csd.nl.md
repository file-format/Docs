{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over CSD Steam Game Data Backup-bestandsindeling en API's.",
  "title" :"CSD-bestandsindeling - Steam Game-gegevensback-upbestand",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Wat is een CSD-bestand?

Een CSD-bestand is een back-upbestand van een game dat is gegenereerd door de gameservice **Steam** waarmee gebruikers **Valve**-games kunnen downloaden en beheren. Het bevat de back-upgegevens met betrekking tot games die kunnen worden gebruikt om een verwijderde game te herstellen. Steam kan de game alleen herstellen vanaf een CSD-bestand als de game is gedownload, geïnstalleerd en gepatcht via Steam. Om het spel van het CSD-bestand te herstellen, gebruikt u de optie Steam → Back-up en herstel Gamesteam en selecteert u het bestand.

## CSD-bestandsindeling - Meer informatie

De interne structuur van het CSD-bestandsformaat is niet publiekelijk beschikbaar en de specificaties van het bestandsformaat zijn niet beschikbaar voor ontwikkelaar. CSD-bestanden gaan vergezeld van de CSM- en ISS-bestanden, die ook Steam-gamebestandsindelingen zijn.

### Waar vind je Steam-back-upbestanden?

De volledige Steam-back-upbestanden zijn te vinden op de volgende locaties:

* C:\Program Files (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - Aangepaste configuraties en configuratiescripts
* \downloads\ - Aangepaste inhoud voor multiplayer-games
* \maps\ - Aangepaste kaarten die zijn geïnstalleerd of gedownload tijdens multiplayer-games
* \materialen\ - Aangepaste texturen en skins
* \SAVE\ - Opgeslagen spellen voor één speler

De locatie van games die door derden zijn gemaakt, kan echter verschillen en wordt bepaald door de ontwikkelaar van de game.

### Herstellen vanuit CSD-back-upbestand

Installeer Steam en log in op het juiste Steam-account (zie Steam installeren voor verdere instructies)
* Start Steam
* Klik op "Steam" in de linkerbovenhoek van de Steam-applicatie
* Selecteer "Back-up maken en games herstellen..."
* Selecteer "Een eerdere back-up herstellen"
* Blader naar de locatie van de back-upbestanden van de game
* Ga verder door de Steam-vensters om de benodigde games te installeren.

## Referenties

* [De Steam Backup-functie gebruiken](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

