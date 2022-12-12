---
date: 2019-12-09
keywords: arj, .arj, formát souboru arj, jak otevřít soubory arj, přípona .arj, přípona arj
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru ARJ
linktitle: ARJ
description: "Přečtěte si o formátu souboru ARJ a rozhraních API, která mohou vytvářet a otevírat soubory ARJ."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Co je soubor ARJ? ##

ARJ (Archived by Robert Jung) je vysoce účinný komprimovaný archivní soubor vyvinutý Robertem K. Jungem. ARJ byl vyvinut pro DOS a rané verze Windows na počátku 90. let. Soubory ARJ jsou užitečné pro zálohování nebo sdílení velkého počtu souborů, protože nemusíte sledovat všechny tyto soubory a je třeba zpracovávat pouze jeden soubor. Pro archivní soubory ARJ se používá přípona .arj.

## Formát souboru ARJ ##

Soubor ARJ obsahuje dva typy záhlaví:

- Hlavní záhlaví: Na začátku archivu je jedno hlavní záhlaví.
- Lokální záhlaví: Lokální záhlaví jsou přítomna před každým souborem.

|Offset|Typ|Počet|Popis|
|---|---|---|---|
|0000h|slovo|1|ID=0EA60h|
|0002h|slovo|1|základní velikost záhlaví|
|0004h|byte|1|Velikost záhlaví|
|0005h|byte|1|Číslo verze archivu|
|0006h|byte|1|Potřebné minimální číslo verze|
|0007h|byte|1|Hostitelský OS:</br> 0 - MS-DOS</br> 1 - PRIMOS</br> 2 - UNIX</br> 3 - AMIGA</br> 4 - MAC-OS (System xx)</br> 5 - OS/2</br> 6 - JABLKO GS</br> 7 - ATARI ST</br> 8 - DALŠÍ</br> 9 - VAX VMS|
|0008h|byte|1|Interní příznaky, bitmapové:</br> 0 - žádné heslo / heslo</br> 1 - vyhrazeno</br> 2 - soubor pokračuje na dalším disku</br> 3 - je k dispozici pole počáteční pozice souboru</br> 4 - překlad cesty ( "\" na "/" )|
|0009h|byte|1|Metoda komprese:</br> 0 - uloženo</br> 1 - nejvíce komprimované</br> 2 - stlačený</br> 3 - komprimováno rychleji</br> 4 - nejrychlejší komprimace|
|000Ah|byte|1|Typ souboru:</br> 0 - binární</br> 1 - 7bitový text</br> 2 - záhlaví komentáře</br> 3 - adresář</br> 4 - štítek svazku|
|000Bh|byte|1|rezervováno|
|000Ch|dword|1|Datum/čas původního souboru ve formátu MS-DOS|
|0010h|dword|1|Velikost komprimovaného souboru|
|0014h|dword|1|Velikost původního souboru"|
|0018h|dword|1|CRC-32 původního souboru|
|001Ah|slovo|1|Umístění specifikace souboru v souboru|
|001Ch|slovo|1|Atributy souboru|
|001Eh|slovo|1|Data hostitele|
|?|dword|1|Počáteční pozice rozšířeného souboru|
|????h|dword|1|CRC-32 základního záhlaví|
|????h|word|1|Velikost prvního rozšířeného záhlaví|
|????h+"SIZ"+2|dword|1|CRC-32 rozšířeného záhlaví|
|????h+"SIZ"+6|byte|?|Komprimovaný soubor|

## Reference ##

- [ARJ - Wikipedie](https://en.wikipedia.org/wiki/ARJ)

