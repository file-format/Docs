{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Soubor", "Rozšíření", "Formát souboru", "Přípona souboru", "RJS", "Soubor Ruby Javascript"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Ruby Javascript File",
  "description":"Zjistěte, co je formát souboru RJS a rozhraní API, která mohou vytvářet a otevírat soubory RJS.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Co je soubor RJS?

Soubor s příponou .rjs je kombinací kódu Ruby a JavaScriptu, který umožňuje vývojářům Rails používat Ruby k vytváření dynamického kódu JavaScript. Ruby kód je zabudován do funkcí Java a je kompilován na webovém serveru, který vyžaduje, aby na serveru běžel Ruby engine. RJS je podobný [RHTML](/cs/web/rhtml/); jediný rozdíl je v tom, že lateral obsahuje kód Ruby v [HTML](/cs/web/html/), zatímco obsahuje kód Ruby ve funkcích Javascriptu.

## Formát souboru RJS

Soubory RJS jsou kódovány jako prostý text jako jakýkoli jiný skriptovací nebo programovací jazyk. Když si klient takovou stránku vyžádá, na serveru se spustí kód Ruby a do prohlížeče klienta se vrátí pouze kód HTML a Javascript. Syntaxe souboru RJS je podobná syntaxi kombinace Ruby a syntaxe JavaScriptu, takže do funkcí JavaScriptu je vložen pouze kód Ruby.

### Příklad RJS

Následující příklad ukazuje jednoduchý kód Ruby nezávisle a poté vložený do funkce JavaScriptu.

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
a následující je RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Reference

* [RJS](https://github.com/makevoid/rjs)

