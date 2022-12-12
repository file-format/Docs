{
  "date" : "2021-09-16", 
  "keywords" :[ "hta", "plik", "rozszerzenie", "format pliku", "implementacja hta", "Przewodnik programowania", "przykład hta", "aplikacja HTML", "aplikacja języka znaczników hipertekstowych", "pliki HTA", "Aplikacja Microsoft HTML"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTA - Pliki Aplikacji HTML",
  "description":"Poznaj format plików HTA i interfejsy API, które mogą tworzyć i otwierać pliki HTA.",
  "linktitle" : "HTA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-16"
}

## Czym jest plik HTA?

Skrót HTMLA oznacza **Hypertext Markup Language Application** to program zgodny z systemem Microsoft Windows. Kod źródłowy tego programu zawiera więcej niż jeden język skryptowy, taki jak [HTML](/pl/web/html/) i [JavaScript](/pl/web/js/). W przypadku interfejsu użytkownika preferowana jest aplikacja HTML, podczas gdy w celu spełnienia wymagań logiki programu używany jest dowolny inny język skryptowy.

Aplikacja HTML jest niezależna od modelu zabezpieczeń przeglądarki internetowej i działa jako w pełni zaufana aplikacja. Rozszerzenie używane dla plików dotyczących tych aplikacji to HTA. Aplikacje te zawierają cechy HTML wraz z właściwościami innych języków skryptowych.


## Krótka historia ##

HTA została po raz pierwszy wprowadzona w 1999 roku przez Microsoft wraz z wydaniem Internet Explorera 5. Była kompatybilna z Internet Explorerem, więc mogła być uruchamiana tylko w systemie operacyjnym Windows. Technologia ta została opatentowana w 2003 roku. Pliki HTA są wykonywane podobnie jak inne pliki .exe. Pliki HTA są również kompatybilne z dzisiejszą zaktualizowaną wersją systemu Windows 11.


## Specyfikacja techniczna ##

HTA mają taki sam format, jak każda inna strona HTML, a niektóre atrybuty służą do kontrolowania stylów obramowań lub ikon programów. Ponadto przedstawiono argumenty przemawiające za uruchomieniem HTA. Aplikacje te można uruchamiać za pomocą programu o nazwie mshta.exe. Dostęp do niego można uzyskać, klikając dwukrotnie plik. Programy te działają automatycznie wraz z Internet Explorerem. Oprócz innych specyfikacji, nie są one niezależne od przeglądarki silnika Trident, ale są niezależne od Internet Explorera. Oznacza to, że można je wykonać bez użycia przeglądarki Internet Explorer.

Tagi są używane w celu dostosowania wyglądu tych aplikacji. Konwersja aplikacji Microsoft HTML do formatu HTA jest prostsza, tzn. wystarczy zmienić rozszerzenie. Ponieważ wiemy, że te aplikacje są w pełni zaufane, mają więcej funkcji i zalet w porównaniu do prostych plików HTML. Do tworzenia HTA można wykorzystać edytory tekstu. Edytory te mogą zostać nabyte przez firmę Microsoft lub inne zaufane źródło.


## Przykład formatu pliku HTA ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## Odniesienie ##

* [HTA – Wikipedia](https://en.wikipedia.org/wiki/HTML_Application)



