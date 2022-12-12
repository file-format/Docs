{
  "date" : "2019-10-11",
  "keywords" :[ "plik j2c", "format pliku j2c", "co to jest plik j2c", "plik", "przykład j2c", "rozszerzenie pliku j2c", "rozszerzenie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"Poznaj format pliku J2C i interfejsy API, które mogą tworzyć i otwierać pliki J2C.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## Czym jest plik J2C?

Plik z rozszerzeniem .j2c jest wariantem formatu pliku JPEG i jest kompresowany za pomocą kompresji falkowej. Ma niemal identyczny system znaczników i segmentów jak format pliku JPEG 2000. Format pliku J2C jest zdefiniowany w części 1 stanowiska JPEG 2000 i obsługuje zarówno kompresję stratną, jak i bezstratną. Strumień kodu JPEG 2000 został zaprojektowany do osadzenia w [JP2](/pl/image/jp2/) lub innym formacie pliku, chociaż może sam pojawić się w pliku. Plik J2C można otworzyć za pomocą programów Adobe Photoshop 2020, Adobe Illustrator 2020 i Corel Paintshop Pro.

## Format pliku J2C

Format pliku J2C jest taki sam jak JPEG 2000, który często jest zapisywany jako .jp2 i .jpc. To sprawia, że pliki J2C stosują to samo podejście do kodowania metadanych w formacie XML, w którym Standard 12234-1 jest używany jako odniesienie między tagami Exif a komponentami XML. Jest dodatkowo ulepszony przez rozszerzenie JPEG 2000 część 2, które łączy mechanizm animacji i konfiguracje strumienia kodu w jeden obraz. Pliki o rozszerzonym formacie są zapisywane jako [.jpx](/pl/image/jpx/).

### Układ pliku JPEG2000

JPEG2000 obsługuje różnorodne aplikacje w oparciu o zgodność z rozszerzalnymi formatami plików. Chociaż najprostszy typ może zawierać pojedynczy obraz, bardziej złożone typy mogą obejmować serię obrazów ułożonych jeden na drugim lub sekwencjonowanych na podstawie czasu.

#### Pudełko JP2
Jest to blok konstrukcyjny najwyższego poziomu formatu pliku JP2 i zawiera pola typu i długości w nagłówku oraz sekcję danych. Najbardziej godnym uwagi typem skrzynki jest ciągła skrzynka strumienia kodu. To pudełko przechowuje w swojej sekcji danych strumień kodu JPEG2000.

#### JPEG2000 CodeStream

JPEG2000 CodeStream to sekwencja bajtów wymagana do zdekodowania skompresowanego obrazu JPEG2000. W przypadku, gdy plik nie ma nic innego niż ten strumień kodu, nazywa się go surowym plikiem strumienia kodu. Zwykle strumień kodu JPEG to zastosowanie algorytmu kompresji JPEG2000 na obrazie, choć nie jest to jedyny sposób.

#### Części płytek ####

Obraz zakodowany w formacie JPEG2000 to zbiór jednostek danych zwanych pakietami. Pakiety te są utrzymywane w strumieniu kodu wewnątrz grup pakietów zwanych częściami kafelków. Przed zakodowaniem obrazu koder dzieli obraz na prostokątną siatkę bloków, zwaną kafelkami, gdzie każdy kafelek jest kodowany oddzielnie, niezależnie od innych kafelków.

{{< figure src="../JPEG2000_Codestream.png" alt="Format pliku JPEG2000" >}}

## Kompresja J2C
JPEG 2000 wykorzystuje technologię kompresji falkowej, dzięki czemu jest szybka w oparciu o fakt, że stosunkowo niewiele pikseli jest pokazywanych w dowolnej rzutni lub oknie, w którym przeglądarka wyświetla obraz. Można to podkreślić faktem, że w przypadku obrazów o bardzo dużym rozmiarze (w gigabajtach) na ekranie pojawi się tylko kilka megabajtów pikseli. Pomaga to w szybkim pobieraniu i renderowaniu tylko tej części danych obrazu, która jest wymagana do wypełnienia wyświetlanych pikseli. Wymaga to również szybkiej technologii dekompresji, aby przyspieszyć mechanizm pobierania obrazu w celu tworzenia wymaganych obrazów w locie.

J2C wykorzystuje szybką dekompresję i pobiera tylko niezbędne informacje dla danych pikselowych, aby szybko wyrenderować część widocznych obrazów na ekrany. J2C jest przeznaczony przede wszystkim do przeglądania danych, a nie ich edycji.

## Identyfikacja J2C
Pliki JPEG 2000 mają bajty sygnatury `FF 4F FF 51`.

### Typy mimów
Zarejestrowane typy MIME dla plików JPEG 2000 obejmują:
* obraz/j2c
* obraz/jpx
* obraz/jpm
* wideo/mj2

## Ulepszenia w stosunku do standardu JPEG
Ulepszenia w stosunku do standardu JPEG obejmują:
* Doskonała wydajność kompresji
* Reprezentacja wielu rozdzielczości
* Progresywna transmisja według pikseli i dokładności rozdzielczości
* Wybór bezstratnej lub stratnej kompresji
* Odporność na błędy, elastyczny format pliku
* Obsługa wysokiego zakresu dynamicznego
* Informacje przestrzenne kanału bocznego

## Bibliografia ##
* [Taubman, Dawid; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

