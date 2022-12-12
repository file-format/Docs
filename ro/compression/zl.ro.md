{
  "date" : "2019-12-09",
  "keywords" :[ "fișier zl", "format fișier zl", "ce este un fișier zl", "fișier", "exemplu zl", "extensie fișier zl", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - Format de fișier comprimat ZLIP",
  "description":"Aflați despre formatul de fișier ZL și despre API-urile care pot crea și deschide fișiere ZL.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## Ce este un fișier ZL?

Un fișier cu extensia .zl este un format de fișier comprimat ZLIP care utilizează o variantă a algoritmului de compresie DEFLATE pentru comprimarea fișierelor. Este independent de tipul CPU, sistemul de operare, sistemul de fișiere și setul de caractere și, prin urmare, poate fi utilizat pentru schimbul de informații. Specificațiile tehnice ale compresiei ZLIP sunt disponibile pe [site-ul IETF](https://tools.ietf.org/html/rfc1950) și pot fi consultate din perspectiva dezvoltatorului.

## Format de fișier ZL

Un flux zlib are următoarea structură:

* `CMF (Compression Method and flags)` - Acest octet este împărțit într-o metodă de compresie pe 4 biți și un câmp de informații pe 4 biți, în funcție de metoda de compresie.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (Compression method)` - Identifică metoda de compresie utilizată în fișier. Valorile sale și metoda de compresie corespunzătoare sunt după cum urmează.

| Valoarea CM| Compresie|
|---|---|
|CM = 8|DEFLATE cu o dimensiune a ferestrei de până la 32K|
|CM = 15|Rezervat|

* `CINFO (Informații despre compresie)` - Pentru CM = 8, CINFO este logaritmul de bază 2 al dimensiunii ferestrei LZ77, minus opt (CINFO=7 indică o dimensiune a ferestrei de 32K).

* `FLG (FLaGs)` - Acest octet de steag este împărțit după cum urmează:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Referințe ##

* [Specificații de format de fișier Zlib](https://tools.ietf.org/html/rfc1950)

