{
  "date" : "2021-09-08",
  "keywords" :[ "plik gam", "format pliku gam", "co to jest plik gam", "plik", "przykład gry", "rozszerzenie pliku gry", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku GAM i interfejsy API, które mogą tworzyć i otwierać pliki GAM.",
  "title" :"GAM - Zapisany plik gry",
  "linktitle" : "GAM",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Czym jest plik GAM?
Plik z rozszerzeniem .gam jest używany przez różne gry wideo, aby zachęcić graczy do kontynuowania od miejsca, w którym przerwali, przy następnym uruchomieniu programu. Oznacza to zatem, że plik GAM zapisuje informacje o tym, co użytkownik zrobił w jakim czasie. Pliki te mogą być zapisywane automatycznie przez oprogramowanie do gier lub gracze mogą zostać poproszeni o zapisanie, jeśli chcą kontynuować stan gry, z którego opuszczają.
## Format pliku GAM
Format pliku GAM jest zasadniczo używany do przechowywania danych gry w zapisywanych grach. Plik GAM nie przechowuje informacji o stworzeniach, przedmiotach ani obszarze, zamiast tego zapisuje dane dotyczące członków drużyny oraz ogólne lub globalne zmienne, które mają wpływ na członków drużyny.
### Struktura pliku GAM
Plik GAM ma następującą strukturę:
- Nagłówek
- Członkowie partii
- Dane pliku CRE członka partii
- NPC (którzy nie są w drużynie)
- Statystyki zabójstw NPC (osadzone w strukturze NPC)
- Dane pliku NPC CRE
- Zmienne (w przestrzeni nazw GLOBAL)
- Wpisy do dziennika
- Znane informacje
- Przechowywane lokalizacje
- Lokalizacje samolotów kieszonkowych
- Znajomy dodatek


 




## Bibliografia


* [Format pliku GAM](https://gibberlings3.github.io/iesdp/file_formats/ie_formats/gam_v2.0.htm#GAMEV2_0_Stored)


