{
  "date": "2021-05-24",
  "keywords": [
"rjs",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Failo plėtinys",
"RJS",
"Ruby Javascript failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RJS – Ruby Javascript failas",
  "description": "Sužinokite, kas yra RJS failo formatas ir API, kurios gali kurti ir atidaryti RJS failus.",
  "linktitle": "RJS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-RJ-ltS"
}
},
  "lastmod": "2021-05-24"
}

## Kas yra RJS failas?

Failas su plėtiniu .rjs yra Ruby kodo ir JavsScript derinys, leidžiantis Rails kūrėjams naudoti Ruby dinaminiam JavaScript kodui kurti. Ruby kodas yra įterptas į Java funkcijas ir yra sukompiliuotas žiniatinklio serveryje, kuriam reikalingas, kad Ruby variklis veiktų serveryje. RJS yra panašus į [RHTML](/web/rhtml/); vienintelis skirtumas yra tas, kad šoninėje dalyje yra Ruby kodas [HTML](/web/html/), o javascript funkcijose yra Ruby kodas.

## RJS failo formatas

RJS failai yra koduojami paprastu tekstu, kaip ir bet kuri kita scenarijų ar programavimo kalba. Klientui paprašius tokio puslapio, serveryje vykdomas Ruby kodas, o į kliento naršyklę grąžinamas tik HTML ir Javascript kodas. RJS failo sintaksė yra panaši į Ruby ir JavaScript sintaksės derinio sintaksę, todėl JavaScript funkcijose yra įterptas tik Ruby kodas.

### RJS pavyzdys

Toliau pateiktame pavyzdyje rodomas paprastas Ruby kodas atskirai ir įterptas į JavaScript funkciją.

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
ir toliau yra RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Nuorodos

* [RJS](https://github.com/makevoid/rjs)


