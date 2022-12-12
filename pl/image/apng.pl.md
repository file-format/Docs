{
  "date" : "2019-10-11",
  "keywords" :["plik apng", "format pliku apng", "co to jest plik apng", "plik", "przykład apng", "rozszerzenie pliku apng", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku APNG - animowany przenośny plik graficzny sieci",
  "description":"Poznaj format pliku APNG i interfejsy API, które mogą tworzyć i otwierać pliki APNG.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## Czym jest plik ANG?

Plik z rozszerzeniem .apng (Animowana przenośna grafika sieciowa) jest formatem grafiki rastrowej i jest nieoficjalnym rozszerzeniem przenośnej grafiki sieciowej ([PNG](/pl/image/png/) ). Składa się z wielu klatek (każda z obrazu PNG), które reprezentują sekwencję animacji. Daje to podobną wizualizację jak plik [GIF](/pl/image/gif/). Pliki APNG obsługują obrazy 24-bitowe i przezroczystość 8-bitową. APNG jest wstecznie kompatybilny z nieanimowanymi plikami GIF. Pliki APNG używają tego samego rozszerzenia .png i mogą być otwierane przez aplikacje takie jak Mozilla Firefox, Chrome z obsługą APNG, aplikacje iMessage na iOS 10.

## Krótka historia

* Specyfikacje APNG zostały stworzone w 2004 roku w celu zapewnienia obsługi animowanych obrazów PNG
* Dekodery APNG zostały opracowane ze znacznie mniejszymi rozmiarami i przy użyciu tylnej części dekodera PNG
* Po ciągłych obradach sformułowano nowy typ obrazu/apng typu MIME, zachowując takie samo rozszerzenie jak .png zamiast .apng
* APNG został oficjalnie odrzucony przez grupę PNG 20 kwietnia 2007 r. ze względu na jego jednolitość do obrazów PNG, a jednocześnie ma inne specyfikacje

## Format pliku APNG

Pliki APNG są przechowywane jako pliki binarne na dysku i wykorzystują rozszerzone specyfikacje PNG dla animowanych obrazów. Pierwsza ramka pliku APNG to normalny strumień PNG, który jest odczytywany przez dekodery PNG w celu wyświetlenia. Format pliku APNG jest zgodny ze specyfikacjami PNG, a dane są przechowywane w segmentach zwanych porcjami. Jednak APNG wprowadziło następujące nowe fragmenty:

`Animation Control Chunk (acTL)` — wskazuje, że ten plik jest animowanym plikiem PNG, a nie zwykłym plikiem PNG. Działa jako znacznik i znajduje się przed fragmentem IDAT. Zawiera również ilość klatek oraz informacje o czasach zapętlenia animacji

`Frame Control Chunk` - Pojawia się na początku każdej i zawiera informacje o metadanych, takie jak wymiary, pozycja, zastosowanie przezroczystości oraz informacje o zastąpieniu poprzedniej lub następnej klatki po jej zakończeniu.

`Frame Data Chunk` - Przechowuje zawartość ramki i zaczyna się od numeru sekwencyjnego. Ten numer sekwencyjny ma taką samą strukturę jak fragment IDAT obrazu domyślnego.

{{< figure src="../APNG.png" alt="Animowany plik PNG — format pliku APNG" >}}

APNG jest wstecznie kompatybilny z PNG, ponieważ specyfikacje boczne zostały zaprojektowane w taki sposób, że aplikacja czytająca plik PNG ma po prostu ignorować fragmenty, których nie rozumie. Specyfikacje dotyczące głębi bitowej, typu koloru, kompresji, filtrów, metod przeplotu i informacji o palecie są używane tak samo, jak w przypadku domyślnego formatu PNG.

## APNG kontra GIF

Ponieważ GIF jest już na miejscu i jest używany przez długi czas, możesz się zastanawiać, czym APNG różni się od GIF. Poniżej znajduje się zestaw porównań APNG i GIF, który daje krótkie wyobrażenie o obu formatach plików.

||APNG|GIF|
---|---|---|
|Opublikowano|2004|1987|
|Głębia koloru|24 bity|8 bitów|
|Liczba klatek|Nieograniczona|10 klatek na sekundę|
|Przejrzystość|Pełna i częściowa|Pełna|
|Kompresja|Bardzo dobra|Dobra|

## Bibliografia

* [Format pliku APNG](https://en.wikipedia.org/wiki/APNG)
* [Oficjalne specyfikacje formatu PNG](https://www.w3.org/TR/PNG/)

