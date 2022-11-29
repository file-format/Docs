{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Fil", "Tillägg", "Filformat", "Filtillägg", "RJS", "Ruby Javascript-fil"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Ruby Javascript-fil",
  "description":"Läs mer om vad som är RJS-filformat och API:er som kan skapa och öppna RJS-filer.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Vad är RJS fil?

En fil med tillägget .rjs är en kombination av Ruby-kod och Javascript som gör att Rails-utvecklare kan använda Ruby för att producera dynamisk JavaScript-kod. Ruby-koden är inbäddad i Java-funktioner och kompileras på webbservern som kräver att Ruby-motorn körs på servern. RJS liknar [RHTML](/sv/web/rhtml/); den enda skillnaden är att lateralen innehåller Ruby-kod i [HTML](/sv/web/html/) medan den innehåller Ruby-kod i Javascript-funktioner.

## RJS filformat

RJS-filer är kodade i vanlig text som alla andra skript- eller programmeringsspråk. När en sådan sida efterfrågas av klienten exekveras Ruby-koden på servern och endast HTML- och Javascript-kod returneras till klientens webbläsare. Syntaxen för RJS-filen liknar den för kombinationen av Ruby- och JavaScript-syntax så att endast Ruby-koden är inbäddad i JavaScript-funktioner.

### RJS-exempel

Följande exempel visar en enkel Ruby-kod oberoende och sedan inbäddad i en JavaScript-funktion.

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
och följande är RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Referenser

* [RJS](https://github.com/makevoid/rjs)

