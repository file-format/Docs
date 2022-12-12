---
date: 2021-03-21
keywords: mpc, format pliku Musepack, rozszerzenie .mpc
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Dowiedz się więcej o formacie plików MPC i interfejsach API, które mogą tworzyć i otwierać pliki MPC."
title: MPC — format pliku kompresji audio Musepack
linktitle: MPC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-28
---

## Czym jest plik MPC?

Plik z rozszerzeniem .mpc to format pliku audio [Musepack](https://musepack.net/), który wykorzystuje kompresję dźwięku z silnym naciskiem na wysoką jakość. Dzięki temu możesz nawet nie zauważyć różnic w jakości dźwięku oryginalnego pliku [WAV](/pl/audio/wav/) i skompresowanego pliku MPC. Wykorzystuje algorytmy MPEG-1 Layer-2 w celu uzyskania wysoce zoptymalizowanej kompresji. Format pliku Musepack MPC jest open source z licencją BSD/GNU LGPL. [Repozytorium SVN](http://svn.musepack.net/) firmy Musepack umożliwia pobranie najnowszego zaktualizowanego kodu dla kodeka. Aplikacje, które mogą otwierać pliki MPC, to między innymi VLC Media Player, JetAudio i Winamp.

## Format pliku MPC

Plik MPC wykorzystuje algorytmy MPEG-1 Layer-2 do kompresji plików audio. Jest to format niezależny od kontenera i umożliwia również kodowanie surowego strumienia. Format nie wykorzystuje żadnego wewnętrznego przycinania i można go przesyłać strumieniowo z cięciem z dokładnością do próbki. Jego spakowany strumień umożliwia multipleksowanie do kontenerów audio i wideo, takich jak [MKV](/pl/video/mkv/).

## Bibliografia

* [Musepack MPC – Wikipedia](https://en.wikipedia.org/wiki/Musepack)
* [Musepack MPC](https://musepack.net/)

