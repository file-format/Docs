{
  "date" : "2020-08-20",
  "keywords" :["plik ttf", "format pliku ttf", "co to jest plik ttf", "plik", "przykład ttf", "rozszerzenie pliku ttf", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - format pliku czcionek TrueType",
  "description":"Czcionki TrueType (TTF) są oparte na specyfikacjach technologii czcionek cyfrowych, pierwotnie zaprojektowanych przez Apple, Inc. Zarówno Apple, jak i Microsoft używały TTF w systemach operacyjnych Mac i Windows.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Czym jest plik TTF?

Plik z rozszerzeniem .ttf reprezentuje pliki czcionek oparte na technologii czcionek specyfikacji TrueType. Został pierwotnie zaprojektowany i uruchomiony przez firmę Apple Computer, Inc dla systemu Mac OS, a później został przyjęty przez firmę Microsoft dla systemu operacyjnego Windows. Czcionki TrueType zapewniają najwyższą jakość wyświetlania na ekranach komputerów i drukarek bez uzależnienia od rozdzielczości. Wszystkie nowoczesne aplikacje korzystające z czcionek mogą pracować z plikami TTF. Pliki czcionek TTF są swobodnie dostępne w Internecie i można je również konwertować na inne formaty plików czcionek, takie jak OTF i WOFF.

## Krótka historia

Zaprojektowany przez firmę Apply Computer, Inc. w latach 80. dla systemu MacOS, format czcionki TTF miał na celu rozwiązanie niektórych ograniczeń technicznych formatu Type 1 firmy Adobe. Firma Apple włączyła obsługę czcionek TrueType do komputerów Mac w 1991 roku. Celem projektowania czcionek TTF była wydajność przechowywania i przetwarzania oraz rozszerzalność. W oparciu o tę rozszerzalność istniejące czcionki można konwertować do formatu TrueType.

Firma Microsoft po raz pierwszy użyła czcionek TrueType w systemie Windows 3.1 w kwietniu 1992 r., po tym, jak firma Apple zgodziła się udzielić firmie Microsoft licencji TrueType. Poprawiło to mechanizm rasteryzacji oraz poprawiło jego wydajność i wydajność.

## Specyfikacje formatu plików True Type

Plik czcionek TrueType to plik binarny składający się z sekwencji połączonych tabel. Każda tabela jest sekwencją słów i ma nazwę znaną jako `Tag`. Każdy znacznik jest typu danych uint32 i składa się z czterech znaków. Pierwsza tabela w pliku to katalog czcionek, który daje dostęp do innych tabel w pliku czcionek. Dane dotyczące czcionek są zawarte w innych tabelach następujących po tabeli katalogu czcionek. Ponieważ każda tabela jest dostępna za pomocą jej znacznika, tabele mogą pojawiać się w pliku w dowolnej kolejności.

Wymagane tabele i ich nazwy znaczników przedstawiono w poniższej tabeli.

|**Tag**|**Tabela**|
---|---|
|'mapa'| mapowanie znaków na glify|
|'glif'| dane glifów|
|'głowa'| nagłówek czcionki|
|'hej'| nagłówek poziomy|
|'hmtx'| metryki poziome|
|'miejsce'| indeks do lokalizacji|
|'maks'| maksymalny profil|
|'imię'| nazewnictwo|
|'post'| PostScript|

### Typy danych
Czcionki TrueType używają standardowych liczb całkowitych i dodatkowych typów danych wymienionych w poniższej tabeli.

|**Typ danych** | **Opis** |
---|---|
|krótkiFrak| 16-bitowy ułamek ze znakiem|
|Naprawiono| 16,16-bitowa liczba stałoprzecinkowa ze znakiem|
|Słowo| 16-bitowa liczba całkowita ze znakiem, która opisuje wielkość w jednostkach F, najmniejszą mierzalną odległość w przestrzeni em.|
|uFWord| 16-bitowa liczba całkowita bez znaku, która opisuje wielkość w jednostkach FUNits, czyli najmniejszą mierzalną odległość w przestrzeni em.|
|F2Kropka14| 16-bitowa stała liczba ze znakiem, przy czym 14 niższych bitów reprezentuje ułamek.|
|długaDataCzas| Długi wewnętrzny format daty w sekundach od północy 12:00 1 stycznia 1904. Jest reprezentowany jako 64-bitowa liczba całkowita ze znakiem.|

### Katalog czcionek

Pierwsza tabela w czcionce TrueType to katalog czcionek, który zapewnia dostęp do informacji wymaganych do uzyskania dostępu do danych w innych tabelach. Ponadto składa się z:

* `Podtabela przesunięcia` - przechowuje zapis tabel w czcionce i dostarcza informacji o przesunięciu, aby uzyskać dostęp do każdej tabeli w katalogu
* `Table Directory` - Zawiera wpisy dla każdej tabeli w czcionce

#### Przesunięcie tabeli podrzędnej
Podtabela przesunięć jest pokazana poniżej.

|**Typ**|**Nazwa**|**Opis**|
---|---|---|
|uint32| typ skalera| Znacznik wskazujący skaler OFA, który ma być użyty do rasteryzacji tej czcionki; więcej informacji znajdziesz w uwagach na temat typu skalera.|
|uint16| liczbaTabele| liczba stołów|
|uint16| szukajZakres| (maksymalna potęga 2 <= numTabel)*16|
|uint16| Selektor wpisu| log2(maksymalna potęga 2 <= numTabel)|
|uint16| Przesunięcie zakresu| numTables*16-searchRange|

#### Katalog tabel
Katalog tabeli znajduje się zaraz po podtabeli przesunięcia. Jego struktura jest przedstawiona w poniższej tabeli.

|**Typ**|**Nazwa**|**Opis**|
---|---|---|
|uint32| tag| 4-bajtowy identyfikator|
|uint32| suma kontrolna| suma kontrolna dla tej tabeli|
|uint32| offset| przesunięcie od początku sfnt|
|uint32| długość| długość tej tablicy w bajtach (rzeczywista długość bez wypełnienia)|

Każda tabela w pliku czcionek musi mieć własny wpis w katalogu tabeli. Wpisy w tabeli muszą być posortowane rosnąco według tagów.


## Bibliografia
* [Instrukcja obsługi czcionek TrueType](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [Omówienie formatu TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

