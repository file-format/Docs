{
  "date" : "2021-09-08",
  "keywords" :[ "plik mgx", "format pliku mgx", "co to jest plik mgx", "plik", "przykład mgx", "rozszerzenie pliku mgx", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się więcej o formacie pliku Age of Empires 2 Expansion Replay MGX i interfejsach API, które mogą tworzyć i otwierać pliki MGX.",
  "title" :"MGX - Powtórka rozszerzenia Age of Empires 2",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Czym jest plik MGX?

Plik z rozszerzeniem .mgx to nagrany plik gry Age of Empires II: The Conquerors, który można odtworzyć w programie Age of Empires II. Zawiera pełne nagranie kampanii rozgrywanej przez użytkownika. Można go załadować i odtwarzać w programie Age of Empires II. Po ponownym odtworzeniu gra pokazuje wszystkie wydarzenia i scenariusze, które użytkownik zaplanował na potrzeby kampanii i rozegrał.

## Format pliku MGX — więcej informacji

Wewnętrzny format pliku MGX został opracowany i udostępniony jako częściowo potwierdzona informacja na [Age of Empires 2: The Conquerors — Specyfikacja formatu pliku zapisu gry](https://github.com/stefan-kolb/aoc-mgx-format). Specyfikacje przedstawiają szczegóły w poniższych sekcjach.

### Definicje struktur

Uważa się, że definicje struktury formatu pliku GPX są oparte na [deklaracjach BinData Ruby Gem](https://github.com/dmendel/bindata/wiki), które umożliwiają odczytywanie i zapisywanie ustrukturyzowanych danych binarnych. Pozwala to programiście określić format danych binarnych, które są następnie odczytywane i zapisywane przez BinData.

### Wiadomości MGX

Komunikaty MGX opierają się na dwóch typach komunikatów.

* GAMESTART - określa komendy startowe gry i nie jest jeszcze zatwierdzony
* CZAT - opisuje komunikaty czatu w grze. Zarówno gracze, jak i sama gra (Gaia) mogą emitować komunikaty w grze.

### AKCJE ROZGRYWKI

Istnieje kilka [działań GAMEPLAY](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions), które zostały pobrane i których szczegóły są dostępne.

## Bibliografia

* [Age of Empires 2: The Conquerors — Specyfikacja formatu pliku zapisu stanu gry](https://github.com/stefan-kolb/aoc-mgx-format)

