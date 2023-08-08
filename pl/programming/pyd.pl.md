---
date: 2022-05-09
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format pliku PYD — dynamiczny moduł Pythona
linktitle: PYD
description: "Dowiedz się o formacie pliku PYD i interfejsach API, które mogą tworzyć i otwierać pliki PYD."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Czym jest plik PYD?

Plik PYD to biblioteka dołączana dynamicznie napisana w Pythonie, która może być uruchamiana przez inny kod Pythona w czasie wykonywania. Zawiera jeden lub więcej modułów Pythona, które ułatwiają ponowne wykorzystanie kodu i zapewniają architekturę modułów do pisania aplikacji. Pliki PYD można tworzyć i zapisywać z rozszerzeniem .pyd, np. helloworld.pyd. Twórcy aplikacji mogą użyć instrukcji importu, aby dołączyć moduły PYD do swoich aplikacji. Pliki PYD można otwierać za pomocą Python Software Foundation Python, który jest dostępny dla systemów Windows, Mac i Linux.

## Format pliku PYD — więcej informacji

Pliki PYD są napisane w języku programowania Python i są generowane przez kompilację kodu Pythona.

## Różnica między formatami plików PY i PYD

Plik [PY](/pl/programming/py/) zawiera kod źródłowy, który jest wykonywany tak, jak jest i nie może być dołączany jako kod wielokrotnego użytku w innych aplikacjach Pythona. Jednak plik PYD jest dynamicznie połączoną biblioteką, która ma być używana w systemie operacyjnym Windows.

## Jak utworzyć plik PYD?

Plik PYD można utworzyć, tworząc moduł o nazwie np. exmaple.pyd. Moduł ten będzie zawierał całą funkcjonalność w postaci jednej lub kilku funkcji np. PyMod_example(). Kiedy program zawiera tę bibliotekę i wywołuje ją, można to zrobić poprzez zaimportowanie modułu i wtedy zostanie uruchomiona funkcja PyMod_example().

## Bibliografia ##

* [Tworzenie rozszerzeń Pythona w C/C++](https://sebsauvage.net/python/mingw.html)
* [Python (język programowania) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

