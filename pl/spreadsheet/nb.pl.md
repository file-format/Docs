{
  "date" : "2019-12-16",
  "keywords" :["NB", "plik", "rozszerzenie", "format pliku", "Mathematica", "Arkusz kalkulacyjny" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się, czym są interfejsy API plików NB, które mogą tworzyć i otwierać pliki NB.",
  "title" :"NB - format pliku notatnika Mathematica",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## Czym jest plik NB?

Plik z rozszerzeniem .nb to format pliku notatnika Wolfram, który zapisuje instrukcje dotyczące instrukcji matematycznych w pliku tekstowym. Może zawierać wiele różnych typów danych, takich jak obliczenia na żywo, dowolne dynamiczne interfejsy, pełny zestaw danych wejściowych, wprowadzanie obrazu, automatyczne adnotacje kodu, kompletny interfejs programistyczny wysokiego poziomu oraz tysiące starannie zorganizowanych funkcji i opcji. Instrukcje tekstowe to dane wejściowe i wyjściowe Mathematica, które są generowane i aktualizowane w miarę umieszczania instrukcji wejściowych w pliku.

## Format pliku Wolfram Notebook NB — więcej informacji

Pliki Wolfram Notebook NB są zapisywane w formacie zwykłego tekstu, który jest formatem pliku czytelnym dla człowieka. Zawartość notatnika jest podzielona na sekcje jako zwykły tekst, z których każda jest reprezentowana przez grupy komórek, podobnie jak w arkuszu kalkulacyjnym. Zakres tych grup jest określony przez nawias na końcu każdej komórki. Styl przypisany do komórki określa jej rolę w notatniku, jak opisano poniżej.

### Notatniki jako język Wolfram

Gdy zamierza się zapisać Notatnik składający się z instrukcji matematycznych do wykonania przez Wolfram Language Kernal, komórkom w dokumencie automatycznie przypisywany jest styl tekstu „Wejście”. Mówi to jądru, aby uważało je za instrukcje wykonywane, gdy użytkownik wprowadzi kombinację klawiszy `Shift+Return`. Notatnik Mathematica wygląda tak, jak pokazano w poniższym przykładzie.

{{< figure src="../Wolfram Notebook.jpeg" alt="Format pliku Wolfram Notebook" >}}

### Notatniki jako dokumenty

Notebooki Mathematica mogą być w formacie dokumentu, aby pokazać, co widzisz, co otrzymujesz (WYSIWYG). Dokumenty te są takie same, jak wyświetlane na ekranie lub na papierze drukowanym i są interaktywne. W tym celu do komórki przypisany jest „Styl tekstu”, aby wyświetlić zawartość bez wykonywania instrukcji przez jądro.

## Eksportuj zeszyty Mathematica

Notatniki Mathematica można eksportować do wielu różnych formatów plików, takich jak PDF, grafika, GIS, pliki skompresowane i arkusze kalkulacyjne.

## Bibliografia

* [Podstawy notatnika Mathematica](https://reference.wolfram.com/language/guide/NotebookBasics.html)

