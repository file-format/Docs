{
  "date" : "2021-05-24",
  "keywords" :["rjs", "File", "Extension", "File Format", "File Extension", "RJS", "Ruby Javascript File"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Ruby Javascript fájl",
  "description":"További információ az RJS fájlformátumról és az API-król, amelyek RJS fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Mi az RJS fájl?

Az .rjs kiterjesztésű fájl a Ruby kód és a JavsScript kombinációja, amely lehetővé teszi a Rails fejlesztői számára, hogy a Ruby segítségével dinamikus JavaScript kódot állítsanak elő. A Ruby kód be van ágyazva a Java függvényekbe, és a webszerveren van lefordítva, amelyhez a Ruby motornak futnia kell a szerveren. Az RJS hasonló a következőhöz: [RHTML](/hu/web/rhtml/); az egyetlen különbség az, hogy az oldalsó Ruby kódot tartalmaz a [HTML](/hu/web/html/), míg a Ruby kódot a Javascript függvényekben.

## RJS fájlformátum

Az RJS fájlok egyszerű szöveggel vannak kódolva, mint bármely más szkript- vagy programozási nyelv. Amikor egy ilyen oldalt a kliens kér, a Ruby kód lefut a szerveren, és csak a HTML és a Javascript kód kerül vissza a kliens böngészőjébe. Az RJS fájl szintaxisa hasonló a Ruby és a JavaScript szintaxis kombinációjának szintaxisához, így csak a Ruby kód van beágyazva a JavaScript függvényekbe.

### RJS példa

A következő példa egy egyszerű Ruby-kódot mutat be egymástól függetlenül, majd JavaScript-függvénybe ágyazva.

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
és a következő a RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Hivatkozások

* [RJS](https://github.com/makevoid/rjs)

