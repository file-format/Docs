{
  "date" : "2021-09-06",
  "keywords" :["btr", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Baza danych Btrieve" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku BTR i interfejsy API, które mogą tworzyć i otwierać pliki BTR.",
  "title" :"BTR - Plik Bazy Danych Btrieve",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Czym jest plik BTR?

Plik z rozszerzeniem .btr to plik bazy danych utworzony przez aplikację transakcyjnej bazy danych [Btrieve](https://www.actian.com/). W przeciwieństwie do systemów zarządzania relacyjnymi bazami danych (RBMS), Btrieve opiera się na Indexed Sequential Access Method (ISAM), która jest sposobem przechowywania danych w celu szybkiego wyszukiwania. Plik BTR przechowuje zbiór rekordów i służy do generowania raportów zgodnie z wymaganiami. Pliki BTR można otwierać za pomocą Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility i Legend Software BTRIEVE Viewer.

## Struktura pliku BTR — więcej informacji

Wewnętrzna struktura danych i wyrównanie każdego bajtu w strukturze pliku BTR nie jest publicznie dostępna. Jednak Btrieve
udostępnia [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm), którego można użyć do odczytania informacji z plików BTR. Jest kompatybilny z następującymi językami programowania i środowiskami programistycznymi.

* Embarcadero C/C++
* Embarcadero Delphi
* GNU C/C++
* Micro Focus COBOL
* Microsoft Visual Basic
* Microsoft VisualC++
* Watcom C/C++

Pobieranie danych z pliku BTR zależy od powiązanego z nim pliku DDF. Bez DDF odzyskanie informacji z takiego pliku nie będzie łatwe.

## Bibliografia

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Wprowadzenie do interfejsów API Btreive](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

