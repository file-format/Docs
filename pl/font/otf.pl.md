{
  "date" : "2020-08-20",
  "keywords" :[ "plik otf", "format pliku otf", "co to jest plik otf", "plik", "przykład otf", "rozszerzenie pliku otf", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - format pliku czcionek TrueType",
  "description":"Poznaj format plików OTF i interfejsy API, które mogą tworzyć i otwierać pliki OTF.",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Czym jest plik OTF?

Plik z rozszerzeniem .otf odnosi się do formatu czcionki OpenType. Format czcionki OTF jest bardziej skalowalny i rozszerza istniejące funkcje formatów [TTF](/pl/font/ttf/) dla typografii cyfrowej. Opracowany przez Microsoft i Adobe, OTF łączy cechy formatów czcionek PostScript i TrueType. To sprawia, że format OTF jest dostosowany do większości systemów zapisu i dlatego jest jednolicie używany na głównych platformach komputerowych. Format czcionki OpenType jest obsługiwany przez systemy Mac OS X i Windows 2000 oraz nowsze.

## Krótka historia

Wymóg czcionek OpenType powstał jako wymóg bardziej wyrazistego formatu czcionki, który poradziłby sobie z precyzyjną typografią. Ponadto miał spełniać wymagania złożonego zachowania wielu światowych systemów pisma. Microsoft próbował licencjonować zaawansowaną technologię typograficzną Apple, znaną jako GX Typography, na początku lat 90-tych. Nie poszło to dobrze iw rezultacie Microsoft zaczął ulepszać swoją własną technologię czcionek TrueType w 1994 roku. Modyfikacje obejmowały również wprowadzenie bardziej odpowiedniego formatu czcionki, który również spełnia funkcje formatów czcionek Type 1 (PostScript) firmy Adobe.

Firma Adobe w 1996 roku dołączyła do firmy Microsoft w jej wysiłkach zmierzających do zastąpienia zarówno TrueType firmy Apple, jak i własnych formatów czcionek Type 1. Doprowadziło to do połączenia obu podstawowych formatów czcionek w celu przezwyciężenia ograniczeń i dodania nowych rozszerzeń. Ta nowa technologia została wprowadzona w tym samym roku pod nazwą **OpenType**.

## Specyfikacje formatu plików OTF

Specyfikacje OTF są publicznie dostępne przez firmę Microsoft i można się do nich odwoływać z perspektywy programisty. Podobnie jak TTF, używa tej samej struktury kontenera „sfnt” i jest zgodny ze specyfikacjami TrueType. Dane w pliku czcionek OpenType są wykorzystywane do różnych celów, takich jak obliczanie układu tekstu, definiowanie glifów jako konturów TrueType lub Compact Font Format (CFF), dostarczanie monochromatycznych lub kolorowych map bitowych lub dokumentów SVG jako alternatywnych opisów glifów oraz informacji o metadanych.

### Typy danych OTF
Pliki OTF używają następujących typów danych, które są w Big Endian.

|Typ danych| Opis|
---|---|
|uint8| 8-bitowa liczba całkowita bez znaku.|
|int8| 8-bitowa liczba całkowita ze znakiem.|
|uint16| 16-bitowa liczba całkowita bez znaku.|
|int16| 16-bitowa liczba całkowita ze znakiem.|
|uint24| 24-bitowa liczba całkowita bez znaku.|
|uint32| 32-bitowa liczba całkowita bez znaku.|
|int32| 32-bitowa liczba całkowita ze znakiem.|
|Naprawiono| 32-bitowa liczba stałoprzecinkowa ze znakiem (16,16)|
|SŁOWO| int16, który opisuje ilość w jednostkach projektu czcionki.|
|UFWORD| uint16, który opisuje ilość w jednostkach projektu czcionki.|
|F2DOT14| 16-bitowa stała liczba ze znakiem z niskimi 14 bitami ułamka (2,14).|
|LONGDATETIME| Data i czas wyrażone w sekundach od północy 12:00, 1 stycznia 1904, UTC. Wartość jest reprezentowana jako 64-bitowa liczba całkowita ze znakiem.|
|Oznaczenie| Tablica czterech jednostek uint8 (długość = 32 bity) używana do identyfikacji tabeli, osi zmienności projektu, skryptu, systemu językowego, funkcji lub linii bazowej|
|Odsunięcie16| Krótkie przesunięcie do tabeli, takie samo jak uint16, przesunięcie NULL = 0x0000|
|Odsunięcie32| Długie przesunięcie do tabeli, takie samo jak uint32, przesunięcie NULL = 0x00000000|
|Wersja16Kropka16| Spakowana wartość 32-bitowa z głównymi i pomocniczymi numerami wersji. (Patrz numery wersji tabeli.)|

### Katalog tabel OTF

Plik OTF zaczyna się od katalogu tabeli. Ten katalog jest zbiorem tabel najwyższego poziomu w pliku czcionek. W zależności od liczby czcionek w pliku katalog tabeli może znajdować się w innym miejscu w pliku. Na przykład, jeśli plik czcionek zawiera tylko jedną czcionkę, katalog tabeli zaczyna się od bajtu 0 pliku. W przypadku wielu kolekcji czcionek OpenType,
początek katalogu tabeli jest wskazany w nagłówku TTCHeader.

|Typ |Nazwa |Opis|
---|---|---|
|uint32 |sfntWersja| 0x00010000 lub 0x4F54544F („OTTO”)|
|uint16| numTables |Liczba tabel.|
|uint16| searchRange |Maksymalna potęga 2 mniejsza lub równa numTables, razy 16 ((2\**floor(log2(numTables))) * 16, gdzie „**” jest operatorem potęgującym).|
|uint16 |entrySelector Log2 o maksymalnej potędze 2 mniejszej lub równej numTables (log2(searchRange/16), co jest równe floor(log2(numTables))).|
|uint16 |rangeShift |numTables razy 16, minus searchRange ((numTables * 16) - searchRange).|
|tabelaRekord| tableRecords[numTables] |Tablica rekordów tabeli — po jednej dla każdej tabeli najwyższego poziomu w czcionce|


### Rekord tabeli

Dla każdej tabeli najwyższego poziomu w czcionce istnieje Rekord tabeli, który składa się z następujących pól.

|Wpisz| Imię| Opis|
---|---|---|
|Oznaczenie| TabelaTag| Identyfikator tabeli.|
|uint32| suma kontrolna| Suma kontrolna dla tej tabeli.|
|Odsunięcie32| offset| Przesunięcie od początku pliku czcionki.|
|uint32| długość Długość tej tabeli.|

Każda tabela w pliku czcionek OpenType jest reprezentowana przez nazwy znane jako znaczniki tabeli. Konieczne jest, aby wszystkie rekordy w tablicy były posortowane rosnąco według tagów.

## Bibliografia
* [Specyfikacje czcionek OpenType firmy Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [Omówienie formatu TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

