{
  "date": "2019-12-09",
  "keywords": [
"zl failą",
"zl failo formatas",
"kas yra zl failas",
"failą",
"zl pavyzdys",
"zl failo plėtinį",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZL – ZLIP suspausto failo formatas",
  "description": "Sužinokite apie ZL failo formatą ir API, kurios gali kurti ir atidaryti ZL failus.",
  "linktitle": "ZL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-z-ltl"
}
},
  "lastmod": "2021-04-14"
}

## Kas yra ZL failas?

Failas su plėtiniu .zl yra ZLIP suspausto failo formatas, kuriame failams glaudinti naudojamas DEFLATE glaudinimo algoritmo variantas. Jis nepriklauso nuo procesoriaus tipo, operacinės sistemos, failų sistemos ir simbolių rinkinio, todėl gali būti naudojamas keistis informacija. Techninės ZLIP glaudinimo specifikacijos pateikiamos [IETF site](https://tools.ietf.org/html/rfc1950) ir gali būti pateikiamos kūrėjo požiūriu.

## ZL failo formatas

Zlib srauto struktūra yra tokia:

 * CMF (glaudinimo metodas ir vėliavėlės) – šis baitas yra padalintas į 4 bitų glaudinimo metodą ir 4 bitų informacijos lauką, atsižvelgiant į glaudinimo metodą.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
 * CM (glaudinimo metodas) – nurodo faile naudojamą glaudinimo metodą. Jo reikšmės ir atitinkamas suspaudimo metodas yra tokios.

| CM vertė| Suspaudimas|
|---|---|
|CM = 8|DEFLATE, kai lango dydis iki 32K|
|CM = 15|Rezervuota|

 * CINFO (suspaudimo informacija) – CM = 8, CINFO yra LZ77 lango dydžio bazinis 2 logaritmas, atėmus aštuonis (CINFO=7 reiškia 32K lango dydį).

 * FLG (FLaGs) – šis vėliavėlės baitas padalintas taip:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Nuorodos Nr.

* [Zlib failo formato specifikacijos](https://tools.ietf.org/html/rfc1950)


