{
  "date" : "2019-10-11",
  "keywords" :[ "plik bmp", "format pliku bmp", "co to jest plik bmp", "plik", "przykład bmp", "rozszerzenie pliku bmp", "rozszerzenie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Format Pliku Obrazu",
  "description":"Poznaj format pliku BMP i interfejsy API, które mogą tworzyć i otwierać pliki BMP.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# Co to jest plik BMP? #

Pliki z rozszerzeniem .BMP reprezentują pliki obrazów bitmapowych, które są używane do przechowywania cyfrowych obrazów bitmapowych. Te obrazy są niezależne od karty graficznej i są również nazywane formatem pliku mapy bitowej niezależnej od urządzenia (DIB). Ta niezależność służy otwieraniu pliku na wielu platformach, takich jak Microsoft Windows i Mac. Format pliku BMP może przechowywać dane jako dwuwymiarowe obrazy cyfrowe zarówno w formacie monochromatycznym, jak i kolorowym z różnymi głębiami kolorów.

## Specyfikacje formatu plików BMP ##

Mapy bitowe niezależne od urządzenia pomagają w wymianie map bitowych między urządzeniami i aplikacjami. Ze względu na ciągłą ewolucję tego formatu plików, informacje zawarte w nagłówkach mogą się różnić w zależności od wersji Bitmap. Pojedynczy plik mapy bitowej składa się ze struktur o stałym i zmiennym rozmiarze w określonej kolejności.

Struktury w pliku Bitmap są ułożone w następującej kolejności:


|Struktura|Opcjonalne|Rozmiar|Cel
---|---|---|---|
|Nagłówek pliku|Nie|14|Do przechowywania ogólnych informacji o pliku obrazu bitmapowego
|Nagłówek DIB|Nie|Stały rozmiar|Do przechowywania szczegółowych informacji o obrazie bitmapowym i definiowania formatu pikseli
|Dodatkowe maski bitowe|Tak|12 lub 16 bajtów|Aby zdefiniować format pikseli
|Paleta kolorów|Półopcjonalna|Rozmiar-zmienny|Aby zdefiniować kolory używane przez dane obrazu mapy bitowej
|Odstęp1|Tak|Rozmiar-zmienny|Wyrównanie struktury
|Macierz pikseli|Nie|Rozmiar-zmienny|Format pikseli jest zdefiniowany przez nagłówek DIB lub dodatkowe maski bitowe.
|Gap2|Tak|Rozmiar-zmienny|Wyrównanie struktury
|Profil kolorów ICC|Tak|Rozmiar-zmienny|Aby zdefiniować profil kolorów do zarządzania kolorami

Gdy obraz bitmapowy jest ładowany do pamięci, staje się strukturą DIB, używaną przez system Windows za pośrednictwem interfejsu API GDI. Nagłówek pliku nie jest częścią tej struktury danych. Kolor może również składać się z 16-bitowych wpisów, które stanowią indeksy aktualnie przywoływanej palety zamiast wyraźnych definicji kolorów RGB. Przyjrzyjmy się bliżej niektórym z nich, zwłaszcza nagłówkom.

### Nagłówek pliku mapy bitowej ###

Nagłówek pliku mapy bitowej jest podobny do innych nagłówków plików używanych do identyfikacji pliku. Ponieważ istnieją różne warianty formatu pliku BMP, pierwsze 2 bajty formatu pliku BMP to znak „B”, a następnie znak „M” w kodowaniu ASCII. Wszystkie wartości całkowite są przechowywane w formacie little-endian.

|Przesunięcie szesnastkowe|Odsunięcie dziesiętne|Rozmiar|Przeznaczenie
---|---|---|---|
|00|0|2 bajtów|Pole nagłówka używane do identyfikacji pliku BMP i DIB to 0x42 0x4D w systemie szesnastkowym, tak samo jak BM w ASCII. Może następować po możliwych wartościach.* **BM** – Windows 3.1x, 95, NT, ... itd. * **BA** – tablica map bitowych struktury OS/2 * **CI** – struktura OS/2 kolorowa ikona * **CP** – wskaźnik koloru stałego OS/2 * **IC** – ikona struktury OS/2 * **PT** – wskaźnik OS/2
|02|2|4 bajty|Rozmiar pliku BMP w bajtach
|06|6|2 bajty|Zarezerwowane; rzeczywista wartość zależy od aplikacji, która tworzy obraz
|08|8|2 bajty|Zarezerwowane; rzeczywista wartość zależy od aplikacji, która tworzy obraz
|0A|10|4 bajtów|Przesunięcie, tj. adres początkowy bajtu, w którym można znaleźć dane obrazu mapy bitowej (tablica pikseli).

#### Nagłówek DIB (nagłówek informacji o mapie bitowej) ####

Ten nagłówek zawiera szczegółowe informacje o obrazie. Na podstawie tych informacji zostanie ustalona aplikacja, która posłuży do wyświetlenia obrazu na ekranie. Wszystkie takie nagłówki zawierają pole DWORD (32-bitowe), określające ich rozmiar, dzięki czemu aplikacja może łatwo określić nagłówek użyty w obrazie. Wynika to głównie z faktu, że format DIB przeszedł kilka rozszerzeń. Poniżej znajduje się nagłówek DIB z wymienionymi polami.

#### Paleta kolorów ####

Paleta kolorów BMP to tablica struktur, które określają wartości intensywności RGB każdego koloru w palecie kolorów urządzenia wyświetlającego. Każdy piksel w danych mapy bitowej przechowuje pojedynczą wartość używaną jako indeks w palecie kolorów. Informacje o kolorze przechowywane w elemencie w tym indeksie określają kolor tego piksela. Dostępność kolorów w pliku mapy bitowej różni się w następujący sposób:

* Jedno, 4 i 8-bitowe — oczekuje się, że zawsze będą zawierać paletę kolorów
* Szesnaście, 24 i 32-bitowe — nigdy nie zawierają palet kolorów
* Szesnastobitowe i 32-bitowe pliki BMP - zawierają wartości masek pól bitowych zamiast palety kolorów

#### Przechowywanie pikseli ####

Piksele mapy bitowej są przechowywane jako bity upakowane w wierszach, gdzie rozmiar każdego wiersza jest zaokrąglany w górę do wielokrotności 4 bajtów (32-bitowy DWORD) przez dopełnienie. Całkowitej ilości bajtów wymaganych do przechowywania pikseli obrazu nie można bezpośrednio obliczyć, po prostu zliczając bity. Ponieważ w grę wchodzi dopełnienie, wymagany jest efekt zaokrąglenia rozmiaru każdego wiersza do wielokrotności 4 bajtów. Bajty dopełniające (niekoniecznie 0) należy dołączyć na końcu wierszy, aby długość wierszy była wielokrotnością czterech bajtów. Gdy tablica pikseli jest ładowana do pamięci, każdy wiersz musi zaczynać się od adresu pamięci, który jest wielokrotnością liczby 4.

Obraz jest faktycznie opisany przez 32-bitową reprezentację DWORD tablicy pikseli. Zwykle piksele są przechowywane „od dołu do góry”, zaczynając od lewego dolnego rogu, przechodząc od lewej do prawej, a następnie rząd po rzędzie od dołu do góry obrazu. Formaty pikseli i ich implikacje są wymienione poniżej:

* Format 1 bit na piksel (1bpp) obsługuje 2 różne kolory (na przykład: czarny i biały).
* Format 2-bitowy na piksel (2bpp) obsługuje 4 różne kolory i przechowuje 4 piksele na 1 bajt, przy czym piksel z lewej strony znajduje się w dwóch najbardziej znaczących bitach. Każda wartość piksela to 2-bitowy indeks w tablicy zawierającej maksymalnie 4 kolory.
* Format 4-bitowy na piksel (4bpp) obsługuje 16 różnych kolorów i przechowuje 2 piksele na 1 bajt, przy czym piksel z lewej strony jest bardziej znaczącym półbajtem. Każda wartość piksela jest 4-bitowym indeksem w tablicy zawierającej do 16 kolorów.
* Format 8 bitów na piksel (8bpp) obsługuje 256 różnych kolorów i przechowuje 1 piksel na 1 bajt. Każdy bajt jest indeksem w tablicy zawierającej do 256 kolorów.
* Format 16-bitowy na piksel (16bpp) obsługuje 65536 różnych kolorów i przechowuje 1 piksel na 2-bajtowe SŁOWO. Każde SŁOWO może definiować próbki alfa, czerwieni, zieleni i błękitu piksela.
* Format 24-bitowych pikseli (24bpp) obsługuje 16 777 216 różnych kolorów i przechowuje wartość 1 piksela na 3 bajty. Każda wartość piksela definiuje czerwone, zielone i niebieskie próbki piksela (8.8.8.0.0 w notacji RGBAX). W szczególności w kolejności: niebieski, zielony i czerwony (8 bitów na każdą próbkę).
* Format 32-bitowy na piksel (32bpp) obsługuje 4 294 967 296 różnych kolorów i przechowuje 1 piksel na 4-bajtowy DWORD. Każdy DWORD może definiować próbki alfa, czerwone, zielone i niebieskie piksela.

## Bibliografia ##

* [Format Windows MetaFile](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [Format pliku BMP](https://en.wikipedia.org/wiki/BMP_file_format)

