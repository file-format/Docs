{
  "date" : "2021-04-08",
  "keywords" :[ "soubor dar", "formát souboru dar", "co je soubor dar", "soubor", "příklad dar", "přípona souboru dar", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Formát souboru Disk Archiver",
  "description":"Další informace o formátu souborů DAR a rozhraních API, která mohou vytvářet a otevírat soubory DAR.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Co je soubor DAR?

Soubor s příponou .dar je komprimovaný archiv vytvořený pomocí archivu DAR Disk. Může vytvořit zálohu/archivu pro celý disk nebo skupinu souborů. Byl vytvořen jako náhrada za souborový formát [TAR](/cs/compression/tar/) v OS UNIX a lze jej vytvořit jako rozdělené archivní soubory pro velký počet souborů. Archiv DAR podporuje možnost smazání souborů ze systému, které jsou propojeny s hlavními soubory v archivu. Díky své schopnosti poskytovat rozdílové, přírůstkové a dekrementální zálohování je lepší než soubory TAR.

## Formát souboru DAR

Soubory DAR jsou komprimované archivy, které mohou používat jakoukoli kompresi pro jednotlivé soubory, jako je [gzip](/cs/compression/gz/), [bzip2](/cs/compression/bz2/), lzo, xz nebo lzma. Přesný formát souboru DAR závisí na tom, jaký typ formátování je použit ke kompresi obsahu archivu. Umožňuje také volitelné šifrování Blowfish, Twofish, AES, Serpent, Camellia a šifrování a podpis veřejným klíčem (OpenPGP).

### Funkce DAR

Některé z funkcí formátu souboru DAR jsou následující.

* Stará se o jakýkoli typ inodu (adresář, prosté soubory, symbolické odkazy, speciální zařízení, pojmenovaná potrubí, zásuvky, dveře, ...)
* Stará se o pevně propojené inody (pevně propojené prosté soubory, char zařízení, bloková zařízení, pevně propojené symbolické odkazy)
* Postará se o řídké soubory
* Stará se o rozšířené atributy souborů Linux,
* Stará se o linuxový soubor ACL
* Stará se o rozvětvení souborů Mac OS X
* Stará se o některé atributy specifické pro souborový systém, jako je datum narození souborového systému HFS+ a neměnný, žurnálování dat, bezpečné mazání, slučování bez ocasu, nesmazatelné, noatime atributy souborového systému ext2/3/4.
* Komprese na soubor pomocí gzip, bzip2, lzo, xz nebo lzma (na rozdíl od komprimace celého archivu). Jednotlivec se může rozhodnout nekomprimovat již komprimované soubory na základě jejich přípony názvu souboru.
* Rychlé rozbalování souborů odkudkoli v archivu
* Rychlý výpis obsahu archivu díky uložení katalogu souborů v archivu
* Živé zálohování souborového systému: detekuje, kdy byl soubor změněn, když byl čten pro zálohování, a může se pokusit uložit jej až do stanoveného maximálního počtu opakování
* Hash soubor (MD5, SHA1 nebo SHA-512) generovaný za běhu pro každý řez, výsledný soubor je kompatibilní s md5sum nebo sha1sum, aby bylo možné rychle zkontrolovat integritu každého řezu
* Nezávislé na souborovém systému: lze jej použít k obnovení systému na oddíl jiné velikosti a/nebo na oddíl s jiným souborovým systémem[5]

## Reference

* [DAR](http://dar.linux.free.fr/)
* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

