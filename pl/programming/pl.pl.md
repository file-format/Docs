{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "plik", "rozszerzenie", "format", "Perl", "język Perl", "pliki PL", "programowanie"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format plików PL i interfejsy API, które mogą tworzyć i otwierać pliki PL.",
  "title" :"Plik PL - format pliku skryptu Perla",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## Czym jest plik PL?

Plik z rozszerzeniem .pl to plik Perl Script, który jest językiem skryptowym. Są one kompilowane i uruchamiane przy użyciu oprogramowania Perl Interpreter. Plik skryptu PL zawiera wiersze kodu, zmienne i komentarze. Języki skryptowe są stosunkowo trudne
zrozumieć inne formaty plików programistycznych, takie jak [PHP](/pl/programming/php/). Pliki PL można tworzyć i są kompatybilne z systemami Windows, macOS i Linux.

## Krótka historia języka skryptowego Perla

Ten język był po raz pierwszy używany w 1987 roku, więc te pliki mają swój początek w tym roku. W 1989 został wydany Perl 2. Później został zaktualizowany i zmodyfikowany aż do wersji 5.35, a kolejna wersja ma zostać wydana w przyszłym roku.

W każdej aktualizacji dodawane były narzędzia dotyczące funkcjonalności, wydajności i wyglądu języka oraz plików. W tych latach było wiele poprawek dotyczących wersji. Pierwotnie był to podstawowy język skryptowy, ale obecnie obejmuje również wiele innych modułów. Pierwotnie był to bardzo prosty język, ale skrypty tego języka były dość trudne do zrozumienia, ponieważ były zwarte.

## Specyfikacje rozszerzeń formatu plików Perla

Istnieją pewne właściwości lub specyfikacje tych plików programistycznych, niektóre z nich są następujące:

* Kod zawarty w tych plikach jest w formacie zwykłego tekstu i służy do tworzenia skryptów
* Skryptowanie serwera, parsowanie tekstu i administrowanie serwerem to główne aspekty, które obejmuje skrypt tego języka
* Wiele popularnych programów powiązanych z tym językiem to Active state Active Perl i Bare Bones BBEdit (kompatybilne z Mac OS)
* Ten język jest uważany za język wysokiego poziomu
* W przypadku Win32 użytkownik może być zmuszony do zainstalowania natywnej dystrybucji binarnej języka
* Wymaga niektórych narzędzi skryptowych, aby stały się wykonywalne w różnych zestawach Windows Resource Kit
* Visual Studio .NET to znany framework do tworzenia języków programowania. Narzędzie Active State znane jako Visual Perl służy do dodawania Perla do Visual Studio
* W plikach pierwsza linia kodu źródłowego opisuje informacje o używanym tłumaczu. Pliki PL zwykle zaczynają się od linii **#!/usr/bin/perl**, która mówi komputerowi, aby uruchomił ten skrypt za pomocą interpretera Perla zainstalowanego na komputerze


## Przykłady skryptów PL

```
#!/usr/bin/perl
print "Hello, world\n";
```

To wydrukuje

```
Hello, World
```

### Komentarz jednowierszowy ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Komentarz wielowierszowy ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Przypisanie zmiennej ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Przypisanie zmiennej skalarnej ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Proste operacje skalarne ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Bibliografia ##

- [Python (język programowania) - Wikipedia](https://en.wikipedia.org/wiki/Python_(język_programowania))

