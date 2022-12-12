{
  "date" : "2020-03-16",
  "keywords" :["Plik IGES", "Format pliku", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format plików IGES i interfejsy API, które mogą tworzyć i otwierać pliki IGES.",
  "title" :"Format Pliku IGES",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Czym jest plik IGE?

Plik z rozszerzeniem .iges służy do wymiany informacji projektowych między aplikacjami do projektowania wspomaganego komputerowo (CAD). IGES oznacza wstępne specyfikacje wymiany grafiki. Informacje wymieniane za pomocą IGES obejmują schemat obwodu, model krawędziowy, powierzchnię o dowolnym kształcie lub reprezentacje modelowania brył. IGES znajduje zastosowanie w tradycyjnych rysunkach technicznych, analizie modeli i funkcjach produkcyjnych. Format może wymieniać informacje projektowe 2D lub 3D między programami CAD. Pliki IGES można otwierać za pomocą kilku aplikacji CAD, takich jak Autodesk i CADSoftTools ABViewer. Dostępnych jest również kilka interfejsów API do programowego otwierania i konwertowania plików IGES.

## Format pliku IGES

Pliki IGES są w formacie tekstowym ASCII i można je otworzyć w dowolnym edytorze tekstu, aby wyświetlić zawartość pliku. Informacje tekstowe w pliku IGES są reprezentowane w formacie „Hollerith”. Zwykły plik IGES może zawierać tysiące linii reprezentujących informacje 2D lub 3D, które można wymieniać zgodnie z tym formatem. Plik IGES jest podzielony na pięć sekcji, oznaczonych wielką literą w 73. kolumnie. Te sekcje to `Start` (S), `Global` (G), `Data Entry` (D), `Parameter Data` (P) i `Zakończ` (T). Sekcje Wprowadzanie danych i Dane parametrów są powszechnie oznaczane skrótami odpowiednio DE i PD.

### Nagłówek pliku IGES

Sekcje Start i Global zawierają podstawowe informacje o:
* Nazwa pliku i jego źródło
* Ograniczniki sekcji danych parametrów
* Autor pliku i inne informacje ogólne.

Sekcje Start i Global z przykładowego dokumentu na Wikipedii są następujące.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Jak widać, pole startowe zawiera czytelne dla człowieka opisy pliku, aw kolumnach 1-72 dowolne znaki, z linią kończącą się nagłówkiem sekcji i numerem linii sekcji. Sekcja Start musi zawierać co najmniej 1 linię. Sekcja globalna zawiera dane preprocesora. Musi być również obecny w pliku i kończyć się formatem G000000#.

### Sekcja wprowadzania danych (DE) i danych parametrów (PD).

#### Sekcja wprowadzania danych
Plik IGES składa się z kilku jednostek, które zawierają informacje o podstawowych danych formatu pliku IGES. Jednostka zawiera informacje o różnych elementach formatu danych IGES i służy do rysowania. Częściej używane jednostki obejmują:
* Łuk kołowy
* Krzywa złożona
* Łuk stożkowy
* Samolot
* Linia

To tylko kilka, a w IGES jest około 150 różnych podmiotów. Każda jednostka jest identyfikowana przez numer typu, taki jak:
* ŁUK OKRĄGŁY (typ 100)
* LINIA (Typ 110)

##### Właściwości jednostki

Każda zadeklarowana jednostka ma następujące właściwości.

|Nazwa pola|Opis|
---|---|
|Typ podmiotu |To jest opisywany typ podmiotu. Na przykład 116 opisuje jednostkę Point.|
|Wskaźnik PD |Podaje lokalizację danych encji w sekcji Dane parametrów. Ta lokalizacja to po prostu numer wiersza w sekcji PD, która zawiera pierwszy wiersz danych tej jednostki.|
|Struktura |Zero lub wskaźnik do encji definicji. Nie dotyczy większości podmiotów|
|Wzór czcionki linii| Liczba lub wskaźnik do elementu wzoru czcionki linii. Liczba oznacza: * 0 Nie określono wzoru (domyślnie) * 1 Jednolity * 2 Przerywany * 3 Fantom * 4 Linia środkowa * 5 Kropkowany|
|Poziom| Określa poziomy, które mają być skojarzone z tą jednostką. Pozwala podmiotowi pojawiać się na więcej niż jednym poziomie|
|Wyświetl| Określa opcje wyświetlania. Są to: 0 Wskazuje jednakową widoczność i charakterystykę we wszystkich widokach. Domyślny wskaźnik do encji View (typ 410), z którego można go przeglądać Odwołanie do encji View Visible Associativity (typ 402, formularz 3)
|Wskaźnik macierzy transformacji| Odwołuje się do jednostki macierzy transformacji (typ 124) lub domyślnie wynosi zero (brak transformacji)|
|Powiązanie wyświetlania etykiet| Odwołuje się do powiązania wyświetlania etykiety (typ 402, formularz 5), które definiuje sposób wyświetlania etykiety jednostki.|
|Numer statusu| Zawiera cztery sekcje po dwa numery. 1-2: Pusty stan. Albo 00 dla normalnego, albo 01 dla wygaszonego. 3-4: Przełącznik podmiotu podrzędnego: to 00 dla niezależnego, 01 dla zależnego fizycznie, 02 dla zależnego logicznie i 03 dla obu. 5-6: Flaga użycia jednostki: jest albo 00 dla geometrii, 01 dla adnotacji, 02 dla definicji, 03 dla innej, 04 dla logicznej, 05 dla parametrycznej 2D i 06 dla geometrii konstrukcyjnej. Wreszcie, 7-8 to hierarchia, gdzie 00 oznacza globalną górę w dół (użyj cech tej encji), 01 to globalne odroczenie (nie używaj cech tej encji), a 02 to użycie właściwości hierarchii (użyj encji hierarchii (typ 406, formularz 10)określenie cech grupowania hierarchicznego).|
|Numer sekwencyjny| Określony przez D#, gdzie # to numer wiersza dla tej sekcji (nie od początku pliku). Jest to również używane do wskazania tej jednostki wprowadzania danych.|
|Typ podmiotu| jest podany dwa razy na listę podmiotów|
|Liczba grubości linii| Określa grubość podczas wyświetlania elementu. Najmniejsza to 1, 0 to wartość domyślna|
|Numer koloru| Określa kolor elementu. Dozwolone wartości całkowite to: 0 Brak koloru (domyślnie) 1 Czarny 2 Czerwony 3 Zielony 4 Niebieski 5 Żółty 6 Magenta 7 Cyjan 8 Biały|
|Liczba linii parametru| Określa liczbę wierszy, które ten element zajmuje w sekcji danych parametrów|
|Numer formularza| Wskazuje formę lub reprezentację tej jednostki. Zmienia sposób interpretacji danych parametru. Wartość domyślna to 0|
|Zarezerwowane pole| Nie używany|
|Zarezerwowane pole| Nie używany|
|Etykieta podmiotu| Identyfikator określony przez aplikację - wyrównany do prawej|
|Numer indeksu dolnego| Kwalifikator liczbowy dla etykiety jednostki. Oba razem tworzą unikalny identyfikator podmiotu|
|Numer sekwencyjny Patrz wyżej. |Będzie to D#+1, ponieważ każdy element jest określony w dwóch wierszach.|

#### Sekcja danych parametrów
Po sekcji Wpisy danych następuje sekcja Dane parametrów. Wymienia dane dla każdego odpowiedniego wpisu i wymienia parametry jednostki na podstawie ograniczników określonych w sekcji Globalne (zwykle przecinki oddzielają parametry, a średnik kończy listę).


## Bibliografia
* [IGES autorstwa WikiPedia](https://en.wikipedia.org/wiki/IGES)

