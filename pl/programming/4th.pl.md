
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"4. plik - format pliku w czwartym języku",
  "description":"Dowiedz się, co to jest format pliku .4, z przykładami i interfejsami API, które umożliwiają tworzenie i otwieranie plików 4..",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Co to jest czwarty plik?

Plik z rozszerzeniem .4. jest plikiem programistycznym stworzonym dla **Forth Programming Language**. Zawiera kod źródłowy programów napisanych w języku programowania Forth i generuje dane wyjściowe podczas wykonywania programu. Jest to po prostu kolejny plik języka programowania podobny do pliku źródłowego [C](/pl/programming/c/) i [C++](/pl/programming/cpp/).

## Czwarty format pliku — więcej informacji


### Przykładowy kod czwartego języka programowania

Oto przykład prostego programu napisanego w Forth, który oblicza silnię danej liczby:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

W tym przykładzie słowo silnia przyjmuje pojedynczy argument n i zwraca jego silnię. Słowo dup duplikuje wartość na wierzchu stosu, drop odrzuca wartość na wierzchu stosu, a * mnoży dwie wartości na wierzchu stosu. Konstrukcje if i Begin/until kontrolują przebieg programu.

Aby skorzystać z tego programu, należy wprowadzić definicję do interpretera Forth, a następnie wywołać silnię z liczbą, dla której ma zostać znaleziona silnia:

```
10 factorial .
```
Dałoby to wynik 3628800, który jest silnią liczby 10.

## Bibliografia

* [Czwarty język programowania](https://en.wikipedia.org/wiki/Forth_(programming_language))

