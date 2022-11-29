---
date: 2019-12-13
keywords: flac, flac-filformat, .flac-tillägg, flac-fil, flac vs mp3
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Lär dig om FLAC-filformat och API:er som kan skapa och öppna FLAC-filer."
title: FLAC filformat
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Vad är en FLAC fil?

FLAC (Free Lossless Audio Codec) är ett förlustfritt komprimeringsljudkodningsformat utvecklat av Xiph.Org Foundation. FLAC är ett royaltyfritt öppet format som sparas med tillägget .flac. Digitalt ljud komprimerat med FLAC-algoritmen reduceras vanligtvis till 50 till 70 procent i storlek. FLAC-filer kan dekomprimeras till en identisk kopia av originalljudfilerna.

## FLAC filformat

Detta är en översikt över FLAC-bitströmmen.

- **fLaC-markör**: Denna markör läggs till i början av streamen. Den följs av ett eller flera metadatablock.
- **Metadatablock**: 128 typer av metadatablock stöds av FLAC; för närvarande definieras följande.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME**: Ljuddatan består av en eller flera ljudramar.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## Kort historik över FLAC-filformat

Josh Coalson påbörjade utvecklingen av FLAC 2000. Den första versionen av FLAC släpptes den 20 juli 2001. FLAC införlivades under flaggan Xiph.Org den 20 januari 2003. Utvecklingen av FLAC flyttades till Xiph.Org git-förvaret med lanseringen av version 1.3.0 den 26 mars 2013.

## Sammansättning av FLAC-projektet

FLAC-projektet består av följande:

- Streama format.
- Enkelt containerformat för strömmen (FLAC).
- libFLAC: Ett bibliotek med referenskodare, avkodare och metadatagränssnitt.
- libFLAC++: Ett objektorienterat omslag för libFLAC.
- flac: Ett kommandoradsprogram för att koda och avkoda FLAC-strömmar.
- metaflac: En kommandoradsmetadataredigerare för FLAC.
- Input plugins för musikspelare som Winamp, XMMX, etc.
- Ogg containerformat (Ogg FLAC).

## FLAC design

Beroende på musikens densitet och amplitud kan storleken på den komprimerade filen vara 80 % mindre än originalfilen.

### Källkodare ###

- Den stöder bara heltalssampel och inte flyttal. Den kan hantera PCM-bitupplösning från 4 till 32 bitar per sampling och samplingshastighet från 1Hz till 65 535 Hz. FLAC-kodning är begränsad till 24 bitar per sampel.
- Kanaler kan grupperas för att dra fördel av interkanalkorrelationer för att öka komprimeringen.
- CRC-kontrollsummor används för att identifiera skadade ramar.
- För konvertering av ljudprover använder FLAC linjär prediktion.

### Metadata ###

- FLAC stöder ReplayGain (används för att uppfatta och normalisera ljudstyrkan).
- FLAC använder samma system som används i Vorbis-kommentarer för taggning.
- libFLAC används av de flesta FLAC-applikationer för kodning/avkodning.
- libFLAC API är organiserat i strömmar, sökbara strömmar och filer för att öka abstraktionen från bas FLAC-bitström.

### Kompression ###

libFLAC använder komprimeringsnivåer från 0 till 8 där 0 är den snabbaste och 8 är den långsammaste komprimeringsnivån. De komprimerade filerna är alltid förlustfria även om avvägningen är mellan hastighet och storlek.

## FLAC vs MP3
MP3 är ett komprimeringsformat med förlust, vilket innebär att det kan skära av en del av ljudet för att minska dess storlek efter att ha tillämpat komprimering. Medan FLAC är ett förlustfritt filformat vilket innebär att du kan höra ljudet i dess renaste form. Tidigare var de förlustfria filformaten CDA eller WAV som inte var mycket utrymmeseffektiva som FLAC. Följande tabell visar jämförelsen mellan dessa två format för några viktiga termer:

|Term|FLAC|MP3|
---|---|---|
|**Datakvalitet**|Ingen förlust av ljuddata| Vissa data kan gå förlorade vid komprimering av ljuddata|
|**Storlek**|Större filstorlek jämfört med förlustformat. Så behöver större lagringskapacitet| Mindre filstorlek, lämplig att spela på kompakta ljudenheter med lite lagringsutrymme |
|**Hårdvarukrav**| Behöver högkvalitativ ljudutrustning och enorm lagringskapacitet |Enorma ljudbibliotek kan sparas på ett mindre lagringsutrymme. Lämplig för handhållna enheter, såsom ljudspelare eller mobiltelefoner|
|**Distribution över internet**|Kan inte distribueras enkelt över internet på grund av enorm filstorlek |Kompakt filstorlek gör det enkelt att distribuera över internet|
|**Kompatibilitet**|Den mest populära musik- och ljudlyssningscodec som i stort sett är kompatibel med alla enheter på planeten.Kompatibel med nya generationens datorer, telefoner, AV-mottagare, blu-ray-spelare, streamingenheter som Roku eller Fire TV|

## Referenser ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

