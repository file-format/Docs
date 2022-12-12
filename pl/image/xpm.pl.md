{
  "date" : "2019-10-11",
  "keywords" :[ "plik xpm", "format pliku xpm", "co to jest plik xpm", "plik", "przykład xpm", "rozszerzenie pliku xpm", "rozszerzenie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - Format pliku X PixMap",
  "description":"Poznaj format pliku XPM i interfejsy API, które mogą tworzyć i otwierać pliki XPM.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik XPM?

Plik z rozszerzeniem .xpm to format pliku obrazu używany przez system X Windows. Obsługuje przezroczyste piksele i zwykle celuje w tworzenie piksmap ikon. Obsługuje dane monochromatyczne, w skali gra i kolorowe pixmapy. Zostały one zaprojektowane tak, aby można je było edytować ręcznie i można je było uwzględnić w kodzie [C](/pl/programming/c/). W tym celu pliki XPM są w formacie zwykłego pliku tekstowego i są zgodne ze składnią języka programowania C. Pliki XPM można otwierać za pomocą różnych aplikacji do przeglądania obrazów, takich jak
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView i Canvas X.

## Format pliku XPM

Format pliku XPM wykorzystuje składnię C, aby można je było zintegrować z programami C i C++. Składa się z następujących sześciu różnych sekcji.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

Sekcje są w rzeczywistości tablicą ciągów znaków w następujący sposób.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Poniżej znajdują się szczegóły każdej sekcji.

`<Values> ` — Ta sekcja jest łańcuchem znaków zawierającym cztery lub sześć liczb całkowitych o podstawie 10 i odpowiadających:

* szerokość i wysokość pixmapy
* liczba kolorów
* liczba znaków na piksel
* opcjonalne współrzędne punktu aktywnego i znacznik XPMEXT

`<Colors> ` - Ta sekcja zawiera tyle ciągów znaków, ile jest kolorów. Każdy ciąg jest następujący:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Ta sekcja składa się z<height> struny i<width> \*<chars_per_pixel> postacie. Każdy<chars_per_pixel> łańcuch długości powinien być jedną z wcześniej zdefiniowanych grup w pliku<Colors> Sekcja.

`<Extension> ` - Sekcja rozszerzenia musi być oznaczona etykietą, jeśli nie jest pusta, w pliku<Values> Sekcja. Może składać się z kilku<Extension> podrozdziały, które mogą być dwojakiego rodzaju:

* jeden samodzielny ciąg złożony w następujący sposób: XPMEXT<extension-name><extension-data>
* lub blok składający się z kilku łańcuchów:XPMEXT<extension-name><related extension-data composed of several strings>

## Bibliografia

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [Podręcznik XPM](http://www.xfree86.org/current/xpm.pdf)

