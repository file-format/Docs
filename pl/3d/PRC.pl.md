---
date: 2019-10-11
keywords: prc, .prc, format pliku prc, jak otwierać pliki prc, rozszerzenie .prc, rozszerzenie prc
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku PRC
linktitle: PRC
description: "Dowiedz się więcej o formacie plików PRC i interfejsach API, które umożliwiają tworzenie i otwieranie plików PRC."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## Formaty plików PRC
Rozszerzenia „.prc” są używane w formacie pliku Product Representation Compact 3D oraz w formacie pliku e-book firmy MobiPocket.

## Co to jest plik Product Representation Compact (PRC)?

PRC (Product Representation Compact) to format pliku 3D zoptymalizowany do przechowywania, ładowania i wyświetlania danych 3D, zwłaszcza pochodzących z systemów CAD (projektowanie wspomagane komputerowo). Jest to sekwencyjny plik binarny, napisany w sposób przenośny. PRC może służyć do osadzania danych 3D w pliku PDF. PRC obsługuje większość głównych konstrukcji CAD, takich jak zespoły i części, drzewa elementów 3D, reprezentacja dokładnej geometrii, reprezentacja triangulowana i znaczniki. PRC używa rozszerzenia .prc, a używany typ mediów internetowych to *model/prc*.

PRC to uniwersalny format plików, który w zależności od zastosowania może być przechowywany przy użyciu zwykłej kompresji w celu bezpośredniego przedstawienia danych CAD lub przy użyciu wysokiej kompresji w celu zmniejszenia rozmiaru pliku. Dane 3D zapisane w formacie PDF w formacie PRC są kompatybilne z aplikacjami CAM i CAE.

### Specyfikacja formatu pliku Product Representation Compact (PRC).

Plik PRC ma jedną główną sekcję nagłówka, po której następuje jedna lub więcej struktur plików, po których na końcu znajduje się jeden plik modelu. Struktura plików ma jeden nagłówek, po którym następują następujące sekcje danych:

- **Globalne**: Zawiera odniesienia do struktur plików i kolorów, stylów linii i układów współrzędnych dla każdego elementu drzewa struktury pliku.
- **Drzewo**: Zawiera opis drzewa elementów, takich jak wystąpienia produktów, definicje części, elementy reprezentacji i znaczniki.
- **Teselacja**: Zawiera wszystkie mozaikowane (triangulowane) dane w elementach liści drzewa (elementy reprezentacji i znaczniki).
- **Geometria**: Zawiera wszystkie dokładne dane geometrii i topologii elementów liścia drzewa (elementy reprezentacji).
- **Dodatkowa geometria**: Zawiera podsumowanie danych geometrii. Pozwala to na częściowe załadowanie pliku bez ładowania całej geometrii.

Poniżej przedstawiono strukturę typowego pliku PRC.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## Co to jest plik e-booka MobiPocket z rozszerzeniem PRC
Format pliku e-booka wprowadzony przez francuską firmę **Mobipocket** również używa rozszerzenia „.prc”. Początkowo Mobipocket uruchomił bezpłatną aplikację dla wielu inteligentnych urządzeń, takich jak tablety, PDA i smartfony. Rozszerzenie „.prc” jest w rzeczywistości identyczne z rozszerzeniem .mobi, ale jest używane zwłaszcza w urządzeniach PDA, które obsługują tylko rozszerzenia **.prc** lub **.pdb**.

### Specyfikacje formatu pliku Mobipocket PRC
Format pliku MobiPocket PRC jest oparty na standardzie Open eBook przy użyciu XHTML, a także może zawierać JavaScript i ramki. Dostępna jest również obsługa natywnych zapytań SQL, które mają być używane z osadzonymi bazami danych.

Czytnik Mobipocket ma bibliotekę strony głównej. Czytelnicy mogą wstawiać puste strony w dowolnej części książki i dodawać zmienne rysunki. Obiektami takimi jak adnotacje, zakładki, poprawki, notatki i rysunki można zarządzać z jednego miejsca. Obrazy są konwertowane do formatu GIF i mają maksymalny rozmiar 64K, który jest wystarczający dla telefonów komórkowych z małymi ekranami. Mobipocket Reader posiada elektroniczne zakładki oraz wbudowany słownik.

Czytnik posiada tryb pełnoekranowy do czytania i obsługuje wiele PDA, Komunikatorów i Smartfonów. Produkty Mobipocket obsługują większość systemów operacyjnych Palm, Windows, Symbian, BlackBerry, ale nie Android. Czytnik pracuje pod Linuksem lub Mac OS X z wykorzystaniem WINE.

## Bibliografia

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [Specyfikacja formatu PRC](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCRReference/PRC_Format_Specification/index.html)
- [Porównanie formatów e-booków – Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

