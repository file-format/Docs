{
  "date" : "2019-10-11",
  "keywords" :["plik j2k", "format pliku j2k", "co to jest plik j2k", "plik", "przykład j2k", "rozszerzenie pliku j2k","rozszerzenie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2K",
  "description":"Poznaj format pliku J2K i interfejsy API, które mogą tworzyć i otwierać pliki J2K.",
  "linktitle" : "J2K",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-03"
}

## Czym jest plik J2K?

Plik **J2K** to obraz skompresowany przy użyciu kompresji falkowej zamiast kompresji DCT. Ten format plików jest używany przez pliki Joint Photographic Experts Group (JPEG) 2000. Pliki J2K przechowują informacje o metadanych pliku obrazu w formacie XML, w przeciwieństwie do plików .jpeg lub .jpg, które używają do tego celu formatu EXIF. Pliki J2K obsługują 15-bitowy kolor, przezroczystość alfa i bezstratną kompresję. Istnieje kilka komercyjnych interfejsów API do dekodowania obrazów JPEG 2000, takich jak J2K-Codec. Plik J2K można otworzyć w systemie operacyjnym Windows przy użyciu standardowych przeglądarek obrazów.

## Format pliku J2K ##

Format pliku J2K jest taki sam jak JPEG 2000, który często jest zapisywany jako .jp2 i .jpc. To sprawia, że pliki J2K stosują to samo podejście do kodowania metadanych w formacie XML, w którym standard 12234-1 jest używany jako odniesienie między znacznikami Exif a komponentami XML. Jest dodatkowo ulepszony przez rozszerzenie JPEG 2000 część 2, które łączy mechanizm animacji i konfiguracje strumienia kodu w jeden obraz. Takie rozszerzone pliki formatu plików są zapisywane jako .jpx.

### Układ pliku JPEG2000 ###

JPEG2000 obsługuje różnorodne aplikacje w oparciu o zgodność z rozszerzalnymi formatami plików. Chociaż najprostszy typ może zawierać pojedynczy obraz, bardziej złożone typy mogą obejmować serię obrazów ułożonych jeden na drugim lub sekwencjonowanych na podstawie czasu.

#### Pudełko JP2 ####
Jest to blok konstrukcyjny najwyższego poziomu formatu pliku JP2 i zawiera pola typu i długości w nagłówku oraz sekcję danych. Najbardziej godnym uwagi typem skrzynki jest ciągła skrzynka strumienia kodu. To pudełko przechowuje w swojej sekcji danych strumień kodu JPEG2000.

#### JPEG2000 CodeStream ####

JPEG2000 CodeStream to sekwencja bajtów wymagana do zdekodowania skompresowanego obrazu JPEG2000. W przypadku, gdy plik nie ma nic innego niż ten strumień kodu, nazywa się go surowym plikiem strumienia kodu. Zwykle strumień kodu JPEG to zastosowanie algorytmu kompresji JPEG2000 na obrazie, choć nie jest to jedyny sposób.

#### Części płytek ####

Obraz zakodowany w formacie JPEG2000 to zbiór jednostek danych zwanych pakietami. Pakiety te są utrzymywane w strumieniu kodu wewnątrz grup pakietów zwanych częściami kafelków. Przed zakodowaniem obrazu koder dzieli obraz na prostokątną siatkę bloków, zwaną kafelkami, gdzie każdy kafelek jest kodowany oddzielnie, niezależnie od innych kafelków.

{{< figure src="../JPEG2000_Codestream.png" alt="Format pliku JPEG2000" >}}

## Kompresja J2K ##
JPEG 2000 wykorzystuje technologię kompresji falkowej, dzięki czemu jest szybka w oparciu o fakt, że stosunkowo niewiele pikseli jest pokazywanych w dowolnej rzutni lub oknie, w którym przeglądarka wyświetla obraz. Można to podkreślić faktem, że w przypadku obrazów o bardzo dużym rozmiarze (w gigabajtach) na ekranie pojawi się tylko kilka megabajtów pikseli. Pomaga to szybko pobrać i renderować tylko tę część danych obrazu, która jest wymagana do wypełnienia wyświetlanych pikseli. Wymaga to również szybkiej technologii dekompresji, aby przyspieszyć mechanizm pobierania obrazu w celu tworzenia wymaganych obrazów w locie.

J2K wykorzystuje szybką dekompresję i pobiera tylko niezbędne informacje dla danych pikselowych, aby szybko wyrenderować część widocznych obrazów na ekrany. J2K jest przeznaczony przede wszystkim do przeglądania danych, a nie ich edycji.

## Identyfikacja J2K ##
Pliki JPEG 2000 mają bajty podpisu 6A 50 20 20.

### Typy MIME ###
Zarejestrowane typy MIME dla plików JPEG 2000 obejmują:
* obraz/jp2
* obraz/jpx
* obraz/jpm
* wideo/mj2

## Ulepszenia w stosunku do standardu JPEG ##
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

