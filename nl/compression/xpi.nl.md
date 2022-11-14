{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - Cross-platform installatiepakketbestand",
  "description":"Meer informatie over XPI-bestandsindeling en API's die XPI-bestanden kunnen maken en openen.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Wat is een XPI-bestand?

Een XPI-bestand is een installatiearchief dat is gecomprimeerd om de grootte van het bestand te verkleinen. Het wordt gebruikt door Mozilla-applicaties voor de installatie van plug-ins en add-on-bestanden. Het bevat een installatiescript of een manifest in de hoofdmap van het bestand, samen met een aantal gegevensbestanden. Een XPI-bestand kan thema's, toolkits of Firefox-plug-ins bevatten die de gebruiker kan installeren om deel uit te maken van de Firefox-browser, Thunderbird of SeaMonkey.

## XPI-bestandsindeling - Meer informatie

XPI-bestanden worden op schijf opgeslagen als [ZIP](/nl/compression/zip/)-archieven die meerdere bestanden combineren in één gecomprimeerd bestand. De bestanden in een XPI-bestand kunnen een installatiescriptbestand bevatten zoals JS en webbestanden zoals [CSS](/nl/web/css/), [HTML](/nl/web/html/) en [JSON](/nl/web/json/ ). Soms kan het ook [PNG](/nl/image/png/) afbeeldingsbestanden bevatten die door add-on als pictogrammen kunnen worden gebruikt.

### Hoe de inhoud van het XPI-bestand te bekijken?

Een XPI-bestand is praktisch een ZIP-archief waarvan de inhoud kan worden bekeken met behulp van de volgende stappen.

* Wijzig de extensie van het bestand van XPI naar ZIP
* Pak de inhoud van het bestand uit met een standaard decompressieprogramma zoals WinZip (Windows, Mac), 7-Zip (Windows) of Apple Archive Utility (Mac).

### Installeer XPI-bestand op Firefox Android

Meestal zijn mensen benieuwd of XPI-bestanden in Firefox op Android-apparaten kunnen worden geïnstalleerd. Op Android kunt u een add-on installeren vanuit een XPI-bestand door het bestand te zoeken en te openen met Firefox.

## Referenties

* [XPInstall - Wikipedia](https://en.wikipedia.org/wiki/XPInstall)
* [Hoe kan ik een XPI-bestandsextensie openen?](https://support.mozilla.org/en-US/questions/1009049)

