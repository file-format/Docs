{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Plik FMW — format pliku środowiska roboczego FME",
  "description":"Dowiedz się o formacie pliku FMW i interfejsach API, które umożliwiają tworzenie i otwieranie plików FMW.",
  "linktitle" : "FMW",
  "menu" : {
    "docs" : {
      "identifier":"gis-fmw-pl",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Czym jest plik FMW?

Plik FMW to plik projektu utworzony za pomocą oprogramowania FME Workbench (jest częścią pakietu FME Desktop), który służy do transformacji danych przestrzennych. Zawiera ustawienia zdefiniowane przez użytkownika używane do manipulacji danymi przestrzennymi, takie jak zbiory danych wejściowych, właściwości translacji, projekcje i ustawienia wyjściowe. Ustawienia manipulacji danymi przestrzennymi są przechowywane jako układ wizualny i można je łatwo edytować i ponownie zapisać.

Pliki FMW możesz otwierać za pomocą [Safe Software FME Desktop](https://www.safe.com/fme/fme-desktop/).

## Format pliku FMW — więcej informacji

Pliki FMW są zapisywane na dysku jako pliki binarne i można je odczytać wyłącznie za pomocą oprogramowania FME Desktop. Oprogramowanie może również odczytywać dane z wielu formatów relacyjnych baz danych, a także obsługuje szereg formatów danych.

### Szybkie fakty dotyczące FMW

|Fakt|Wartość|
---|---|
|Czytelnik/Pisarz|Czytelnik|
|Poziom licencji|Podstawowy|
|Zależności|Brak|
|Typ zbioru danych|Plik|
|Typ funkcji|Naprawiono|
|Typowe rozszerzenia plików|.fmw|
|Wsparcie tłumaczeń automatycznych|Tak|
|Atrybuty zdefiniowane przez użytkownika|Nie|
|Wsparcie układu współrzędnych|Nie|
|Ogólna obsługa kolorów|Nie|
|Indeks przestrzenny|Nie|
|Wymagany schemat|Nie|
|Wsparcie transakcji|Nie|
|Atrybut typu geometrii|Brak|
|Wsparcie kodowania|Nie|

### Obsługa geometrii FMW

|Geometria|Obsługiwane?|
---|---|
|łącznie|nie|
|kółka|nie|
|łuk kołowy|nie|
|wielokąt pączka|nie|
|łuk eliptyczny|nie|
|elipsy|nie|
|linia|nie|
|żaden|tak|
|punkt|nie|
|wielokąt|nie|
|raster|nie|
|solidnie|nie|
|powierzchnia|nie|
|tekst|nie|
|z wartości|nie|


## Bibliografia

* [Bezpieczne oprogramowanie FME Desktop](https://www.safe.com/fme/fme-desktop/)

* [FMW Quick Facts](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_ReadersWriters/fmw/quick_facts_fmw.htm)

