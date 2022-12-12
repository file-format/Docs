{
  "date" : "2019-10-11",
  "keywords" :[ "soubor tbz", "formát souboru tbz", "co je soubor tbz", "soubor", "příklad tbz", "přípona souboru tbz", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Bzip Compressed Tar Archive",
  "description":"Další informace o formátu souboru TBZ a rozhraních API, která mohou vytvářet a otevírat soubory TBZ.",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Co je soubor TBZ?

Soubor s příponou .tbz je komprimovaný archiv, který používá kompresi BZIP pro zmenšení velikosti souborů obsahu. Soubory TBZ jsou ve skutečnosti archivované soubory UNIX [TAR](/cs/compression/tar/), které jsou pak komprimovány pomocí BZIP. Nejnovější komprese druhé úrovně je [BZIP2](/cs/compression/bz2/), která nahradila BZIP. Formát souboru TBZ je vhodný pro přenos velkých souborů. Soubory TBZ lze otevřít/extrahovat pomocí softwarových aplikací, jako jsou 7-Zip, PeaZip a jZip. Uživatelé Linuxu a macOS mohou také otevřít TBZ pomocí příkazu BZIP2 z okna terminálu.

## Formát souboru TBZ

Soubory TBZ jsou ve skutečnosti komprimované archivy vytvořené pomocí komprese BZIP/[BZIP2](/cs/compression/bz2). Pro tento formát souboru nejsou k dispozici žádné formální specifikace. Neoficiální [reverzně vytvořené specifikace] (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) však ukazují, že stream .bz2 se skládá ze 4bajtového záhlaví, které následuje o nula nebo více komprimovaných bloků.

## Reference ##

* [Specifikace formátu BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

