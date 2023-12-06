{
"data": "2023-05-15",
  "keywords": [
"plik csx",
"co to jest plik csx",
"co zawiera plik csx",
"jaki jest format pliku csx",
"plik",
"rozszerzenie pliku csx",
"rozszerzenie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format pliku CSX - skrypt Visual C#",
  "description":"Dowiedz się o formacie CSX i interfejsach API, które umożliwiają tworzenie i otwieranie plików CSX.",
"tytuł linku": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
      "parent": "programming"
}
},
"lastmod": "15.05.2023"
}

## Czym jest plik CSX?

Visual C# Script (znany również jako CSX) to format pliku używany przez silnik skryptowy Roslyn w ekosystemie .NET firmy Microsoft. Pliki CSX zawierają kod C#, który można wykonać bezpośrednio, bez konieczności wykonywania osobnego etapu kompilacji.

Format CSX jest specyficzny dla ekosystemu Microsoft i nie jest powszechnie używanym formatem plików w ogólnym programowaniu. Pliki CSX są często używane w scenariuszach, w których wymagane jest szybkie prototypowanie lub funkcjonalność skryptów. Umożliwiają tworzenie i uruchamianie programów w języku C# w prostszy sposób w porównaniu z tworzeniem pełnoprawnej skompilowanej aplikacji.

Aby wykonać pliki CSX, można użyć narzędzi takich jak .NET Interactive Notebooks, które zapewniają interaktywne środowisko do uruchamiania kodu C#. Do pracy z plikami CSX można również używać Visual Studio Code z rozszerzeniem C# i .NET Core SDK.

## Co zawiera plik CSX?

Plik CSX (skrypt C#) zawiera kod C#, który można wykonać bezpośrednio. Może zawierać dowolny prawidłowy kod C#, taki jak deklaracje zmiennych, funkcje, klasy i inne konstrukcje programistyczne.

Oto przykład tego, co może zawierać plik CSX:

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

Pliki CSX mogą również zawierać instrukcje importu, odniesienia do bibliotek zewnętrznych i inne funkcje języka C# obsługujące funkcjonalność kodu. Kod jest interpretowany i wykonywany na bieżąco, bez konieczności kompilacji, dzięki czemu nadaje się do zadań związanych ze skryptami i szybkim prototypowaniem.

## Jaki jest format pliku CSX?

Format CSX (skrypt C#) jest zgodny z prostym formatem tekstowym. Zwykle ma rozszerzenie pliku .csx, aby odróżnić go od zwykłych plików kodu źródłowego C# (.cs).

Pliki CSX można edytować za pomocą dowolnego edytora tekstu lub zintegrowanego środowiska programistycznego (IDE), które obsługuje podświetlanie składni C#. Gdy plik CSX będzie gotowy, można go uruchomić przy użyciu narzędzi takich jak .NET Interactive Notebooks, interfejs wiersza poleceń (CLI) .NET Core lub środowisko IDE z obsługą skryptów C#.

## Bibliografia
* [Programowanie w języku C# przy użyciu kodu Visual Studio](https://code.visualstudio.com/docs/languages/csharp)

