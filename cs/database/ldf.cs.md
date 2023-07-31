{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "přípona", "soubor", "formát souboru", "Typ databázového souboru", "Formát databázového souboru", "Soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů LDF a rozhraních API, která mohou vytvářet a otevírat soubory LDF.",
  "title" :"LDF - formát souboru hlavní databáze serveru SQL",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Co je soubor LDF?

Soubor s příponou .ldf je soubor protokolu spravovaný serverem Microsoft SQL Server, což je systém správy relačních databází (RDBMS). Všechny transakce provedené na primárních databázových souborech ([MDF](/cs/database/mdf/)) (jako je vložení, aktualizace, odstranění) jsou zaznamenány v souboru LDF. Soubory LDF jsou kritickými součástmi každé databáze. V případě selhání systému je soubor protokolu použit k obnovení databáze do konzistentního stavu. Soubor protokolu transakcí se může zvětšit, pokud transakce nejsou plně potvrzeny. Soubory LDF lze otevřít pomocí softwarové aplikace Microsoft SQL Server.

## Operace zaznamenané v souboru LDF

Soubor protokolu SQL zaznamenává následující operace:

* Začátek a konec každé transakce.

* Každá úprava dat dat (vložení, aktualizace nebo odstranění). To také zahrnuje změny provedené systémovými uloženými procedurami nebo příkazy jazyka DDL (Data Definition Language) v jakékoli tabulce, včetně systémových tabulek.

* Každý rozsah a přidělení stránek nebo deallocation.

* Vytvoření nebo odstranění tabulky nebo indexu.

## Formát souboru LDF

Soubor LDF se skládá ze záznamů transakcí serveru SQL Server, které jsou uspořádány jako řetězec záznamů protokolu. Každý záznam protokolu má pořadové číslo protokolu (LSN), které je vyšší než LSN předchozího záznamu. Řetězce jsou v souboru zřetězeny za sebou. Díky moderním vysokorychlostním počítačům lze záznamy vkládat tam, kde existuje LSN2 v souboru protokolu před LSN1. Protože jsou operace zaznamenávány v seriálu, byla změna popsaná LSN2 provedena po záznamu protokolu LSN1. Záznamy pro konkrétní transakci jsou propojeny zpětně pomocí ukazatelů, které se používají a urychlují vrácení transakce.
 

## Reference

* [Databázové soubory a skupiny souborů](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Průvodce architekturou a správou protokolu transakcí](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql- server-ver15)

