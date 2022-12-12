{
  "date" : "2019-10-11",
  "keywords" :["plik tga", "format pliku tga", "co to jest plik tga", "plik", "przykład tga", "rozszerzenie pliku tga", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku TGA - plik obrazu graficznego TARGA",
  "description":"Poznaj format plików TGA i interfejsy API, które mogą tworzyć i otwierać pliki TGA.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik TGA?

Plik z rozszerzeniem .tga jest formatem grafiki rastrowej i został stworzony przez firmę Truevision Inc. Został zaprojektowany dla płyt TARGA (Truevision Advanced Raster Adapter) i zapewniał obsługę wyświetlania Highcolor/truecolor dla komputerów PC zgodnych z IBM. Obsługuje 8, 16, 24 i 32 bity na piksel oraz 8-bitowy kanał alfa. Obsługuje również bezstratną kompresję RLE, którą można zastosować w celu zmniejszenia rozmiaru obrazu. Cyfrowe zdjęcia i tekstury używają formatu obrazu TGA.

## Krótka historia

Formacja formatu plików TGA powstała w 1984 roku przez AT&T EPICenter (później wyodrębniony i utworzony jako niezależny podmiot znany jako Truevision), który pracował nad marketingiem nowych technologii opracowanych przez AT&T dla buforów ramek kolorów. EPICenter pracował już nad dwiema pierwszymi kartami, VDA (Video Display Adapter) i ICB (płyta do przechwytywania obrazu), dla których prace nad dwoma typami plików, .vda i .icb, były już w toku. Te formaty plików zostały skodyfikowane i wprowadzono mniej szeroki specyficzny format plików TGA. TGA było rozszerzeniem tego, co było już w użyciu, i dostarczało informacji, takich jak szerokość, wysokość, głębokość pikseli, powiązana mapa kolorów i pochodzenie obrazu.

Wersja 2.0 TGA, opublikowana w 1989 roku, zawierała kilka ulepszonych funkcji, takich jak:

* Miniatury
* Kanał alfa
* Wartość Gamma
* Metadane tekstowe

Głównymi współtwórcami wersji TGA 2.0 są Shawn Steiner z Truevision, Kevin Fiedly i David Spoelstra.

## Specyfikacje formatu plików TGA TARGA

Plik TGA składa się z 2 głównych części:

* Nagłówek
* Informacje o pikselach kolorów

Wszystkie wartości w pliku TGA są podane w littl-endian zgodnie ze specyfikacją formatu.

### Nagłówek TGA

Nagłówek pliku TGA składa się z następujących 5 pól.

|Nr pola|Długość |Nazwa pola |Opis|
---|---|---|---|
|1| 1 bajt |Długość identyfikatora| Długość pola ID obrazu (0-255)|
|2| 1 bajt |Typ mapy kolorów| Czy mapa kolorów jest dołączona (0 — wskazuje, że do tego obrazu nie dołączono danych mapy kolorów. 1 — wskazuje, że do tego obrazu dołączono mapę kolorów.)|
|3| 1 bajt |Typ obrazu| Typy kompresji i kolorów (0- Brak danych obrazu. 1- Nieskompresowany, obraz z mapą kolorów, 2- Nieskompresowany, obraz True Color, 9- Zakodowany obraz w pełnej długości, obraz z mapą kolorów, 11- Zakodowany w pełnej długości, obraz czarno-biały )|
|4| 5 bajtów |Specyfikacja mapy kolorów| Opisuje mapę kolorów|
|5| 10 bajtów |Specyfikacja obrazu| Wymiary i format obrazu|

### Dane obrazu i mapy kolorów

|Nr pola |Długość |Pole |Opis|
---|---|---|---|
|6 |Z pola długości identyfikatora obrazu| Identyfikator obrazu| Opcjonalne pole zawierające informacje identyfikujące|
|7 |Z pola specyfikacji mapy kolorów| Dane mapy kolorów| Tabela przeglądowa zawierająca dane mapy kolorów|
|8 |Z pola specyfikacji obrazu| Dane obrazu| Przechowywane zgodnie z deskryptorem obrazu|

### Strefa programisty (opcjonalnie)

TGA w wersji 2.0 zapewnia obsługę dodatkowych ulepszeń/dodatków, które wielu programistów chciało przechowywać więcej informacji. Informacja jest opcjonalna, więc jeśli dekoder TGA nie jest w stanie jej zinterpretować, zostanie zignorowana.

### Obszar rozszerzenia (opcjonalnie)

|Nr pola| Długość| Pole |Opis|
---|---|---|---|
|10| 2 bajty |Rozmiar rozszerzenia |Rozmiar w bajtach obszaru rozszerzenia, zawsze 495|
|11| 41 bajtów| Nazwisko autora | Nazwisko autora. Jeśli nie jest używany, bajty powinny być ustawione na NULL (\0) lub spacje|
|12| 324 bajty| Komentarz autora| Komentarz, zorganizowany w cztery wiersze, każdy składający się z 80 znaków plus NULL|
|13| 12 bajtów| Znacznik daty/godziny |Data i godzina utworzenia obrazu|
|14| 41 bajtów| Identyfikator zadania||
|15| 6 bajtów| Czas pracy| Godziny, minuty i sekundy spędzone na tworzeniu pliku (do rozliczeń itp.)|
|16| 41 bajtów| Identyfikator oprogramowania |Aplikacja, która utworzyła plik.|
|17| 3 bajty| Wersja oprogramowania||
|18| 4 bajty| Kluczowy kolor||
|19| 4 bajty| Współczynnik proporcji pikseli||
|20| 4 bajty| Wartość gamma||
|21| 4 bajty| Przesunięcie korekcji kolorów |Liczba bajtów od początku pliku do tabeli korekcji kolorów, jeśli jest obecna|
|22| 4 bajty| Znaczek pocztowy | Liczba bajtów od początku pliku do obrazu znaczka pocztowego, jeśli istnieje|
|23| 4 bajty| Przesunięcie linii skanowania| Liczba bajtów od początku pliku do tabeli linii skanowania, jeśli jest obecna|
|24| 1 bajt| Typ atrybutów| Określa kanał alfa|

### Stopka pliku (opcjonalnie)

Ostatnie 26 bajtów pliku reprezentuje stopkę, która, jeśli jest obecna, oznacza, że prawdopodobnie jest to plik TGA w wersji 2.

|Nr pola| Długość| Pole| Opis|
---|---|---|---|
|28| 4 bajty| Przesunięcie przedłużenia| Przesunięcie w bajtach od początku pliku|
|29| 4 bajty| Przesunięcie obszaru deweloperskiego| Przesunięcie w bajtach od początku pliku|
|30| 16 bajtów| Podpis| Zawiera "TRUEVISION-XFILE"|
|31| 1 bajt| | Zawiera "."|
|32| 1 bajt| | Zawiera NULL|


## Bibliografia

* [Specyfikacje formatu plików TGA 2.0](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [TGA z Wikipedii](https://en.wikipedia.org/wiki/Truevision_TGA)

