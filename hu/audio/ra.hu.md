---
date: 2019-12-13
keywords: ra, ra fájlformátum, .ra kiterjesztésű, valódi hangfájlformátum, ra hangformátum, RealAudio fájlformátum
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Ismerje meg az RA fájlformátumot és az API-kat, amelyek RA-fájlokat hozhatnak létre és nyithatnak meg."
title: RA fájlformátum
linktitle: RA
menu:
  docs:
    parent: "audio"
lastmod: 2020-28-12
---

## Mi az RA fájl?

A RealAudio (RA) a Real Networks, Inc. által kifejlesztett és 1995 áprilisában kiadott szabadalmaztatott hangformátum. Fájljaihoz a .ra kiterjesztést használja. Alacsony bitrátájú, valamint nagy hűségű audiokodekeket használ. Az RA-t számos internetes rádióállomás használta audio streaminghez az interneten keresztül. A BBC weboldala 2009-ig erősen használta az RA-t, de 2011 márciusában megszűnt.

## Fájlkiterjesztés a RealNetworks által ##

A RealNetworks az RA fájlformátumot használta a hanghoz. A RealNetworks 1997-ben kezdte el kínálni a videoformátumot ([RealVideo](/hu/video/rv/)) .rv kiterjesztéssel. A [RealMedia (RM)](/hu/video/rm/) hang- és videoformátumok kombinálására szolgált. A RealProduce (Real kódolója) legújabb kiadásában az RV formátumot használják a videofájlokhoz, és a [RealMedia Variable Bitrate (RMVB)](/hu/video/rmvb/) formátumot a VBR (Variable Bitrate) videofájlokhoz.

## Streaming audio ##

Az RA-t streaming médiaformátumként fejlesztették ki, és HTTP-n keresztül streamelhető. Az audiofájl lejátszása azonnal megkezdődik, amint megérkezik a fájl első része, és a lejátszás a fájl többi részének letöltése után folytatódik.

A RealAudio első verziója a szabadalmaztatott PNA vagy PNM protokollt használta a hang streamelésére. Később áttértek az IETF szabványosított RTSP-re (Real Time Streaming Protocol) a kapcsolatok kezelésére. Az adatok küldésére az RDT (Real Data Transfer) protokollt használták. A protokollt kezdetben titokban tartották, de később a Helix projekten keresztül nyilvánosságra hozták egy részét.

A RealAudio fájlok streameléséhez az oldalak többsége a RAM (Real Audio Metadata) vagy a SMIL (Synchronized Multimedia Integration Language) fájlra hivatkozik. Ez a fájl a felhasználó médialejátszójának betöltésére és a hang streamelésére szolgál a fájlban található URL-ről.

## RealAudio Audio kodekek ##

Itt található a négy karakteres kóddal azonosított audio kodekek listája, valamint a RealAudio verziója, amely bevezette.

|Kodek|RealAudio verzió|
|---|---|
|lpcJ és 14_4|1|
|28_8|2|
|dnet|3|
|sipr|4/5|
|főzni|6|
|atrc|8|
|raac|9|
|racp|10|
|ralf|10|

## Referenciák ##

- [RealAudio - Wikipedia](https://en.wikipedia.org/wiki/RealAudio)

