---
date: 2019-12-13
keywords: m3u, m3u-bestandsindeling, .m3u-extensie, m3u multimedia-afspeellijst, m3u-afspeellijstindeling
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Meer informatie over de M3U-bestandsindeling en API's die M3U-bestanden kunnen maken en openen."
title: M3U-bestandsindeling
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Wat is een M3U-bestand? ##

M3U (MP3-URL) is een audio-afspeellijstbestand dat is opgeslagen met de extensie .m3u. M3U is geen echt audiobestand, het verwijst alleen naar audio- en soms videobestanden. M3U is door Fraunhofer ontwikkeld voor gebruik met Winplay3-software. Het wordt ook ondersteund door verschillende mediaspelers en software.

## M3U-bestandsindeling

Er is geen officiële specificatie voor het M3U-bestandsformaat, het is een de-facto standaard. M3U is een tekstbestand zonder opmaak dat de extensie .m3u gebruikt als de tekst is gecodeerd in de standaard niet-Unicode-codering van het lokale systeem of met de extensie .m3u8 als de tekst UTF-8-gecodeerd is. Elke vermelding in het M3U-bestand kan een van de volgende zijn:

- Absoluut pad naar het bestand
- Bestandspad ten opzichte van het M3U-bestand.
- URL

### Uitgebreide M3U ###

In de uitgebreide M3U worden aanvullende richtlijnen geïntroduceerd die beginnen met "#" en eindigen met een dubbele punt (:) als ze parameters hebben. Hieronder vindt u een lijst met richtlijnen voor uitgebreide M3U.

- **#EXTM3U** - Dit is de bestandsheader die Extended M3U aangeeft en moet de eerste regel van het bestand zijn.
- **#EXTENC:** - Tekstcodering. Het moet de 2e regel van het bestand zijn.
- **#EXTINF:** - Wordt gebruikt voor trackinformatie en andere aanvullende eigenschappen.
- **#PLAYLIST:** - De titel van de afspeellijst
- **#EXTGRP:** - Begin naamgroepering
- **#EXTALB:** - Albuminformatie
- **#EXTART:** - Albumartiest
- **#EXTGENRE** - Albumgenre
- **#EXTM3A** - Afspeellijst met één bestand voor albumtracks of hoofdstukken.
- **#EXTBYT:** - Bestandsgrootte in bytes.
- **#EXTBIN:** - Binaire gegevens volgen.
- **#EXTIMG:** - Logo, omslag of andere afbeeldingen.

### HLS M3U ###

HLS (HTTP Live Streaming) is gemaakt door Apple om audio en radio naar iOS-apparaten te streamen. Het is gebaseerd op de UTF-8-gecodeerde uitgebreide M3U. Het werd in 2017 gestandaardiseerd als RFC 8216 door IETF. De tags voor de HLS-afspeellijst beginnen met "#EXT-X-". Hieronder vindt u een lijst met tags voor HLS

- **EXT-X-VERSION** - Geeft de compatibiliteitsversie van het bestand aan op basis van de media en de server.
- **#EXT-X-START:** - Geeft het gewenste startpunt voor de afspeellijst aan.
- **#EXT-X-PLAYLIST-TYPE:** - Geeft het type afspeellijst (EVENT of VOD).
- **#EXT-X-TARGETDURATION:** - Het specificeert de maximale duur van het segment.
- **#EXT-X-MEDIA-SEQUENCE:** - Het geeft het mediavolgordenummer aan.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Het geeft aan dat alle mediasamples onafhankelijk zijn en kunnen worden gedecodeerd zonder andere segmenten.
- **#EXT-X-MEDIA:** - Het wordt gebruikt om media-afspeellijsten met elkaar in verband te brengen die alternatieve weergaven van dezelfde inhoud bevatten.
- **#EXT-X-STREAM-INF:** - Het specificeert een variantstroom die deel uitmaakt van de uitvoeringen.
- **#EXT-X-BYTERANGE:** - Geeft aan dat het mediasegment een subbereik is van de bron die wordt geïdentificeerd door zijn URI.
- **#EXT-X-DISCONTINUITY** - Geeft discontinuïteit aan tussen de voorgaande en volgende mediasegmenten.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Het maakt synchronisatie mogelijk tussen verschillende uitvoeringen van dezelfde Variant Stream of verschillende Variant Streams.
- **#EXT-X-KEY:** - Specificeert hoe mediasegmenten moeten worden ontsleuteld.
- **#EXT-X-MAP:** - Specificeert hoe u de sectie Media-initialisatie kunt verkrijgen. Het is vereist om de toepasselijke mediasegmenten te ontleden.
- **#EXT-X-PROGRAM-DATE-TIME:** - Het associeert het eerste voorbeeld van het mediasegment met een absolute datum en/of tijd.
- **#EXT-X-DATERANGE:** - Het associeert een gegevensbereik.
- **#EXT-XI-FRAMES-ONLY** - Geeft aan dat elk mediasegment in de afspeellijst een enkel I-frame beschrijft.
- **EXT-XI-FRAME-STREAM-INF** - Dit geeft aan dat het afspeellijstbestand I-frames van multimediapresentatie bevat.
- **#EXT-X-SESSION-DATA:** - Hiermee kunnen willekeurige sessiegegevens worden
opgenomen in een Master-afspeellijst.
- **#EXT-X-SESSION-KEY:** - Het staat coderingssleutels toe. De client kan deze sleutels vooraf laden zonder eerst de afspeellijst te lezen.
- **#EXT-X-ENDLIST** - Dit geeft aan dat er geen mediasegmenten meer aan het bestand worden toegevoegd.

Het volgende is de lijst met typen internetmedia die door M3U worden gebruikt:

- **application/vnd.apple.mpegurl**: het is het enige geregistreerde mediatype (geregistreerd in 2009) voor M3U dat wordt gebruikt om te verwijzen naar de afspeellijsten in HLS-toepassingen.
- De volgende typen internetmedia worden gebruikt door niet-HLS-toepassingen.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## M3U Voorbeeld ##

Dit is een voorbeeld van het M3U-bestand.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Referenties ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [HTTP Live Streaming](https://tools.ietf.org/html/rfc8216)

