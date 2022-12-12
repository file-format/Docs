{
  "date" : "2019-12-10",
  "keywords" :["DIF", "plik", "rozszerzenie", "format pliku", "Plik wymiany danych", "Arkusz kalkulacyjny"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Twój przewodnik po formatach plików, aby wiedzieć, co to jest rozszerzenie pliku DIF i interfejsy API, które mogą tworzyć i otwierać pliki DIF.",
  "title" :"DIF – format pliku wymiany danych",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Czym jest plik DIF?

DIF to skrót od Data Interchange Format, który służy do importowania/eksportowania danych z arkuszy kalkulacyjnych między różnymi aplikacjami. Należą do nich Microsoft Excel, OpenOffice Calc, StarCalc i wiele innych. Przechowuje dane zawarte w jednym arkuszu kalkulacyjnym, co jest jedynym ograniczeniem tego formatu pliku.

## Krótka historia formatu plików DIF ##

Format pliku DIF został opracowany przez firmę Software Arts, Inc. na początku lat 80. Specyfikacje formatu plików dla DIF zostały zawarte w VisiCalc, który był pierwszym arkuszem kalkulacyjnym dla komputerów osobistych. Te specyfikacje były chronione prawami autorskimi w 1981 roku i były zastrzeżonym znakiem towarowym firmy Software Arts Products Corp.

## Format pliku DIF ##

DIF przechowuje zawartość arkusza kalkulacyjnego w pliku tekstowym ASCII, który umożliwia przeglądanie i edycję za pomocą edytora tekstu. Format ma swoje miejsce na liście formatów serializacji danych ze względu na charakterystykę wymiany danych. Plik DIF składa się z 2 sekcji; nagłówek i dane.

Wszystko w DIF jest reprezentowane przez 2- lub 3-liniowy fragment. Nagłówki otrzymują 3-liniowy fragment; dane, 2.

* Fragmenty nagłówka zaczynają się od identyfikatora tekstowego, który składa się wyłącznie z wielkich liter, tylko znaków alfabetu i ma mniej niż 32 litery. Następny wiersz musi być parą liczb, a trzeci wiersz musi być ciągiem znaków ujętym w cudzysłowy.
* Fragmenty danych zaczynają się od pary liczb, a następny wiersz to ciąg znaków w cudzysłowie lub słowo kluczowe.

### Wartości ###

Wartość zajmuje dwa wiersze, pierwszy to para liczb, a drugi to ciąg znaków lub słowo kluczowe. Pierwsza liczba pary oznacza typ:

* −1 – typ dyrektywy, druga liczba jest ignorowana, następna linia to jedno z tych słów kluczowych:
** BOT – początek krotki (początek wiersza)
** EOD – koniec danych
* 0 – typ liczbowy, wartość to druga liczba, poniższy wiersz to jedno z tych słów kluczowych:
** V – obowiązuje
** ND – niedostępne
** BŁĄD – błąd
** TRUE – prawdziwa wartość logiczna
** FAŁSZ – fałszywa wartość logiczna
* 1 – typ string, druga liczba jest ignorowana, następna linia to string w cudzysłowach

### Fragment nagłówka DIF ###

Fragment nagłówka pliku DIF składa się z linii identyfikatora, po której następują dwie linie wartości. Wartości liczbowe w porcjach nagłówka używają tylko pustego ciągu zamiast słów kluczowych ważności. Szczegóły tych fragmentów nagłówka są następujące.

* TABELA - po wersji następuje wartość liczbowa, niewykorzystany drugi wiersz wartości zawiera komentarz generatora
* WEKTORY - liczba kolumn następuje jako wartość liczbowa
* KRÓTKI - liczba wierszy następuje jako wartość liczbowa
* DANE - po fikcyjnej wartości liczbowej 0 następują dane do tabeli, każdy wiersz poprzedzony wartością BOT, cała tabela zakończona wartością EOD

### DIF Przykład ###

Poniższy przykład pokazuje zawartość prostego arkusza i jego równoważną reprezentację DIF.


|Imię|Wiek
---|---|
|Bob|34
|Arkusz|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Bibliografia ##

* [ DIF – Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)

