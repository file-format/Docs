{
  "date" : "2021-04-08",
  "keywords" :[ "soubor lzma", "formát souboru lzma", "co je soubor lzma", "soubor", "příklad lzma", "přípona souboru lzma", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - LZMA komprimovaný formát souboru",
  "description":"Co je soubor LZMA a rozhraní API, která mohou vytvářet a otevírat soubory LZMA.",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## Co je soubor LZMA?

Soubor s příponou .lzma je komprimovaný archivní soubor vytvořený metodou komprese LZMA (Lempel-Ziv-Markov chain Algorithm). Ty se nacházejí/používají hlavně v operačním systému Unix a jsou podobné jiným kompresním algoritmům, jako je [ZIP](/cs/compression/zip/) pro minimalizaci velikosti souboru. LZMA je starší formát souboru, který je nebo byl nahrazen formátem .xz. Typ MIME formátu .lzma je \`application/x-lzma'. Tento formát souboru navrhl Igor Pavlov pro použití v LZMA SDK.

## Formát souboru LZMA

Soubor LZMA se skládá ze dvou hlavních částí:

1. Záhlaví
1. Komprimovaná data


### Záhlaví LZMA

Soubory LZMA mají 13bajtové záhlaví, za kterým následují komprimovaná data LZMA. Hlavička LZMA se skládá z:

* Vlastnosti
* Velikost slovníku
* Nekomprimovaná velikost

#### Vlastnosti záhlaví LZMA

Pole Vlastnosti obsahuje tři vlastnosti. V závorce je uvedena zkratka a za ní rozsah hodnot vlastnosti. Pole se skládá z

1) počet doslovných kontextových bitů (lc, [0, 8]);
2) počet doslovných bitů pozice (lp, [0, 4]); a
3) počet bitů pozice (pb, [0, 4]).

#### Velikost slovníku LZMA

To je uloženo jako 32bitové celé číslo typu little endian bez znaménka s hodnotami v rozsahu 2^n a 2^n + 2^(n-1). LZMA Utils může dekomprimovat soubory s libovolnou velikostí slovníku.

#### Nekomprimovaná velikost
Nekomprimovaná velikost je uložena jako 64bitové malé endian celé číslo bez znaménka. Speciální hodnota 0xFFFF_FFFF_FFFF_FFFF označuje, že nekomprimovaná velikost je neznámá. Hodnota je reprezentována značkou konce užitečného zatížení (\*) tehdy a pouze tehdy, když je neznámá velikost nekomprimované.

## Reference

* [Formát souboru LZMA](https://svn.python.org/projects/external/xz-5.0.3/doc/lzma-file-format.txt)
* [Algoritmus řetězce Lempel–Ziv–Markov](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)

