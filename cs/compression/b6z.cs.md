{
  "date" : "2019-10-11",
  "keywords" :[ "soubor b6z", "formát souboru b6z", "co je soubor b6z", "soubor", "příklad b6z", "přípona souboru b6z", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát archivního souboru B6Z - B6ZIP",
  "description":"Další informace o formátu souborů B6Z a rozhraních API, která mohou vytvářet a otevírat soubory B6Z.",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Co je soubor B6Z?

Soubor s příponou .b6z je komprimovaný archivní soubor vytvořený v softwarové aplikaci macOS [B6Zip](http://b6zip.com), která se používá ke kompresi a dekomprimaci souborů. Je to poměrně nový formát archivu, který umožňuje vyšší kompresní poměr. B6Z má otevřenou architekturu a podporuje velikost souborů až 900 000 PB. Podporuje kompresi dat, obnovu po chybách a rozkládání souborů. Obslužný software B6Zip je k dispozici zdarma na MacOS pro otevírání různých typů komprimovaných souborů včetně B6Z.

## Formát souboru B6Z

Formát souboru B6Z je založen na otevřené architektuře a poskytuje solidní kompresi pomocí šifrovacího algoritmu AES-256. Používá LZMA2 jako výchozí metodu komprese, ale podporuje také další metody komprese, jak je uvedeno níže.

|Metoda|Popis|
---|---|
|LZMA |Optimalizovaná verze algoritmu LZ77|
|LZMA2| Vylepšená verze LZMA|
|Vypustit| Běžný algoritmus LZ77|
|BZip2| Standardní algoritmus BWT|
|PPMD| PPMdH Dmitrije Shkarina|

Obslužný program B6Zip podporuje všechny tyto kompresní standardy a je vysoce optimalizovaný, což vede k vysoké rychlosti. Podporuje práci s formáty souborů [ZIP](/cs/compression/zip/), [TAR](/cs/compression/tar/) a [RAR](/cs/compression/rar/). Soubory B6Z mají typ MIME application/x-b6z-compressed.

## Reference

* [B6Zip](http://b6zip.com)

