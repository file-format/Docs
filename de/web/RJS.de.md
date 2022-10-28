{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Datei", "Erweiterung", "Dateiformat", "Dateierweiterung", "RJS", "Ruby Javascript-Datei"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Ruby Javascript-Datei",
  "description":"Erfahren Sie mehr über das RJS-Dateiformat und die APIs, die RJS-Dateien erstellen und öffnen können.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Was ist eine RJS-Datei?

Eine Datei mit der Erweiterung .rjs ist eine Kombination aus Ruby-Code und JavsScript, die es Rails-Entwicklern ermöglicht, mit Ruby dynamischen JavaScript-Code zu erstellen. Ruby-Code ist in Java-Funktionen eingebettet und wird auf dem Webserver kompiliert, der erfordert, dass die Ruby-Engine auf dem Server ausgeführt wird. RJS ähnelt [RHTML](/de/web/rhtml/); Der einzige Unterschied besteht darin, dass die Seite Ruby-Code in [HTML](/de/web/html/) enthält, während sie Ruby-Code in Javascript-Funktionen enthält.

## RJS-Dateiformat

RJS-Dateien sind wie jede andere Skript- oder Programmiersprache im Klartext codiert. Wenn eine solche Seite vom Client angefordert wird, wird der Ruby-Code auf dem Server ausgeführt und nur der HTML- und Javascript-Code werden an den Browser des Clients zurückgegeben. Die Syntax der RJS-Datei ähnelt der Kombination aus Ruby- und JavaScript-Syntax, sodass nur der Ruby-Code in JavaScript-Funktionen eingebettet ist.

### RJS-Beispiel

Das folgende Beispiel zeigt einen einfachen Ruby-Code, der unabhängig und dann in eine JavaScript-Funktion eingebettet ist.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
und folgendes ist das RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Verweise

* [RJS](https://github.com/makevoid/rjs)

