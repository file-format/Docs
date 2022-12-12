{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Plik", "Rozszerzenie", "Format pliku", "Rozszerzenie pliku", "RJS", "Plik Javascript Ruby"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Plik JavaScript Ruby",
  "description":"Dowiedz się, czym jest format pliku RJS i interfejsy API, które mogą tworzyć i otwierać pliki RJS.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Czym jest plik RJS?

Plik z rozszerzeniem .rjs jest kombinacją kodu Ruby i JavsScript, która pozwala programistom Rails używać Ruby do tworzenia dynamicznego kodu JavaScript. Kod Ruby jest osadzony w funkcjach Java i jest kompilowany na serwerze WWW, który wymaga uruchomienia silnika Ruby na serwerze. RJS jest podobny do [RHTML](/pl/web/rhtml/); jedyna różnica polega na tym, że strona boczna zawiera kod Ruby w [HTML](/pl/web/html/), podczas gdy zawiera kod Ruby w funkcjach JavaScript.

## Format pliku RJS

Pliki RJS są kodowane zwykłym tekstem, jak każdy inny język skryptowy lub programistyczny. Gdy klient żąda takiej strony, kod Ruby jest wykonywany na serwerze, a do przeglądarki klienta zwracany jest tylko kod HTML i Javascript. Składnia pliku RJS jest podobna do kombinacji składni Ruby i JavaScript, tak że tylko kod Ruby jest osadzony w funkcjach JavaScript.

### Przykład RJS

Poniższy przykład pokazuje prosty kod Ruby niezależnie, a następnie osadzony w funkcji JavaScript.

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
a poniżej jest RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Bibliografia

* [RJS](https://github.com/makevoid/rjs)

