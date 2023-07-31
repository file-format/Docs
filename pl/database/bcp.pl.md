{
  "date" : "2020-11-11",
  "keywords" :["BCP", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Pliki bazy danych"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku BCP i interfejsy API, które mogą tworzyć i otwierać pliki BCP.",
  "title" :"BCP — format pliku masowego kopiowania programu SQL Server",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Czym jest plik BCP?

BCP (Bulk Copy Format) to techniczny format danych Microsoft SQL Server, który definiuje struktury danych do przechowywania wartości różnych typów danych bazy danych na potrzeby importu/eksportu. Format w pełni definiuje interpretację każdej kolumny danych, tak aby można było odczytać zestaw wartości określonych w pliku danych. Narzędzie [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) używa formatu pliku BCP do odczytu dane z takiego pliku i zidentyfikować go.


## Format pliku BCP

Plik formatu BCP jest dokumentem XML, który określa kolejność kolumn, nazwę i typ danych. Pozwala użytkownikom importować/eksportować duże ilości danych z pliku danych, określając te pola. Jest to pomocne przy masowym imporcie wartości danych z plików danych. Liczba i kolejność pól danych w pliku danych może być inna niż w kolumnach tabeli docelowej. W tym momencie przychodzi z pomocą plik formatu danych BCP, określając kolejność i typ kolumn do importowania danych.

Struktura pliku formatu jest przedstawiona w następującym formacie.

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### Typy danych BCP

|Typ danych|Zakres|Reprezentacja|
---|---|---|
|BigInt|-263 (-9 223 372 036 854 775 808) do 263-1 (9 223 372 036 854 775 807)|`BigInt = ["-"]1*19CYFR`|
|Dwójkowy|od 1 do 8000 bajtów|kodowany szesnastkowo w formacie Unicode `Binary = 32000OCTET`|
|Bit|0 lub 1|prosty ciąg Unicode Bit = "0" / "1"|
|Znaki|od 1 do 8000|Format ciągu Unicode, znak = 16000OKTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET z n = 4 x (2 147 483 647)|
|Data|0001-01-01 do 9999-12-31|Format ciągu RRRR-MM-DD|
|DataCzas|1753-01-01 00:00:00.000 do 9999-12-31 23:59:59.997| Format ciągu Unicode RRRR-MM-DD hh:mm:ss[.nnn]|
|DataCzas2|0001-01-01 00:00:00.0000000 do 9999-12-31 23:59:59.9999999.| Format ciągu Unicode RRRR-MM-DD gg:mm:ss[.nnnnnnn]|
|Przesunięcie daty i godziny|0001-01-01 od 00:00:00.0000000 do 9999-12-31 23:59:59,9999999 w strefie czasowej uniwersalnego czasu koordynowanego (UTC)| Unicode RRRR-MM-DD gg:mm:ss[.nnnnnnn] [{+|-}gg:mm] format ciągu|
|Dziesiętne|-1038 + 1 do 1038 – 1|Format ciągu znaków Unicode `Dziesiętne = ["-"] 0*38CYFRY ["."0*38CYFRY]`|
|Float|-1,79E+308 do -2,23E-308; 0; od 2.23E-308 do 1.79E+308|Format znaków Unicode|
|Obraz|sekwencja bajtów z zakresu od 0 do 231 – 1 (2 147 483 647)|format znaków Unicode zakodowany szesnastkowo|
|Int|-231 (-2 147 483 648) do 231 – 1 (2 147 483 647)|Format ciągu Unicode|

## Bibliografia

* [Format BCP — Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

