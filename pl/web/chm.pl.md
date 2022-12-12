{
  "date" : "2019-10-11",
  "keywords" :[ "chm","plik chm", "format pliku chm", "typ pliku chm", "plik", "typ", "co to jest plik chm" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CHM - skompilowany format pliku pomocy HTML",
  "description" :"Dowiedz się, co to jest plik CHM i interfejsy API, które mogą je tworzyć i otwierać.",
  "linktitle" : "CHM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik CHM?

Format pliku CHM reprezentuje plik pomocy Microsoft **[HTML](/pl/web/html/)**, który składa się ze zbioru stron HTML. Zawiera indeks umożliwiający szybki dostęp do tematów i nawigację do różnych części dokumentu pomocy. Plik CHM można przeszukiwać pod kątem zawartości za pomocą dostarczonej opcji wyszukiwania. CHM to zastrzeżony przez firmę Microsoft format pliku pomocy online, który jest często używany w dokumentacji oprogramowania. Ponadto jest używany w kilku innych aplikacjach, takich jak przewodniki szkoleniowe, interaktywne książki i biuletyny elektroniczne. Większość nowoczesnych środowisk programistycznych firmy Microsoft obsługuje generowanie dokumentacji CHM z informacji dostępnych w aplikacji.

Wyjątkowa zdolność formatu pliku CHM do zaimplementowania połączonego spisu treści i indeksu wyróżnia go spośród innych standardowych stron HTML. Wygenerowany plik CHM ma stosunkowo mały rozmiar, dzięki czemu można go łatwo dystrybuować z pakietami oprogramowania. Narzędzie do tworzenia pomocy, HTML Help Workshop, zapewnia łatwy w użyciu system do tworzenia projektów pomocy i powiązanych z nimi plików oraz zarządzania nimi. Pliki CHM mogą zawierać tekst, obrazy i hiperłącza; widoczne w przeglądarce internetowej; używany przez system Windows i inne programy jako rozwiązanie pomocy online.

## Format pliku CHM

Ostateczna postać wygenerowanego pliku CHM zależy od tego, jak zaprojektowany jest system pomocy i czy jest przeznaczony dla aplikacji, czy strony internetowej. Plik CHM obsługuje kompresję danych z kompresją LZX w celu wygenerowania skompresowanych plików HTML. Posiada wbudowaną wyszukiwarkę umożliwiającą szybkie przeszukiwanie treści wraz z możliwością łączenia wielu plików .CHM. Plik CHM składa się z zestawu plików HTML, połączonego spisu treści i pliku indeksu.

### Pliki HTML

Niezależnie od tego, czy tworzysz tematy pomocy do dystrybucji w programie, czy w sieci Web, dokumenty, które tworzysz, są tworzone przy użyciu specjalnego języka formatowania znanego jako Hypertext Markup Language (HTML). Pliki tematyczne HTML mają rozszerzenie nazwy pliku .htm lub .html.

Chociaż każdy temat pomocy lub strona sieci Web, którą tworzysz, wydaje się być dokumentem zawierającym tekst, grafikę lub animowane obrazy, pliki .htm są w rzeczywistości dokumentami tekstowymi, które mają specjalne kody formatowania HTML. Te kody, zwane tagami, informują przeglądarkę, jak wyświetlić każdą stronę. Tylko tekst, który pojawia się w temacie lub na stronie internetowej, znajduje się w pliku .htm. Wszelkie wyświetlane grafiki, dźwięki, animowane obrazy lub inne elementy to osobne pliki, na które wskazuje plik HTML. Przeglądarka kopiuje lub pobiera grafikę, dźwięki lub inne elementy, gdy widzi znaczniki, które ją o tym informują.

### Spis treści (TOC)
Plik spisu treści pomocy (.hhc) to plik HTML zawierający tytuły tematów dla spisu treści. Gdy użytkownik otworzy spis treści w skompilowanym pliku pomocy (lub na stronie internetowej) i kliknie tytuł tematu, otworzy się plik HTML powiązany z tym tytułem.

### Plik indeksu
Plik indeksu (.hhk) to plik HTML zawierający pozycje indeksu (słowa kluczowe) dla Twojego indeksu. Gdy użytkownik otworzy indeks w skompilowanym pliku pomocy lub na stronie sieci Web i kliknie słowo kluczowe, otworzy się plik HTML skojarzony ze słowem kluczowym.

## Komponenty pomocy HTML

Pomoc HTML składa się z kilku komponentów. Należą do nich:

* `HTML Help Workshop`: narzędzie do tworzenia pomocy z łatwym w użyciu interfejsem graficznym do tworzenia plików projektów, plików tematów HTML, plików zawartości, plików indeksów i wszystkiego, czego potrzebujesz do stworzenia systemu pomocy online lub witryny sieci Web .
* `HTML Help ActiveX control`: mały, modułowy program używany do wstawiania nawigacji pomocy i dodatkowych funkcji okna do pliku HTML.
* `Podgląd pomocy HTML`: w pełni funkcjonalne i konfigurowalne trzypanelowe okno, w którym mogą pojawiać się tematy pomocy online.
* `Microsoft HTML Help Image Editor`: internetowe narzędzie graficzne do tworzenia zrzutów ekranu; oraz do konwertowania, edytowania i przeglądania plików graficznych.
* `Aplet HTML Help Java`: mały program oparty na Javie, którego można użyć zamiast kontrolki ActiveX do wstawienia nawigacji pomocy do pliku HTML.
* `Program wykonywalny Pomocy HTML`: program, który wyświetla i uruchamia pomoc po kliknięciu skompilowanego pliku pomocy.
* `Kompilator pomocy HTML`: program, który kompiluje projekt, zawartość, indeks, temat i inne pliki w skompilowany plik pomocy.
* `Przewodnik tworzenia pomocy w formacie HTML`: przewodnik online zaprojektowany, aby pomóc autorom pomocy w korzystaniu z Pomocy HTML w celu zaprojektowania systemu pomocy. Przewodnik zawiera również kompletną pomoc w formacie HTML dla programistów oraz informacje o znacznikach HTML dla autorów.

## Bibliografia

* [Pomoc Microsoft HTML](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/microsoft-html-help-1-4-sdk)
* [Skompilowana pomoc HTML firmy Microsoft](https://en.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)

