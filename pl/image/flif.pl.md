---
date: 2020-08-12
keywords: flif, .flif, format pliku flif, jak otwierać pliki flif, rozszerzenie .flif, rozszerzenie flif
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku FLIF
linktitle: FLIF
description: "Dowiedz się więcej o formacie plików FLIF i interfejsach API, które umożliwiają tworzenie i otwieranie plików FLIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Czym jest plik FLIF? ##

FLIF (Free Lossless Image Format) to bezstratny format obrazu, który wykorzystuje rozszerzenie .flif dla swoich plików. FLIF twierdzi, że przewyższa [PNG](/pl/image/png/), bezstratny [WebP](/pl/image/webp/), bezstratny BPG i bezstratny JPEG 2000 pod względem współczynnika kompresji. FLIF wykorzystuje progresywny przeplot, dzięki czemu każde częściowe pobranie obrazu może zostać użyte jako kodowanie stratne dla całego obrazu.

## Krótka historia ##

FLIF został ogłoszony we wrześniu 2015 r., A wersja alfa została wydana w październiku 2015 r. We wrześniu 2016 r. Została wydana pierwsza stabilna wersja FLIF.

## Projekt FLIF ##

FLIF wykorzystuje wariant CABAC (kontekstowe adaptacyjne binarne kodowanie arytmetyczne), MANIAC (Meta-adaptacyjne kodowanie arytmetyczne bliskie zeru całkowitemu) do kompresji. MANIAC to algorytm kodowania entropijnego opracowany przez Jona Sneyersa i Pietera Wuille'a. W MANIAC konteksty to węzły drzew decyzyjnych, które są uczone dynamicznie w czasie kodowania. To sprawia, że model kontekstu jest bardziej specyficzny dla obrazu i skutkuje lepszą kompresją. FLIF ma następujące funkcje:

- Obsługuje bezstratną kompresję
- Obsługuje kompresję stratną z przetwarzaniem wstępnym enkodera
- Obsługuje skalę szarości, RGB i RGBA
- Obsługuje głębię kolorów od 1 do 16 bitów na kanał
- Obsługuje pliki z przeplotem i bez przeplotu
- Obsługuje progresywne dekodowanie częściowo pobranych plików
- Obsługuje animacje
- Obsługuje osadzone profile kolorów ICC, metadane Exif i XMP
- Ma ograniczoną obsługę kompresji plików Camera Raw (RGGB)

## Format pliku FLIF ##

Plik FLIF składa się z następujących czterech części:

## Główny nagłówek ##

Główny nagłówek zawiera główne metadane, w tym szerokość, wysokość, głębię kolorów, liczbę klatek.

|Typ|Wartość|Opis|
|---|---|---|
|4 bajty|"FLIF"|Magia|
|4 bity|3 = ni nadal; 4 = nadal; 5 = brak animacji; 6 = i anim|Przeplot, animacja|
|4 bity|1 = Skala szarości; 3 = RGB; 4 = RGBA|Liczba kanałów (nb_kanałów)|
|1 bajt|'0','1','2' ('0'=custom)|Bajty na kanał (Bpc)|
|wariant|szerokość-1|szerokość|
|wariant|wysokość-1|wysokość|
|varint|nb_frames-2 (tylko w przypadku animacji)|Liczba klatek (nb_frames)|

## Fragmenty metadanych ##

Ta część zawiera metadane inne niż piksele, takie jak metadane Exif/XMP, profil kolorów ICC itp., które są zakodowane przy użyciu kompresji DEFLATE. Te kawałki są definiowane podobnie do kawałków PNG, z tą różnicą, że rozmiar uchwytu jest zakodowany ze zmienną liczbą bajtów. Nazwy fragmentów mogą składać się z 4 liter (4 bajtów) lub wartości mniejszej niż 32, co wskazuje na nieopcjonalny fragment.

Poniżej znajduje się przykład opcjonalnych uchwytów:

