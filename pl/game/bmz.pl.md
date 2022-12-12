{
  "date" : "2021-10-20",
  "keywords" :["plik bmz", "format pliku bmz", "co to jest plik bmz", "plik", "przykład bmz", "Plik Zip mapy bonusowej portalu", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku Portal Bonus Map ZIP BMZ i interfejsy API, które mogą tworzyć i otwierać pliki BMZ.",
  "title" :"BMZ - Plik ZIP mapy bonusowej portalu",
  "linktitle" : "BMZ",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Czym jest plik BZZ?

Plik BMZ to dodatkowy plik mapy używany przez grę 3D polegającą na rozwiązywaniu zagadek `Portal` opracowaną przez firmę Valve. Zawiera dodatkową mapę, którą mogą tworzyć również zewnętrzni twórcy społeczności i importować ją do gry za pomocą wbudowanego interfejsu użytkownika. BMZ jest dostarczany jako plik archiwum [ZIP](/pl/compression/zip/), zawierający pliki BSP, TGA i [BNS](/pl/game/bns/). Pliki BMZ można otwierać za pomocą Valve Portal i Valve Portal 2.

## Format pliku BMZ

BMZ są zapisywane jako pliki ZIP i można je wyodrębnić za pomocą standardowych narzędzi do wyodrębniania ZIP, takich jak WinZIP lub WinRAR. Po rozpakowaniu pliku BMZ można znaleźć następujące pliki:

* BSP — Plik mapy
* TGA — plik z logo
* BNS — plik skryptu mapy bonusowej portalu

## Jak tworzyć i instalować dodatkowe pliki map

Społeczność programistów w Valve Software opracowała wytyczne dla osób, które chcą [tworzyć i instalować mapy bonusowe](https://developer.valvesoftware.com/wiki/Bonus_Maps). Obejmuje następujące kroki:

1. Dodanie map bonusowych BSP do moda
1. Dodanie obrazu miniatury
1. Tworzenie plików z opisem bonusów (.BNS)

## Bibliografia

* [Utwórz i zainstaluj dodatkowe pliki map — za pomocą oprogramowania Valve](https://developer.valvesoftware.com/wiki/Bonus_Maps)
* [Skrypt wyzwania portalu](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

