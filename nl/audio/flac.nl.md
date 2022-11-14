---
date: 2019-12-13
keywords: flac, flac-bestandsindeling, .flac-extensie, flac-bestand, flac vs mp3
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Lees meer over de FLAC-bestandsindeling en API's die FLAC-bestanden kunnen maken en openen."
title: FLAC-bestandsindeling
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Wat is een FLAC-bestand?

FLAC (Free Lossless Audio Codec) is een lossless compressie-audiocoderingsformaat ontwikkeld door Xiph.Org Foundation. FLAC is een royaltyvrije open indeling die wordt opgeslagen met de .flac-extensie. Digitale audio die wordt gecomprimeerd met behulp van het FLAC-algoritme, wordt doorgaans teruggebracht tot 50 tot 70 procent. FLAC-bestanden kunnen worden gedecomprimeerd tot een identieke kopie van de originele audiobestanden.

## FLAC-bestandsindeling

Dit is een overzicht van de FLAC bitstream.

- **fLaC-markering**: deze markering wordt toegevoegd aan het begin van de stream. Het wordt gevolgd door een of meer metadatablokken.
- **Metadatablokken**: 128 soorten metadatablokken worden ondersteund door FLAC; momenteel zijn de volgende gedefinieerd.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME**: de audiogegevens zijn samengesteld uit een of meer audioframes.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## Korte geschiedenis van het FLAC-bestandsformaat

Josh Coalson begon met de ontwikkeling van FLAC in 2000. De eerste versie van FLAC werd uitgebracht op 20 juli 2001. FLAC werd op 20 januari 2003 opgenomen onder de Xiph.Org-vlag. De ontwikkeling van FLAC werd verplaatst naar de Xiph.Org git-repository met de release van versie 1.3.0 op 26 maart 2013.

## Samenstelling van FLAC-project

Het FLAC-project bestaat uit het volgende:

- Stream-indelingen.
- Eenvoudig containerformaat voor de stream (FLAC).
- libFLAC: een bibliotheek met referentie-encoders, decoders en metadata-interface.
- libFLAC++: een objectgeoriënteerde wrapper voor libFLAC.
- flac: een opdrachtregelprogramma om FLAC-streams te coderen en te decoderen.
- metaflac: een metadata-editor voor de opdrachtregel voor FLAC.
- Invoerplug-ins voor muziekspelers zoals Winamp, XMMX, enz.
- Ogg-containerformaat (Ogg FLAC).

## FLAC-ontwerp

Afhankelijk van de dichtheid en amplitude van de muziek, kan de grootte van het gecomprimeerde bestand 80% kleiner zijn dan het originele bestand.

### Bron Encoder ###

- Het ondersteunt alleen integersamples en geen floating-point. Het kan PCM-bitresoluties aan van 4 tot 32 bits per sample en een samplefrequentie van 1Hz tot 65.535 Hz. FLAC-codering is beperkt tot 24 bits per sample.
- Kanalen kunnen worden gegroepeerd om te profiteren van interkanaalcorrelaties om de compressie te verhogen.
- CRC-controlesommen worden gebruikt om beschadigde frames te identificeren.
- Voor de conversie van audiosamples gebruikt FLAC lineaire voorspelling.

### Metagegevens ###

- FLAC ondersteunt ReplayGain (gebruikt om luidheid in audio waar te nemen en te normaliseren).
- FLAC gebruikt hetzelfde systeem dat wordt gebruikt in Vorbis-opmerkingen voor tagging.
- libFLAC wordt door de meeste FLAC-applicaties gebruikt voor codering/decodering.
- libFLAC API is georganiseerd in streams, doorzoekbare streams en bestanden om de abstractie van de basis-FLAC-bitstream te vergroten.

### Compressie ###

libFLAC gebruikt compressieniveaus van 0 tot 8 waarbij 0 het snelste is en 8 het langzaamste compressieniveau. De gecomprimeerde bestanden zijn altijd verliesvrij, hoewel de afweging tussen snelheid en grootte is.

## FLAC versus MP3
De MP3 is een compressie-indeling met verlies, wat betekent dat het een deel van de audio kan afsnijden om de grootte te verkleinen na het toepassen van compressie. Terwijl FLAC een verliesvrij bestandsformaat is, wat betekent dat u de audio in zijn puurste vorm kunt horen. Eerder waren de verliesvrije bestandsindelingen CDA of WAV, die niet veel ruimte-efficiënt waren als FLAC. De volgende tabel toont de vergelijking tussen deze twee formaten voor enkele belangrijke termen:

|Termijn|FLAC|MP3|
---|---|---|
|**Gegevenskwaliteit**|Geen verlies van audiogegevens| Sommige gegevens kunnen verloren gaan bij het comprimeren van audiogegevens|
|**Grootte**|Grotere bestandsgrootte in vergelijking met formaten met verlies. Dus grotere opslagcapaciteit nodig| Kleinere bestandsgrootte, geschikt om af te spelen op compacte audioapparaten met weinig opslagruimte |
|**Hardwarevereisten**| Hoogwaardige audioapparatuur en enorme opslagcapaciteit nodig | Enorme audiobibliotheken kunnen worden opgeslagen in een kleinere opslagruimte. Geschikt voor draagbare apparaten, zoals audiospelers of mobiele telefoons|
|**Distributie via internet**|Kan niet gemakkelijk via internet worden verspreid vanwege enorme bestandsgrootte |Compacte bestandsgrootte maakt het gemakkelijk om via internet te verspreiden|
|**Compatibiliteit**|De meest populaire codec voor het luisteren naar muziek en audio die vrijwel compatibel is met elk apparaat ter wereld.Compatibel met nieuwe generatie pc's, telefoons, AV-ontvangers, blu-ray-spelers, streaming-apparaten zoals Roku of Fire TV|

## Referenties ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

