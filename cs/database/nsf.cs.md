{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "rozšíření", "soubor", "formát souboru", "Typ souboru databáze", "Formát souboru databáze", "Soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů NSF a rozhraních API, která mohou vytvářet a otevírat soubory NSF.",
  "title" :"Formát souboru NSF - formát databáze Lotus Notes",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Co je soubor NSF?

Soubor s příponou .nsf (Notes Storage Facility) je formát databázového souboru používaný [software IBM Notes](https://en.wikipedia.org/wiki/HCL_Domino), který byl dříve známý jako Lotus Notes. Definuje schéma pro ukládání různých druhů objektů, jako jsou e-maily, schůzky, dokumenty, formuláře a pohledy. Všechny tyto informace jsou obsaženy v jediném souboru NSF pro obchodní spolupráci, který je podobný souboru PST/OST. Některé z aplikací, které mohou otevřít soubory NSF, zahrnují IBM Lotus Notes a IBM Domino.

## Specifikace formátu souborů NSF

Soubory NSF jsou binární povahy a jejich specifikace jsou dostupné od Joachima Metze na [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc). Podle těchto podrobností obsahuje soubor NSF:

* Záhlaví souboru
* Záhlaví databáze

Kromě toho se skládá z:

* Superblok
* Blok deskriptoru kbelíku
* Bitmapa
* Record Relocation Vector kbelík
* Souhrnné kbelíky
* Nesouhrnné kbelíky


### Záhlaví souboru NSF

Záhlaví souboru NSF má velikost 6 bajtů. Skládá se z:

|Offset|Velikost|Hodnota|Popis|
---|---|---|---|
0|2|0x1a 0x00|Podpis|
2|4| |Velikost hlavičky databáze|

### Hlavička databáze

Hlavička databáze NSD obsahuje následující potvrzené hodnoty.

* Informace o databázi
* Identifikátor databáze (DBID)
* Informace o replikaci
* Příznaky vyrovnávací paměti databázových informací
* Název
* Kategorie
* Třída
* Třída návrhu (název šablony)
* Speciální identifikátory poznámek
* Polstrování
* Informace o databázi 2
* Informace o databázi 3
* Informace o databázi 4
* Informace o databázi 5
* Polstrování
* Identifikátor instance databáze (DBIID)
* Historie replikací

## Reference

* [Formát NSF – Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

