{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Plik ZST — standardowy format pliku skompresowanego ZST",
  "description":"Dowiedz się o formacie pliku ZST i interfejsach API, które umożliwiają tworzenie i otwieranie plików ZST.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-pl",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Czym jest plik ZST?

Plik ZST to skompresowany plik generowany przy użyciu algorytmu kompresji Zstandard (zstd). Jest to skompresowany plik tworzony przez algorytm przy użyciu bezstratnej kompresji. Plików ZST można używać do kompresji różnych typów plików, takich jak bazy danych, systemy plików, sieci i gry. Standard Z podlega przepisowi [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878), który opisuje ogólny mechanizm kompresji, typ multimediów i kodowanie treści.

## Format pliku ZST

Pliki ZST są przechowywane w skompresowanym formacie pliku na dysku. Mechanizm kompresji jest zgodny z opisem w dokumencie RFC 8878, który jest przestarzałym dokumentem RFC 8478.

## Ramki ZST

Plik ZST składa się z jednej lub więcej klatek. Każda ramka może być ramką Zstandardową lub ramką możliwą do pominięcia. Ramka Zstandard zawiera skompresowane dane, natomiast ramka możliwa do pominięcia zawiera niestandardowe metadane użytkownika.

### Zstandardowa rama

Rama Zstandard ma następującą budowę.

|Pole|Rozmiar w bajtach|
---|---|
|Magiczny_Number |4 bajty|
|Nagłówek_ramki |2-14 bajtów|
|Blok_danych |n bajtów|
|[Więcej bloków danych] ||
|[Content_Checksum] |4 bajty|

### Klatka możliwa do pominięcia

Ramka możliwa do pominięcia umożliwia wstawianie metadanych zdefiniowanych przez użytkownika w strumieniu połączonych ramek. Struktura ramki możliwej do pominięcia jest następująca.

|Magiczny_Number |Rozmiar_ramki |Dane_użytkownika|
---|---|---|
|4 bajty |4 bajty |n bajtów|

## Bibliografia ##

* [Kompresja standardowa RFC 8878 Z] (https://www.rfc-editor.org/rfc/rfc8878)


