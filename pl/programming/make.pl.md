{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Make File - Plik skryptu Makefile Xcode",
  "description":"Poznaj format XCode MakeFile i interfejsy API, które mogą tworzyć i otwierać pliki MakeFile.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Czym jest plik MAKE?

Plik MAKE to plik skryptu XCode, który organizuje kompilację kodu. Służy do kompilowania i łączenia programów z wielu plików kodu źródłowego. Pomaga to zdecydować, które części dużej aplikacji wymagają ponownej kompilacji, gdy aplikacja wymaga aktualizacji. Spraw, aby pliki używały serii instrukcji do uruchomienia w zależności od tego, które pliki uległy zmianie.

## Przykład formatu pliku MAKE

Poniższa zawartość jest wykonywana za pomocą narzędzia Make, a dane wyjściowe są następujące.

```
hello:
	echo "hello world"
```
**Utwórz dane wyjściowe**

```
$ make
echo "hello world"
hello world
```

## Bibliografia
* [XCode i Make - fora Apple](https://developer.apple.com/forums/thread/657458)
* [Przewodnik po języku C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

