{
  "date" : "2019-10-11",
  "keywords" :[ "soubor bz2", "formát souboru bz2", "co je soubor bz2", "soubor", "příklad bz2", "přípona souboru bz2", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - komprimovaný formát souboru",
  "description":"Naučte se vědět, co je soubor BZ2 a rozhraní API, která mohou vytvářet a otevírat soubory BZ2.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## Co je soubor BZ2?

BZ2 jsou komprimované soubory generované pomocí [BZIP2](http://www.bzip.org/) open source kompresní metody, většinou na systému UNIX nebo Linux. Používá se pro kompresi jednoho souboru a není určen pro archivaci více souborů. To je na rozdíl od formátu souboru TAR na stejných platformách, který archivuje více souborů do jednoho souboru, ale bez komprese. Soubory komprimované jako BZ2 lze dekomprimovat pomocí aplikací jako [WinZip](https://www.winzip.com/win/en/). BZIP2 používá kompresní algoritmus Run-Length Encoding (RLE) nebo [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) k dosažení vysoké úrovně komprese.

## Formát souboru BZ2

Pro tento formát souboru nejsou k dispozici žádné formální specifikace. Neoficiální [reverzně vytvořené specifikace](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) však ukazují, že stream .bz2 se skládá ze 4bajtového záhlaví, které následuje o nula nebo více komprimovaných bloků. Bezprostředně za ním následuje značka konce toku obsahující 32bitové CRC pro celý zpracovaný tok ve formátu prostého textu. Mezi komprimovanými bloky není žádná výplň a všechny bloky jsou bitově zarovnány.

## Rozbalte/rozbalte soubor BZ2

Soubor BZ2 můžete rozbalit ve Windows a Mac OS pomocí softwaru, jako je WinZip. V linuxu následující příkaz v terminálu.

```
bzip2 -d filename.bz2
```

## Reference

* [Specifikace formátu BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

