---
date: 2019-12-13
keywords: ra, formát souboru ra, přípona .ra, formát skutečného zvukového souboru, zvukový formát ra, formát souboru RealAudio
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Přečtěte si o formátu souboru RA a rozhraních API, která mohou vytvářet a otevírat soubory RA."
title: Formát souboru RA
linktitle: RA
menu:
  docs:
    parent: "audio"
lastmod: 2020-28-12
---

## Co je soubor RA?

RealAudio (RA) je proprietární zvukový formát vyvinutý společností Real Networks, Inc. a vydaný v dubnu 1995. Pro své soubory používá příponu .ra. Používá nízkobitové i vysoce věrné zvukové kodeky. RA byl používán pro streamování zvuku přes internet mnoha internetovými rozhlasovými stanicemi. Webová stránka BBC používala RA až do roku 2009, ale v březnu 2011 byla ukončena.

## Přípona souboru od RealNetworks ##

RealNetworks používal formát souboru RA pro zvuk. RealNetworks začal nabízet video formát ([RealVideo](/cs/video/rv/)) v roce 1997 s příponou .rv. [RealMedia (RM)](/cs/video/rm/) byl použit pro kombinaci audio a video formátů. S nejnovější verzí RealProduce (kodér Realu) se formát RV používá pro video soubory a formát [RealMedia Variable Bitrate (RMVB)](/cs/video/rmvb/) se používá pro video soubory VBR (Variable bitrate).

## Streamování zvuku ##

RA byl vyvinut jako formát streamovaného média a lze jej streamovat pomocí HTTP. Zvukový soubor se začne přehrávat, jakmile je přijata první část souboru, a pokračuje v přehrávání, jakmile se stáhne zbytek souboru.

První verze RealAudio používala proprietární protokol PNA nebo PNM pro streamování zvuku. Později přešli na standardizovaný IETF RTSP (Real Time Streaming Protocol) pro správu připojení. K odesílání dat používali protokol RDT (Real Data Transfer). Protokol byl zpočátku držen v tajnosti, ale později byly některé z nich zveřejněny prostřednictvím projektu Helix.

Chcete-li streamovat soubory RealAudio, většina stránek odkazuje na soubor RAM (Real Audio Metadata) nebo SMIL (Synchronized Multimedia Integration Language). Tento soubor se používá k načtení přehrávače médií uživatele a streamování zvuku z adresy URL obsažené v souboru.

## RealAudio Audio kodeky ##

Zde je seznam zvukových kodeků, z nichž každý je identifikován čtyřznakovým kódem spolu s verzí RealAudio, která jej zavedla.

|Kodek|Verze RealAudio|
|---|---|
|lpcJ a 14_4|1|
|28_8|2|
|dnet|3|
|sipr|4/5|
|vařit|6|
|atrc|8|
|raac|9|
|racp|10|
|ralf|10|

## Reference ##

- [RealAudio - Wikipedie](https://en.wikipedia.org/wiki/RealAudio)

