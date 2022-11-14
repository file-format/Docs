{
  "date" : "2021-05-24",
  "keywords" :["rjs", "File", "Estensione", "Formato file", "Estensione file", "RJS", "File Javascript Ruby"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - File Javascript Ruby",
  "description":"Scopri cos'è il formato di file RJS e le API che possono creare e aprire file RJS.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Che cos'è un file RJS?

Un file con estensione .rjs è una combinazione di codice Ruby e JavsScript che consente agli sviluppatori Rails di utilizzare Ruby per produrre codice JavaScript dinamico. Il codice Ruby è incorporato nelle funzioni Java ed è compilato sul server web che richiede che il motore Ruby sia in esecuzione sul server. RJS è simile a [RHTML](/it/web/rhtml/); l'unica differenza è che il laterale contiene il codice Ruby in [HTML](/it/web/html/) mentre contiene il codice Ruby nelle funzioni Javascript.

## Formato file RJS

I file RJS sono codificati in testo normale come qualsiasi altro linguaggio di scripting o programmazione. Quando una tale pagina viene richiesta dal client, il codice Ruby viene eseguito sul server e solo il codice HTML e Javascript viene restituito al browser del client. La sintassi del file RJS è simile a quella della combinazione di Ruby e sintassi JavaScript in modo tale che solo il codice Ruby sia incorporato nelle funzioni JavaScript.

### Esempio RJS

L'esempio seguente mostra un semplice codice Ruby in modo indipendente e quindi incorporato in una funzione JavaScript.

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
e di seguito è il RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Riferimenti

* [RJS](https://github.com/makevoid/rjs)

