---
date: 2020-08-12
keywords: jxr, .jxr, format pliku jxr, jak otwierać pliki jxr, rozszerzenie .jxr, rozszerzenie jxr
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku JXR
linktitle: JXR
description: "Dowiedz się więcej o formacie plików JXR i interfejsach API, które umożliwiają tworzenie i otwieranie plików JXR."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Czym jest plik JXR? ##

JPEG XR (JPEG rozszerzony zakres) to format pliku dla obrazów fotograficznych o ciągłych przejściach tonalnych. Jest to standard kompresji nieruchomych obrazów oparty na technologii HD Photo opracowanej przez firmę Microsoft. Obsługuje zarówno kompresję stratną, jak i bezstratną.

## Krótka historia ##

Windows Media Photo został po raz pierwszy ogłoszony przez firmę Microsoft na konferencji WinHEC 2006. W listopadzie 2006 r. zmieniono jego nazwę na HD Photo. JPEG XR został zatwierdzony jako międzynarodowy standard ISO/IEC 29199-2 w dniu 19 czerwca 2009 r. ITU-T i ISO/IEC opublikowały wniosek specyfikację formatu (ITU-T T.833 | ISO/IEC 29199-3), zestaw testów zgodności (ITU-T T.834 | ISO/IEC 29199-4) oraz oprogramowanie referencyjne (ITU-T T.835 | ISO /IEC 29199-5) dla JPEG XR po ukończeniu specyfikacji kodowania obrazu w 2010 roku. Raport techniczny opisujący architekturę przepływu pracy dla JPEG XR został opublikowany w 2011 roku.

## Projekt JPEG XR ##

W porównaniu do JPEG, JPEG XR oferuje kilka ulepszeń, w tym:

- **Lepsza kompresja**: JPEG XR oferuje wyższy stopień kompresji.
- **Kompresja bezstratna**: JPEG XR obsługuje kompresję bezstratną.
- **Struktura kafelkowa**: Obraz JPEG XR można podzielić na regiony kafelkowe, z których każdy region może być dekodowany oddzielnie.
- **Większa dokładność kolorów**: JPEG XR obejmuje wewnętrzną konwersję do przestrzeni kolorów YCoCg w celu obsługi obrazów wykorzystujących przestrzeń kolorów RGB. JPEG XR obsługuje również 16-bitowy na komponent (64-bitowy na piksel) model kolorów CMYK w liczbach całkowitych. JPEG XR obsługuje format kolorów zmiennoprzecinkowych ze współdzielonym wykładnikiem RGBE dla obrazów HDR. JPEG XR obsługuje również kodowanie w skali szarości i wielokanałowe kodowanie kolorów.
- **Mapa przezroczystości**: JPEG XR obsługuje kanał alfa dla przezroczystości.
- **Modyfikacja obrazu w domenie skompresowanej**: obrazy JPEG XR można konwertować do kodowania stratnego, zmniejszać rozdzielczość, przycinać, odwracać, obracać, a strukturę kafelków można zmieniać bez pełnego dekodowania pliku.
- **Obsługa metadanych**: Plik obrazu JPEG XR może zawierać profil kolorów ICC w celu zapewnienia spójnej reprezentacji kolorów na wielu urządzeniach. Format obsługuje również formaty metadanych Exif i XMP.

## Format kontenera ##

Dane obrazu JPEG XR można przechowywać w formacie kontenera podobnym do TIFF przy użyciu tabeli znaczników Image File Directory (IFT). Plik JXR zawiera następujące elementy w znacznikach IFD:

- Dane obrazu: Są to ciągłe, samodzielne dane obrazu.
- Opcjonalne dane kanału alfa: jeśli jest obecny, dane obrazu można skompresować oddzielnie, umożliwiając obsługę aplikacji, które nie obsługują przezroczystości.
- Metadane
- Opcjonalne metadane XMP
- Opcjonalne metadane Exif

Ponieważ jest oparty na formacie TIFF, dziedziczy wszystkie ograniczenia formatu TIFF, takie jak limit rozmiaru pliku 4 GB.

## Bibliografia ##

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

