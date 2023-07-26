{
  "date" : "2021-04-08",
  "keywords" :[ "soubor lz", "formát souboru lz", "co je soubor lz", "soubor", "příklad lz", "přípona souboru lz", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Lzip komprimovaný formát souboru",
  "description":"Další informace o formátu souborů LZ a rozhraních API, která mohou vytvářet a otevírat soubory LZ.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Co je soubor LZ?

Soubor s příponou .lz je komprimovaný archivní soubor vytvořený pomocí Lzip, což je bezplatný nástroj příkazového řádku pro kompresi. Podporuje zřetězení pro kompresi podpůrných souborů. Soubory LZ mají typ média application/lzip a podporují vyšší kompresní poměry než [BZ2](/cs/compression/bz2/). LZ jsou založeny na algoritmu LZMA (Lempel-Ziv-Markovův řetězec) a obsahují 32bitový kontrolní součet CRC a identifikační bajty pro kontrolu integrity souboru.

## Komprimovaný formát LZMA

Komprimovaný formát LZMA se skládá z komprimovaného proudu bitů, který je zakódován pomocí adaptivního binárního kodéru rozsahu. Proud je rozdělen do paketů. Každý paket popisuje buď jeden bajt, nebo sekvenci LZ77. Délka a vzdálenost každého paketu je implicitně nebo explicitně zakódována.

Sedm typů paketů je následujících ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Sbalený kód (bitová sekvence) |Název paketu |Popis paketu|
---|---|---|
|0 + byteCode| LIT| Jeden bajt zakódovaný pomocí adaptivního binárního kodéru rozsahu.|
|1+0 + len + dist| ZÁPAS| Typická sekvence LZ77 popisující délku a vzdálenost sekvence.|
|1+1+0+0| SHORTREP| Jednobajtová sekvence LZ77. Vzdálenost je rovna naposledy použité vzdálenosti LZ77.|
|1+1+0+1 + jen| LONGREP[0]| Sekvence LZ77. Vzdálenost je rovna naposledy použité vzdálenosti LZ77.|
|1+1+1+0 + jen| LONGREP[1]| Sekvence LZ77. Vzdálenost se rovná druhé naposledy použité vzdálenosti LZ77.|
|1+1+1+1+0 + jen| LONGREP[2]| Sekvence LZ77. Vzdálenost je rovna třetí naposledy použité vzdálenosti LZ77.|
|1+1+1+1+1 + jen| LONGREP[3]| Sekvence LZ77. Vzdálenost je rovna čtvrté naposledy použité vzdálenosti LZ77.|


## Reference

* [LZMA – Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

