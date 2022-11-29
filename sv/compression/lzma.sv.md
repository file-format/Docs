{
  "date" : "2021-04-08",
  "keywords" :[ "lzma fil", "lzma filformat", "vad är en lzma fil", "fil", "lzma exempel", "lzma filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - LZMA komprimerat filformat",
  "description":"Vad är en LZMA-fil och API:er som kan skapa och öppna LZMA-filer.",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## Vad är LZMA fil?

En fil med tillägget .lzma är en komprimerad arkivfil skapad med komprimeringsmetoden LZMA (Lempel-Ziv-Markov chain Algorithm). Dessa finns/används huvudsakligen på Unix operativsystem och liknar andra komprimeringsalgoritmer som [ZIP](/sv/compression/zip/) för att minimera filstorleken. LZMA är ett äldre filformat som håller på att eller har ersatts av .xz-formatet. MIME-typen för .lzma-formatet är \`application/x-lzma'. Det här filformatet designades av Igor Pavlov för användning i LZMA SDK.

## LZMA filformat

LZMA-filen består av två huvuddelar:

1. Rubrik
1. Komprimerad data


### LZMA Header

LZMA-filerna har en 13-byte header som följs av LZMA-komprimerade data. LZMA-huvudet består av:

* Egenskaper
* Ordboksstorlek
* Okomprimerad storlek

#### LZMA Header Properties

Fältet Egenskaper innehåller tre egenskaper. En förkortning anges inom parentes, följt av egenskapens värdeintervall. Fältet består av

1) antalet bokstavliga kontextbitar (lc, [0, 8]);
2) antalet bokstavliga positionsbitar (lp, [0, 4]); och
3) antalet positionsbitar (pb, [0, 4]).

#### LZMA-ordbokstorlek

Detta lagras som ett osignerat 32-bitars litet endian heltal med värden från 2^n och 2^n + 2^(n-1). LZMA Utils kan dekomprimera filer med valfri ordboksstorlek.

#### Okomprimerad storlek
Den okomprimerade storleken lagras som osignerat 64-bitars litet endian heltal. Ett specialvärde på 0xFFFF_FFFF_FFFF_FFFF indikerar att okomprimerad storlek är okänd. Värdet representeras av End of Payload Marker (\*) om och endast om okomprimerad storlek är okänd.

## Referenser

* [LZMA-filformat](https://svn.python.org/projects/external/xz-5.0.3/doc/lzma-file-format.txt)
* [Lempel–Ziv–Markov-kedjaalgoritm](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)

