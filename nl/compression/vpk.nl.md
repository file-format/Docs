{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VPK-bestand - PlayStation Vita-toepassingspakketbestandsindeling",
  "description":"Meer informatie over VPK-bestandsindeling en API's die VPK-bestanden kunnen maken en openen.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## Wat is een VPK-bestand?

Een bestand met de extensie .vpk is een gecomprimeerd archiefpakketbestand dat wordt gebruikt om apps van derden te installeren op de Sony PlayStation Vita-gameconsole. Deze bestanden kunnen alleen worden geïnstalleerd op de jailbreak Vita PlayStation van HENkaku, waardoor de PS Vita en PSTV aangepaste, door de gebruiker gemaakte inhoud konden gebruiken. Een VPK-archiefbestand bevat alle inhoud waaruit het spel bestaat, inclusief afbeeldingen zoals [PNG](/nl/image/png/)-bestanden, instellingsbestanden zoals [.bin](/nl/disc-and-media/bin/), en alle configuraties in [XML](/nl/web/xml/) bestandsformaat.

## VPK-bestandsindeling

VPK-bestanden worden op schijf opgeslagen als standaard gecomprimeerde [ZIP](/nl/compression/zip/)-archieven. Deze kunnen meerdere mappen en andere bijbehorende bestanden bevatten voor de apps van derden die op Vita Gaming Console moeten worden geïnstalleerd. Om de inhoud van het VPK-pakketbestand te bekijken, hernoemt u de extensie van .vpu naar .zip en extraheert u de inhoud met behulp van standaard decompressieprogramma's zoals WinZip of WinRAR.

Valvesoftware heeft gedetailleerde informatie over het [VPK-bestandsformaat](https://developer.valvesoftware.com/wiki/VPK_File_Format) waarnaar kan worden verwezen vanuit het perspectief van de ontwikkelaar.

## Hoe VPK-bestanden te installeren?

De VPK-bestanden kunnen worden geïnstalleerd vanaf het opdrachtregelprogramma VPK.exe. Op Windows OS kunnen bestanden worden neergezet op het vpk.exe-bestand dat een \*.vpk retourneert met alle verpakte bestanden. Als alternatief kan de opdrachtregeltool als volgt worden gebruikt.

### Maak VPK en voeg bestanden toe

```
vpk <dirname>
```

### VPK-bestanden uitpakken

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK-kijker

* [VRF VPK-viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## Referenties

* [VPK-bestandsindeling](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [VPK-bestanden](https://developer.valvesoftware.com/wiki/VPK)

