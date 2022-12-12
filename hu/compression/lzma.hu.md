{
  "date" : "2021-04-08",
  "keywords" :[ "lzma fájl", "lzma fájlformátum", "mi az lzma fájl", "fájl", "lzma példa", "lzma fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - LZMA tömörített fájlformátum",
  "description":"Mi az az LZMA fájl és API-k, amelyek LZMA fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## Mi az LZMA fájl?

Az .lzma kiterjesztésű fájl egy tömörített archív fájl, amelyet az LZMA (Lempel-Ziv-Markov lánc-algoritmus) tömörítési módszerrel hoztak létre. Ezek főként Unix operációs rendszeren találhatók/használhatók, és hasonlóak más tömörítési algoritmusokhoz, mint például a [ZIP](/hu/compression/zip/) a fájlméret minimalizálása érdekében. Az LZMA egy régebbi fájlformátum, amelyet az .xz formátum jelenleg vagy felváltott. Az .lzma formátum MIME típusa \`application/x-lzma'. Ezt a fájlformátumot Igor Pavlov tervezte az LZMA SDK-ban való használatra.

## LZMA fájlformátum

Az LZMA fájl két fő részből áll:

1. Fejléc
1. Tömörített adatok


### LZMA fejléc

Az LZMA-fájlok 13 bájtos fejléccel rendelkeznek, amelyet az LZMA tömörített adatok követnek. Az LZMA fejléc a következőkből áll:

* Tulajdonságok
* Szótár mérete
* Tömörítetlen méret

#### LZMA fejléc tulajdonságai

A Tulajdonságok mező három tulajdonságot tartalmaz. Zárójelben van egy rövidítés, majd a tulajdonság értéktartománya. A mező a következőkből áll

1) a literális kontextusbitek száma (lc, [0, 8]);
2) a literális pozícióbitek száma (lp, [0, 4]); és
3) a pozícióbitek száma (pb, [0, 4]).

#### LZMA szótár mérete

Ez egy előjel nélküli 32 bites kis endian egész számként van tárolva 2^n és 2^n + 2^(n-1) értékekkel. Az LZMA Utils bármilyen szótármérettel ki tudja tömöríteni a fájlokat.

#### Tömörítetlen méret
A tömörítetlen méret előjel nélküli 64 bites kis endian egész számként kerül tárolásra. A 0xFFFF_FFFF_FFFF_FFFF speciális érték azt jelzi, hogy a tömörítetlen méret ismeretlen. Az értéket az End of Payload Marker (\*) jelöli akkor és csak akkor, ha a tömörítetlen méret ismeretlen.

## Hivatkozások

* [LZMA fájlformátum](https://svn.python.org/projects/external/xz-5.0.3/doc/lzma-file-format.txt)
* [Lempel–Ziv–Markov láncalgoritmus](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)

