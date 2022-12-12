---
date: 2019-12-13
keywords: ra, format pliku ra, rozszerzenie .ra, prawdziwy format pliku audio, format audio ra, format pliku RealAudio
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Dowiedz się więcej o formacie plików RA i interfejsach API, które umożliwiają tworzenie i otwieranie plików RA."
title: Format pliku RA
linktitle: RA
menu:
  docs:
    parent: "audio"
lastmod: 2020-28-12
---

## Czym jest plik RA?

RealAudio (RA) to zastrzeżony format audio opracowany przez Real Networks, Inc. i wydany w kwietniu 1995 roku. Wykorzystuje rozszerzenie .ra dla swoich plików. Wykorzystuje kodeki audio o niskiej przepływności i wysokiej wierności. RA był używany do strumieniowego przesyłania dźwięku przez Internet przez wiele internetowych stacji radiowych. Witryna BBC intensywnie korzystała z RA do 2009 r., Ale zaprzestano jej w marcu 2011 r.

## Rozszerzenie pliku przez RealNetworks ##

RealNetworks użył formatu pliku RA dla dźwięku. Firma RealNetworks zaczęła oferować format wideo ([RealVideo](/pl/video/rv/)) w 1997 roku z rozszerzeniem .rv. [RealMedia (RM)](/pl/video/rm/) został użyty do połączenia formatów audio i wideo. W najnowszej wersji RealProduce (koder firmy Real) format RV jest używany do plików wideo, a format [RealMedia Variable Bitrate (RMVB)](/pl/video/rmvb/) do plików wideo VBR (Variable bitrate).

## Strumieniowe przesyłanie dźwięku ##

RA został opracowany jako format mediów strumieniowych i może być przesyłany strumieniowo za pomocą protokołu HTTP. Odtwarzanie pliku audio rozpoczyna się natychmiast po odebraniu pierwszej części pliku i jest kontynuowane podczas pobierania reszty pliku.

Pierwsza wersja RealAudio wykorzystywała zastrzeżony protokół PNA lub PNM do strumieniowego przesyłania dźwięku. Później przeszli na znormalizowany przez IETF protokół RTSP (Real Time Streaming Protocol), aby zarządzać połączeniami. Do przesyłania danych wykorzystali protokół RDT (Real Data Transfer). Protokół był początkowo utrzymywany w tajemnicy, ale później część z niego została upubliczniona w ramach projektu Helix.

Aby przesyłać strumieniowo pliki RealAudio, większość stron łączy się z plikiem RAM (Real Audio Metadata) lub SMIL (Synchronized Multimedia Integration Language). Ten plik służy do ładowania odtwarzacza multimedialnego użytkownika i przesyłania strumieniowego dźwięku z adresu URL zawartego w pliku.

## Kodeki audio RealAudio ##

Oto lista kodeków audio, z których każdy jest identyfikowany przez czteroznakowy kod wraz z wersją RealAudio, która je wprowadziła.

|Kodek|Wersja RealAudio|
|---|---|
|lpcJ i 14_4|1|
|28_8|2|
|dnet|3|
|łyk|4/5|
|gotować|6|
|atrc|8|
|raac|9|
|zgrzyt|10|
|Ralf|10|

## Bibliografia ##

- [RealAudio - Wikipedia](https://en.wikipedia.org/wiki/RealAudio)

