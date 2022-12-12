---
date: 2019-10-11
keywords: vob, .vob, format pliku vob, format pliku .vob, rozszerzenie .vob, rozszerzenie vob, format wideo vob, pliki vob dvd
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Dowiedz się o formacie pliku VOB i interfejsach API, które mogą tworzyć i otwierać pliki VOB."
title: Format pliku VOB
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Czym jest plik VOB? ##

Pliki VOB są zwykle przechowywane w katalogu VIDEO_TS na płycie DVD z rozszerzeniem .vob. Pliki VOB zawierają dane wideo i audio, a także inne dane, takie jak menu i napisy. VOB jest oparty na formacie strumienia programu MPEG-2, ale ma dodatkowe ograniczenia i specyfikacje w strumieniach prywatnych. Pliki VOB są ścisłym podzbiorem strumieni programów MPEG, więc wszystkie pliki VOB są strumieniami programów MPEG, ale wszystkie strumienie programów MPEG nie są zgodne z VOB.

## Struktura DVD Video ##

Kiedy DVD jest otwierane na komputerze, VIDEO_TS jest katalogiem najwyższego poziomu z AUDIO_TS. AUDIO_TS jest puste i nie jest używane. W katalogu VIDEO_TS znajdują się pliki VOB, BUP i IFO. Pliki VOB zawierają zawartość MPEG. Są one podzielone na części o wielkości 1 GB lub mniejszej, dzięki czemu są kompatybilne ze wszystkimi systemami operacyjnymi. Pliki IFO zawierają informacje dotyczące menu i struktury tytułów. Pliki BUK to pliki kopii zapasowych plików IFO o tej samej nazwie. Pliki te mają być fizycznie przechowywane w osobnym obszarze, aby w przypadku uszkodzenia pliku IFO z powodu fizycznego uszkodzenia DVD plik BUK mógł dostarczyć tych samych informacji.

### Układ fizyczny ###

- Wszystkie pliki na dysku muszą być ciągłe.
- Powiązane pliki powinny znajdować się obok siebie (VOB, IFO, BUP).
- Pliki ponumerowane powinny być w porządku rosnącym.

## Ochrona przed kopiowaniem ##

Wiele dysków DVD z filmami jest zaszyfrowanych i uniemożliwia kopiowanie danych z dysku DVD. Klucze uwierzytelniające i deszyfrujące są potrzebne do odtworzenia plików, które znajdują się w niedostępnym obszarze wejściowym płyty DVD. Te klucze są używane przez oprogramowanie do odszyfrowywania CSS, które jest obecne w odtwarzaczu DVD lub odtwarzaczu programowym. Bez kluczy nie można odtwarzać plików wideo, ponieważ podczas otwierania plików wymagane będzie podanie kluczy.

## Bibliografia ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Struktura katalogów](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

