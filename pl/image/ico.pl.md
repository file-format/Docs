{
  "date" : "2019-10-11",
  "keywords" :[ "plik ico", "format pliku ico", "co to jest plik ico", "plik", "przykład ico", "rozszerzenie pliku ico", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Format Pliku Obrazu",
  "description":"Poznaj format plików ICO i interfejsy API, które mogą tworzyć i otwierać pliki ICO.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik IKO?

Pliki z rozszerzeniem ICO to typy plików graficznych używane jako ikony do reprezentacji aplikacji w [Microsoft Windows](https://www.microsoft.com/en-us/windows). Są one dostępne w różnych rozmiarach, obsługiwanych kolorach i rozdzielczościach, aby sprostać wymaganiom wyświetlacza. Innym podobnym formatem pliku obrazu w systemie Microsoft Windows jest [CUR](/pl/image/cur/) do reprezentacji kursora i definiuje punkt aktywny w nagłówku obrazu. W systemie MacOS formaty plików ICNS służą temu samemu celowi, co pliki ICO. Kilka witryn internetowych i aplikacji udostępnia funkcję tworzenia takich plików i konwertowania innych formatów obrazów, takich jak [BMP](/pl/image/bmp/), [PNG](/pl/image/png/) itp. do formatu pliku ikony. Oficjalnym typem nośnika internetowego zarejestrowanym przez IANA dla plików ICO jest image/vnd.microsoft.icon.

## Krótka historia ##

Ikony zostały wprowadzone wraz z uruchomieniem systemu Microsoft Windows 1.0. Były to 32x32 w rozmiarze i były monochromatyczne. Wraz z pojawieniem się win32 wprowadzono obsługę obrazów ikon w prawdziwych kolorach o wymiarach do 256x256 pikseli. Windows XP jako pierwszy zapewnił obsługę 32-bitowych kolorowych obrazów ikon, umożliwiając dodanie do ikony półprzezroczystych obszarów, takich jak cienie, antyaliasing i efekty przypominające szkło. Microsoft zalecał tylko rozmiary ikon do 48 × 48 pikseli dla systemu Windows XP. System Windows Vista dodał widok ikon o wymiarach 256 × 256 pikseli do Eksploratora Windows, a także obsługę skompresowanego formatu [PNG](/pl/ image / png /). W przypadku użytkowników korzystających z wyższych rozdzielczości i trybów wysokiej rozdzielczości DPI zalecane są większe formaty ikon (takie jak 256×256).

## Format pliku ICO ##

Pojedynczy plik ICO składa się z jednego lub więcej małych obrazów o wielu rozmiarach i głębi kolorów. Obecność obrazów o wielu rozmiarach służy do odpowiedniego skalowania przy różnych rozdzielczościach ekranu. Wszystkie wartości w plikach ICO/CUR są reprezentowane w kolejności bajtów [little-endian](https://en.wikipedia.org/wiki/Little-endian).

Plik ICO składa się z nagłówka ikony, katalogu ikon,

|Pole|Opis
---|---|
|Nagłówek ikony|Przechowuje ogólne informacje o pliku ICO.
|Katalog[1..n]|Przechowuje ogólne informacje o każdym obrazie w pliku.
|Ikona #1|Rzeczywiste „dane” pierwszego obrazu w starym formacie AND/XOR DIB lub nowszym PNG
|...|
|Ikona #n|Dane dla ostatniego obrazu ikony

### Nagłówek ###

|Przesunięcie|Rozmiar (w bajtach)|Cel
---|---|---|
|0|2|Zarezerwowane. Zawsze musi być 0.
|2|2|Określa typ obrazu: 1 dla obrazu ikony (.ICO), 2 dla obrazu kursora (.CUR). Inne wartości są nieprawidłowe.
|4|2|Określa liczbę obrazów w pliku.

### Katalog ###

Katalog zawarty w pliku ICO, reprezentowany jako struktura ICONDIR, zawiera strukturę ICONDIRECTORY dla każdego obrazu w pliku. Po tym samym następuje ciągły blok wszystkich danych mapy bitowej obrazu. Jest to jak pokazano poniżej.

|Przesunięcie|Rozmiar|Opis
---|---|---|
|0 (0)|1|Szerokość, powinna wynosić 0, jeśli 256 pikseli
|1 (1)|1|Wysokość, powinna wynosić 0, jeśli 256 pikseli
|2 (2)|1|Liczba kolorów powinna wynosić 0, jeśli więcej niż 256 kolorów
|3 (3)|1|Zarezerwowane, powinno być 0
|4 (4)|2|Płaszczyzny kolorów w formacie .ICO powinny mieć wartość 0 lub 1 lub punkt aktywny X w formacie .CUR
|6 (6)|2|Bity na piksel w formacie .ICO lub hotspot Y w formacie .CUR
|8 (8)|4|Rozmiar danych mapy bitowej w bajtach.
|12 (C)|4|Przesunięcie w pliku.

## Bibliografia ##

* [ICO – przez Wikipedię](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

