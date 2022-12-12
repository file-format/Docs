{
  "date" : "2020-11-11",
  "keywords" :["NSF", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się o formacie plików NSF i interfejsach API, które mogą tworzyć i otwierać pliki NSF.",
  "title" :"Format pliku NSF — format bazy danych Lotus Notes",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Czym jest plik NFS?

Plik z rozszerzeniem .nsf (Notes Storage Facility) to format pliku bazy danych używany przez [oprogramowanie IBM Notes](https://en.wikipedia.org/wiki/HCL_Domino), który wcześniej był znany jako Lotus Notes. Definiuje schemat przechowywania różnego rodzaju obiektów, takich jak e-maile, spotkania, dokumenty, formularze i widoki. Wszystkie te informacje są zawarte w jednym pliku NSF do współpracy biznesowej, podobnym do pliku PST/OST. Niektóre aplikacje, które mogą otwierać pliki NSF, to IBM Lotus Notes i IBM Domino.

## Specyfikacje formatu plików NSF

Pliki NSF mają charakter binarny, a ich specyfikacje są dostępne u Joachima Metza na [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database% 20plik%20format.asciidoc). Zgodnie z tymi szczegółami plik NSF składa się z:

* Nagłówek pliku
* Nagłówek bazy danych

Ponadto składa się z:

* Superblok
* Blok deskryptora zasobnika
* Mapa bitowa
* Rekordowe wiadro wektora relokacji
* Podsumowanie wiadra
* Zasobniki niepodsumowujące


### Nagłówek pliku NSF

Nagłówek pliku NSF ma rozmiar 6 bajtów. Składa się ona z:

|Przesunięcie|Rozmiar|Wartość|Opis|
---|---|---|---|
0|2|0x1a 0x00|Podpis|
2|4| |Rozmiar nagłówka bazy danych|

### Nagłówek bazy danych

Nagłówek bazy danych NSD zawiera następujące potwierdzone wartości.

* Informacje o bazie danych
* Identyfikator bazy danych (DBID)
* Informacje o replikacji
* Flagi bufora informacyjnego bazy danych
* Tytuł
* Kategorie
* Klasa
* Klasa projektowa (nazwa szablonu)
* Specjalne identyfikatory nut
* Wyściółka
* Informacje z bazy danych 2
* Informacje z bazy danych 3
* Informacje z bazy danych 4
* Informacje z bazy danych 5
* Wyściółka
* Identyfikator instancji bazy danych (DBIID)
* Historia replikacji

## Bibliografia

* [Format NSF - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

