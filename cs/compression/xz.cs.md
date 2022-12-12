{
  "date" : "2022-01-23",
  "keywords" :[ "soubor xz", "formát souboru", "co je soubor xz", "soubor", "příklad xz", "přípona souboru xz", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor XZ – komprimovaný archiv XZ",
  "description":"Další informace o formátu souboru XZ a rozhraních API, která mohou vytvářet a otevírat soubory XZ.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## Co je soubor XZ?

XZ je komprimovaný formát souboru, který využívá kompresní algoritmus LZMA2. Byl navržen jako náhrada za oblíbené formáty gzip a bzip2 a oproti těmto starším standardům nabízí řadu výhod. Soubory XZ jsou dobře podporovány na mnoha platformách a lze je rychle a snadno dekomprimovat. I když nejsou tak běžné jako soubory [ZIP](/cs/compression/zip/) nebo [RAR](/cs/compression/rar/), archivy XZ lze použít k ukládání velkého množství dat bez obětování kvality komprese. Pokud potřebujete komprimovat nebo dekomprimovat velké soubory, stojí za zvážení přípona souboru XZ.

## Formát souboru XZ

Soubor XZ se vygeneruje a uloží jako binární soubory na disk. Ke kompresi dat používá algoritmus LZMA a může dosáhnout kompresního poměru až 50 %. Soubory XZ se obvykle používají pro distribuci softwaru a zálohy. Lze je dekomprimovat pomocí nástroje XZ, který je součástí většiny distribucí Linuxu.

## Rozbalte soubory XZ v systému Linux/Unix

Chcete-li rozbalit soubory XZ, nainstalujte nejprve balíček `xz-utils`:
```
$ sudo apt-get install xz-utils
```

Pomocí příkazu `unxz` extrahujte soubory .xz:
```
$ unxz compressed_xz_file.xz
```

nebo pomocí volby --decompress XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## Reference

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)

