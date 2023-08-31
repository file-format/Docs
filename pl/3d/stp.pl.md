---
date: 2022-01-31
keywords: stp, .stp, format pliku stp, jak otwierać pliki stp, rozszerzenie .stp, rozszerzenie stp
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format pliku STP
linktitle: STP
description: "Dowiedz się więcej o formacie pliku STP i interfejsach API, które mogą tworzyć i otwierać pliki STP."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Czym jest plik STP?

Plik STP to plik CAD 3D używany do wymiany danych produktu między aplikacjami CAD i CAM. Zawiera informacje o obiektach 3D i jest zapisywany podobnie do formatu pliku **STEP**. Pliki STP ułatwiają wymianę danych między aplikacjami zgodnie z protokołami aplikacji [STEP](/pl/3d/step/) ISO 10303-2xx. Ten ISO definiuje mechanizm kodowania reprezentacji danych w języku modelowania danych EXPRESS. Pliki STP można otwierać w aplikacjach takich jak **Autodesk Fusion 360**.

## Format pliku STP — więcej informacji

Pliki STP są zapisywane na dysku w zwykłym formacie pliku ASCII. Zawierają one informacje o modelach 3D w postaci zwykłego tekstu, który może być odczytywany przez aplikacje CAD/CAM w celu załadowania tych modeli.

Pliki STP są również zapisywane z rozszerzeniem .step i składają się z sekwencji rekordów. Istotne cechy dotyczące tych plików obejmują:

* Zestaw znaków jest zdefiniowany jako punkty kodowe ISO 10646.
* „ISO-10303-21;” to pierwsze znaki w pierwszym rekordzie.
* Komentarze są otoczone znakami „/*” i „*/”.
* Ostatni rekord zawiera „END-ISO-10303-21;” czy plik STEP jest zgodny z wersją 2002.
* W przypadku zgodności z wersją 2016 po „END-ISO-10303-21” może znajdować się jeden lub więcej podpisów cyfrowych; terminator.
* Podziały wierszy są oznaczone przez „\N\”, a podziały stron przez „\F\”.

## Otwórz pliki STP

Pliki STP można otwierać w przeglądarkach STP oraz edytorach tekstu.

### Otwórz pliki STP za pomocą przeglądarek STP

Różne aplikacje CAD mogą otwierać pliki STP do przeglądania w systemach Windows, MacOS i Linux. Obejmują one:

* Autodesk Fusion 360 (wieloplatformowy)
* FreeCAD (wieloplatformowy)
* IMSI TurboCAD (Windows, Mac)
* Systemy Dassault CATIA (Windows, Linux)

### Otwórz pliki STP za pomocą edytorów tekstu

Pliki STP są zapisywane jako zwykłe pliki tekstowe. Umożliwia to otwieranie plików STP za pomocą edytorów tekstu. Popularne edytory tekstu, takie jak Notatnik i Notepad ++ w systemie operacyjnym Windows oraz Apple TextEdit w systemie MacOS, mogą otwierać pliki STP. Po otwarciu w edytorze tekstu użytkownik może edytować właściwości pliku STP. Może to jednak prowadzić do uszkodzenia pliku w przypadku nieprawidłowej aktualizacji właściwości.

## Jak przekonwertować pliki STP

Istnieje kilka aplikacji, które mogą konwertować pliki STP na inne formaty plików. Aplikacje CAD, które mogą konwertować pliki STP, obejmują:

* Autodesk Fusion 360
* IMSI TurboCAD
* Siemens Solid Edge

Oprócz tego istnieje kilka aplikacji internetowych, które mogą konwertować pliki STP na inne formaty plików. Te aplikacje online umożliwiają przesyłanie plików STP na serwery w chmurze, gdzie są konwertowane do żądanego formatu i zwracane z powrotem do pobrania.

Autodesk Fusion 360 może konwertować pliki STP do następujących formatów plików 3D i CAD.

* [OBJ](/pl/3d/obj/)
* [3MF](/pl/3d/3mf/)
* [DWG](/pl/cad/dwg/)
* [DXF](/pl/cad/dxf/)
* [ASM](/pl/cad/asm/)
* [IGES](/pl/cad/iges/)
* [STL](/pl/cad/stl/)
* [FBX](/pl/3d/fbx/)
* F3D
* [PLN](/pl/3d/pln/)

## Bibliografia

* [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

