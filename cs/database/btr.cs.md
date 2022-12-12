{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "rozšíření", "soubor", "formát souboru", "Typ databázového souboru", "Formát databázového souboru", "Btrieve Database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů BTR a rozhraních API, která mohou vytvářet a otevírat soubory BTR.",
  "title" :"BTR - Btrieve Database File",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Co je soubor BTR?

Soubor s příponou .btr je databázový soubor vytvořený transakční databázovou aplikací [Btrieve](https://www.actian.com/). Na rozdíl od systémů pro správu relačních databází (RBMS) je Btrieve založen na metodě indexovaného sekvenčního přístupu (ISAM), což je způsob ukládání dat pro rychlé vyhledávání. Soubor BTR uchovává kolekci záznamů a používá se ke generování sestav podle požadavků. Soubory BTR lze otevřít pomocí Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility a Legend Software BTRIEVE Viewer.

## Struktura souboru BTR – Další informace

Vnitřní struktura dat a zarovnání každého bajtu ve struktuře souboru BTR nejsou veřejně dostupné. Nicméně, Btrieve
poskytuje [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm), které lze použít ke čtení informací ze souborů BTR. Je kompatibilní s následujícími programovacími jazyky a vývojovými prostředími.

* Embarcadero C/C++
* Embarcadero Delphi
* GNU C/C++
* Micro Focus COBOL
* Microsoft Visual Basic
* Microsoft Visual C++
* Watcom C/C++

Načítání dat ze souboru BTR závisí na přidruženém souboru DDF s ním. Bez DDF nebude snadné získat informace z takového souboru.

## Reference

* [Btrieve – Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Úvod do Btreive API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

