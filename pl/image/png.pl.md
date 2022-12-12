{
  "date" : "2019-10-11",
  "keywords" :[ "plik png", "format pliku png", "co to jest plik png", "plik", "przykład png", "rozszerzenie pliku png", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku PNG - Plik Obrazu Rastrowego",
  "description":"Poznaj format plików PNG i interfejsy API, które mogą tworzyć i otwierać pliki PNG.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik PNG?

Plik **PNG** (Portable Network Graphics) to format pliku obrazu rastrowego wykorzystujący bezstratną kompresję. Ten format pliku został utworzony jako zamiennik formatu Graphics Interchange Format ([GIF](/pl/image/gif/)) i nie ma ograniczeń dotyczących praw autorskich. Jednak format pliku PNG nie obsługuje animacji. Format pliku PNG obsługuje bezstratną kompresję obrazu, co czyni go popularnym wśród użytkowników. Z biegiem czasu PNG ewoluował jako jeden z powszechnie używanych formatów plików graficznych.

## Krótka historia formatu pliku PNG

Głównym powodem powstania formatu plików PNG był opatentowany algorytm kompresji Lempel-Ziv-Welch, zastosowany w formacie pliku GIF. To wraz z innymi ograniczeniami GIF stworzyło potrzebę zastąpienia formatu pliku [**GIF**](/pl/image/gif/). Pierwsza propozycja i nazwa formatu plików PNG pojawiła się w styczniu 1995 roku. Poniżej wymieniono najważniejsze wydarzenia dotyczące formatów plików PNG:

* Październik 1996: Wersja 1.0 specyfikacji PNG została wydana, a później pojawiła się jako [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. To samo stało się rekomendacją W3C w październiku 1996.
* Grudzień 1998: Wydano wersję 1.1 z niewielkimi zmianami i trzema nowymi fragmentami.
* Sierpień 1999: Wydano wersję 1.2, dodającą jeden dodatkowy fragment.
* Listopad 2003: PNG stał się normą międzynarodową (ISO/IEC 15948:2003). Ta wersja PNG różni się tylko nieznacznie od wersji 1.2 i nie dodaje żadnych nowych porcji.
* Marzec 2004: ISO/IEC 15948:2004

## Funkcjonalne porównanie GIF i PNG

Format pliku PNG został zaprojektowany tak, aby był prosty i przenośny, nieobciążony prawnie, wymienny, elastyczny i solidny. W poniższej tabeli wymieniono funkcje GIF, które oprócz nowych funkcji są dziedziczone przez format pliku PNG.

|Opis|GIF|PNG|
---|---|---|
|Obrazy kolorów indeksowych do 256 kolorów|Tak|Tak|
|Obsługa przesyłania strumieniowego|Tak|Tak|
|Przezroczystość|Tak|Tak|
|Informacje dodatkowe|Tak|Tak|
|Niezależność sprzętu i platformy|Tak|Tak|
|Skuteczne|Tak|Tak|
|Obrazy Truecolor do 48 bitów na piksel|Nie|Tak|
|Obrazy w skali szarości do 16 bitów na piksel|Nie|Tak|
|Pełny kanał alfa (ogólne maski przezroczystości)|Nie|Tak|
|Informacje o gamma obrazu|Nie|Tak|
|Niezawodność|Nie|Tak|
|Szybsza wstępna prezentacja|Nie|Tak|

## Struktura pliku PNG

Prawie wszystkie systemy operacyjne obsługują otwieranie plików PNG. Na przykład przeglądarka Microsoft Windows ma możliwość otwierania plików PNG, ponieważ system operacyjny ma domyślnie obsługę dostępną w ramach instalacji. Plik PNG składa się z `podpisu` PNG, po którym następuje seria //fragmentów//.

### Nagłówek pliku PNG

Pierwsze osiem bajtów pliku PNG zawsze zawiera następujące wartości (dziesiętne):

{{{137 80 78 71 13 10 26 10 }}}

Ten podpis wskazuje, że pozostała część pliku zawiera pojedynczy obraz PNG, składający się z serii fragmentów rozpoczynających się fragmentem IHDR i kończących się fragmentem IEND.

### Kawałki ###

Każdy fragment składa się z czterech części:

**Długość:** 4-bajtowa liczba całkowita bez znaku określająca liczbę bajtów w polu danych fragmentu. Długość liczy tylko pole danych, a nie samo, kod typu porcji lub CRC. Zero to prawidłowa długość. Chociaż kodery i dekodery powinny traktować długość jako unsigned, jej wartość nie może przekraczać 231 bajtów.

**Typ fragmentu:** 4-bajtowy kod typu fragmentu. Dla wygody w opisie i badaniu plików PNG kody typów są ograniczone do wielkich i małych liter ASCII (AZ i az lub 65-90 i 97-122 po przecinku). Jednak kodery i dekodery muszą traktować kody jako stałe wartości binarne, a nie ciągi znaków. Na przykład niewłaściwe byłoby reprezentowanie kodu typu IDAT za pomocą odpowiedników tych liter w EBCDIC. Dodatkowe konwencje nazewnictwa dla typów fragmentów omówiono w następnej sekcji.

**Dane fragmentu:** Bajty danych odpowiednie dla typu fragmentu, jeśli istnieje. To pole może mieć zerową długość.

**CRC:** 4-bajtowy CRC (Cyclic Redundancy Check) obliczany na podstawie poprzedzających bajtów w porcji, w tym kodu typu porcji i pól danych porcji, ale bez pola długości. CRC jest zawsze obecny, nawet w przypadku porcji niezawierających danych.

Długość danych porcji może wynosić maksymalnie dowolną liczbę bajtów; w związku z tym implementatorzy nie mogą zakładać, że fragmenty są wyrównane na jakichkolwiek granicach większych niż bajty.

Porcje mogą pojawiać się w dowolnej kolejności, z zastrzeżeniem ograniczeń nałożonych na każdy typ porcji. (Jednym z godnych uwagi ograniczeń jest to, że IHDR musi pojawić się jako pierwszy, a IEND jako ostatni; dlatego fragment IEND służy jako znacznik końca pliku.) Może pojawić się wiele fragmentów tego samego typu, ale tylko wtedy, gdy jest to wyraźnie dozwolone dla tego typu.

#### Typy kawałków

Typy fragmentów są podzielone na fragmenty **krytyczne** i **pomocnicze** na podstawie 4-bajtowej wartości ASCII z rozróżnianiem wielkości liter przypisanej do typu fragmentu. Wszystkie implementacje muszą rozumieć i pomyślnie renderować standardowe fragmenty krytyczne. Prawidłowy obraz PNG musi zawierać fragment IHDR, jeden lub więcej fragmentów IDAT oraz fragment IEND.

### Kompresja

Metoda kompresji PNG 0 (jedyna obecnie zdefiniowana metoda kompresji dla PNG) określa kompresję zmniejszania/nadmuchiwania z przesuwanym oknem o maksymalnej długości 32768 bajtów. Kompresja Deflate jest pochodną LZ77 używaną w programach zip, gzip, pkzip i pokrewnych. Przeprowadzono szeroko zakrojone badania potwierdzające jego status bez patentu. Skompresowane dane w strumieniu danych zlib są przechowywane jako seria bloków, z których każdy może reprezentować surowe (nieskompresowane) dane, dane skompresowane LZ77 zakodowane za pomocą stałych kodów Huffmana lub dane skompresowane LZ77 zakodowane za pomocą niestandardowych kodów Huffmana. Bit znacznika w ostatnim bloku identyfikuje go jako ostatni blok, umożliwiając dekoderowi rozpoznanie końca skompresowanego strumienia danych.

#### Filtrowanie przed kompresją

Filtry wstępnej kompresji są stosowane w celu przygotowania danych obrazu do optymalnej kompresji. Metoda filtra PNG definiuje pięć podstawowych typów filtrów w następujący sposób:

|Typ filtra|Nazwa|Przewidywana wartość|
---|---|---|
|0|Brak|Linia skanowania jest przesyłana niezmodyfikowana|
|1|Sub|Przesyła różnicę między każdym bajtem a wartością odpowiedniego bajtu poprzedniego piksela.|
|2|W górę|Filtr Up() jest taki sam jak filtr Sub() z tą różnicą, że piksel bezpośrednio nad bieżącym pikselem, a nie tylko po jego lewej stronie, jest używany jako predyktor.|
|3|Średnia|Filtr Average() wykorzystuje średnią z dwóch sąsiednich pikseli (lewego i górnego) do przewidywania wartości piksela.|
|4|Paeth|Filtr Paeth() oblicza prostą funkcję liniową trzech sąsiednich pikseli (lewy, górny, lewy górny), a następnie wybiera jako predyktor sąsiedni piksel najbliższy obliczonej wartości.|

Algorytmy filtrowania są stosowane do „bajtów”, a nie do pikseli, niezależnie od głębi bitowej lub typu koloru obrazu. Algorytmy filtrujące działają na sekwencji bajtów utworzonej przez linię skanowania. Jeśli obraz zawiera kanał alfa, dane alfa są filtrowane w taki sam sposób jak dane obrazu.

Kiedy obraz jest z przeplotem, każde przejście wzoru z przeplotem jest traktowane jako niezależny obraz do celów filtrowania. Filtry działają na sekwencjach bajtów utworzonych przez piksele faktycznie przesłane podczas przejścia, a „poprzednia linia skanowania” to ta, która została przesłana wcześniej w tym samym przebiegu, a nie ta sąsiednia w całym obrazie. Należy zauważyć, że podobraz przesyłany w jednym przejściu jest zawsze prostokątny, ale ma mniejszą szerokość i/lub wysokość niż pełny obraz. Filtrowanie nie jest stosowane, gdy ten obraz podrzędny jest pusty.

## Bibliografia ##

* [PNG — strona główna](http://www.libpng.org/pub/png/)

