{
  "date" : "2019-10-11",
  "keywords" :[ "plik shp", "format pliku shp", "co to jest plik shp", "plik", "przykład shp", "rozszerzenie pliku shp", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - plik kształtów ESRI",
  "description":"Poznaj format pliku SHP i interfejsy API, które mogą tworzyć i otwierać pliki SHP.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik SHP?

SHP to rozszerzenie pliku dla jednego z podstawowych typów plików używanych do reprezentacji ESRI Shapefile. Reprezentuje informacje geoprzestrzenne w postaci danych wektorowych, które mają być używane przez aplikacje systemów informacji geograficznej (GIS). Format został opracowany jako otwarte specyfikacje w celu ułatwienia współdziałania między ESRI a innymi produktami oprogramowania.

## Reprezentacja danych

Jak wspomniano, format pliku kształtu opisuje informacje geoprzestrzenne zbioru danych jako cechy wektorowe. Te cechy wektorowe obejmują:

* punkty
* linie
* wielokąty

Te cechy w połączeniu mogą reprezentować prawie każdy rodzaj kształtów, takich jak studnie wodne, granice państw, punkty przestrzenne, przepływ rzek, jeziora itp. Każdy element wektorowy może mieć atrybuty, które faktycznie definiują przeznaczenie tego elementu. Na przykład plik kształtu zawierający miasta Los Angeles może mieć nazwę miasta i temperaturę jako atrybuty, które zapewniają sensowną reprezentację danych przestrzennych.

## Powiązane pliki

Samodzielny plik shp nie może być używany przez aplikacje do zrozumienia zawartych w nim danych. Aby nadać sens informacjom zawartym w takim pliku, plik kształtu wykorzystuje następujące dodatkowe pliki obowiązkowe.

* plik shx - plik indeksu
* plik dbf - plik dBASE, który przechowuje wszystkie atrybuty kształtów w głównym pliku
* plik prj - przechowuje informacje o projekcie pliku

Mogą istnieć również inne opcjonalne pliki, które mają taką samą nazwę jak plik główny.

## Specyfikacje formatu plików SHP

Otwarte specyfikacje pliku shapefile są dostępne online w ESRI w formie [Opisu technicznego](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) i szczegółowo opisują ogólną strukturę pliku. Informacje w głównym pliku .shp składają się z nagłówków i rekordów. Po nagłówku pliku o stałej długości następują rekordy o zmiennej długości, gdzie każdy rekord składa się z nagłówka rekordu o stałej długości, po którym następuje zawartość rekordu o zmiennej długości.

### Główny nagłówek pliku SHP

Główny nagłówek pliku zaczyna się od początku pliku i ma długość 100 bajtów. Organizacja tego głównego nagłówka pliku wraz z pozycją bajtów, wartością, typem i kolejnością bajtów jest przedstawiona w poniższej tabeli.


|Bajty|Pole|Wartość|Typ|Kolejność bajtów
---|---|---|---|---|
|0-3|Kod pliku|9994|Liczba całkowita|Big Endian
|4-23|Nieużywane|0|Liczba całkowita|Big Endian
|24-27|Długość pliku|Długość pliku|Całkowita|Big Endian
|28-31|Wersja|1000|Liczba całkowita|Little Endian
|32-35|Typ kształtu|Typ kształtu|Liczba całkowita|Little Endian
|36-67|Minimalny prostokąt ograniczający|Xmin, Ymin, Xmax i Ymax|double|Little Endian
|68-83|Obwiednia|Zmin, Zmax|podwójne|Little Endian
|84-99|Obwiednia|Mmin, Mmax|podwójne|

Należy zauważyć, że wartość długości pliku jest całkowitą długością pliku wyrażoną w słowach 16-bitowych, która obejmuje również pięćdziesiąt słów 16-bitowych składających się na nagłówek.

#### Typy kształtów

Wartości pól typów kształtów w powyższej tabeli są następujące:


|Wartość|Typ kształtu
---|---|
|0|Nowy kształt
|1|Punkt
|3|Polilinia
|5|Wielokąt
|8|Wielokrotność
|11|PunktZ
|13|PoliliniaZ
|15|WielokątZ
|18|WielopunktowyZ
|21|PunktM
|23|PolikaM
|25|WielokątM
|28|WielopunktowyM
|31|MultiPatch

### Rekordy danych ###

Po głównym nagłówku pliku następują rekordy o zmiennej długości, przy czym każdy rekord składa się z nagłówka rekordu o stałej długości, po którym następuje zawartość rekordu o zmiennej długości.

#### Nagłówek rekordu ####

Nagłówek rekordu zawiera informacje o numerze rekordu i długości zawartości rekordu o stałej długości 8 bajtów. Organizacja nagłówka rekordu jest następująca:


|Bajty|Pole|Wartość|Typ|Kolejność bajtów
---|---|---|---|---|
|0-3|Numer rekordu|Numer rekordu|Całkowity|Duży
|4-7|Długość rekordu|Długość rekordu|Całkowita|Duża

#### Zawartość rekordu ####

Zawartość rekordu pliku kształtu składa się z typu kształtu, po którym następują dane geometryczne dla tego kształtu. Typ kształtu 0 reprezentuje pusty kształt, który nie ma danych geometrycznych dla kształtu. Długość zawartości rekordu jest odzwierciedleniem części kształtu i wierzchołków. Weźmy przykład typu Point Shape, aby wyjaśnić, w jaki sposób rekord zawiera informacje o takim typie kształtu.

Punkt reprezentuje określoną lokalizację geograficzną w kolejności X, Y, gdzie każda współrzędna jest reprezentowana przez wartość podwójnej precyzji. W poniższej tabeli przedstawiono rozmieszczenie typu kształtu Punkt.


|Bajty|Typ kształtu|Wartość|Typ|Liczba|Kolejność bajtów
---|---|---|---|---|---|
|0-3|Typ kształtu|1|Całkowity|1|Mały
|4-11|X|X|podwójne|1|Małe
|12-19|T|Y|podwójne|1|Małe

Przykłady innych typów kształtów można znaleźć w dokumencie opisu technicznego ESRI.

## Bibliografia ##

* [Opis techniczny ESRI Shapefile](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) autorstwa ESRI

