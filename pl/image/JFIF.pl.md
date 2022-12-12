---
date: 2020-08-12
keywords: jfif, .jfif, format pliku jfif, jak otwierać pliki jfif, rozszerzenie .jfif, rozszerzenie jfif
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Plik JFIF - Co to jest plik .jfif?
linktitle: JFIF
description: "Dowiedz się więcej o formacie pliku JFIF i interfejsach API, które umożliwiają tworzenie i otwieranie plików JFIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Czym jest plik JFIF?

JFIF (JPEG File Interchange Format (JFIF)) to plik formatu obrazu, który używa rozszerzenia .jfif. JFIF opiera się na JIF (JPEG Interchange Format), zmniejszając złożoność i rozwiązując jego ograniczenia.

## Krótka historia JFIF

Rozwój dokumentu JFIF był prowadzony przez Erica Hamiltona, a pod koniec 1991 r. Zawarto porozumienie w sprawie pierwszej wersji. Wersja 1.02 została opublikowana 7 września 1992 r. RFC 2046 określał, że format JFIF jest używany do przesyłania obrazów JPEG przez Internet. JFIF został opublikowany przez ECMA w 2009 r. i został znormalizowany przez ITU-T w 2011 r. jako zalecenie T.871 oraz przez ISO/IEC w 2013 r. jako ISO/IEC 10918-5

## Format pliku JFIF ##

Plik JFIF składa się z sekwencji znaczników zgodnie z definicją w części 1 standardu JPEG. Każdy znacznik składa się z dwóch bajtów (FF, po którym następuje bajt określający typ znacznika). Znaczniki mogą być samodzielne lub wskazywać początek segmentu znacznika.

JFIF pozwala wielu komponentom, takim jak Y, Cb, Cr, mieć różne rozdzielczości, ale ich wyrównanie nie jest zdefiniowane. W przeciwieństwie do JPEG, JFIF może dostarczać informacje o rozdzielczości i współczynniku proporcji. JFIF definiuje również używany model kolorów.

### Struktura plików ##

|Segment|Kod|Opis|
|---|---|---|
|SOI|FF D8|Początek obrazu|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|dodatkowe segmenty znaczników|
|SOS|FF DA|Początek skanowania|
||skompresowane dane obrazu||
|EOI|FF D9|Koniec obrazu|

Standard JFIF definiuje następujące segmenty:

### Segment znacznika JFIF APP0 ###

Jest to obowiązkowy segment zawierający parametry obrazu. Może również zawierać osadzoną nieskompresowaną miniaturę.

|Pole|Rozmiar (bajty)|Opis|
|---|---|---|
|Znacznik APP0|2|FF E0|
|Długość|2|Długość segmentu bez znacznika APP0|
|Identyfikator|5|JFIF (4A 46 49 46 00) w ASCII zakończony bajtem zerowym|
|Wersja JFIF|2|Wersja JFIF|
|Jednostki gęstości|1|Jednostki dla następujących pól gęstości pikseli</br> 00 : Brak jednostek; szerokość:wysokość proporcji pikseli jest równa Ydensity:Xdensity</br> 01 : Piksele na cal</br> 02 : Piksele na centymetr|
|Xdensity|2|Gęstość pikseli w poziomie większa od zera|
|Ygęstość|2|Pionowa gęstość pikseli większa od zera|
|Xthumbnail|1|Pozioma liczba pikseli osadzonej miniatury RGB. Może wynosić zero|
|Ythumbnail|1|Pionowa liczba pikseli osadzonej miniatury RGB. Może wynosić zero|
|Dane miniatur|3 × n|Nieskompresowane 24-bitowe dane miniatur rastrowych RGB|

### Rozszerzenie JFIF Segment znacznika APP0 ###

Jest to opcjonalna sekcja, która, jeśli jest zdefiniowana, musi znajdować się bezpośrednio po segmencie znacznika JFIF APP0. Ta sekcja jest obsługiwana przez JFIF w wersji 1.02 i nowszych i umożliwia osadzanie miniatur w trzech różnych formatach.

|Pole|Rozmiar (bajty)|Opis|
|---|---|---|
|Znacznik APP0|2|FF E0|
|Długość|2|Długość odcinka bez znacznika APP0|
|Identyfikator|5|JFXX (4A 46 58 58 00) w ASCII zakończony bajtem zerowym|
|Format miniatury|1|Określa, jaki format danych jest używany dla następującej osadzonej miniatury:</br> 10 : Format JPEG</br> 11: 1 bajt na piksel w formacie z paletą</br> 13: 3 bajty na piksel Format RGB|
|Dane miniatury|zmienna||

## Konwersja JFIF do innych formatów plików graficznych

JFIF można konwertować do popularnych formatów plików graficznych, takich jak [PNG](/pl/image/png/), [JPG](/pl/image/jpg/) i [PDF](/pl/pdf/).

## Bibliografia ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