|Nazwa fragmentu|Opis|Zawartość (po dekompresji DEFLATE)|
|---|---|---|
|iCCP|profil kolorów ICC|surowe dane profilu kolorów ICC|
|eXif|Metadane Exif|Nagłówek "Exif\0\0", po którym następuje nagłówek TIFF i dane EXIF|
|eXmp|Metadane XMP|XMP zawarte w xpakiecie tylko do odczytu bez dopełnienia|

### Konwencja nazewnictwa ###

- **Pierwsza litera**: Duże litery są używane w przypadku fragmentów krytycznych, a małe w przypadku porcji niekrytycznych.
- **Druga litera**: Wielkie litery są używane dla fragmentów publicznych, a małe dla fragmentów prywatnych
- **Trzecia litera**: Wielkie litery są używane w przypadku uchwytów, które są potrzebne do prawidłowego wyświetlenia obrazu, a małe litery nie są ważne do wyświetlenia obrazu.
- **Czwarta litera**: Wielka litera jest używana w przypadku uchwytów, które można bezpiecznie kopiować na ślepo. Uchwyty z małymi literami zależą od danych obrazu.

## Drugi nagłówek ##

Zawiera informacje dotyczące rzeczywistego kodowania pikseli.

|Typ|Opis|Warunek|Wartość domyślna|
|---|---|---|---|
|1 bajt|Bajt NUL (0x00), nazwa fragmentu strumienia bitów FLIF16||
|uni_int(1,16)|Bity na piksel kanałów|Bpc == '0': powtórz(nb_channels)|8 if Bpc == '1', 16 if Bpc == '2'|
|uni_int(0,1)|Flaga: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Liczba pętli|nb_frames > 1||
|uni_int(0,60_000)|Opóźnienie ramki w ms|nb_frames > 1: repeat(nb_frames)|
|uni_int(0,1)|Flaga: has_custom_cutoff_and_alpha|||
|uni_int(1,128)|odcięcie|ma_niestandardowe_odcięcie_i_alfa|2|
|uni_int(2,128)|dzielnik alfa|has_custom_cutoff_and_alpha|19|
|uni_int(0,1)|Flaga: ma_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Suka|ma_custom_bitchance||
|zmienna|Transformacje (patrz poniżej)|||
|uni_int(1) = 0|Bit wskaźnika: zrobione z transformacjami|||
|uni_int(0,2)|Predyktor niewidocznych pikseli|alpha_zero && przeplot && zakres alfa obejmuje zero||

**Kanały**

|Numer kanału|Opis|
|---|----|
|0|Czerwony lub Szary|
|1|Zielony|
|2|Niebieski|
|3|Alfa|

**Transformacje**

|Typ|Opis|
|---|---|
|uni_int(1) = 1|Bit wskaźnika: jeszcze nie zrobione|
|uni_int(0,13)|Identyfikator transformacji|
|zmienna|Dane transformacji (w zależności od transformacji)|

Transformacja służy do modyfikowania danych pikseli w celu lepszej kompresji i śledzenia faktycznie występujących wartości pikseli.

## Dane pikseli ##

Ta część zawiera rzeczywiste dane pikseli zakodowane przy użyciu kodowania entropijnego MANIAC. Piksele mogą być kodowane przy użyciu kodowania z przeplotem lub bez przeplotu.

### Metoda z przeplotem ###

W tej metodzie definiowane są poziomy powiększenia. Zoomlevel 0 jest używany dla pełnego obrazu, zoomlevel 1 jest używany dla wszystkich parzystych wierszy, zoomlevel 2 jest używany dla wszystkich parzystych kolumn na poziomie zoom 1. Innymi słowy, każdy parzysty poziom zoomu 2k jest próbkowaną w dół wersją obraz w skali 1:2^k. Poziomy powiększenia są kodowane od najwyższego do najniższego.

### Metoda bez przeplotu ###

W tej metodzie kodowanie drzew MANIAC rozpoczyna się natychmiast po kodowaniu pikseli.

## Bibliografia ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

