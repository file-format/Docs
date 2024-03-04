{
  "date": "2021-07-29",
  "keywords": [
"md5 failą",
"md5 failo formatas",
"kas yra md5 failas",
"failą",
"md5 pavyzdys",
"md5 failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MD5 – MD5 kontrolinės sumos failas",
  "description": "Sužinokite apie MD5 failą ir API, kurios gali kurti ir atidaryti MD5 failus.",
  "linktitle": "MD5",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-md-lt5"
}
},
  "lastmod": "2021-07-29"
}

## Kas yra MD5 failas?

MD5 failas yra kontrolinės sumos failas, naudojamas failo vientisumui patikrinti. Jis panašus į susieto failo piršto atspaudą ir yra unikaliai generuojamas naudojant algoritmą, kuris naudoja failo bitų skaičių. Jis naudojamas failui patikrinti naudojant tokią programinę įrangą kaip [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). Vienas iš MD5 failų naudojimo pranašumų yra patikrinti, ar atsisiųsti failai nėra sugadinti.

## MD5 failo formatas – daugiau informacijos

Paprastai MD5 failas išsaugomas tokiu pačiu pavadinimu kaip ir originalus failo pavadinimas, bet su plėtiniu .md5. Pavyzdžiui, jei susieto failo pavadinimas yra abc_987_123456.grb, atitinkamas MD5 failo pavadinimas bus abc_987_123456.grb.md5. MD5 failai padeda nustatyti, ar gautas arba atsisiųstas failas nėra sugadintas ar paveiktas kenkėjiško turinio. Trumpai tariant, MD5 failai garantuoja failo išsamumą.


## Kaip patikrinti MD5 kontrolinę sumą?

Vienas failas gali būti patikrintas / patvirtintas MD5 naudojant [md5sum](https://en.wikipedia.org/wiki/Md5sum) įrankį, kaip nurodyta toliau.

```
md5sum -c abc_987_123456.grb.md5
```

## Nuorodos

* [md5sum – Vikipedija](https://en.wikipedia.org/wiki/Md5sum)


