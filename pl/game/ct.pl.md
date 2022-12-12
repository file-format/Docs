{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku CT i interfejsy API, które mogą tworzyć i otwierać pliki CT.",
  "title" :"CT - Plik tabeli kodów Cheat Engine",
  "linktitle" : "CT",
  "menu" : {
    "docs" : {
      "identifier": "game-ct",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Czym jest plik CT?

Plik CT to plik tabeli kodów utworzony za pomocą oprogramowania [Cheat Engine] (https://www.cheatengine.org/), który służy do tworzenia modyfikacji gier opartych na systemie Windows w celu oszukiwania. Cheat Engine, silnik do oszukiwania o otwartym kodzie źródłowym, bada uruchamiające się gry i rejestruje ich lokalizacje adresowe. Te informacje i ich nadpisania są zapisywane w pliku CT, który jest następnie ładowany przez graczy w celu zmiany właściwości gry, takich jak stan zdrowia, najwyższy wynik i pozostałe życia.

## Format pliku Cheat Engine CT

Pliki CT są zapisywane z lokalizacjami adresowymi i innymi powiązanymi informacjami, które można zhakować w grze. W większości przypadków pliki są zapisywane jako skompresowane archiwa [ZIP](/pl/compression/zip/), które można łatwo rozpakować za pomocą dowolnego standardowego narzędzia do dekompresji, takiego jak WinZIP lub 7-Zip.

## Jak korzystać z tabel kodów

1. Pobierz tabelę i skopiuj ją do folderu Cheat Engine
1. Uruchom Cheat Engine
1. Uruchom grę;
1. Użyj kombinacji ALT+TAB i wybierz grę z listy procesów za pomocą Cheat Engine
1. Jeśli tabela znajduje się w innym folderze, po prostu naciśnij Control + O i poprowadź Cheat Engine do tego folderu. Następnie wybierz tabelę (zwykle nazwa_procesu.ct);
1. Po załadowaniu tabeli, jeśli jest tam skrypt, po prostu go sprawdź.
1. ALT+TAB wróć do gry i baw się dobrze.

## Bibliografia

* [Cheat Engine](https://www.cheatengine.org/)

