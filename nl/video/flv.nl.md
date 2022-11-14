---
date: 2019-10-11
keywords: flv, .flv, flv-bestandsformaat, .flv-bestandsformaat, .flv-extensie, flv-extensie, flv-videoformaat
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Meer informatie over FLV-bestandsindelingen en API's die FLV-bestanden kunnen maken en openen."
title: FLV-bestandsindeling
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Wat is een FLV-bestand? ##

FLV (Flash Video) is een containerbestandsformaat met de extensie .flv. FLV wordt gebruikt om audio-/video-inhoud via internet te leveren met behulp van Adobe Flash Player of Adobe Air. De gegevens in FLV-bestanden worden op dezelfde manier gecodeerd als SWF-bestanden. De directe ondersteuning is in 2003 aan Flash Player 7 toegevoegd. Adobe-systemen hebben in 2007 F4V gemaakt vanwege de beperkingen van FLV.

### Codering ###

FLV-bestanden bevatten videobitstreams van Sorenson Spark, een eigen variant van de H.263-videostandaard. Het is het vereiste compressieformaat voor Flash Player 6 en 7. Versie 8 van Flash Player-ondersteuning voor On2 TrueMotion VP6-videobitstreams. Het is het aanbevolen compressieformaat voor Flash Player 8 en hoger. FLV ondersteunt audio in MP3, Nellymoser Asao Codec en de open-source Speex-codec. Het ondersteunt ook ongecomprimeerde audio of audio in ADPCM-formaat. AAC (HE-AAC/AAC SBR, AAC Main Profile en AAC-LC) worden ondersteund door de recente versies van Flash Player 9.

## Structuur ##

FLV-bestanden bestaan uit Header en Packets. Een FLV-bestand begint met de koptekst. De kop heeft de volgende velden.

- **Handtekening**: de waarde is FLV
- **Versie**: de standaardwaarde is 1. Alleen 0x01 is geldig.
- **Vlaggen**: 0x04 wordt gebruikt voor audio en 0x01 wordt gebruikt voor video, dus 0x05 wordt gebruikt voor zowel audio als video.
- **Kopgrootte**: de standaardwaarde is 9. Het wordt gebruikt om een nieuwere uitgebreide koptekst over te slaan.

Na de header komen de Packets. Het FLV-bestand is opgesplitst in meerdere pakketten, FLV-tags genaamd, met headers van 15 bytes. De pakketten bevatten de metadata voor audio, video, scripts, encryptie-informatie en payload. De FLV-pakketten hebben de volgende velden.

- **Gereserveerd**: het is gereserveerd voor FMS en moet 0 zijn.
- **Filter**: Geeft aan of de pakketten worden gefilterd of niet.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Pakkettype**: dit definieert het type inhoud in het pakket.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Gegevensgrootte**: dit geeft de lengte van het bericht aan.
- **Tijdstempel lager**: hiermee wordt de tijdstempel in milliseconden opgeslagen waarop de taggegevens van toepassing zijn. Het is ingesteld op NULL voor het eerste pakket.
- **Timestamp Upper**: extensie om een uint32_be-waarde te creëren.
- **Stream-ID**: dit is ingesteld op NULL voor de eerste stream.
- **Payloadgegevens**: dit zijn de gegevens op basis van het pakkettype.

## Referenties ##

- [Flash-video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

