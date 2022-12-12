---
date: 2019-12-09
keywords: arc, .arc, format pliku arc, jak otwierać pliki arc, rozszerzenie .arc, rozszerzenie arc
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku ARC
linktitle: ARC
description: "Dowiedz się więcej o formacie pliku ARC i interfejsach API, które umożliwiają tworzenie i otwieranie plików ARC."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Czym jest plik ARC?

ARC to bezstratny format kompresji danych i archiwizacji opracowany przez firmę System Enhancement Associates (SEA). Format pliku i aplikacja, która go tworzy, nazywa się ARC. ARC był bardzo popularny we wczesnych latach BBS dial-up, ponieważ łączył funkcje kompresji i archiwizacji wielu plików w tym samym pliku. ARC został później zastąpiony przez [ZIP](/pl/compression/zip/), który oferował lepsze współczynniki kompresji.

Rozszerzenie pliku .arc jest używane przez kilka innych niepowiązanych typów plików archiwów, takich jak format ARC używany przez Internet Archive do przechowywania wielu zasobów internetowych, inny format ARC używany przez archiwizator FreeArc, inny format używany przez Nintendo dla zasobów itp. .

## Krótka historia formatu pliku ARC

Program ARC został napisany przez Thoma Hendersona z System Enhancement Associates w 1985 roku. Ten program grupował pliki w jeden plik archiwum, a także je kompresował. Pliki generowane przez program ARC korzystały z rozszerzenia .arc. SEA wydała kod źródłowy ARC w 1986 roku, a ARC został przeniesiony na Unix i Atari ST przez Howarda Chu w 1987 roku.

Phil Katz opracował PKARC i PKXARC do archiwizacji i wyodrębniania plików. Pliki działały z formatem pliku ARC i były znacznie szybsze. W przeciwieństwie do ARC, Katz podzielił funkcje kompresji i archiwizacji między dwa różne pliki, co zmniejszyło zapotrzebowanie na pamięć do ich uruchomienia.

Po procesie sądowym między SEA i Katz, SEA wycofała się z rynku oprogramowania typu shareware i opracowała ARC + Plus z pełnoekranowym interfejsem użytkownika. Format ARC nie jest już powszechny na PC.

## Format pliku ARC

Plik ARC składa się z sekwencji nagłówka pliku i pliku, po których następuje znacznik końca archiwum, jak pokazano poniżej.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### Nagłówek pliku ARC ###

|Przesunięcie|Etykieta|Typ|Wartość|Opis|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Metoda|
|02|ARCFNT|DS|12|nazwa_pliku|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Rozmiar skompresowany|
|13|ARCDAT|DW|0000|Data pliku (MSDOS)|
|15|ARCTIM|DW|0000|Czas pliku (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Rozmiar nieskompresowany|
|1D|ARCFIL|DS|ARCNSZ| |

### Metody kompresji ###

Bajt metody kompresji wskazuje zastosowaną metodę kompresji. Poniżej przedstawiono metody kompresji stosowane w przypadku pliku ARC.

|Metoda|Nazwa|Opis|
|---|---|---|
|0|Przechowywane|Bez kompresji|
|1|Pakowane|Powtórzone kodowanie długości bieżącej (RLE)|
|2|Ściśnięte|Kodowanie Huffmana|
|3|Crunched|LZW z buforem 4K, kody 12-bitowe|
|4|Crunched|Najpierw pakowanie, potem bufor LZW 4K z 12 bitami|
|5|Crunched|Pakowanie, LZW, bufor 4K, zmienna długość (9-12 bitów)|
|6|Squashed|LZW, bufor 8K, zmienna długość (9-13 bitów)|
|7|Crushed|Pakowanie, następnie bufor LZW 8K, 2-13 bitów (PAK 1.0)|
|8|Dystyl|Dynamiczny Huffman z buforem 8K (PAK 2.0)|

## Bibliografia

- [ARC (format pliku) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

