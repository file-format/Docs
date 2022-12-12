{
  "date" : "2019-10-11",
  "keywords" :["vb", "plik", "rozszerzenie", "format pliku", "Visual Basic", "Przewodnik po programowaniu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - plik kodu Visual Basic",
  "description":"Poznaj format pliku VB i interfejsy API, które mogą tworzyć i otwierać pliki VB.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik VB?

Plik VB to plik kodu źródłowego utworzony w języku Visual Basic, który został stworzony przez Microsoft do tworzenia aplikacji .NET. Innym podobnym językiem o innej składni jest C#, którego pliki są zapisywane z rozszerzeniem pliku [.CS](/pl/programming/cs/). Format pliku zapewnia język programowania niskiego poziomu do pisania kodu, który jest kompilowany w celu wygenerowania ostatecznego pliku wyjściowego w postaci EXE lub DLL. Można je tworzyć i kompilować za pomocą programu Microsoft Visual Studio. Microsoft Visual Studio Express może być również używany do tworzenia i aktualizowania takich plików, co jest darmowym IDE. Prosty projekt Visual Studio [rozwiązanie](/pl/programming/sln/) utworzony w języku VB może zawierać jeden lub więcej takich plików. Pliki zaznaczone do włączenia do kompilacji są wymienione w pliku [CSPROJ](/pl/programming/csproj/), który jest częścią projektu i nakazuje kompilatorowi użycie zaznaczonych plików.

## Format pliku VB — więcej informacji

Pliki VB to formaty plików tekstowych, które można otwierać w dowolnym edytorze tekstu w celu edycji. Jednak po otwarciu w obsługiwanym IDE z odpowiednim podświetleniem składni kod jest łatwy do odczytania i uporządkowania. Prosty plik VB zawiera:

* Deklaracja przestrzeni nazw — w odniesieniu do określonej funkcjonalności zdefiniowanej przez tę konkretną przestrzeń nazw
* Deklaracja zmiennych - Aby zadeklarować zmienne na poziomie klasy dla konkretnej implementacji
* Deklaracja metod - Deklaracja metod dla określonej funkcjonalności

## Przykład formatu pliku VB

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



