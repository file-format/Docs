{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku ZIM - Plik archiwum OpenZIM",
  "description":"Poznaj format pliku ZIM i interfejsy API, które mogą tworzyć i otwierać pliki ZIM.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Czym jest plik ZIM? ##

Pliki z rozszerzeniem .zim to archiwa utworzone w celu przechowywania treści Wiki w trybie offline. Jest uważany za najbardziej odpowiedni otwarty format pliku do przechowywania Wikipedii na USB. Przechowuje zawartość witryny w zwartym formacie. Jego nazwa pochodzi od „Zeno IMproved”, który był wcześniejszym formatem pliku Zeno. ZIM jest utrzymywany przez projekt [openZIM ](https://openzim.org/), który jest sponsorowany przez Wikimedia CH i wspierany przez Fundację Wikimedia. Pliki ZIM można otwierać za pomocą aplikacji takich jak Kiwix i ZIMReader. Projekt OpenZIM był gospodarzem implementacji formatu pliku ZIM na [Github](https://github.com/openzim) za wkład społeczności OpenSource.

## Specyfikacje formatu plików ZIM

Format pliku ZIM został opracowany na podstawie [formatu pliku Zeno](https://openzim.org/wiki/Zeno_file_format) i nie jest wstecznie kompatybilny. Specyfikacje formatu formatu plików ZIM są [dostępne online](https://openzim.org/wiki/ZIM_file_format) przez openZIM w celach informacyjnych dla programistów. OpenZIM dostarczył implementację open source C++, [LibZim](https://openzim.org/wiki/Zimlib), do odczytu i zapisu plików ZIM.

Format pliku ZIM wykorzystuje kompresję LZMA2, aby zawartość była zwarta.

{{< figure src="../ZIM_File_Format.jpeg" alt="Format pliku ZIM" >}}


### Nagłówek ZIM

Plik ZIM zaczyna się od nagłówka z przesunięciem 0. Wszystkie składniki są oparte na little-endian, a wszystkie liczby całkowite są liczbami całkowitymi bez znaku, tj. uint_16, uint_32, uint_64.

|Nazwa pola |Typ| Przesunięcie| Długość| Opis|
---|---|---|---|---|
|magiczna liczba| liczba całkowita| 0| 4| Magiczna liczba do rozpoznania formatu pliku musi być 72173914 (0x44D495A)|
|Wersja główna| liczba całkowita| 4| 2| Główna wersja formatu pliku ZIM (5 lub 6)|
|podrzędna wersja| liczba całkowita| 6| 2| Mniejsza wersja formatu pliku ZIM|
|uuid| liczba całkowita| 8| 16| unikalny identyfikator tego pliku zim|
|Liczba artykułów| liczba całkowita| 24| 4| całkowita liczba artykułów|
|liczba klastrów| liczba całkowita| 28| 4| całkowita liczba klastrów|
|Poz.urlPtr| liczba całkowita| 32| 8| pozycja listy wskaźników katalogu uporządkowana według adresu URL|
|tytułPtrPoz| liczba całkowita| 40| 8| pozycja listy wskaźników katalogów uporządkowana według tytułu|
|ClusterPtrPos| liczba całkowita| 48| 8| pozycja listy wskaźników klastra|
|mimeListPos| liczba całkowita| 56| 8| pozycja listy typów MIME (również rozmiar nagłówka)|
|strona główna| liczba całkowita| 64| 4| strona główna lub 0xffffffff, jeśli nie ma strony głównej|
|układ strony| liczba całkowita| 68| 4| strona układu lub 0xffffffffff, jeśli nie ma strony układu|
|Pozycja sumy kontrolnej| liczba całkowita| 72| 8| wskaźnik do sumy kontrolnej md5 tego pliku bez samej sumy kontrolnej. Wskazuje to zawsze 16 bajtów przed końcem pliku.|

## Bibliografia ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

