{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Skompresowane audio-wideo", "Plik", "Rozszerzenie", "Format pliku", "Kontener multimedialny", "XVid", "DivX", "Kodeki", "Resource Interchange File Format", "RIFF "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku AVI - plik z przeplotem audio-wideo",
  "description":"Poznaj format plików AVI i interfejsy API, które mogą tworzyć i otwierać pliki AVI.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## Co to jest plik AVI? ##

Format pliku **AVI** to format pliku multimedialnego kontenera audio-wideo, który został wprowadzony przez firmę Microsoft. Przechowuje dane audio i wideo utworzone i skompresowane przy użyciu kilku kodeków (koderów/dekoderów), takich jak **XVid** i **DivX**. Ponieważ różne kodeki mogą być używane do kodowania zawartości AVI, aplikacje pobierające, tj. odtwarzacze AVI, powinny być w stanie je otworzyć tylko wtedy, gdy mają zainstalowane wymagane kodeki, za pomocą których utworzono zawartość AVI. Format jest domyślnie obsługiwany na wszystkich platformach **Microsoft Windows**, a także na prawie wszystkich innych głównych platformach. Kilka aplikacji i interfejsów API umożliwia tworzenie/zapisywanie, odczytywanie i konwertowanie plików AVI do innych popularnych formatów, takich jak MP4, MOV, WMV itp.

## Format pliku AVI ##

Plik z rozszerzeniem .avi to plik AVI. Jest to podformat formatu Resource Interchange File Format (RIFF). RIFF organizuje dane w bloki lub „kawałki”, które są identyfikowane za pomocą znacznika FourCC. Plik AVI to po prostu jeden „fragment” pliku w formacie RIFF.

W pierwszej części nagłówek pliku jest identyfikowany przez znacznik „hdrl”; jego zawartość obejmuje szerokość, wysokość i liczbę klatek wideo. W drugiej porcji podrzędnej znacznik ruchu reprezentuje liczbę klatek na sekundę filmu. Wideo AVI składa się z rzeczywistych danych audio/wideo w tym fragmencie. Istnieje również trzeci opcjonalny podfragment ze znacznikiem „idx1”, który wskazuje pozycję w pliku poszczególnych fragmentów danych należących do pliku.

### Ograniczenia ###

* Informacje o współczynniku proporcji nie mogą być zakodowane w oryginalnej specyfikacji AVI, chociaż późniejsza specyfikacja OpenDML (AVI 2.0) oferuje znormalizowaną metodę
* Chociaż pliki AVI są szeroko stosowane w postprodukcji filmowej i telewizyjnej, różne podejścia do dodawania do nich kodu czasowego konkurują ze sobą, wpływając na użyteczność formatu.
* Plik wideo zakodowany w AVI nie może wykorzystywać techniki kompresji, która wymaga danych przyszłych klatek poza kodowaną klatką (ramka B)
* Problematyczne jest używanie plików AVI ze zmienną szybkością transmisji bitów (VBR) (takich jak dźwięk MP3 o częstotliwości próbkowania poniżej 32 kHz)
* Plik AVI kodujący filmy fabularne w standardowej rozdzielczości, jak zwykle używany, może wiązać się z narzutem około 5 MB na godzinę, w zależności od sposobu wykorzystania pliku
* Napisy muszą być zakodowane na stałe w strumieniu wideo lub dystrybuowane w osobnym pliku w przypadku, gdy pliki AVI nie mogą pomieścić załączników, takich jak czcionki i napisy

## Krótka historia ##

AVI został wprowadzony przez firmę Microsoft w 1992 roku w celu zapewnienia solidniejszego i bardziej zaawansowanego formatu plików audio i wideo. Format szybko stał się popularny w Internecie, umożliwiając użytkownikom udostępnianie plików wideo bezpośrednio i pośrednio za pośrednictwem pamięci masowej w chmurze.

## Bibliografia ##

* [AVI – z Wikipedii](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

