{
  "date" : "2019-10-11",
  "keywords" :[ "plik gif", "format pliku gif", "co to jest plik gif", "plik", "przykład gif", "rozszerzenie pliku gif", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Format Pliku Obrazu",
  "description":"Poznaj format plików GIF i interfejsy API, które mogą tworzyć i otwierać pliki GIF.",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest plik GIF? ##

GIF lub Graphical Interchange Format to rodzaj mocno skompresowanego obrazu. Należący do firmy Unisys format GIF wykorzystuje algorytm kompresji LZW, który nie obniża jakości obrazu. Dla każdego obrazu GIF zwykle dopuszcza do 8 bitów na piksel i do 256 kolorów w całym obrazie. W przeciwieństwie do obrazu [JPEG](/pl/image/jpeg/), który może wyświetlać do 16 milionów kolorów i dość dotyka granic ludzkiego oka. Kiedy pojawił się Internet, pliki GIF pozostawały najlepszym wyborem, ponieważ wymagały niskiej przepustowości i były kompatybilne z grafiką, która zużywa jednolite obszary koloru. Animowany GIF łączy wiele obrazów lub klatek w jeden plik i wyświetla je w sekwencji, aby wygenerować animowany klip lub krótki film. Ograniczenia kolorów wynoszą do 256 dla każdej klatki i prawdopodobnie będą najmniej odpowiednie do reprodukcji innych obrazów i fotografii z gradientem kolorów.

## Format pliku GIF ##

Koncepcyjnie pliki GIF mają obszar graficzny o stałym rozmiarze wypełniony zero lub więcej obrazów. Niektóre pliki GIF dzielą obszar graficzny lub bloki o stałym rozmiarze na podobrazy, które mogą funkcjonować jako animowane klatki w przypadku animowanego GIF-a. Format GIF wykorzystuje głębię pikseli od 1 do 8 bitów do przechowywania danych mapy bitowej. Model kolorów RGB i dane palety są zawsze używane do przechowywania obrazów. W zależności od wersji nagłówek o stałej długości („GIF87a” lub „GIF89a”) określa początek typowego pliku GIF.

Obecnie dostępne są dwie wersje GIF: 87a i 89a. Pierwszy to oryginalny format GIF, a drugi to nowy format GIF. W tym formacie pliku charakterystyka bloków i wymiary w pikselach są wymienione w deskryptorze ekranu logicznego o stałej długości. Istnienie i rozmiar globalnej tabeli kolorów można określić za pomocą deskryptora ekranu, który śledzi dalsze szczegóły, jeśli są obecne. Zwiastun to ostatni bajt pliku, który zawiera pojedynczy bajt średnika ASCII. Typowy układ pliku GIF87a jest następujący:

### Nagłówek ###

Nagłówek zawiera sześć bajtów i służy do określenia typu pliku jako GIF. Chociaż deskryptor ekranu logicznego jest oddzielony od rzeczywistego nagłówka, czasami jest uważany za drugi nagłówek. Ta sama struktura, która jest używana do przechowywania nagłówka, może przechowywać deskryptor ekranu logicznego. Wszystkie pliki GIF zaczynają się od 3-bajtowego podpisu i używają znaków „GIF” jako identyfikatora. Wersja ma również rozmiar trzech bajtów i deklaruje wersję pliku GIF.

### Logiczny deskryptor ekranu ###

Deskryptor obrazu o stałej długości określa ekran i informacje o kolorze niezbędne do utworzenia obrazu GIF. Pola Wysokość i Szerokość zawierają najmniejszą wartość rozdzielczości ekranu, niezbędną do wyświetlenia danych obrazu. Jeśli urządzenie wyświetlające nie jest w stanie wyświetlić określonej rozdzielczości, konieczne będzie skalowanie w celu odpowiedniego wyświetlenia obrazu. Informacje o ekranie i mapie kolorów są wyświetlane w czterech podpolach poniższej tabeli (przy czym bit 0 jest najmniej znaczącym bitem):


|Bity|Podpola
---|---|
|0-2|Rozmiar globalnej tabeli kolorów
|3|Flaga sortowania tabeli kolorów
|4-6|Rozdzielczość kolorów
|7|Globalna flaga tabeli kolorów

#### Globalna tabela kolorów ####

Opcjonalna globalna tabela kolorów jest umieszczana zaraz po logicznym deskryptorze ekranu. Ta tabela jest mapowana w celu indeksowania danych kolorów pikseli w danych obrazu. W przypadku braku globalnej tabeli kolorów każdy obraz w pliku GIF używa swojego koloru lokalnego. Lepiej jest podać domyślną tabelę kolorów, jeśli brakuje globalnej i lokalnej tabeli kolorów. Seria trzybajtowych trójek tworzy elementy tablicy kolorów. Każdy bajt charakteryzuje wartość koloru RGB. Kolory czerwony, zielony i niebieski są używane jako wartości każdego elementu tabeli kolorów. Wpisy w globalnej tabeli kolorów obejmują maksymalnie 256 wpisów i zawsze reprezentują potęgę dwójki.

#### Dane obrazu ####

Dane obrazu przechowują bajt niezakodowanych symboli, po których następuje połączona lista sub- wraz z danymi zakodowanymi w LZW.

#### Przyczepa ####

Trailer reprezentuje pojedynczy bajt danych, który jest ostatnim znakiem w pliku. Wartość tego bajtu wynosi na stałe 3Bh i określa koniec strumienia danych. Każdy plik GIF musi zawierać zwiastun na końcu każdego pliku.

## Bibliografia ##

* [Format pliku GIF](https://en.wikipedia.org/wiki/GIF)

