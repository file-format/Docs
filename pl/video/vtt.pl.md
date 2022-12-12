---
date: 2022-01-06
keywords: vtt, .vtt, format pliku vtt, format pliku .vtt, rozszerzenie .vtt, rozszerzenie vtt
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Dowiedz się więcej o pliku .vtt i interfejsach API, które mogą tworzyć i otwierać pliki VTT."
title: Format pliku VTT — plik ścieżek tekstowych wideo z sieci Web
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## Czym jest plik VTT?

Plik VTT to plik tekstowy zawierający informacje do wyświetlania ścieżek tekstowych w określonym czasie (takich jak napisy lub podpisy) przy użyciu formatu Web Video Text Tracks (WebVTT). Ścieżki tekstowe w określonym czasie zawierają informacje, takie jak napisy lub podpisy. Celem pliku VTT jest dodanie nakładek tekstowych do pliku<video> . Format jest nieco podobny do plików SRT. Pliki tekstowe oparte na WebVTT są kodowane przy użyciu UTF-8. Plik VTT zawiera informacje, takie jak napisy, opisy, podpisy, opisy, rozdziały i metadane. Będąc zwykłymi plikami tekstowymi, pliki VTT można otwierać za pomocą edytorów tekstu, takich jak Microsoft Notepad, Apple TextEdit i Notepad ++.

## Format pliku VTT — więcej informacji

Pliki VTT używają formatu pliku WebVTT do zapisywania informacji o sekwencyjnych ścieżkach tekstowych. Każda ścieżka tekstowa o określonym czasie składa się z pojedynczej linii lub wielu linii, zwanych również „wskazówką”, jak pokazano w poniższym przykładzie.

### Przykład pliku VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### Struktura pliku VTT

Poniżej przedstawiono wymagania dotyczące struktury pliku VTT.

* Opcjonalny znacznik kolejności bajtów (BOM).
* Ciąg "WEBVTT".
* Opcjonalny nagłówek tekstowy po prawej stronie WEBVTT.
* Pusta linia, która odpowiada dwóm kolejnym znakom nowej linii.
* Zero lub więcej wskazówek lub komentarzy.
* Zero lub więcej pustych linii.

## Bibliografia

* [VTT – W3 Schools](https://www.w3.org/TR/webvtt1/)
* [WebVTT – Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

