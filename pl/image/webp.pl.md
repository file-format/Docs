{
  "date" : "2019-10-11",
  "keywords" :["plik webp", "format pliku webp", "co to jest plik webp", "plik", "przykład webp", "rozszerzenie pliku webp","rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP — format pliku obrazu rastrowego Google",
  "description":"Poznaj format pliku WEBP i interfejsy API, które mogą tworzyć i otwierać pliki WEBP.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik WEBP?

WebP, wprowadzony przez Google, to nowoczesny format plików rastrowych obrazów internetowych oparty na bezstratnej i stratnej kompresji. Zapewnia taką samą jakość obrazu przy jednoczesnym znacznym zmniejszeniu rozmiaru obrazu. Ponieważ większość stron internetowych używa obrazów jako skutecznej reprezentacji danych, użycie obrazów WebP na stronach internetowych powoduje szybsze ładowanie stron internetowych. Według Google, bezstratne obrazy WebP są o 26% mniejsze w porównaniu z plikami [PNG](/pl/image/png/), podczas gdy obrazy stratne WebP są o 25-34% mniejsze niż porównywalne obrazy [JPEG](/pl/image/jpeg/). Obrazy są porównywane na podstawie indeksu podobieństwa strukturalnego (SSIM) między WebP a innymi formatami plików graficznych. WebP to siostrzany projekt formatu kontenera multimedialnego [WebM](https://en.wikipedia.org/wiki/WebM).

## Przegląd funkcji WebP ##

Obrazy WebP wykorzystują proces kompresji oparty na przewidywaniu pikseli z otaczających je bloków, w wyniku czego piksele są używane wielokrotnie w jednym pliku. Obsługuje animowane obrazy i oczekuje się, że w przyszłości będzie obsługiwał więcej funkcji. Firma Google udostępniła kod źródłowy [online](https://developers.google.com/speed/webp/download) swojego kodera i dekodera, aby można go było używać w razie potrzeby. Obraz WebP zapewnia obsługę:

* **Kompresja stratna:** Kompresja stratna jest oparta na kodowaniu klatek kluczowych [VP8](http://en.wikipedia.org/wiki/VP8). VP8 to format kompresji wideo stworzony przez On2 Technologies jako następca formatów VP6 i VP7.
* **Kompresja bezstratna:** Format kompresji bezstratnej został opracowany przez zespół WebP.
* **Przezroczystość:** 8-bitowy kanał alfa jest przydatny w przypadku obrazów graficznych. Kanał alfa może być używany razem ze stratnym RGB, funkcją, która nie jest obecnie dostępna w żadnym innym formacie.
* **Animacja:** Obsługuje animowane obrazy w prawdziwych kolorach.
* **Metadane:** Może zawierać metadane EXIF i XMP (używane na przykład przez aparaty fotograficzne).
* **Profil kolorów:** Może mieć osadzony profil ICC.

Stratna kompresja WebP wykorzystuje kodowanie predykcyjne do kodowania obrazu, tę samą metodę, która jest używana przez kodek wideo VP8 do kompresji klatek kluczowych w filmach. Kodowanie predykcyjne wykorzystuje wartości w sąsiednich blokach pikseli do przewidywania wartości w bloku, a następnie koduje tylko różnicę.

Bezstratna kompresja WebP wykorzystuje już widoczne fragmenty obrazu w celu dokładnej rekonstrukcji nowych pikseli. Może również użyć lokalnej palety, jeśli nie zostanie znalezione żadne interesujące dopasowanie.

## Format pliku ##

Format pliku WebP jest oparty na formacie dokumentu RIFF (format wymiany zasobów). Kontener WebP zapewnia obsługę dodatkowych funkcji niż zawieranie tylko pojedynczego obrazu zakodowanego jako klatka kluczowa VP8. Podstawowym elementem pliku RIFF jest fragment, który składa się z:


|Pole|Opis
---|---|
|Chunk FourCC: 32 bity|4-znakowy kod ASCII używany do identyfikacji porcji
|Rozmiar porcji: 32 bity (uint32)|Rozmiar porcji bez tego pola, identyfikatora porcji lub wypełnienia
|Ładunek fragmentu: Bajty rozmiaru fragmentu|Ładunek danych. Jeśli rozmiar fragmentu jest nieparzysty, dodawany jest pojedynczy bajt dopełnienia ~-~-, który powinien wynosić 0 ~-~-
|ChunkHeader („ABCD”)|Używany do opisania nagłówka FourCC i rozmiaru kawałka poszczególnych kawałków, gdzie „ABCD” to FourCC dla kawałka. Rozmiar tego elementu to 8 bajtów.

### Nagłówek WebP ###

Nagłówek pliku WebP wygląda następująco:

* Nagłówek RIFF - 32 bity reprezentujące znaki ASCII 'R' 'I' 'F' 'F'
* Rozmiar pliku - 32 bity (uint32) reprezentujące rozmiar pliku w bajtach począwszy od offsetu 8. Maksymalna wartość tego pola to 2^32 minus 10 bajtów, a więc rozmiar całego pliku to co najwyżej 4GiB minus 2 bajty .
* 'WEBP' - 32 bity reprezentujące znaki ASCII 'W' 'E' 'B' 'P'

### Stratny format pliku ###

Obrazy WebP używają stratnego formatu pliku, jeśli obraz jest oparty na kodowaniu stratnym i nie wymaga żadnych zaawansowanych/rozszerzonych funkcji, takich jak przezroczystość, animacja, alfa itp. Obrazy stratne są mniejsze i są również obsługiwane przez starsze aplikacje.

Plik WebP w tym przypadku składa się z:

* 12-bajtowy nagłówek pliku WebP
* Kawałek VP8

[Przewodnik po formatach i dekodowaniu danych VP8](https://tools.ietf.org/html/rfc6386) ilustruje specyfikacje formatu strumienia bitów VP8.

### Bezstratny format pliku ###

Ten układ jest używany, gdy obraz jest oparty na bezstratnym kodowaniu i nie ma potrzeby korzystania z zaawansowanych funkcji zapewnianych przez format zewnętrzny. Starsze aplikacje mogą jednak nie być w stanie odczytać takich plików.

Plik WebP w tym przypadku składa się z:

* 12-bajtowy nagłówek pliku WebP
* Kawałek VP8L

## Bibliografia ##

* [Informacje dla programistów WebP — od Google](https://developers.google.com/speed/webp/)
* [Format pliku WebP – według Wikipedii](https://en.wikipedia.org/wiki/WebP)

