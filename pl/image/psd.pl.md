{
  "date" : "2019-10-11",
  "keywords" :[ "plik psd", "format pliku psd", "co to jest plik psd", "plik", "przykład psd", "rozszerzenie pliku psd", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD — format pliku obrazu programu Photoshop",
  "description":"Poznaj format pliku PSD i interfejsy API, które mogą tworzyć i otwierać pliki PSD.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik PSD?

PSD, Photoshop Document, reprezentuje natywny format pliku Adobe Photoshop używany do projektowania i tworzenia grafiki. Pliki PSD mogą zawierać warstwy obrazu, warstwy dopasowania, maski warstw, adnotacje, informacje o pliku, słowa kluczowe i inne elementy specyficzne dla programu Photoshop. Pliki programu Photoshop mają domyślne rozszerzenie .PSD i maksymalną wysokość i szerokość 30 000 pikseli oraz limit długości do dwóch gigabajtów.

## Specyfikacje formatu plików PSD ##

Dane w pliku PSD są przechowywane w kolejności bajtów big endian. Oznacza to zamianę krótkich i długich liczb całkowitych podczas odczytu lub zapisu na platformie Windows. Format pliku programu Photoshop jest podzielony na pięć głównych części. Ma wiele znaczników długości, których można użyć do przechodzenia z jednej sekcji do drugiej. Znaczniki długości są zwykle uzupełniane bajtami w celu zaokrąglenia do najbliższego przedziału 2 lub 4 bajtów. Pięć głównych części to:

* Nagłówek pliku
* Dane trybu koloru
* Zasoby obrazu
* Informacje o warstwie i masce
* Dane obrazu

Aby zapewnić zgodność, dane powinny być zapisywane we wszystkich tych polach w sekcji, ponieważ program Photoshop może próbować odczytać całą sekcję. Oznacza to również, że podczas zapisywania do pliku w pominiętych polach będą zapisywane zera. Pole długości w sekcjach rozdzielonych długością powinno być używane do decydowania, kiedy przerwać czytanie. W większości przypadków pole długości wskazuje liczbę kolejnych bajtów, a nie rekordów. Podczas czytania pliku należy pamiętać o następujących kwestiach.

* Wartości w kolumnie „Długość” we wszystkich tabelach wyrażone są w bajtach.
* Wszystkie wartości zdefiniowane jako łańcuch znaków Unicode składają się z:
* Pole o długości 4 bajtów, reprezentujące liczbę znaków w łańcuchu (nie w bajtach).
* Ciąg wartości Unicode, dwa bajty na znak.

### Nagłówek pliku ###

Nagłówek pliku zawiera podstawowe właściwości obrazu.

|Długość|Opis
---|---|
|4|Podpis: zawsze równy '8BPS' . Nie próbuj czytać pliku, jeśli podpis nie pasuje do tej wartości.
|2|Wersja: zawsze równa 1. Nie próbuj czytać pliku, jeśli wersja nie pasuje do tej wartości. (~*~*PSB~*~* wersja to 2.)
|6|Zarezerwowane: musi wynosić zero.
|2|Liczba kanałów w obrazie, w tym kanały alfa. Obsługiwany zakres to od 1 do 56.
|4|Wysokość obrazu w pikselach. Obsługiwany zakres to od 1 do 30 000.
|4|Szerokość obrazu w pikselach. Obsługiwany zakres to od 1 do 30 000.
|2|Głębokość: liczba bitów na kanał. Obsługiwane wartości to 1, 8, 16 i 32.
|2|Tryb koloru pliku. Obsługiwane wartości to: Bitmap # 0; Skala szarości nr 1; Indeksowany nr 2; RGB nr 3; CMYK nr 4; Wielokanałowy nr 7; Dwutonowy nr 8; Laboratorium nr 9.

### Sekcja danych trybu koloru ###

Sekcja danych trybu koloru ma następującą strukturę:


|Długość|Opis
---|---|
|4|Długość następujących danych koloru
|zmienna|Dane koloru

Dane trybu koloru są dostępne tylko dla koloru indeksowanego i bichromii zgodnie z definicją w polu trybu w sekcji Nagłówek pliku. We wszystkich innych trybach ta sekcja jest reprezentowana przez 4-bajtowe wartości wyzerowane. W przypadku obrazów w kolorze indeksowanym długość wynosi 768, a dane kolorów zawierają tabelę kolorów obrazu w kolejności bez przeplotu. W przypadku obrazów bichromii dane kolorów zawierają specyfikację bichromii (której format nie jest udokumentowany). Inne aplikacje, które odczytują pliki programu Photoshop, mogą traktować obraz bichromii jako obraz w odcieniach szarości i po prostu zachowywać informacje o bichromii podczas odczytywania i zapisywania pliku.

### Sekcja zasobów graficznych ###

Trzecia sekcja pliku zawiera zasoby obrazu. Zaczyna się od pola długości, po którym następuje seria bloków zasobów.


|Długość|Opis
---|---|
|4|Długość sekcji zasobów obrazu. Długość może wynosić zero.
|Zmienna|Zasoby obrazu (bloki zasobów obrazu)

Zasoby obrazów służą do przechowywania danych innych niż piksele powiązanych z obrazami, takich jak ścieżki narzędzi pióra. Nazywa się je blokami zasobów, ponieważ przechowują dane, które były przechowywane w zasobach komputera Macintosh we wczesnych wersjach programu Photoshop. Podstawowa struktura bloków zasobów obrazu jest przedstawiona poniżej:


|Długość|Opis
---|---|
|4|Podpis: '8BIM'
|2|Unikalny identyfikator zasobu. Identyfikatory zasobów obrazu zawierają listę identyfikatorów zasobów używanych przez program Photoshop.
|Zmienna|Nazwa: Łańcuch Pascala, dopełniony w celu wyrównania rozmiaru (nazwa pusta składa się z dwóch bajtów 0)
|4|Rzeczywisty rozmiar danych zasobów, które następują
|Zmienna|Dane zasobu, opisane w sekcjach dotyczących poszczególnych typów zasobu. Jest wyściełany, aby wyrównać rozmiar.

Zasoby obrazów używają kilku standardowych numerów identyfikacyjnych.

### Informacje o warstwie i masce ###

Czwarta sekcja pliku programu Photoshop zawiera informacje o warstwach i maskach, takie jak liczba warstw, kanały w warstwach, zakresy mieszania, klucze warstw dopasowania, warstwy efektów i parametry masek. Jeśli nie ma warstw ani masek, ta sekcja jest reprezentowana przez wyzerowane 4-bajtowe pole. Podczas czytania tego rozdziału należy zwrócić szczególną uwagę na długość odcinków ze względu na wyzerowane wartości. Układ sekcji Warstwy i Maski jest następujący:


|Długość|Opis
---|---|
|4|Długość sekcji informacji o warstwie i masce. (Długość PSB wynosi 8 bajtów.)
|Zmienna|Informacje o warstwie
|Zmienna|Globalne informacje o masce warstwy
|Zmienna|Seria tagowanych bloków zawierających różne typy danych.

#### Informacje o warstwie ####

Poniższa tabela przedstawia organizację wysokiego poziomu informacji o warstwach.


|Długość|Opis
---|---|
|4|Długość sekcji informacji o warstwach, zaokrąglona w górę do wielokrotności 2. (Długość PSB wynosi 8 bajtów.)
|2|Liczba warstw. Jeśli jest to liczba ujemna, jej wartością bezwzględną jest liczba warstw, a pierwszy kanał alfa zawiera dane przezroczystości dla scalonego wyniku.
|Zmienna|Informacje o każdej warstwie. Zobacz Rekordy warstw opisuje strukturę tych informacji dla każdej warstwy.
|Zmienna|Dane obrazu kanału. Zawiera jeden lub więcej rekordów danych obrazu dla każdej warstwy. Warstwy są w takiej samej kolejności, jak w informacjach o warstwach

### Dane obrazu ###

Dane dotyczące pikseli obrazu są zawarte w sekcji danych obrazu pliku. Rozmieszczenie danych w sekcji danych obrazu jest w porządku planarnym, tzn. najpierw wszystkie dane czerwone, potem wszystkie dane zielone itd. Każda płaszczyzna jest przechowywana w kolejności linii skanowania, bez bajtów dopełniających. Sekcja danych obrazu jest ułożona w formacie jak pokazano w poniższej tabeli.

|Długość|Opis
---|---|
|2|Metoda kompresji: *0 = surowe dane obrazu * 1 = skompresowane RLE dane obrazu zaczynają się od liczby bajtów dla wszystkich linii skanowania (wierszy * kanałów), przy czym każda liczba jest przechowywana jako wartość dwubajtowa. Następują skompresowane dane RLE, z każdą linią skanowania skompresowaną oddzielnie. Kompresja RLE jest tym samym algorytmem kompresji, który jest używany przez procedurę PackBits ROM Macintosha oraz standard TIFF. *2 = ZIP bez predykcji *3 = ZIP z predykcją.
|Zmienna|Dane obrazu. Kolejność planarna = RRR GGG BBB itd.

## Bibliografia ##

* [Specyfikacje formatu plików PSD — firma Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Format pliku Adobe Photoshop](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

