---
date: 2021-03-21
keywords: mpc, formát souboru Musepack, přípona .mpc
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Přečtěte si o formátu souboru MPC a rozhraních API, která mohou vytvářet a otevírat soubory MPC."
title: MPC - Musepack Audio Compression File Format
linktitle: MPC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-28
---

## Co je soubor MPC?

Soubor s příponou .mpc je formát zvukového souboru [Musepack](https://musepack.net/), který používá kompresi zvuku se silným důrazem na vysokou kvalitu. Díky tomu si ani nevšimnete rozdílů v kvalitě zvuku původního souboru [WAV](/cs/audio/wav/) a komprimovaného souboru MPC. K dosažení vysoce optimalizované komprese používá algoritmy MPEG-1 Layer-2. Formát souboru Musepack MPC je open source s licencí BSD/GNU LGPL. [SVN repozitář](http://svn.musepack.net/) od Musepack umožňuje získat nejnovější aktualizovaný kód pro kodek. Aplikace, které mohou otevírat soubory MPC, zahrnují kromě několika dalších aplikací VLC Media Player, JetAudio a Winamp.

## Formát souboru MPC

Soubor MPC používá ke kompresi zvukových souborů algoritmy MPEG-1 Layer-2. Je to formát nezávislý na kontejneru a umožňuje také kódování raw streamu. Formát nepoužívá žádné vnitřní ořezávání a je streamovatelný se vzorkově přesným řezáním. Jeho Packetized stream umožňuje multiplexování do audio a video kontejnerů, jako je [MKV](/cs/video/mkv/).

## Reference

* [Musepack MPC – Wikipedia](https://en.wikipedia.org/wiki/Musepack)
* [Musepack MPC](https://musepack.net/)

