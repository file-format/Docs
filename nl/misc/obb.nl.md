{
  "date" : "2022-02-16",
  "keywords" :[ "obb-bestand", "obb-bestandsindeling", "wat is een obb-bestand", "bestand", "obb-voorbeeld", "obb-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBB-bestandsindeling - Android-ondoorzichtig binair Blob-bestand",
  "description":"Meer informatie over OBB-bestandsindeling en API's die OBB-bestanden kunnen maken en openen.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## Wat is een OBB-bestand?

Een OBB-bestand is een uitbreidingsbestand dat aanvullende gegevens bevat naast het Android [APK](/nl/compression/apk/)-bestand. Google Play Store staat niet toe dat een Android APK-bestand groter is dan 100 MB. Maar voor sommige toepassingen kunnen naast de APK-bestanden ook high-definition afbeeldingen, mediabestanden of andere grote activa nodig zijn. Dat is waar de OBB-bestandstypen binnenkomen. Google Play maakt het mogelijk om deze uitbreidingsbestanden als aanvulling op het APK-bestand bij te voegen.

## OBB-bestandsindeling

OBB-bestanden worden samen met de APK-bestanden opgeslagen als binaire bestanden. Wanneer een APK de OBB-bestanden vergezelt, host Google Play de uitbreidingsbestanden op zijn server en worden er geen extra kosten aan de ontwikkelaar in rekening gebracht. Deze extra bestanden worden opgeslagen in de gedeelde opslag van het apparaat op een SD-kaart of een op USB monteerbare partitie wanneer de app wordt gedownload voor installatie.

De OBB-bestanden worden gedownload en geïnstalleerd bij het downloaden. Maar in sommige gevallen worden deze gedownload voor installatie wanneer de toepassing voor het eerst wordt uitgevoerd.

### OBB Maximale bestandsgrootte

Met Google Play Store kunt u OBB-uitbreidingsbestanden uploaden met een grootte tot 2 GB. Het wordt aanbevolen om grote bestanden te uploaden als gecomprimeerde [ZIP](/nl/compression/zip/)-bestanden voor efficiënt uploaden via internet.

Deze uitbreidingsbestanden kunnen worden gehost als **hoofd** primair uitbreidingsbestand voor aanvullende bronnen die nodig zijn voor de app, of als een optioneel patchuitbreidingsbestand bedoeld voor kleine updates van het hoofduitbreidingsbestand.

## Referenties

* [Android-ontwikkelaars - Uitbreidingsbestanden](https://developer.android.com/google/play/expansion-files)

