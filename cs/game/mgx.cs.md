{
  "date" : "2021-09-08",
  "keywords" :[ "soubor mgx", "formát souboru mgx", "co je soubor mgx", "soubor", "příklad mgx", "přípona souboru mgx", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru Age of Empires 2 Expansion Replay MGX a rozhraních API, která mohou vytvářet a otevírat soubory MGX.",
  "title" :"MGX - Age of Empires 2 Expansion Replay",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Co je soubor MGX?

Soubor s příponou .mgx je nahraný soubor pro hru Age of Empires II: The Conquerors, který lze přehrát v programu Age of Empires II. Obsahuje kompletní záznam kampaně hrané uživatelem. Lze jej načíst a přehrát v rámci programu Age of Empires II. Po přehrání hra ukazuje všechny události a scénáře, které si uživatel pro kampaň naplánoval a hrál.

## Formát souboru MGX – Další informace

Interní formát souboru souboru MGX byl vypracován a je k dispozici jako částečně ověřená informace o [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx- formát). Specifikace uvádějí podrobnosti v následujících částech.

### Definice struktury

Předpokládá se, že definice struktury formátu souboru GPX jsou založeny na [deklaracích BinData Ruby Gem] (https://github.com/dmendel/bindata/wiki), které poskytují způsob, jak číst a zapisovat strukturovaná binární data. To umožňuje programátorovi specifikovat formát binárních dat, která pak BinData čte a zapisuje.

### Zprávy MGX

Zprávy MGX jsou založeny na dvou typech zpráv.

* GAMESTART - určuje příkazy ke spuštění hry a není dosud ověřen
* CHAT - popisuje zprávy chatu ve hře. Jak hráči, tak samotná hra (Gaia) mohou vysílat zprávy ve hře.

### AKCE HRANÍ

Existuje několik [GAMEPLAY akcí](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions), které byly získány a jejichž podrobnosti jsou k dispozici.

## Reference

* [Age of Empires 2: The Conquerors — Specifikace formátu souboru Savegame](https://github.com/stefan-kolb/aoc-mgx-format)

