{
  "date" : "2019-10-11",
  "keywords" :["plik tiff", "format pliku tiff", "co to jest plik tiff", "plik", "przykład tiff", "rozszerzenie pliku tiff", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - format pliku obrazu",
  "description":"Poznaj format pliku TIFF i interfejsy API, które mogą tworzyć i otwierać pliki TIFF.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik TIFF?

TIFF lub TIF, Tagged Image File Format, reprezentuje obrazy rastrowe przeznaczone do użytku na różnych urządzeniach zgodnych z tym standardem formatu plików. Jest w stanie opisywać dane obrazu dwupoziomowego, w skali szarości, w palecie kolorów i w pełnym kolorze w kilku przestrzeniach kolorów. Obsługuje zarówno stratne, jak i bezstratne schematy kompresji, aby wybrać między przestrzenią a czasem dla aplikacji korzystających z formatu. Format nie jest zależny od maszyny i jest wolny od ograniczeń, takich jak procesor, system operacyjny lub systemy plików.

## Krótka historia formatu pliku TIFF

Format pliku TIFF został początkowo stworzony przez Aldus Corporation jesienią 1986 roku, po serii spotkań z różnymi producentami skanerów i twórcami oprogramowania. Głównym celem formatu plików TIFF było zapewnienie wspólnego formatu plików zeskanowanych obrazów dla wszystkich dostawców skanerów biurkowych. Począwszy od obsługi tylko binarnego formatu obrazu, format ewoluował do obsługi obrazów w skali szarości i kolorów wraz z upływem czasu. Początkowa wersja specyfikacji formatu plików TIFF może być oznaczona jako Reivision 3.0, ponieważ istniały dwie wcześniejsze wersje robocze. Główna wersja 5.0 została opublikowana w 1988 roku, która dodała obsługę obrazów z paletą kolorów i kompresję LZW. Wersja 6.0 formatów plików TIFF została opublikowana później w 1992 roku. W 1994 roku firma Adobe Systems przejęła firmę Aldus, a specyfikacje są obecnie dostępne i obsługiwane przez firmę Adobe Systems.

## Specyfikacje formatu plików TIFF

Format pliku TIFF jest rozszerzalny i przeszedł kilka zmian, co pozwala na włączenie nieograniczonej ilości informacji prywatnych lub informacji specjalnego przeznaczenia. Plik TIFF zaczyna się od 8-bajtowego nagłówka, w którym bajty są ponumerowane od 0 do N. Największy możliwy plik TIFF ma długość 2**32 bajtów. Plik zaczyna się od 8-bajtowego nagłówka pliku obrazu, który bezpośrednio wskazuje plik obrazu (IFD). IFD zawiera informacje o obrazie, jak również wskaźniki do rzeczywistych danych obrazu.

### Nagłówek pliku TIFF

8-bajtowy nagłówek pliku TIFF zawiera następujące informacje:

**Bajty 0-1:** Kolejność bajtów używana w pliku. Dozwolone wartości to: „II” (4949.H) „MM” (4D4D.H).

W formacie „II” kolejność bajtów jest zawsze od najmniej znaczącego do najbardziej znaczącego bajtu, zarówno dla 16-bitowych, jak i 32-bitowych liczb całkowitych. Nazywa się to kolejnością bajtów little-endian. W formacie „MM” kolejność bajtów jest zawsze od najbardziej znaczącego do najmniej znaczącego, zarówno dla 16-bitowych, jak i 32-bitowych liczb całkowitych. Nazywa się to kolejnością bajtów big-endian.

**Bajty 2-3:** Dowolna, ale starannie wybrana liczba (42), która dodatkowo identyfikuje plik jako plik TIFF. Kolejność bajtów zależy od wartości bajtów 0-1.

**Bajty 4-7:** Przesunięcie (w bajtach) pierwszego IFD. Katalog może znajdować się w dowolnym miejscu w pliku po nagłówku, ale musi zaczynać się na granicy słowa. W szczególności katalog plików obrazu może podążać za danymi obrazu, które opisuje. Czytelnicy muszą podążać za wskazówkami, dokąd mogą prowadzić. Termin przesunięcie bajtu jest zawsze używany w tym dokumencie w odniesieniu do lokalizacji względem początku pliku TIFF. Pierwszy bajt pliku ma przesunięcie równe 0.

### Katalog plików obrazu

IFD zawiera informacje o obrazie, jak również wskaźniki do rzeczywistych danych obrazu. Składa się z 2-bajtowej liczby wpisów w katalogu (tj. liczby pól), po której następuje sekwencja 12-bajtowych wpisów w polach , po którym następuje 4-bajtowe przesunięcie następnego IFD (lub 0, jeśli nie ma). Plik TIFF musi zawierać co najmniej 1 IFD, a każdy IFD musi zawierać co najmniej jeden wpis.

#### Wpis IFD

Każdy 12-bajtowy wpis IFD ma następujący format.


|Bajty|Opis
---|---|
|0-1|Znacznik identyfikujący pole
|2-3|Typ pola
|4-7|Liczba wskazanego typu
|8-11|Przesunięcie wartości, przesunięcie pliku (w bajtach) wartości pola. Oczekuje się, że wartość rozpocznie się na granicy słowa; odpowiednie przesunięcie wartości będzie zatem liczbą parzystą. To przesunięcie pliku może wskazywać dowolne miejsce w pliku, nawet po danych obrazu

Pole TIFF to jednostka logiczna składająca się ze znacznika TIFF i jego wartości. Ta koncepcja logiczna jest realizowana jako wpis IFD plus rzeczywista wartość, jeśli nie pasuje do części wartości/przesunięcia, ostatnich 4 bajtów wpisu IFD. Terminy pole TIFF i wpis IFD są stosowane zamiennie w większości kontekstów.

### Linia bazowa TIFF ###

Baseline TIFF jest rdzeniem TIFF, podstawowymi elementami, które wszyscy główni programiści TIFF powinni obsługiwać w swoich produktach. Zgodność z formatem TIFF jest uzależniona od przestrzegania podstawowych wymagań TIFF. Wymagania te są dobrze udokumentowane w dokumencie specyfikacji 6.0.

#### Wiele obrazów na plik ####

W pliku TIFF może znajdować się więcej niż jeden IFD. Każdy IFD definiuje podtekst. Jednym z potencjalnych zastosowań podtekstów jest opisywanie powiązanych obrazów, takich jak strony faksu. Czytnik Baseline TIFF nie jest wymagany do odczytywania żadnych IFD poza pierwszym.

#### Typy obrazów ####

Podstawowy obraz TIFF ma następujące typy:

**Dwupoziomowy:** obraz dwupoziomowy zawiera dwa kolory — czarny i biały. TIFF umożliwia aplikacji zapisywanie danych dwupoziomowych w formacie „biały to zero” lub „czarny to zero”. Pole, w którym zapisywane są te informacje, nosi nazwę **Interpretacja fotometryczna**.

* Pełny kolor RGB

Informacje dotyczące interpretacji fotometrycznej dla obrazów dwupoziomowych są następujące:

Znacznik = 262 (106.H)
Typ = KRÓTKI
**Wartości**

|Wartość|Opis|
---|---|
|0|Dla obrazów dwupoziomowych iw skali szarości: 0 jest przedstawiane jako białe. Wartość maksymalna jest przedstawiana w kolorze czarnym. Jest to normalna wartość dla Kompresji#2|
|1|CzarnyIsZero. W przypadku obrazów dwupoziomowych iw skali szarości: 0 jest obrazowane jako czarny. Wartość maksymalna jest przedstawiana jako biała. Jeśli ta wartość jest określona dla Kompresji nr 2, obraz powinien być wyświetlany i drukowany w odwrotnej kolejności.|

**Skala szarości:** obrazy w skali szarości to uogólnienie obrazów dwupoziomowych. Obrazy dwupoziomowe mogą przechowywać tylko dane obrazu czarno-białego, ale obrazy w skali szarości mogą również przechowywać odcienie szarości. Aby opisać takie obrazy, musisz dodać lub zmienić następujące pola. Pozostałe wymagane pola są takie same, jak w przypadku obrazów dwupoziomowych. W przypadku obrazów w skali szarości, kompresja nr 1 lub 32773 (PackBits). W formacie Baseline TIFF obrazy w skali szarości można przechowywać jako dane nieskompresowane lub skompresowane za pomocą algorytmu PackBits.

Informacje **BitsPerSample** dla obrazów w skali szarości są następujące:

Znacznik = 258 (102.H)
Typ = KRÓTKI

Liczba bitów przypadająca na komponent. Dopuszczalne wartości dla obrazów w skali szarości w formacie Baseline TIFF to 4 i 8, co pozwala na uzyskanie 16 lub 256 różnych odcieni szarości.

**Palette-Color:** Obrazy w palecie kolorów są podobne do obrazów w skali szarości. Nadal mają jeden składnik na piksel, ale wartość składnika jest używana jako indeks w pełnej tabeli przeglądowej RGB. Aby opisać takie obrazy, należy dodać lub zmienić następujące pola. Pozostałe wymagane pola są takie same jak w przypadku obrazów w skali szarości.
Informacje o interpretacji fotometrycznej dla obrazu Palette-Color są następujące:

Fotometryczna interpretacja = 3 (paleta kolorów).
ColorMapTag = 320 (140.H)
Typ = KRÓTKI
N = 3 * (2 bity na próbkę)

To pole definiuje mapę kolorów czerwono-zielono-niebieskich (często nazywaną tabelą przeglądową) dla obrazów z paletą kolorów. W obrazie z paletą kolorów wartość piksela jest używana do indeksowania w tabeli przeglądowej RGB. Na przykład piksel koloru z palety o wartości 0 byłby wyświetlany zgodnie z trójką 0th Red, Green, Blue. W mapie kolorów TIFF wszystkie wartości Red są na pierwszym miejscu, następnie wartości Green, a następnie wartości Blue. Na ColorMap czarny jest reprezentowany przez 0,0,0, a biały przez 65535, 65535, 65535.

**Pełny kolor RGB:** W obrazie RGB każdy piksel składa się z trzech elementów: czerwonego, zielonego i niebieskiego. Nie ma ColorMap. Aby opisać obraz RGB, musisz dodać lub zmienić następujące pola i wartości. Pozostałe wymagane pola są takie same, jak w przypadku obrazów z paletą kolorów.

Liczba bitów na próbkę = 8,8,8. Każdy komponent ma głębokość 8 bitów w obrazie Baseline TIFF RGB.

PhotometricInterpretation = 2 (RGB) i nie ma ColorMap.

Znacznik = 277 (115.H)
Typ = KRÓTKI
Liczba komponentów na piksel. Liczba ta wynosi 3 dla obrazów RGB, chyba że obecne są dodatkowe próbki.

## Bibliografia ##

* [Format pliku TIFF – Wikipedia](https://en.wikipedia.org/wiki/TIFF)

