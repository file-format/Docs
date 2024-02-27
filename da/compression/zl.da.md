{
  "date": "2019-12-09",
  "keywords": [
"zl filen",
"zl filformat",
"hvad er en zl fil",
"fil",
"zl eksempel",
"zl filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZL - ZLIP komprimeret filformat",
  "description": "Lær om ZL filformat og API'er, der kan oprette og åbne ZL filer.",
  "linktitle": "ZL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-z-dal"
}
},
  "lastmod": "2021-04-14"
}

## Hvad er ZL fil?

En fil med filtypen .zl er et ZLIP-komprimeret filformat, der bruger en variant af DEFLATE-komprimeringsalgoritmen til at komprimere filer. Det er uafhængigt af CPU-type, operativsystem, filsystem og tegnsæt, og kan derfor bruges til udveksling af information. Tekniske specifikationer for ZLIP-komprimering er tilgængelige på [IETF site](https://tools.ietf.org/html/rfc1950) og kan henvises fra udviklerens perspektiv.

## ZL filformat

En zlib-stream har følgende struktur:

 * `CMF (Compression Method and flags)` - Denne byte er opdelt i en 4-bit komprimeringsmetode og et 4-bit informationsfelt afhængigt af komprimeringsmetoden.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
 * `CM (Compression method)` - Det identificerer den komprimeringsmetode, der bruges i filen. Dens værdier og tilsvarende komprimeringsmetode er som følger.

| CM Værdi| Kompression|
|---|---|
|CM = 8|DEFLATE med en vinduesstørrelse på op til 32K|
|CM = 15|Reserveret|

 * `CINFO (Compression info)` - For CM = 8 er CINFO base-2-logaritmen for LZ77-vinduesstørrelsen, minus otte (CINFO=7 angiver en 32K-vinduestørrelse).

 * `FLG (FLaGs)` - Denne flagbyte er opdelt som følger:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Referencer ##

* [Zlib filformatspecifikationer](https://tools.ietf.org/html/rfc1950)


