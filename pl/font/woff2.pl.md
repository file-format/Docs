{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Plik WOFF2 — plik w formacie Web Open Font 2.0",
  "description": "Dowiedz się, co to jest plik WOFF2 i interfejsy API, które mogą tworzyć i otwierać plik WOFF2.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-pl2"
}
},
  "lastmod": "2023-01-10"
}

## Co to jest plik WOFF2?

WOFF2 to format pliku czcionki będący bardziej skompresowaną wersją formatu Web Open Font Format (WOFF). Został opracowany jako sposób na zmniejszenie rozmiaru plików czcionek internetowych, umożliwiając ich szybsze ładowanie i zużywanie mniejszej przepustowości. WOFF2 wykorzystuje algorytm kompresji o nazwie Brotli do kompresji danych czcionek, co może skutkować rozmiarami plików znacznie mniejszymi niż równoważne czcionki [WOFF](/font/woff/). Ten format jest obsługiwany przez większość nowoczesnych przeglądarek internetowych, w tym Chrome, Firefox, Safari, Opera i Edge (wersja 14 i nowsze).

## Format pliku WOFF2 — więcej informacji

Wewnętrzna struktura pliku czcionki WOFF2 składa się z kilku różnych części, w tym nagłówka, metadanych, katalogu tabeli i samych danych czcionki.

 1. Nagłówek zawiera informacje o ogólnym formacie pliku, w tym numer wersji i liczbę tabel znajdujących się w pliku.

 1. Sekcja metadanych zawiera takie informacje, jak nazwa czcionki, prawa autorskie i inne informacje związane z czcionką.

 1. Katalog tabel zawiera informacje o różnych tabelach tworzących czcionkę, w tym o ich lokalizacji w pliku i długości.

 1. Same dane czcionki są podzielone na kilka różnych tabel, z których każda zawiera szczegółowe informacje o czcionce, takie jak jej znaki i odpowiadające im glify. Tabele te mogą obejmować:

 * Tabela glyf” zawiera rzeczywiste kontury czcionek, w tym kształt i rozmiar każdego znaku.
 * Tabela head” zawiera ogólne informacje o czcionce, takie jak numer wersji, rozmiar projektu i tak dalej.
 * Tabela hmtx” zawiera informacje o parametrach czcionki, w tym o szerokości i położeniu znaków.
 * Każda tabela jest kompresowana i zapisywana w formacie pliku WOFF2 po zakończeniu procesu kodowania.

Ogólna struktura została zaprojektowana tak, aby umożliwić szybkie analizowanie i dekodowanie, dzięki czemu przeglądarki internetowe mogą szybko i sprawnie ładować i wyświetlać czcionkę na stronie internetowej.

### Nagłówek WOFF2
Nagłówek WOFF zawiera podpis identyfikujący, który wskazuje rodzaj danych zawartych w pliku. Nagłówek WOFF wraz z jego polami wygląda następująco.

|Typ|Nazwa pola|Opis|
---|---|---|
|UInt32|podpis |0x774F4632 'wOF2' |
|UInt32| smak |Wersja sfnt czcionki wejściowej.|
|UInt32| długość |Całkowity rozmiar pliku WOFF.|
|UInt16| numTables |Liczba wpisów w katalogu tabel czcionek.|
|UInt16| zarezerwowane |Zarezerwowane; ustawiony na zero.|
|UInt32| totalSfntSize |Całkowity rozmiar wymagany dla nieskompresowanych danych czcionek, łącznie z nagłówkiem sfnt, katalogiem i tabelami czcionek (łącznie z dopełnieniem).|
|UInt32| totalCompressedSize Całkowita długość skompresowanego bloku danych.|
|UInt16| majorVersion |Główna wersja pliku WOFF.|
|UInt16| minorVersion |Mniejsza wersja pliku WOFF.|
|UInt32| metaOffset |Przesunięcie do bloku metadanych od początku pliku WOFF.|
|UInt32| metaLength |Długość skompresowanego bloku metadanych.|
|UInt32| metaOrigLength |Rozmiar nieskompresowanego bloku metadanych.|
|UInt32| privOffset |Przesunięcie do prywatnego bloku danych, od początku pliku WOFF.|
|UInt32| privLength |Długość prywatnego bloku danych.|


## Bibliografia
 * [Format pliku w3 WOFF2](https://www.w3.org/TR/WOFF2/)

