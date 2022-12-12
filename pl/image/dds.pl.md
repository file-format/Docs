{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku DDS — plik obrazu powierzchni DirectDraw",
  "description":"Poznaj format plików DDS i interfejsy API, które mogą tworzyć i otwierać pliki DDS.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## Czym jest plik DDS?

Plik DDS to plik obrazu rastrowego, który wykorzystuje format kontenera DirectDraw Surface (DDS). Przechowuje nieskompresowane i skompresowane (DXTn) tekstury oraz implementuje różne typy do przechowywania różnych typów danych. Obsługuje również kilka różnych typów danych, takich jak tekstury jednowarstwowe, tekstury z mipmapami, mapy kostek, mapy objętości i tablice tekstur. Dzięki temu pliki DDS mogą przechowywać modele jednostek tekstur gier wideo oprócz zdjęć cyfrowych i tła pulpitu systemu Windows. Format pliku DDS został opracowany przez firmę Microsoft do użytku z DirectX SDK.

## Format pliku DDS

Pliki DDS są zapisywane jako pliki binarne i mogą być używane z DirectX SDK. Wykorzystuje moc DirectX do tworzenia aplikacji do renderowania w czasie rzeczywistym, takich jak gry 3D.

### Układ pliku DDS

[Układ pliku DDS](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) został szczegółowo udokumentowany przez firmę Microsoft. Binarny plik DDS zawiera następujące informacje.

* DWORD (liczba magiczna) zawierająca czteroznakową wartość kodu „DDS” (0x20534444).
* Opis danych w pliku.

DDS_HEADER opisuje dane, a DDS_PIXELFORMAT opisuje format pikseli. Oba zastępują przestarzałe struktury DDSURFACEDESC2, DDSCAPS2 i DDPIXELFORMAT DirectDraw 7.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[Przewodnik po programowaniu formatu plików DDS](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) zawiera szczegółowe informacje techniczne dotyczące tego formatu plików.

## Bibliografia

* [DDS – z Wikipedii](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [Podręcznik techniczny formatu plików ZSoft PCX](http://qzx.com/pc-gpe/pcx.txt)

