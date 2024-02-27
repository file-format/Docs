---
date: 2019-12-13
keywords: flac, flac file format, .flac extension, flac file, flac vs mp3
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltjen om FLAC-filformat og API'er, der kan oprette og åbne FLAC-fils.
title: FLAC-filformularat
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Hvad er en FLAC fil?

FLAC (Free Lossless Audio Codec) er et tabsfrit komprimeret lydkodningsformat udviklet af Xiph.Org Foundation. FLAC er et royaltyfrit åbent format, der er gemt med .flac-udvidelsen. Digital lyd komprimeret ved hjælp af FLAC-algoritmen er typisk reduceret til 50 til 70 procent i størrelse. FLAC-filer kan dekomprimeres til en identisk kopi af de originale lydfiler.

## FLAC filformat

Dette er en oversigt over FLAC-bitstrømmen.

- **fLaC marker**: This marker is added to the beginning of the stream. It is followed by one or more metadata blocks.
- **Metadatablokke**: 128 slags metadatablokke understøttes af FLAC; i øjeblikket er følgende defineret.
  - "**STREAMINFO**: Indeholder information om hele streamen."
  - "**APPLIKATION**: Dette bruges af tredjepartsapplikationer til identifikation."
  - "**PADDING**: Det bruges til at reservere plads til metadata, hvis metadataene vil blive redigeret efter kodning. Når metadataene er redigeret, erstattes udfyldningen af de faktiske metadata."
  - "**SØGETABEL**: Et valgfrit bord til at gemme søgepunkter."
  - "**VORBIS_COMMENT**: Bruges til at gemme menneskelæselige nøgle/værdi-par."
  - "**CUESHEET**: Bruges til at gemme cue sheet-oplysninger."
  - "**BILLEDE**: Bruges til at gemme billeder."
- **FRAME**: Lyddataene er sammensat af en eller flere lydrammer.
  - "**FRAME_HEADER**: Indeholder de grundlæggende oplysninger om strømmen."
  - "**SUBFRAME**: For at mindske kompleksiteten kodes individuelle underrammer separat inden for en ramme (en ramme pr. kanal)."
  - "**FRAME_FOOTER**: Indeholder CRC for hele rammen."

## Kort historie om FLAC-filformat

Josh Coalson began the development of FLAC in 2000. Den første version af FLAC blev udgivet den 20. juli 2001. FLAC blev indlemmet under Xiph.Org-flaget den 20. januar 2003. Udviklingen af FLAC blev flyttet til Xiph.Org git-lageret med udgivelsen af version 1.3.0 den 26. marts 2013.

## Sammensætning af FLAC-projektet

FLAC-projektet består af følgende:

- Stream formater.
- Simpelt containerformat til streamen (FLAC).
- libFLAC: Et bibliotek af referencekodere, dekodere og metadatagrænseflader.
- libFLAC++: En objektorienteret indpakning til libFLAC.
- flac: Et kommandolinjeprogram til at kode og afkode FLAC-streams.
- metaflac: En kommandolinje-metadataeditor til FLAC.
- Input plugins til musikafspillere som Winamp, XMMX osv.
- Ogg container format (Ogg FLAC).

## FLAC design

Afhængigt af musikkens tæthed og amplitude kan størrelsen af den komprimerede fil være 80 % mindre end den originale fil.

### Kildekoder ###

- Det understøtter kun heltalsprøver og ikke floating-point. Den kan håndtere PCM bit-opløsning fra 4 til 32 bit pr. sample og samplinghastighed fra 1Hz til 65.535 Hz. FLAC-kodning er begrænset til 24 bit pr. sample.
- Kanaler kan grupperes for at drage fordel af interkanalkorrelationer for at øge komprimeringen.
- CRC kontrolsummer bruges til at identificere korrupte rammer.
- Til konvertering af lydprøver bruger FLAC lineær forudsigelse.

### Metadata ###

- FLAC understøtter ReplayGain (bruges til at opfatte og normalisere lydstyrken).
- FLAC bruger det samme system, der bruges i Vorbis-kommentarer til tagging.
- libFLAC bruges af de fleste FLAC-applikationer til kodning/afkodning.
- libFLAC API er organiseret i streams, søgbare streams og filer for at øge abstraktionen fra basis FLAC bitstream.

### Kompression ###

libFLAC bruger kompressionsniveauer fra 0 til 8, hvor 0 er det hurtigste og 8 er det langsomste kompressionsniveau. De komprimerede filer er altid tabsfri, selvom afvejningen er mellem hastighed og størrelse.

## FLAC vs MP3
MP3 er et komprimeringsformat med tab, hvilket betyder, at det kan skære en del af lyden for at reducere størrelsen efter at have anvendt komprimering. Hvorimod FLAC er et tabsfrit filformat, hvilket betyder, at du er i stand til at høre lyden i sin reneste form. Tidligere var de tabsfrie filformater CDA eller WAV, som ikke var meget pladseffektive som FLAC. Følgende tabel viser sammenligningen mellem disse to formater for nogle vigtige udtryk:

|Term|FLAC|MP3|
---|---|---|
|**Datakvalitet**|Intet tab af lyddata| Nogle data kan gå tabt ved komprimering af lyddata|
|**Størrelse**|Større filstørrelse sammenlignet med tabsgivende formater. Så har brug for større lagerkapacitet| Mindre filstørrelse, velegnet til at afspille på kompakte lydenheder med lidt lagerplads |
|**Hardwarekrav**| Har brug for lydudstyr af høj kvalitet og enorm lagerkapacitet |Enorme lydbiblioteker kan gemmes på en mindre lagerplads. Velegnet til håndholdte enheder, såsom lydafspillere eller mobiltelefoner|
|**Distribution over internettet**|Kan ikke distribueres nemt over internettet på grund af massiv filstørrelse |Kompakt filstørrelse gør det nemt at distribuere over internettet|
|**Kompatibilitet**|Den mest populære musik- og lydlytning-codec, der stort set er kompatibel med alle enheder på planeten. Kompatibel med den nye generation af pc'er, telefoner, AV-modtagere, blu-ray-afspillere, streamingenheder som Roku eller Fire TV|

## Referencer ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

