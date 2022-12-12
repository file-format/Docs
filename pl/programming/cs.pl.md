{
  "date" : "2019-10-11",
  "keywords" :["cs", "plik", "rozszerzenie", "format pliku", "CSharp", "Język programowania" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - Plik kodu CSharp",
  "description":"Dowiedz się o formacie plików CS i interfejsach API, które mogą tworzyć i otwierać pliki CS.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik CS?

Pliki z rozszerzeniem .cs to pliki kodu źródłowego dla języka programowania C#. Wprowadzony przez firmę Microsoft do użytku z .NET Framework, format pliku zapewnia język programowania niskiego poziomu do pisania kodu, który jest kompilowany w celu wygenerowania ostatecznego pliku wyjściowego w postaci pliku EXE lub DLL. Można je tworzyć i kompilować za pomocą Microsoft Visual Studio. Microsoft Visual Studio Express może być również używany do tworzenia i aktualizowania takich plików, który jest darmowym IDE. Pliki CS są używane do tworzenia aplikacji, które mogą obejmować zarówno proste aplikacje komputerowe, jak i bardziej złożone programy. Prosty projekt Visual Studio [rozwiązanie](/pl/programming/sln/) utworzony w języku C# może zawierać jeden lub więcej takich plików. Pliki zaznaczone do włączenia do kompilacji są wymienione w pliku [CSPROJ](/pl/programming/csproj/), który jest częścią projektu i nakazuje kompilatorowi użycie zaznaczonych plików.

## Format pliku CS ##

Pliki CS to formaty plików tekstowych, które można otwierać w dowolnym edytorze tekstu w celu edycji. Jednak po otwarciu w obsługiwanym IDE z odpowiednim podświetleniem składni kod jest łatwy do odczytania i uporządkowania. Prosty plik CS zawiera:

* Deklaracja przestrzeni nazw — w odniesieniu do określonej funkcjonalności zdefiniowanej przez tę konkretną przestrzeń nazw
* Deklaracja zmiennych - Aby zadeklarować zmienne na poziomie klasy dla konkretnej implementacji
* Deklaracja metod — Deklaracja metod dla określonej funkcjonalności

### Składnia ###

* Średniki służą do oznaczenia końca instrukcji.
* Nawiasy klamrowe służą do grupowania instrukcji. Instrukcje są zwykle pogrupowane w metody (funkcje), metody w klasy, a klasy w przestrzenie nazw.
* Zmienne są przypisywane za pomocą znaku równości, ale porównywane za pomocą dwóch kolejnych znaków równości.
* Nawiasy kwadratowe są używane z tablicami, zarówno w celu ich zadeklarowania, jak i uzyskania wartości o danym indeksie w jednej z nich.

### Przykład ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

