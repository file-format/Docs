{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "podstawy" ],
  "description":"Portable Document Format (PDF) to standardowa reprezentacja dokumentów niezależna od oprogramowania, sprzętu i systemu operacyjnego. Standardy PDF obejmują PDF/A, PDF/E, PDF/UA, PDF/VT i PDF/X.",
  "title" :"Format pliku PDF - Co to jest plik PDF?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) to rodzaj dokumentu stworzony przez firmę Adobe w latach 90. Celem tego formatu plików było wprowadzenie standardu reprezentacji dokumentów i innych materiałów referencyjnych w formacie niezależnym od oprogramowania użytkowego, sprzętu oraz systemu operacyjnego. Format pliku PDF ma pełne możliwości przechowywania informacji, takich jak tekst, obrazy, hiperłącza, pola formularzy, multimedia, podpisy cyfrowe, załączniki, metadane, funkcje geoprzestrzenne i obiekty 3D, które mogą stać się częścią dokumentu źródłowego.

W większości przypadków istniejące dokumenty są konwertowane do formatu PDF, zamiast tworzyć nowy plik PDF od podstaw. Ale to nie znaczy, że nie ma oprogramowania do tworzenia lub manipulowania plikami PDF.

**(Chcesz podzielić się czymś na temat formatu plików PDF? Możesz opublikować swoje ustalenia w sekcji [Wiadomości dotyczące formatu plików PDF](https://news.fileformat.com/t/PDF).)**

## Format pliku PDF — krótka historia

Szybkie przejrzenie osi czasu dotyczącej tworzenia pliku PDF pod względem osi czasu jest następujące:

**1993** — Firma Adobe Systems bezpłatnie udostępniła specyfikacje w formacie PDF

**2008** — PDF został udostępniony jako otwarty standard 1 lipca 2008 r. i opublikowany przez Międzynarodową Organizację Normalizacyjną jako **ISO 32000-1:2008**.

**2008** — firma Adobe opublikowała licencję na patent publiczny do formatu ISO 32000-1, nieodpłatne prawa do wszystkich patentów należących do firmy Adobe, które są niezbędne do tworzenia, używania, sprzedaży i dystrybucji implementacji zgodnych z formatem PDF.

Pierwsza wersja PDF oznaczona jako PDF 1.0, która później przeszła poprawki aż do PDF 1.7. PDF 1.7, który stał się normą ISO 32000-1, zawiera kilka niestandaryzowanych zastrzeżonych technologii, jak również Adobe XML Forms Architecture (XFA) i rozszerzenie JavaScript dla programu Acrobat. To właśnie 28 lipca 2017 roku opublikowano PDF 2.0, znany jako ISO 32000-2:2017, który nie zawiera żadnych niestandaryzowanych technologii.

## Specyfikacje formatu plików PDF

Plik PDF to zestaw bajtów, które można pogrupować w tokeny zgodnie z regułami składni określonymi w specyfikacjach PDF. Jeden lub więcej tokenów jest łączonych w celu utworzenia jednostek składniowych wyższego poziomu, głównie obiektów, które są podstawowymi wartościami danych, z których tworzony jest dokument PDF.

### Struktura plików PDF

Zawartość pliku PDF jest ułożona w następującej kolejności wewnątrz pliku.

|Nagłówek
|Ciało
|Tabela odsyłaczy
|Przyczepa

#### Nagłówek pliku PDF ####

Niezależnie od wersji PDF, plik PDF zaczyna się od nagłówka zawierającego unikalny identyfikator PDF oraz wersję formatu np. %PDF-1.x gdzie x zawiera się w przedziale 1-7.

#### Treść pliku ####

Treść pliku PDF składa się z sekwencji obiektów pośrednich reprezentujących zawartość dokumentu. Obiekty, jak opisano powyżej, reprezentują elementy dokumentu, takie jak czcionki, strony i próbkowane obrazy. Począwszy od PDF 1.5, treść może również zawierać strumienie obiektów, z których każdy zawiera sekwencję obiektów pośrednich.

#### Tabela odsyłaczy ####

Tabela odsyłaczy zawiera informacje, które umożliwiają swobodny dostęp do obiektów pośrednich w pliku, dzięki czemu nie trzeba czytać całego pliku, aby zlokalizować konkretny obiekt. Tabela zawiera jednowierszowy wpis dla każdego obiektu pośredniego, określający przesunięcie bajtowe tego obiektu w treści pliku. (Począwszy od PDF 1.5, niektóre lub wszystkie informacje odsyłaczy mogą być alternatywnie zawarte w strumieniach odsyłaczy.

#### Zwiastun pliku ####

Zwiastun pliku PDF umożliwia zgodnemu czytelnikowi szybkie znalezienie tabeli odsyłaczy i niektórych obiektów specjalnych. Czytelnicy konformistyczni powinni przeczytać plik PDF od końca. Ostatni wiersz pliku powinien zawierać tylko znacznik końca pliku, %%EOF. Dwa poprzednie wiersze będą zawierać, po jednym w każdym wierszu, słowo kluczowe startxref i przesunięcie bajtu w dekodowanym strumieniu od początku pliku do początku słowa kluczowego xref w ostatniej sekcji odsyłacza.

### Obiekty PDF ###

Plik PDF zawiera kilka różnych typów obiektów, które są następujących typów

* Wartości logiczne — reprezentujące warunkową prawdę lub fałsz
* Liczby - wartości całkowite i rzeczywiste
* Ciągi — zawiera znaki w nawiasach
* Nazwy - zaczynają się od przodu / znaku, np. /ASomewhatLongerName daje w wyniku ASomewhatLongerName
* Tablice — PDF obsługuje tablice jednowymiarowe. Tablice o wyższych wymiarach można konstruować, używając tablic jako elementów zagnieżdżonych
* Słowniki - zbiór obiektów w postaci par klucz-wartość. Może mieć zero wpisów.
* Strumienie - reprezentują sekwencję bajtów, która może mieć nieograniczoną długość
* Obiekt zerowy — reprezentuje wartość zerową

Mogą istnieć inne obiekty, takie jak komentarze, które są wprowadzane ze znakiem % i mogą zawierać znaki 8-bitowe.

### Obiekty pośrednie ###

Każdy obiekt w pliku PDF może być oznaczony jako obiekt pośredni. Obiekty pośrednie otrzymują unikalny identyfikator obiektu, za pomocą którego inne obiekty mogą się do niego odwoływać. Odsyłacze do nich są utrzymywane w tabeli indeksów i oznaczane słowem kluczowym xref, które następuje po głównej części i podaje przesunięcie bajtowe każdego obiektu pośredniego od początku pliku.

### Liniowe i nieliniowe układy PDF ###

Układy PDF są klasyfikowane jako liniowe i nieliniowe w zależności od aplikacji docelowych i innych czynników.

Nieliniowe — nieliniowe pliki PDF zajmują mniej miejsca na dysku w porównaniu z liniowymi plikami PDF. Strony PDF dokumentu znajdują się w rozproszonej formie w pliku PDF i dlatego pliki nieliniowe są wolniejsze w porównaniu z plikami liniowymi.

Liniowy PDF — skierowane do internetowych przeglądarek plików PDF, pliki Linear PDF są konstruowane w taki sposób, że są zapisywane na dysku w sposób liniowy. Nie wymaga to wtyczek przeglądarki, aby cały dokument był ładowany przed wyświetleniem.

### Przegląd obiektów ###

Jak wspomniano, treść PDF jest zbiorem wyżej wymienionych obiektów. PDF jest w dużej mierze oparty na PostScript bez funkcji kontrolnych języków programowania, takich jak polecenia if i pętle. Polecenia wydawane przez kod Postscript w celu generowania treści graficznych są gromadzone i tokenizowane oprócz wszelkich plików, grafiki lub czcionek, do których odnosi się dokument. Wszystkie te treści są gromadzone w jednym pliku, co daje złożone dane wyjściowe PostScript.

#### Tekst ####

Tekst w formacie PDF jest reprezentowany przez elementy tekstowe, które w rzeczywistości są wyświetlane z glifami z czcionek. Glif jest kształtem graficznym i podlega wszelkim manipulacjom graficznym, takim jak transformacja współrzędnych. Ze względu na znaczenie tekstu w opisach większości stron, format PDF zapewnia funkcje wyższego poziomu umożliwiające wygodne i wydajne opisywanie, wybieranie i renderowanie glifów.

#### Grafika ####

Operatory graficzne używane w strumieniach treści PDF opisują wygląd stron, które mają być odtworzone na rastrowym urządzeniu wyjściowym. Obiekty są przeznaczone zarówno do zastosowań związanych z drukarkami, jak i wyświetlaczami. Operatorzy grafiki tworzą sześć głównych grup:

* Operatory stanu grafiki manipulują strukturą danych zwaną stanem grafiki, globalną strukturą, w ramach której działają inne operatory grafiki. Stan grafiki obejmuje bieżącą macierz transformacji (CTM), która odwzorowuje współrzędne przestrzeni użytkownika używane w strumieniu treści PDF na współrzędne urządzenia wyjściowego. Zawiera również bieżący kolor, bieżącą ścieżkę przycinania i wiele innych parametrów, które są niejawnymi operandami operatorów malowania.
* Operatory konstrukcji ścieżek określają ścieżki, które definiują kształty, trajektorie linii i różnego rodzaju regiony. Obejmują one operatory rozpoczynania nowej ścieżki, dodawania do niej segmentów linii i krzywych oraz zamykania jej.
* Operatorzy malowania ścieżek wypełniają ścieżkę kolorem, malują wzdłuż niej obrys lub używają jej jako granicy tnącej.
* Inni operatorzy malowania malują pewne samoopisujące się obiekty graficzne. Obejmują one próbkowane obrazy, geometrycznie zdefiniowane odcienie i całe strumienie treści, które z kolei zawierają sekwencje operatorów graficznych.
* Operatory tekstowe wybierają i pokazują glify znaków z czcionek (opisy krojów pisma reprezentujących znaki tekstowe). Ponieważ PDF traktuje glify jako ogólne kształty graficzne, wiele operatorów tekstu można zgrupować z operatorami stanu grafiki lub malowania. Jednak struktury danych i mechanizmy radzenia sobie z opisami glifów i czcionek są wystarczająco wyspecjalizowane.
* Operatorzy oznaczonej treści kojarzą informacje logiczne wyższego poziomu z obiektami w strumieniu treści. Informacje te nie mają wpływu na renderowany wygląd treści; jest to przydatne w przypadku aplikacji korzystających z formatu PDF do wymiany dokumentów.

## Bibliografia ##

* [Format pliku PDF: podstawowa struktura](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)
* [PDF - Wikipedia](https://en.wikipedia.org/wiki/PDF)
* [Odnośnik PDF — Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

