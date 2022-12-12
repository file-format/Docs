{
  "date" : "2021-26-08",
  "keywords" :[ "plik dcr", "format pliku dcr", "co to jest plik dcr", "plik", "przykład dcr", "rozszerzenie pliku dcr", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCR — plik obrazu RAW z aparatu cyfrowego",
  "description":"Poznaj format plików DCR i interfejsy API, które mogą tworzyć i otwierać pliki DCR.",
  "linktitle" : "DCR",
  "menu" : {
    "docs" : {
      "identifier":"image-dcr",
      "parent" : "image"
}
},
  "lastmod" : "2021-26-08"
}

## Czym jest plik DCR? ##
Plik z rozszerzeniem dcr zawiera zawartość zdjęcia cyfrowego zapisanego w formacie Kodak Digital Camera RAW (DCR). DCR to skrót od **Digital Camera Raw**; zawiera nieskompresowaną i bezstratną wersję danych obrazu zarejestrowanych przez aparat cyfrowy Kodak. Profesjonalni fotografowie lubią używać tych plików, ponieważ przechowują obrazy w wyższej jakości niż skompresowane formaty obrazów o niskiej jakości.

## Format pliku DCR
DCR to zastrzeżony format opracowany przez Eastman Kodak Company; określany po prostu jako Kodak. Plik obrazu Digital Camera Raw (DCR) zawiera minimalnie przetworzone dane z przetwornika obrazu aparatu cyfrowego. Te pliki nie są jeszcze przetworzone i dlatego nie są gotowe do drukowania lub edytowania za pomocą edytora grafiki bitmapowej.
Zwykle konwerter RAW przetwarza obraz w szerokiej gamie wewnętrznej przestrzeni kolorów, w której można uzyskać dokładność i udoskonalenie przed konwersją do formatu pliku rastrowego, takiego jak TIFF lub JPEG, w celu przechowywania, drukowania lub dalszej obróbki.
### Zawartość pliku
Struktura surowych plików często jest zgodna z ogólnym wzorcem:
- Krótki nagłówek pliku, który zawiera wskaźnik kolejności bajtów w pliku.
- Metadane czujnika kamery, które są wymagane do interpretacji danych obrazu czujnika, w tym atrybuty CFA, rozmiar czujnika i jego profil kolorów.
- Metadane obrazu, które mogą być przydatne do włączenia do dowolnego środowiska CMS lub bazy danych. Niektóre pliki RAW zawierają znormalizowaną sekcję metadanych z danymi w formacie Exif.
- Miniatura obrazu.
- Pełnowymiarowa konwersja obrazu JPEG, która służy do podglądu pliku na panelu LCD aparatu.
- W przypadku skanów filmów kinowych, kod czasowy, kod klucza lub numer klatki w sekwencji pliku, który reprezentuje sekwencję klatek na zeskanowanej szpuli.
- Dane obrazu czujnika
### Dane obrazu czujnika
Plik RAW pełni w fotografii cyfrowej rolę podobną do kliszy fotograficznej w fotografii filmowej. Pliki RAW zawierają zatem dane w pełnej rozdzielczości odczytane z każdego piksela czujnika obrazu aparatu. Matryca aparatu jest niemal stale pokryta matrycą CFA (Color Filter Array). Może być używana do konwersji obrazowania o wysokim zakresie dynamicznym, gdy dostępne są dane w formacie surowym; jako prostsza alternatywa dla podejścia HDI z wieloma ekspozycjami polegającego na przechwytywaniu trzech oddzielnych obrazów.


## Bibliografia ##

* [Format obrazu surowego – według Wikipedii](https://en.wikipedia.org/wiki/Raw_image_format)
* [Co to jest plik DCR](https://expertphotography.com/dcr-file/)

