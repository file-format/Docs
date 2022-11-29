---
date: 2019-12-13
keywords: ra, ra-filformat, .ra-tillägg, äkta ljudfilformat, ra-ljudformat, RealAudio-filformat
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Lär dig om RA-filformat och API:er som kan skapa och öppna RA-filer." 
title: RA filformat
linktitle: RA
menu:
  docs:
    parent: "audio"
lastmod: 2020-28-12
---

## Vad är RA fil?

RealAudio (RA) är ett eget ljudformat utvecklat av Real Networks, Inc. och släpptes i april 1995. Det använder tillägget .ra för sina filer. Den använder låg-bithastighet samt high fidelity audio codecs. RA användes för ljudströmning över internet av många internetradiostationer. BBC-webbplatsen använde RA kraftigt fram till 2009 men upphörde i mars 2011.

## Filtillägg av RealNetworks ##

RealNetworks använde RA-filformatet för ljud. RealNetworks började erbjuda videoformat ([RealVideo](/sv/video/rv/)) 1997 med tillägget .rv. [RealMedia (RM)](/sv/video/rm/) användes för kombinationen av ljud- och videoformat. Med den senaste versionen av RealProduce (Reals kodare) används RV-format för videofiler och formatet [RealMedia Variable Bitrate (RMVB)](/sv/video/rmvb/) används för VBR (Variable bitrate) videofiler.

## Strömmande ljud ##

RA utvecklades som ett strömmande mediaformat och kan strömmas med HTTP. Ljudfilen börjar spelas så snart den första delen av filen har tagits emot och fortsätter att spelas när resten av filen laddas ner.

Den första versionen av RealAudio använde det proprietära PNA- eller PNM-protokollet för att strömma ljud. Senare bytte de till IETF standardiserade RTSP (Real Time Streaming Protocol) för att hantera anslutningar. För att skicka data använde de RDT-protokollet (Real Data Transfer). Protokollet hölls hemligt till en början men senare offentliggjordes en del av det genom Helix-projektet.

För att streama RealAudio-filer länkar majoriteten av sidorna till filen RAM (Real Audio Metadata) eller SMIL (Synchronized Multimedia Integration Language). Denna fil används för att ladda användarens mediaspelare och strömma ljudet från URL:en som finns i filen.

## RealAudio Audio Codecs ##

Här är en lista över ljudkodekar som var och en identifieras av en kod med fyra tecken tillsammans med den version av RealAudio som introducerade den.

|Codec|RealAudio Version|
|---|---|
|lpcJ och 14_4|1|
|28_8|2|
|dnet|3|
|sipr|4/5|
|kock|6|
|atrc|8|
|raac|9|
|racp|10|
|ralf|10|

## Referenser ##

- [RealAudio - Wikipedia](https://en.wikipedia.org/wiki/RealAudio)

