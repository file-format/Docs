{
  "date" : "2021-10-20",
  "keywords" :["plik sfar", "format pliku sfar", "co to jest plik sfar", "plik", "przykład sfar", "rozszerzenie pliku Mass Effect 3 DLC", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się o formacie plików SFAR Mass Effect 3 i interfejsach API, które mogą tworzyć i otwierać pliki SFAR.",
  "title" :"SFAR - Plik DLC Mass Effect 3",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Czym jest plik SFAR?

Plik z rozszerzeniem .sfar to plik danych gry używany przez Mass Effect 3 do przechowywania DLC (zawartość do pobrania) w skompresowanym, zastrzeżonym archiwum. Mass Effect 3 to gra stworzona przez Electronic Arts, wiodącą firmę zajmującą się tworzeniem gier. Zawartość DLC przechowywana w pliku SFAR służy do rozszerzenia gry o dodatkową zawartość i funkcje.

## Format pliku SFAR — więcej informacji

Pliki SFAR są przechowywane / zapisywane jako skompresowane pliki archiwalne w formacie pliku binarnego. Wykorzystują one zarówno algorytmy kompresji LZX, jak i LZMA do kompresji zawartości. Pliki SFAR można otwierać za pomocą edytora DLC, który jest dostarczany z ME3 Explorer. Oprócz SFAR edytor DLC może wyodrębniać inne pliki gier, takie jak [PCC](/pl/game/pcc/).

## Specyfikacje formatu plików SFAR

Plik SFAR jest podzielony na następujące cztery główne części.

### Nagłówek SFAR

Nagłówek SFF zawiera informacje o różnych fragmentach składających się na plik.

### Tabela plików SFAR

Tabela plików SFAR zawiera listę wpisów plików, z których każdy ma długość 30 bajtów.

### Tabela rozmiarów bloków

Block-Size zawiera wiele wpisów, z których każdy ma długość 2 bajtów. Ta wartość określa rozmiar bloku odpowiadający wpisowi w tabeli plików.

### Bloki

Fragmenty bloków w pliku SFAR zawierają dane zawarte w pliku SFAR.

## Bibliografia

* [Format pliku DLC SFAR – Badania](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

