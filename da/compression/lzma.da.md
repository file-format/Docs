{
  "date": "2021-04-08",
  "keywords": [
"lzma fil",
"lzma filformat",
"hvad er en lzma fil",
"fil",
"lzma eksempel",
"lzma filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZMA - LZMA komprimeret filformat",
  "description": "Hvad er en LZMA fil og API'er, der kan oprette og åbne LZMA filer.",
  "linktitle": "LZMA",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lzm-daa"
}
},
  "lastmod": "2021-04-18"
}

## Hvad er LZMA fil?

En fil med filtypenavnet .lzma er en komprimeret arkivfil, der er oprettet ved hjælp af komprimeringsmetoden LZMA (Lempel-Ziv-Markov chain Algorithm). Disse findes/bruges hovedsageligt på Unix-operativsystemet og ligner andre komprimeringsalgoritmer såsom [ZIP](/compression/zip/) for at minimere filstørrelsen. LZMA er et ældre filformat, som bliver eller er blevet erstattet af .xz-formatet. MIME-typen for .lzma-formatet er \`application/x-lzma'. Dette filformat er designet af Igor Pavlov til brug i LZMA SDK.

## LZMA filformat

LZMA-filen består af to hoveddele:

 1. Header
 1. Komprimerede data


### LZMA Header

LZMA-filerne har en 13-byte header, der efterfølges af de komprimerede LZMA-data. LZMA-headeren består af:

 * Ejendomme
 * Ordbogsstørrelse
 * Ukomprimeret størrelse

#### LZMA Header Egenskaber

Egenskabsfeltet indeholder tre egenskaber. En forkortelse er angivet i parentes, efterfulgt af værdiområdet for egenskaben. Feltet består af

1) antallet af bogstavelige kontekstbits (lc, [0, 8]);
2) antallet af bogstavelige positionsbit (lp, [0, 4]); og
3) antallet af positionsbits (pb, [0, 4]).

#### LZMA Ordbog Størrelse

Dette er gemt som et usigneret 32-bit lille endian heltal med værdier fra 2^n og 2^n + 2^(n-1). LZMA Utils kan dekomprimere filer med enhver ordbogsstørrelse.

#### Ukomprimeret størrelse
Den ukomprimerede størrelse gemmes som usigneret 64-bit lille endian heltal. En speciel værdi på 0xFFFF_FFFF_FFFF_FFFF indikerer, at ukomprimeret størrelse er ukendt. Værdien er repræsenteret af End of Payload Marker (\*), hvis og kun hvis ukomprimeret størrelse er ukendt.

## Referencer

* [LZMA-filformat](https://svn.python.org/projects/external/xz-5.0.3/doc/lzma-file-format.txt)

* [Lempel–Ziv–Markov kædealgoritme](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)


