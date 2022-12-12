{
  "date" : "2021-06-14",
  "keywords" :["SAV", "rozszerzenie", "plik sav", "format pliku sav", "Typ pliku bazy danych", "Format pliku bazy danych", "co to jest plik sav" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku SAV i interfejsy API, które mogą tworzyć i otwierać pliki SAV.",
  "title" :"SAV - plik danych SPSS",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Czym jest plik SAV?
Plik SAV to plik danych stworzony przez Pakiet Statystyczny dla Nauk Społecznych (SPSS), który jest aplikacją szeroko stosowaną przez badaczy rynku, badaczy zdrowia, firmy badawcze, rząd, badaczy edukacji, organizacje marketingowe, eksploratorów danych do analizy statystycznej. SAV zapisany w zastrzeżonym formacie binarnym i składa się ze zbioru danych oraz słownika reprezentującego zbiór danych, zapisuje dane w wierszach i kolumnach.

## Format pliku SAV
Format pliku SAV stał się stosunkowo stabilny, ale nie możemy powiedzieć, że jest statyczny. W razie potrzeby dostępna jest kompatybilność wsteczna i do przodu, ale nie jest ona odpowiednio utrzymywana. Dane w pliku SAV są podzielone na następujące sekcje:

### Nagłówek pliku
Składa się ze 176 bajtów. Pierwsze 4 bajty wskazują ciąg **$FL2** lub **$FL3** w kodowaniu znaków używanym w pliku. Ostatnie trzy bajty oznaczają, że dane w pliku są skompresowane przy użyciu **ZLIB**. Następny 60-bajtowy ciąg zaczyna się od **@(#) SPSS DATA FILE** i określa również system operacyjny oraz wersję SPSS, która utworzyła plik. Następnie nagłówek zawiera sześciocyfrowe pola, zawierające liczbę zmiennych na obserwację i kod cyfrowy do kompresji, a kończy się danymi znakowymi wskazującymi datę i godzinę utworzenia oraz etykietą pliku.
### Rekordy deskryptorów zmiennych
Rekord zawiera ustaloną sekwencję pól, klasyfikującą typ i nazwę zmiennej wraz z informacjami o formatowaniu używanymi przez SPSS. Każdy rekord zmiennej może opcjonalnie zawierać etykietę zmiennej o długości do 120 znaków i maksymalnie trzy specyfikacje brakujących wartości.
### Etykiety wartości
Etykiety wartości są opcjonalne i przechowywane w parach rekordów ze znacznikami całkowitymi 3 i 4. Pierwszy rekord, który jest znacznikiem 3, zawiera sekwencję par pól, z których każda zawiera wartość i powiązaną etykietę wartości. Drugi rekord, czyli znacznik 4, reprezentuje zmienne, do których odnosi się zestaw wartości/etykiet.
### Dokumenty
Pojedynczy lub wiele rekordów ze znacznikiem całkowitym 6. Dokumentacja opcjonalna. zawiera 80-znakowych wierszy.
### Rekordy rozszerzeń
Pojedynczy lub wiele rekordów ze znacznikiem całkowitym 7. Rekordy rozszerzeń dostarczają informacji, które można bezpiecznie zignorować, ale ich zachowanie w wielu sytuacjach umożliwia plikom zapisanym przez nowsze oprogramowanie zachowanie kompatybilności wstecznej. Rekordy rozszerzeń mają znaczniki podtypu liczb całkowitych.
### Terminator słownika
Tylko rekord ze znacznikiem całkowitym 999. Oddziela słownik od obserwacji danych.
### Obserwacje danych
Uważa się, że dane są uporządkowane w kolejności obserwacji, np. wszystkie wartości zmiennych dla pierwszej obserwacji, następnie wszystkie wartości dla drugiej obserwacji itd. Format rekordu danych różni się w zależności od kodu kompresji w rekordzie nagłówka pliku. Część danych pliku .sav można zdekompresować:
- **kod 0**: skompresowany kodem bajtowym
- **kod 1**: skompresowane przy użyciu kompresji ZLIB
 







## Bibliografia ##

* [Rodzina formatów plików danych systemu SPSS (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

