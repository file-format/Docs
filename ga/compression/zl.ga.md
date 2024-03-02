{
  "date": "2019-12-09",
  "keywords": [
"comhad zl",
"formáid comhaid zl",
"cad é comhad zl",
"comhad",
"zl shampla",
"zl síneadh comhad",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZL - ZLIP Formáid Chomhaid Chomhbhrúite",
  "description": "Foghlaim faoi fhormáid comhaid ZL agus APIs ar féidir leo comhaid ZL a chruthú agus a oscailt.",
  "linktitle": "ZL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-z-gal"
}
},
  "lastmod": "2021-04-14"
}

## Cad is comhad ZL ann?

Is formáid comhaid chomhbhrúite ZLIP é comhad le síneadh .zl a úsáideann malairt de algartam comhbhrú DEFLATE chun comhaid a chomhbhrú. Tá sé neamhspleách ar chineál LAP, ar chóras oibriúcháin, ar chóras comhaid, agus ar thacar carachtar, agus mar sin is féidir é a úsáid chun faisnéis a mhalartú. Tá sonraíochtaí teicniúla comhbhrú ZLIP ar fáil ar an [IETF site](https://tools.ietf.org/html/rfc1950) agus is féidir iad a tharchur ó thaobh an fhorbróra de.

## Formáid Comhaid ZL

Tá an struchtúr seo a leanas ag sruth zlib:

 * `CMF (Modh Comhbhrúite agus bratacha)` - Tá an beart seo roinnte ina mhodh comhbhrú 4-giotán agus ina réimse faisnéise 4-giotán ag brath ar an modh comhbhrúite.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
 * `CM (Modh comhbhrúite)` - Aithníonn sé an modh comhbhrú a úsáidtear sa chomhad. Seo a leanas a luachanna agus an modh comhbhrú comhfhreagrach.

| Luach CM| Comhbhrú|
|---|---|
|CM = 8|DEFLATE le méid fuinneoige suas le 32K|
|CM = 15|Forchoimeádta|

 * `CINFO (Eolas comhbhrú)` - I gcás CM = 8, is é CINFO an logarithm bonn-2 de mhéid na fuinneoige LZ77, lúide ocht (Léiríonn CINFO = 7 méid fuinneoige 32K).

 * `FLG (FLaGs)` - Tá an beart bratach seo roinnte mar seo a leanas:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Tagairtí ##

* [Sonraíochtaí Formáid Comhaid Zlib](https://tools.ietf.org/html/rfc1950)


