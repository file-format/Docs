{
  "date" : "2019-10-11",
  "keywords" :["plik exif", "format pliku exif", "co to jest plik exif", "plik", "przykład exif", "rozszerzenie pliku exif", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"Poznaj format pliku EXIF i interfejsy API, które mogą tworzyć i otwierać pliki EXIF.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik EXIF?
EXIF oznacza „Exchangeable Image File Format”, definicję podaną po raz pierwszy przez [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) w 1985 r. Standard jest zarządzany przez Japan Electronics i Information Technology Industries Association (JEITA) na dzień dzisiejszy. EXIF to standard specyfikacji formatów obrazu i dźwięku, używany głównie przez aparaty cyfrowe i skanery.

Standard EXIF zawiera informacje o znakowaniu i metadanych wraz z plikiem obrazu. Metadane mogą zawierać informacje, takie jak model aparatu, czas otwarcia migawki, data i godzina, przysłona, producent, czas ekspozycji, rozdzielczość X, rozdzielczość Y itp. Zwykle dane EXIF są domyślnie ukryte. Aby wyświetlić dane EXIF, należy wybrać właściwości widoku w aplikacji do przeglądania obrazów. Metadane Exif mogą również zawierać miniatury wraz z technicznymi i podstawowymi danymi obrazu w jednym pliku obrazu.

## Historia i wersje ##

* W październiku 1995 r. JEIDA ustanowiła wersję 1. W tej wersji JEIDA zdefiniowała strukturę, która składa się z formatu danych obrazu i informacji o atrybutach oraz podstawowych znaczników.
* Listopad 1997, wersja 1.1 została wprowadzona z większością znaczników z wersji 1, ale dodano również przepisy dotyczące opcjonalnych informacji o atrybutach i operacji formatowania.
* Czerwiec 1998, wersja 2 z przestrzenią kolorów sRGB, skompresowanymi miniaturami i plikami audio.
* Grudzień 1998, wersja 2.1 z ulepszoną pamięcią i informacjami o atrybutach.
* Luty 2002, wersja 2.2, ulepszona wersja 2.1 z dodatkiem uszlachetniania druku.
* Wrzesień 2003, wersja 2.21 z opcjonalną przestrzenią kolorów znaną jako Adobe RGB.

## Format pliku EXIF

EXIF wykorzystuje następujące formaty plików z dodatkiem określonych metadanych.

1. [JPEG](/pl/image/jpeg/) - dyskretna transformata kosinusowa (DCT) dla skompresowanych plików graficznych.
1. [TIFF](/pl/image/tiff/) wersja 6.0 (RGB lub YCbCr) dla nieskompresowanych plików graficznych.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) dla plików audio (liniowy [PCM](https:/ /en.wikipedia.org/wiki/Pulse-code_modulation) lub ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM dla nieskompresowanych danych audio oraz [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) dla skompresowanych danych audio).

### Znacznik używany przez EXIF ###

Znacznik 0xFFE0~~0xFFEF to „Znacznik aplikacji”, używany przez aplikację użytkownika. Na przykład starsze kamery cyfrowe używają formatu JFIF (JPEG File Interchange Format) do przechowywania obrazów. JFIF używa znacznika APP0 (0xFFE0) do wstawiania danych konfiguracji kamery cyfrowej i obrazu miniatury. Ponadto EXIF używa również znacznika aplikacji do wstawiania danych, ale EXIF używa znacznika APP1 (0xFFE1), aby uniknąć konfliktu z formatem JFIF. Wszystkie formaty plików EXIF zaczynają się od tego formatu.


|Znacznik SOI|Znacznik APP1|Dane APP1|Inny znacznik
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Zaczyna się od znacznika SOI (0xFFD8), więc jest to plik JPEG. Następnie natychmiast pojawia się Znacznik APP1. Wszystkie dane EXIF są przechowywane w tym obszarze danych APP1. Część "SSSS" w górnej tabeli oznacza rozmiar obszaru danych APP1 (obszar danych EXIF). Proszę zauważyć, że rozmiar „SSSS” obejmuje również rozmiar samego deskryptora. Po „SSSS” rozpoczynają się dane APP1. Pierwsza część to specjalne dane do identyfikacji, czy używany jest EXIF, czy nie, znak ASCII „EXIF” i 2 bajty 0x00. Po obszarze znacznika APP1 następują inne znaczniki JPEG.

### Struktura danych Exif ###

Zgrubna struktura danych EXIF (APP1) jest pokazana poniżej. Jak omówiono powyżej, dane EXIF zaczynają się od znaku ASCII „EXIF” i 2 bajtów 0x00, po czym następują dane EXIF. EXIF używa formatu TIFF do przechowywania danych.


|FFE1|APP1 Znacznik
---|---|
|SSSS|Dane aplikacji1|Rozmiar danych aplikacji1
|45786966 0000|Nagłówek Exif
|49492A00 08000000|Nagłówek TIFF
|XXXX. . . .|IFD0 (główny obraz)|Katalog
|LLLLLLLL|Link do IFD1
|XXXX. . . .|Obszar danych IFD0
|XXXX. . . .|Exif SubIFD|Katalog
|00000000|Koniec łącza
|XXXX. . . .|Obszar danych Exif SubIFD
|XXXX. . . .|IFD1(obraz miniatury)|Katalog
|00000000|Koniec łącza
|XXXX. . . .|Obszar danych IFD1
|FFD8XXXX. . . XXXXFFD9|Miniatura obrazu

#### Nagłówek TIFF ####

8-bajtowy nagłówek pliku [TIFF](/pl/image/tiff/) zawiera następujące informacje:

`Bajty 0-1:` Kolejność bajtów używana w pliku. Dozwolone wartości to: „II” (4949.H) „MM” (4D4D.H).

W formacie „II” kolejność bajtów jest zawsze od najmniej znaczącego do najbardziej znaczącego bajtu, zarówno dla 16-bitowych, jak i 32-bitowych liczb całkowitych. Nazywa się to kolejnością bajtów little-endian. W formacie „MM” kolejność bajtów jest zawsze od najbardziej znaczącego do najmniej znaczącego, zarówno dla 16-bitowych, jak i 32-bitowych liczb całkowitych. Nazywa się to kolejnością bajtów big-endian.

`Bajty 2-3:` Dowolna, ale starannie wybrana liczba (42), która dodatkowo identyfikuje plik jako plik TIFF. Kolejność bajtów zależy od wartości Bajtów 0-1.

`Bajty 4-7:` Przesunięcie (w bajtach) pierwszego IFD. Katalog może znajdować się w dowolnym miejscu w pliku po nagłówku, ale musi zaczynać się na granicy słowa. W szczególności katalog plików obrazu może podążać za danymi obrazu, które opisuje. Czytelnicy muszą podążać za wskazówkami, dokąd mogą prowadzić. Termin przesunięcie bajtu jest zawsze używany w tym dokumencie w odniesieniu do lokalizacji względem początku pliku TIFF. Pierwszy bajt pliku ma przesunięcie równe 0.

#### Katalog plików obrazów ####

IFD zawiera informacje o obrazie, a także wskaźniki do rzeczywistych danych obrazu. Składa się z 2-bajtowej liczby wpisów w katalogu (tj. liczby pól), po której następuje sekwencja 12-bajtowych wpisów w polach , po którym następuje 4-bajtowe przesunięcie następnego IFD (lub 0, jeśli nie ma). Plik TIFF musi zawierać co najmniej 1 IFD, a każdy IFD musi zawierać co najmniej jeden wpis.

##### Wpis IFD #####

Każdy 12-bajtowy wpis IFD ma następujący format.


|Bajty|Opis
---|---|
|0-1|Znacznik identyfikujący pole
|2-3|Typ pola
|4-7|Liczba wskazanego typu
|8-11|Przesunięcie wartości, przesunięcie pliku (w bajtach) wartości pola. Oczekuje się, że wartość rozpocznie się na granicy słowa; odpowiednie przesunięcie wartości będzie zatem liczbą parzystą. To przesunięcie pliku może wskazywać dowolne miejsce w pliku, nawet po danych obrazu

Pole TIFF to jednostka logiczna składająca się ze znacznika TIFF i jego wartości. Ta koncepcja logiczna jest realizowana jako wpis IFD plus rzeczywista wartość, jeśli nie pasuje do części wartości/przesunięcia, ostatnich 4 bajtów wpisu IFD. Terminy pole TIFF i wpis IFD są stosowane zamiennie w większości kontekstów.

#### Miniatura ####

Format Exif zawiera miniaturę obrazu (z wyjątkiem Ricoh RDC-300Z). Zwykle znajduje się obok IFD1. Istnieją 3 formaty miniatur; Format JPEG (JPEG używa YCbCr), format RGB TIFF, format YCbCr TIFF.

##### Miniatura formatu JPEG #####

Jeśli wartość znacznika kompresji (0x0103) w IFD1 wynosi „6”, format obrazu miniatury to JPEG. Większość obrazów Exif używa formatu JPEG jako miniatury. W takim przypadku możesz uzyskać przesunięcie miniatury o znacznik JpegIFOffset (0x0201) w IFD1, rozmiar miniatury o znacznik JpegIFByteCount (0x0202). Format danych to zwykły format JPEG, zaczyna się od 0xFFD8 i kończy na 0xFFD9. Wygląda na to, że format JPEG i rozmiar 160x120 pikseli są zalecanymi formatami miniatur dla Exif2.1 lub nowszego.

##### Miniatura formatu TIFF #####

Jeśli wartość znacznika kompresji (0x0103) w IFD1 wynosi „1”, format obrazu miniatury jest bez kompresji (nazywany obrazem TIFF). Punktem początkowym danych miniatury jest Tag StripOffset(0x0111), rozmiar miniaturki to suma Tagu StripByteCounts(0x0117).

## Bibliografia ##

* [EXIF – z Wikipedii](https://en.wikipedia.org/wiki/Exif)
* [Format pliku EXIF] (https://www.media.mit.edu/pia/Research/deepview/exif.html)

