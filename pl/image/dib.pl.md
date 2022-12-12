{
  "date" : "2020-01-10",
  "keywords" :[ "plik dib", "format pliku dib", "co to jest plik dib", "plik", "przykład dib", "rozszerzenie pliku dib", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"Poznaj format pliku DIB i interfejsy API, które mogą tworzyć i otwierać pliki DIB.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Czym jest plik DIB?

Bitmapa niezależna od urządzenia (DIB) to plik obrazu rastrowego o strukturze podobnej do standardowych plików bitmap ([BMP]()/image/bmp/)). Zawiera tabelę kolorów opisującą odwzorowanie kolorów RGB na wartości pikseli. Dzięki temu DIB może reprezentować obraz na dowolnym urządzeniu. Można go otworzyć za pomocą prawie wszystkich aplikacji, które mogą otworzyć standardowy plik BMP w systemie Windows i macOS. DIB to pliki binarne i mają złożony format pliku podobny do BMP. Obrazy DIB są niezależne od możliwości wyjściowych urządzeń renderujących pod względem głębi kolorów i liczby pikseli na cal.

## Specyfikacje formatu plików DIB ##
DIB zawiera następujące informacje o kolorze i wymiarze:

* Format kolorów urządzenia, na którym utworzono prostokątny obraz.
* Rozdzielczość urządzenia, na którym utworzono prostokątny obraz.
* Paleta dla urządzenia, na którym utworzono obraz.
* Tablica bitów, która odwzorowuje trójki czerwonego, zielonego, niebieskiego (RGB) na piksele w prostokątnym obrazie.
* Identyfikator kompresji danych, który wskazuje schemat kompresji danych (jeśli istnieje) używany do zmniejszania rozmiaru tablicy bitów.

### Format bloku danych DIB ###

DIB pojawia się w kontekście bloku pamięci w porównaniu z plikami .DIB przechowywanymi na dysku. Blok pamięci ma strukturę zgodną ze specyfikacjami Windows API dla DIB. Rzeczywisty DIB składa się z:
* Nagłówek
* Paleta kolorów
* Dane pikseli

W praktyce praca z danymi palety, nagłówka i obrazu odbywa się tak, jakby były trzema oddzielnymi blokami pamięci. Uchwyt do tego wspólnego bloku pamięci jest przypisywany za pomocą GlobalAlloc i jest znany jako HDIB, który jest używany do wyodrębniania i pracy z danymi nagłówka, tabeli kolorów i pikseli.

### Struktury ###
Informacje zawarte w DIB są reprezentowane przez różne struktury. Obejmują one:

BITMAPInfo — definiuje informacje o wymiarze i kolorze dla DIB
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Składa się z BITMAPINFHEADERA:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
po których następują dwie lub więcej struktur RGBQAD.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Bity danych ###
|Bity|Opis|
---|---|
|Format 1-bitowy (monochromatyczny)|Monochromatyczne mapy bitowe składają się z dwóch kolorów (czarnego i białego). Z powodu tej ograniczonej liczby kolorów mapy bitowe zajmują mniej miejsca na dysku. BitBitCount zwraca true lub false dla reprezentacji obu kolorów. Większość aplikacji całkowicie pomija paletę, jeśli bitBitCount==1.
|4-bitowy format (VGA lub 16 kolorów)|Każdy bajt danych obrazu reprezentuje dwa piksele i bitBitCount==4. Bity te reprezentują kolor piksela w porządku malejącym.
|Format 8-bitowy (256 kolorów)|Ten 8-bitowy format może reprezentować maksymalnie 256 kolorów. Każdy bajt w tablicy danych mapy bitowej obrazu reprezentuje pojedynczy piksel. Wartością tego bajtu jest numer wpisu palety kolorów spośród 256 wpisów reprezentowanych przez bmciColors.
|Format 24-bitowy (TrueColor)|Te mapy bitowe mogą mieć maksymalnie 2^24 kolorów (biBitCount == 24). Każda trzybajtowa sekwencja w tablicy danych mapy bitowej reprezentuje względne intensywności trzech podstawowych barw piksela. Odcienie są opisane jako wartości z zakresu od 0 do 255 i są przechowywane w trzech bajtach w kolejności niebieski, zielony i czerwony. To ważne rozróżnienie, ponieważ większość odniesień do kolorów w systemie Windows używa odwrotnej kolejności: czerwony/zielony/niebieski, więc podczas pracy z obrazami TrueColor należy myśleć o „BGR” zamiast „RGB”. Można określić paletę kolorów, aby przyspieszyć proces rysowania w systemie Windows, w którym to przypadku biClrUsed nie będzie równe 0. Ale jak widać, nie jest to potrzebne, ponieważ same dane piksela zawierają informacje o kolorze.
|32-bitowy format|32-bitowe obrazy mają maksymalnie 2^24 kolorów (biBitCount == 24).

## Bibliografia ##
* [Mapy bitowe niezależne od urządzenia — firma Microsoft](https://docs.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

