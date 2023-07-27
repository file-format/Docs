{
  "date" : "2019-10-11",
  "keywords" :[ "tgs-bestand", "tgs-bestandsformaat", "wat is een tgs-bestand", "bestand", "tgs-voorbeeld", "tgs-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Telegram geanimeerd stickerbestandsformaat",
  "description":"Meer informatie over TGS-bestandsindeling en API's die TGS-bestanden kunnen maken en openen.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Wat is een TGS-bestand?

Een bestand met de extensie .tgs is een geanimeerd stickerbestand dat is geïntroduceerd door de platformonafhankelijke berichtenservice [Telegram](https://core.telegram.org/stickers#animated-stickers). Geanimeerde stickers worden gebruikt door gebruikers van berichten-apps om meer verbeterde en levendige inhoud in berichten te verzenden, in tegenstelling tot de statische afbeeldingen die stilstaande beelden zijn. Telegram gebruikte aanvankelijk de bestandsindeling [WEBP](/nl/image/webp/) voor stickers met stilstaande beelden. Het TGS-bestandsformaat kan animatiegegevens opslaan met hogere resoluties en kleinere bestandsgroottes in vergelijking met de statische WEBP-stickers. TGS-bestanden kunnen worden geopend met toepassingen zoals Telegram, 7-zip, Apple Archive Utility en Corel WinZip.

## TGS-bestandsindeling

Telegram introduceerde het TGS-bestandsformaat in juli 2019 op basis van de Lottie-bibliotheek. Een TGS-bestand bestaat uit [JSON](/nl/web/json/) tekst die wordt geëxporteerd vanuit een animatie in Adobe After Effects. De geëxporteerde JSON-tekst wordt gecomprimeerd met behulp van de gzip-compressie die de bestandsgrootte verkleint. De JSON-informatie over het tekstbestand wordt opgeslagen in een tekstbestand dat de basis wordt van hoge compressiesnelheden.

### Specificaties TGS-stickers

Het TGS-bestandsformaat legt bepaalde beperkingen op aan het maken van TGS-geanimeerde stickers. Een TGS-animatiebestand:

* Sticker-/canvasformaat moet 512х512 pixels zijn.
* Stickerobjecten mogen het canvas niet verlaten.
* De animatieduur mag niet langer zijn dan 3 seconden.
* Alle animaties moeten een lus hebben.
* Stickergrootte mag niet groter zijn dan 64 KB na rendering in Bodymovin.
* Alle animaties moeten worden uitgevoerd met 60 frames per seconde.

### Voorbeeld TGS JSON-tekst

Een voorbeeld van een geanimeerde sticker bevat, wanneer deze is uitgepakt, de volgende JSON-tekstinhoud.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Referenties ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

