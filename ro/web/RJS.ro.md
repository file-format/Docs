{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Fișier", "Extensie", "Format fișier", "Extensie fișier", "RJS", "Fișier Ruby Javascript"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Fișier Javascript Ruby",
  "description":"Aflați despre ce este formatul de fișier RJS și API-urile care pot crea și deschide fișiere RJS.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Ce este un fișier RJS?

Un fișier cu extensia .rjs este o combinație de cod Ruby și JavsScript care permite dezvoltatorilor Rails să folosească Ruby pentru a produce cod JavaScript dinamic. Codul Ruby este încorporat în funcțiile Java și este compilat pe serverul web care necesită ca motorul Ruby să ruleze pe server. RJS este similar cu [RHTML](/ro/web/rhtml/); singura diferență este că lateralul conține cod Ruby în [HTML](/ro/web/html/) în timp ce conține cod Ruby în funcțiile Javascript.

## Format de fișier RJS

Fișierele RJS sunt codificate în text simplu, ca orice alt limbaj de scripting sau de programare. Când o astfel de pagină este solicitată de client, codul Ruby este executat pe server și numai codul HTML și Javascript sunt returnați browserului clientului. Sintaxa fișierului RJS este similară cu cea a combinației dintre sintaxa Ruby și JavaScript, astfel încât numai codul Ruby este încorporat în funcțiile JavaScript.

### Exemplu RJS

Următorul exemplu arată un cod Ruby simplu independent și apoi încorporat într-o funcție JavaScript.

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
și următorul este RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Referințe

* [RJS](https://github.com/makevoid/rjs)

