{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku QT — plik szybkiego filmu",
  "keywords" :[ "QT", "QuickTime video", "qt format", "jak odtwarzać pliki qt", "Quick Movie File", "QTFF", "wideo", "Apple" ],
  "description":"Poznaj format plików QT i interfejsy API, które mogą tworzyć i otwierać pliki QT.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Czym jest plik QT?

Plik z rozszerzeniem .qt to plik kontenera multimediów, który jest używany przez platformę QuickTime do przechowywania zawartości plików multimedialnych. Opracowany przez firmę Apple Inc. QuickTime File Format (QTFF) to multimedialny plik kontenera zawierający audio, wideo lub tekst do późniejszego odtworzenia. Jest to preferowany format wymiany multimediów cyfrowych między urządzeniami, aplikacjami i systemami operacyjnymi. Pliki QT są również zapisywane w formacie [MOV](/pl/video/mov/), który również został opracowany przez firmę Apple Inc. Niektóre aplikacje, które mogą otwierać pliki QT, to Apple QuickTime player, VLC media player i Media Player Classic z K- Pakiet kodeków Lite.

## Format pliku QT

QTFF jest zorientowany obiektowo i udostępnia elastyczną kolekcję obiektów w celu ułatwienia analizowania i rozszerzania. Każda ścieżka w pliku QT zawiera zakodowany cyfrowo strumień multimediów lub odniesienie do danych strumienia multimediów znajdującego się w innym pliku. Hierarchiczna struktura danych składająca się z obiektów zwanych atomami działa jak kontenery ścieżek. Specyfikacje formatu plików dla [Format pliku QT](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html) są oficjalnie dostępne przez firmę Apple Inc w celach informacyjnych dla programistów.

### Opis mediów

Opis multimediów pliku QuickTime jest przechowywany oddzielnie od danych multimedialnych. Informacje takie jak liczba ścieżek, format kompresji wideo i informacje o taktowaniu są przechowywane w opisie multimediów (znanym również jako zasób filmowy, atom filmu lub po prostu film). Dane nośnika są przywoływane przez indeks w tej strukturze nośnika. Dane multimedialne to rzeczywiste przykładowe dane, takie jak klatki wideo i próbki audio, użyte w filmie.

### Atomy

Atom to podstawowa jednostka pliku QuickTime. Istnieją dwa główne pola w każdym atomie przed jakimkolwiek innym polem: pola rozmiaru i typu. Pole rozmiaru pokazuje rozmiar atomu, podczas gdy pole typu wskazuje typ danych przechowywanych w atomie. Z natury atomy są hierarchiczne, co oznacza, że jeden atom może zawierać inne atomy, które nadal mogą zawierać inne. Układ przykładowego atomu pokazano na poniższym obrazku.

Każdy atom ma dwie części, nagłówek i dane. Nagłówek zawiera pola rozmiaru i typu, a część danych zawiera rzeczywiste dane. Ponadto każde pole jest wyjaśnione poniżej:

#### Rozmiar atomu

Nagłówek i zawartość atomu są wskazywane przez 32-bitową liczbę całkowitą znaną jako rozmiar atomu. Pole rozmiaru zawiera rozmiar atomu w bajtach, wyrażony w 32-bitowej liczbie całkowitej bez znaku.

#### Typ atomu

Typ atomu jest również pokazywany przez 32-bitową liczbę całkowitą, która jest najczęściej traktowana jako czteroznakowe pole o wartości knemonicznej, takie jak „moov” (0x6D6F6F76) dla atomu filmowego lub „trak” (0x7472616B) dla atom śladu. Poznanie typu atomu umożliwia interpretację jego danych.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Struktura plików ##

Pliki QT/MOV składają się z następujących po sobie fragmentów. Każdy fragment ma 8-bajtowy nagłówek: 4-bajtowy rozmiar fragmentu (big-endian, najpierw wysoki bajt) i 4-bajtowy typ fragmentu - jeden z predefiniowanych podpisów: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", „clip”, „crgn”, „sync”, „chap”, „tmcd”, „scpt”, „ssrc”, „PICT”. Pierwsza porcja jest typu „ftype” i ma podtyp o przesunięciu 8. MOV zdefiniowany przez podtyp, który musi być „qt”. Aby skomponować plik MOV, potrzebne są iteracyjne fragmenty, dopóki nie zostanie wykryty nieznany typ.

Oto przykładowy przykład: Po sprawdzeniu danych binarnych przykładowego pliku MOV widać, że zaczyna się on od podpisu **ftyp** (szesnastkowo: 66 74 79 70) z przesunięciem 4, które definiuje typ pliku kontenera QuickTime. Podtyp pliku to **qt~_~_** (hex: 71 74 20 20), co wskazuje na typ pliku MOV. Pierwszy blok ma rozmiar 32 (heks: 00 00 00 20, big-endian, najpierw wysoki bajt), rozmiar znajduje się przy przesunięciu 0. Przy przesunięciu 32 (heks: 20) znajduje się drugi fragment, który ma rozmiar 8 i wpisz **mdat** (szesnastkowo: 6D 64 61 74).

Następna porcja znajduje się pod offsetem 32+8#40 (hex: 28) i ma rozmiar 3 263 028 (hex: 00 31 CA 34) i wpisz **mdat** (hex: 6D 64 61 74) z offsetem 44 (hex : 2C). Następny fragment znajduje się pod offsetem 40 + 3 263 028#3 263 068 (hex: 00 31 CA 5C) i ma rozmiar 21 189 (hex: 00 00 52 C5) i typ **moov** (hex: 6D 6F 6F 76) z offsetem 1 836 019 574 (szesnastkowo: 00 31 CA 60). To jest ostatnia porcja, więc całkowity rozmiar pliku wynosi 3 263 068+21 189#3 284 257 bajtów.

## Bibliografia ##

* [Format pliku QT — Apple Inc.](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html)
* [Format pliku QuickTime – Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

