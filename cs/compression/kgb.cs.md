{
  "date" : "2021-04-08",
  "keywords" :[ "soubor kgb", "formát souboru kgb", "co je soubor kgb", "soubor", "příklad kgb", "přípona souboru kgb", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KGB - Formát archivního souboru KGB",
  "description":"Další informace o formátu souborů KGB a rozhraních API, která mohou vytvářet a otevírat soubory KGB.",
  "linktitle" : "KGB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## Co je soubor KGB?

Soubor s příponou .kgb je komprimovaný archivní soubor vytvořený pomocí archivačního softwaru KGB. Archivátor KGB používá kompresní algoritmus [PAQ6](https://en.wikipedia.org/wiki/PAQ6) ke kompresi souborů do archivu KGB. Archivátor KGB byl ukončen a již se nepoužívá. Formát souboru KGB nabízí vyšší míru komprese, ale za cenu minimálních hardwarových požadavků (doporučujeme procesor s taktem 1,5 GHz a 256 MB RAM) a prodlouženou dobu komprese/dekomprese.

## Formát souboru KGB

O formátu souboru KGB nejsou k dispozici žádné podrobnosti o technické implementaci. Nabízí šifrování AES-256 pro ochranu archivovaných souborů. Archivátor KGB byl vyvinut ve Visual [C++](/cs/programming/cpp/) Tomaszem Pawlakem v dubnu 2006 a věřilo se, že komprimuje [1 GB soubor až na 10 MB](https://web.archive.org/ web/20100522074017/http://cshared.com/compress-1-gb-to-10-mb-kgb-archiver/).

## Reference

* [KGB – Wikipedia](https://en.wikipedia.org/wiki/KGB_Archiver)
* [KGB Archiver](https://sourceforge.net/projects/kgbarchiver/)

