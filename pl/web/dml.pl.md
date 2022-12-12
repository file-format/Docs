{
  "date" : "2021-05-25",
  "keywords" :[ "DML", "Plik DML", "Format pliku DML", "Typ pliku DML", "plik", "typ", "co to jest plik DML" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML - Plik DynaScript HTML",
  "description":"Poznaj format pliku DML i interfejsy API, które mogą tworzyć i otwierać pliki DML.",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## Czym jest plik DML?

Plik z rozszerzeniem .dml to plik kodu strony skryptu internetowego utworzony za pomocą DyanScript. DynaScript to dynamiczny język skryptowy [HTML](/pl/web/html/), który jest zgodny z ECMAScript i zapewnia większość tych samych funkcji, co inne języki skryptowe. Jest podobny do kodu ColdFusion i kodu Microsoft Active Server Pages (ASP). Pliki DML można otwierać i przeglądać w standardowych przeglądarkach internetowych, podobnie jak inne strony HTML.

## Format pliku DML

Pliki DML są tworzone w formacie zwykłego pliku tekstowego i można je otwierać za pomocą edytora tekstu, aby wyświetlić kod. Pisanie kodu przy użyciu języka skryptowego DML może służyć do dynamicznego generowania kodu HTML na stronach DML hostowanych po stronie serwera. DynaScripts są zbudowane z następujących elementów języka:


* Znacznik SCRIPT — są one osadzane w dokumentach jako komentarze HTML. Komentarz HTML jest oznaczony przez \ <!-- tag.
* Literały — są to stałe wartości w plikach DynaScript. Przykłady obejmują liczby całkowite, takie jak s 123 , 0x3F , 0123, liczby zmiennoprzecinkowe, takie jak 456,789 , 3.2e-8, wartości logiczne, takie jak prawda lub fałsz, oraz łańcuchy, takie jak „Deszcz w Hiszpanii”
* Zmienne — zmienne DynaScript nie muszą być definiowane ani przypisywane do stałego typu danych. Zmienna musi mieć wartość przed użyciem jej w wyrażeniu; w przeciwnym razie generowane jest ostrzeżenie w czasie wykonywania.
* Wyrażenia — są to kombinacje zmiennych, wartości dosłownych, operatorów i innych wyrażeń. Prawa strona instrukcji przypisania to wyrażenie.
* Operatory — operują na jednym lub kilku wyrażeniach zwanych operandami. Mogą to być operacje trójskładnikowe, binarne lub jednoargumentowe: operatory trójskładnikowe działają na trzech wyrażeniach, operatory binarne działają na dwóch wyrażeniach, a operatory jednoargumentowe działają na jednym.
* Instrukcje — sterują przepływem skryptów, manipulują obiektami i programowaniem ogólnym. Ogólnie rzecz biorąc, te instrukcje są zgodne ze standardową składnią C i Java. Przykładami są pętle if-else, do-while, switch, break, continue itp., jak każdy inny język skryptowy.
* Funkcje — funkcje, podobnie jak każdy inny język skryptowy, umożliwiają umieszczenie zestawu instrukcji raz w dokumencie jako funkcji, a następnie użycie jej kilka razy w całym dokumencie (poprzez wywołanie funkcji). DynaScript obsługuje również funkcje.
* Obiekty — DynaScript jest zorientowany obiektowo i obsługuje „obiekty” oraz podstawowe koncepcje zorientowane obiektowo, takie jak enkapsulacja, polimorfizm i dziedziczenie.

