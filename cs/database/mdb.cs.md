{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "přípona", "soubor", "formát souboru", "Typ databázového souboru", "Formát databázového souboru", "Soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru MDB a rozhraních API, která mohou vytvářet a otevírat soubory MDB.",
  "title" :"Formát souboru MDB - soubor databáze Microsoft Access",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Co je soubor MDB?

Soubor s příponou .mdb je databázový soubor Microsoft Access, což je systém správy relačních databází (RDBMS). Ukládá data do databázových tabulek, které jsou vzájemně propojeny primárním a cizím klíčem. Soubor MDB obsahuje kompletní strukturu databázových tabulek, dotazů, uložených procedur. MDB je výchozí formát souboru pro Microsoft Access 2003. Postranní verze Microsoft Access používají formáty souborů [ACCDB](/cs/database/accdb/), což je k dnešnímu dni nejnovější formát souborů. Soubory MDB lze otevřít pomocí aplikací, jako je Microsoft Access, MDB Viewer, MDBOpener, a lze je převést do formátů ACCDB, [CSV](/cs/spreadsheet/csv/), Excel atd.

## Formát souboru MDB

Pro formát MDB jsou k dispozici veřejné specifikace a zůstává proprietárním formátem souborů společnosti Microsoft. Společnost Microsoft však poskytuje přístup ke konektivitě k souboru MDB pomocí standardu Open Database Connectivity (ODBC) a Visual Basic for Applications (VBA). Neoficiální průvodce MDB poskytuje stručný neformální popis formátu MDB založeného na reverzním inženýrství a lze se do něj obrátit, abyste se dozvěděli o specifikacích.

### Stránky

Podle neoficiálního průvodce MDB se soubor MDB skládá ze stránek s pevnou velikostí (2048 bajtů pro Jeb DB3 a 4096 bajtů pro Jet DB 4). První bajt označuje typ stránky. Níže jsou uvedeny klíčové typy stránek:

`First Page:` Obsahuje informace o hlavičce databáze, které také zahrnují identifikaci verze Jet DB, se kterou je soubor kompatibilní. Kromě toho také obsahuje informace o zabezpečení souborů a mapu využití stránky.

`Stránka definice tabulky:` Stránka definice tabulky určuje sloupce, datové typy, index a další informace. V případě potřeby používá další stránky a zahrnuje mapu stránek, která obsahuje data řádků pro tuto tabulku.

`Datové stránky:` Datové stránky jsou skutečné datové kontejnery, kde jsou data uložena po řádcích. K ukládání dlouhých datových hodnot používá vedlejší stránky.

Jedna databáze Microsoft Access může obsahovat více souborů, které umožňují překročit omezení velikosti souborů a tabulek. To usnadňuje vkládání formulářů a kódu do front-endového MDB souboru na pracovní ploše uživatele a dat do jiných backendových MDB souborů na serverech připojených k síti.

## Reference ##

* [Specifikace přístupu](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Neoficiální průvodce MDB](http://jabakobob.net/mdb/)

