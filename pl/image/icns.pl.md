{
  "date" : "2021-06-29",
  "keywords" :["ICNS", "rozszerzenie", "plik", "format", "obraz", "Obraz ikony Apple", "macOS", "Apple", "Ikona"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - obraz ikony Apple",
  "description":"Poznaj format pliku ICNS i interfejsy API, które mogą tworzyć i otwierać pliki ICNS.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Czym jest plik ICNS? ##

Format ikon używany przez programy macOS nazywa się plikiem ICNS. Pozwala na 1-bitowe i 8-bitowe pasma alfa i zapisuje jeden lub więcej obrazów, zwykle wykonanych z dokumentów [PNG](/pl/image/png/). Ikona programu w przeglądarce i interfejsie macOS jest wyświetlana za pomocą plików ICNS.

W zależności od lokalizacji ta sama ikona stylu może mieć wiele ustawień. Format ICNS przeszedł liczne zmiany i ewoluował do tego stopnia, że może być obecnie używany jako podstawa dla różnych kompatybilnych formatów. Oto kilka innych ważnych punktów, o których musisz wiedzieć:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource i Mac OS icon Resource to tylko niektóre z innych nazw.
* W przypadku informacji o ikonach używane jest źródło w gałęzi zasobów.
* W większości przypadków plik zawiera wiele obrazów. Obsługiwane rozmiary obrazu to 1612 pikseli kwadratowych oraz 1024, 512, 256, 128, 48, 32 i 16 pikseli kwadratowych.


## Format pliku ICNS ##

Format danych ICNS to kapsułka na jeden lub więcej obrazów, obsługująca pasma 1-bitowe i liczne stany obrazu.
System operacyjny może zmienić rozmiar obrazów ikon, aby dopasować je do wymaganego rozmiaru wyświetlacza. Większe obrazy ikon są zwykle zapisywane jako pliki [JPEG](/pl/image/jpeg/) 2000 lub [PNG](/pl/image/png/). Możliwy jest typ zarówno skompresowanych, jak i nieskompresowanych plików ICNS.

Nagłówek i binarne dane ikony tworzą strukturę pliku ICNS. Nagłówek zawiera 8 bajtów danych, z których cztery to literał magiczny, a cztery to długość pliku. Typ i rozmiar każdego obrazu ikony są przechowywane w sekcji danych ikony, po której następują binarne dane obrazu. Rozmiar obrazu określa rozmiar sekcji binarnej.

## Specyfikacja techniczna ##

### Nagłówek ###

|Przesunięcie|Rozmiar|Cel
---|---|---|
|0|4|Magiczny literał, musi być "icns" (0x69, 0x63, 0x6e, 0x73)
|4|4|Długość pliku w bajtach, najpierw msb


### Dane ikony ###

|Przesunięcie|Rozmiar|Cel
---|---|---|
|0|4|Typ ikony
|4|4|Długość danych w bajtach (łącznie z typem i długością), najpierw msb
|8|Zmienna|Dane ikony

### Kompresja ###

Dane pikseli są do pewnego stopnia skompresowane. Piksele 32-bitowe („is32”, „il32”, „ih32”, „it32”) i ARGB („ic04”, „ic05”) są często kompresowane (na kanał) w podobny sposób jak PackBits.

|Wartość potencjalnego klienta|Bajty końcowe|Wynik (nieskompresowany)
---|---|---|
|0 - 127|1 - 128|1 - 128 bajtów
|128 - 255|1 bajt|3 - 130 kopii

## Odniesienie ##

* [ICNS – Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

