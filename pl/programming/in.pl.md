{
  "date" : "2022-04-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku IN - plik wejściowy Autoconf",
  "description":"Poznaj format pliku IN i interfejsy API, które mogą tworzyć i otwierać pliki IN.",
  "linktitle" : "IN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-26"
}

## Czym jest plik IN?

Plik IN jest plikiem wejściowym używanym przez GNU Autoconf podczas budowania aplikacji. Po uruchomieniu procesu konfiguracji skrypt Autoconf (plik .AC) może odwoływać się do jednego lub więcej plików „.in” lub „.h.in”. Pliki IN definiują zmienne, do których odwołuje się instalacja programu, takie jak numer wersji i data wydania aplikacji. Pliki IN mogą być również używane do określania obecności lub braku funkcji w określonej instalacji. Aplikacje takie jak Notatnik i Notepad++ mogą być używane do otwierania i edytowania plików IN.

## Format pliku IN — więcej informacji

Autoconf to składnik systemu kompilacji GNU, który generuje niestandardowe kompilacje aplikacji dla różnych platform. Jest to jedno z kilku narzędzi do budowania GNU. Inne narzędzia to Automake, Gnulib i Libtool. Bez konieczności ręcznej interwencji użytkownika skrypty te mogą dostosowywać pakiety do szerokiej gamy systemów typu UNIX. Autoconf generuje skrypt konfiguracji pakietu z pliku szablonu, który zawiera listę funkcji systemu operacyjnego, z których pakiet może korzystać w postaci wywołań makr M4

## Bibliografia

* [Autoconf](https://www.gnu.org/software/autoconf/)

