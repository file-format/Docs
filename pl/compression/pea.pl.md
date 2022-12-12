{
  "date" : "2021-04-21",
  "keywords" :["plik grochu", "format pliku groszku", "co to jest plik groszku", "plik", "przykład grochu", "rozszerzenie pliku groszku","rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - format pliku archiwum PeaZip",
  "description":"Poznaj format pliku PEA i interfejsy API, które mogą tworzyć i otwierać pliki PEA.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## Czym jest plik PEA?

Plik z rozszerzeniem .pea, akronimem słów Pack, Encrypt i Authenticate, to archiwum [zip](/pl/compression/zip/) utworzone za pomocą oprogramowania do archiwizacji [PeaZip](https://peazip.github.io/). Oferuje kompresję i wiele woluminów wyjściowych oraz oferuje elastyczny model bezpieczeństwa dzięki uwierzytelnionemu szyfrowaniu i kryptografii. Zapewnia to zarówno prywatność, jak i uwierzytelnianie danych. Narzędzie PeaZip jest dostępne jako silnik typu open source, który można skompilować dla różnych systemów operacyjnych zgodnie z wymaganiami.

## Format pliku PEA

[Specyfikacje formatu plików PEA](https://peazip.github.io/pea_help.pdf) są publicznie dostępne w celach informacyjnych dla programistów. Archiwa PEA to pliki binarne z elastycznym modelem bezpieczeństwa i redundantnymi kontrolami integralności, od sum kontrolnych po silne kryptograficznie skróty. Definiuje to trzy różne poziomy komunikacji do sterowania:

* Strumienie — rzeczywisty strumień danych wyjściowych, który składa się z wielu plików wejściowych i może być zapisywany w wielu woluminach wyjściowych
* Obiekty - pliki wejściowe i foldery wysyłane do archiwum .pea
* Woluminy - wyjściowy plik archiwum, który można rozciągnąć do rozmiaru zdefiniowanego przez użytkownika

Każdy z nich jest opcjonalny i można go włączyć zgodnie z wymaganiami użytkownika. Format pliku PEA może przechowywać pojedynczy strumień zawierający nieograniczoną liczbę obiektów. Każdy strumień ma rozmiar do 2^64 bajtów.

Pliki PEA oferują opcjonalną kontrolę integralności i uwierzytelnione szyfrowanie przy użyciu AES w trybie EAX lub HMAC, alternatywnie Twofish i Serpent w trybie EAX.

### Nagłówek archiwum PEA

Nagłówek archiwum ma 10 bajtów i ma następującą strukturę.

|Bajty|Opis|
---|---|
|1 | Magiczne pole bajtów do ujednoznaczniania formatu pliku: $EA|
|1 | Numer wersji|
|1 | Numer wersji|
|1 | Schemat regulacji głośności|
|1 | Deklarowanie systemu operacyjnego, w którym zbudowano strumień|
|1 | Deklarowanie kodowania daty i godziny systemu operacyjnego|
|1 | Deklarowanie kodowania znaków nazw obiektów|
|1 | Deklaracja typu procesora (zakodowana w 7 bitach) i endianizmu (w msb)|
|1 | Zarezerwowane do wykorzystania w przyszłości|

## Bibliografia

* [Specyfikacje formatu pliku PEA] (https://peazip.github.io/pea_help.pdf)
* [Format pliku PEA](https://peazip.github.io/pea-file-format.html#.pea_specifications)

