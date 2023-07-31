{
  "date" : "2020-08-20",
  "keywords" :["plik cff2", "format pliku cff2", "co to jest plik cff2", "plik", "przykład cff2", "rozszerzenie pliku cff2", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Compact Font File Format wersja 2",
  "description":"Dowiedz się o formacie plików CFF2 i interfejsach API do tworzenia i otwierania plików CFF2.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Czym jest plik CFF2?

Format pliku CFF2 to wersja 2.0 formatu pliku CFF i umożliwia wydajne przechowywanie konturów glifów i metadanych podobnych do formatu pliku CFF. CFF2 różni się od CFF tym, że ma być używany w kontekście czcionki OpenType jako tabela „sfnt” ze znacznikiem CFF2. Nie może być używany jako samodzielny program i jest zależny od danych w innych tabelach OpenType.

## Format pliku CFF2

[Specyfikacja formatu pliku CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) zawiera szczegółowe informacje na temat wewnętrznego układu danych, typów danych, tabel i innych wewnętrznych informacji o formacie pliku. Można go skierować w celach informacyjnych dla programistów. Niektóre szczegóły na ich temat są następujące.

### Układ danych

Dane binarne w formacie pliku CFF2 są logicznie zorganizowane jako kilka oddzielnych struktur danych. Układ w danych binarnych jest pokazany w poniższej tabeli.

|Wpis |Komentarze|
---|---|
|Nagłówek |Stała lokalizacja|
|Górny DICT| Stała lokalizacja|
|Globalny indeks Subr| Stała lokalizacja|
|Odmiana |Przechowuj|
|FDSelect |Wyświetlaj tylko wtedy, gdy w INDEXIE DICT czcionek jest więcej niż jeden DICT.|
|Czcionka DICT INDEX ||
|Tablica czcionek DICT| Zawarte w czcionce DICT INDEX.|
|Prywatny DICT| Jeden na czcionkę DICT.|

Tylko pierwsze trzy struktury są oparte na stałych lokalizacjach. Pozostałe są osiągane przez przesunięcia, a ich kolejność można zmienić.

### Typy danych

Format pliku CFF2 wykorzystuje następujące typy danych.

|Nazwa |Zakres |Opis|
---|---|---|
|uint8 |0 do 255 |8-bitowa liczba bez znaku|
|uint16 |0 do 65535| 16-bitowa liczba bez znaku|
|uint32 |0 do 4294967295| 32-bitowa liczba bez znaku|
|Przesunięcie |różne| Przesunięcie o 1, 2, 3 lub 4 bajty (określone przez pole OffSize w tabeli indeksu)|
|Poza rozmiarem |1 do 4| 1-bajtowa liczba bez znaku określa rozmiar pola lub pól przesunięcia|

Przechowuje wszystkie wielobajtowe dane liczbowe i pola przesunięcia w kolejności bajtów big-endian. Format CFF2 jest wolny od bajtów dopełniających, ponieważ nie uwzględnia żadnych ograniczeń wyrównania.

### Dane DICT

Pliki CFF2 zawierają dane słownika czcionek jako pary klucz-wartość w kompaktowym formacie tokenizowanym. Klucze słownika są kodowane jako operatory 1- lub 2-bajtowe, a wartości słownikowe są kodowane jako operandy numeryczne o zmiennej wielkości. Istnieją trzy struktury korzystające z formatu danych DICT: `Top DICT`, `Font DICT` i `Private DICT`. Szereg typów operandów całkowitych o różnych rozmiarach jest zdefiniowanych i zakodowanych, jak pokazano w poniższej tabeli (pierwszy bajt operandu to b0, drugi to b1 itd.).

|Rozmiar |zakres b0 |Zakres wartości |Obliczanie wartości|
---|---|---|---|
|1 |32 do 246| -107 do +107 |b0 - 139|
|2 |247 do 250| +108 do +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251 do 254| -1131 do -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 do +32767| b1 << 8 | b2|
|5 |29| -(2^31) do +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Nagłówek

Dane binarne rozpoczynają się nagłówkiem o formacie pokazanym w poniższej tabeli.

|Typ |Nazwa |Opis|
---|---|---|
|uint8| wersja główna| Sformatuj wersję główną. Ustaw na 2.|
|uint8| wersja drugorzędna| Sformatuj wersję pomocniczą. Ustaw na zero.|
|uint8| rozmiar nagłówka| Rozmiar nagłówka (bajty).|
|uint16| górnaDługośćDict| Długość struktury Top DICT w bajtach.|

## Bibliografia

* [Format pliku CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

