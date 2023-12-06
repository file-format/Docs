{
"datum": "2023-04-20",
  "keywords": [
"ldb soubor",
"co je soubor ldb",
"jaké informace ldb obsahuje",
"jaký je účel souboru ldb",
"rozšíření ldb",
"soubor",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru LDB - Microsoft Access Lock File",
  "description":"Další informace o formátu LDB a o tom, jaké informace obsahuje.",
"linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
      "parent": "misc"
}
},
"lastmod": "2023-04-20"
}

## Co je soubor LDB?

Soubor LDB je soubor zámku používaný aplikací Microsoft Access, aby zabránil více uživatelům současně upravovat stejnou databázi. Když uživatel otevře databázi Accessu, Access vytvoří odpovídající soubor LDB ve stejném adresáři jako databáze. Tento soubor obsahuje informace o tom, kdo aktuálně používá databázi a jaké záznamy upravuje.

Soubor LDB je automaticky vytvořen aplikací Microsoft Access při otevření databáze a je odstraněn při zavření databáze. Je důležité poznamenat, že soubor LDB by nikdy neměl být odstraněn ručně, protože to může způsobit problémy s databází.

Pokud narazíte na problémy s databází Microsoft Access, jedním z potenciálních řešení je pokusit se odstranit soubor LDB spojený s touto databází. Tím se uvolní všechny zámky, které vám mohou bránit v přístupu k databázi. Před pokusem o to však vytvořte zálohu databáze, protože smazání souboru LDB může způsobit ztrátu nebo poškození dat, pokud se provede nesprávně.

## Formát souboru LDB – Další informace

Soubor LDB v aplikaci Microsoft Access obsahuje informace o uživatelích, kteří aktuálně přistupují k databázi, jako je jejich uživatelské jméno, název počítače a čas přihlášení. Soubor LDB také obsahuje informace o všech zámcích, které byly umístěny do databáze, například které záznamy upravuje který uživatel.

Zde je podrobnější seznam typů informací, které lze nalézt v souboru LDB:

- **Jméno uživatele** - jméno uživatele, který aktuálně přistupuje k databázi
- **Název počítače** - název počítače, ze kterého uživatel přistupuje k databázi
- **Čas přihlášení** - čas, kdy uživatel poprvé otevřel databázi
- **Zámky záznamů** - informace o tom, které záznamy jsou aktuálně upravovány kterým uživatelem
- **Zámky objektů** - informace o tom, které databázové objekty (jako jsou tabulky, formuláře nebo sestavy) aktuálně upravuje který uživatel
- **Informace o připojení** - informace o tom, jak je uživatel připojen k databázi (například zda používá místní nebo síťové připojení)

Informace v souboru LDB jsou používány aplikací Microsoft Access k zabránění více uživatelům v provádění konfliktních změn ve stejné databázi současně. Když se uživatel pokusí upravit záznam nebo objekt, který je již uzamčen jiným uživatelem, aplikace Microsoft Access zobrazí zprávu označující, že objekt je již používán. Soubor LDB se aktualizuje, když uživatelé otevírají a zavírají databázi a provádějí změny v uzamčených objektech.

## Reference
* [Co je soubor LDB?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

