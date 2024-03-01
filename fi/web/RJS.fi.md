{
  "date": "2021-05-24",
  "keywords": [
"rjs",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Tiedostopääte",
"RJS",
"Ruby Javascript-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RJS - Ruby Javascript-tiedosto",
  "description": "Opi RJS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata RJS-tiedostoja.",
  "linktitle": "RJS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-RJ-fiS"
}
},
  "lastmod": "2021-05-24"
}

## Mikä on RJS-tiedosto?

Tiedosto, jonka laajennus on .rjs, on yhdistelmä Ruby-koodia ja JavsScriptiä, jonka avulla Rails-kehittäjät voivat käyttää Rubyä dynaamisen JavaScript-koodin tuottamiseen. Ruby-koodi on upotettu Java-toimintoihin ja se käännetään verkkopalvelimelle, joka vaatii Ruby-moottorin olevan käynnissä palvelimella. RJS on samanlainen kuin {{HYPERLINKKI}}; Ainoa ero on, että lateral sisältää Ruby-koodin {{HYPERLINKKI2}}:ssa, kun taas se sisältää Ruby-koodin Javascript-funktioissa.

## RJS-tiedostomuoto

RJS-tiedostot koodataan pelkällä tekstillä kuten mikä tahansa muu komentosarja- tai ohjelmointikieli. Kun asiakas pyytää tällaista sivua, Ruby-koodi suoritetaan palvelimella ja vain HTML- ja Javascript-koodi palautetaan asiakkaan selaimeen. RJS-tiedoston syntaksi on samanlainen kuin Rubyn ja JavaScriptin yhdistelmän syntaksi siten, että vain Ruby-koodi on upotettu JavaScript-toimintoihin.

### RJS Esimerkki

Seuraava esimerkki näyttää yksinkertaisen Ruby-koodin itsenäisesti ja sitten upotettuna JavaScript-funktioon.

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
ja seuraava on RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Viitteet

* [RJS](https://github.com/makevoid/rjs)


