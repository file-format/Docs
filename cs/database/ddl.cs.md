{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "přípona", "soubor", "formát souboru", "Typ souboru databáze", "Formát souboru databáze", "Soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů DDL a rozhraních API, která mohou vytvářet a otevírat soubory DDL.",
  "title" :"Formát souboru DDL - soubor jazyka definice dat",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Co je soubor DDL?

Soubor s příponou .ddl je soubor jazyka definice dat, který se používá k definování schématu databáze. Obsahuje příkazy/příkazy pro práci s databázovými strukturami, jako jsou tabulky, sloupce, záznamy a další pole. Příkazy v souboru DDL jsou zapsány v [SQL](/cs/database/sql/) a mohou provádět operace, jako je vytvoření tabulky v databázi, přetažení a aktualizace. Databázové schéma je vlastněno jeho vytvořeným a lze na něm provádět všechny operace CRUD. Oblíbené aplikace, které mohou vytvářet a otevírat soubory DDL, jsou Windows Text Editor, Jetbrains Intellij Idea a EclipseLink.

## DDL příkazy

Jeden soubor DDL může obsahovat několik příkazů, které se díky správné syntaxi provedou postupně a provedou změny ve schématu, jako je vytváření znakových sad a tabulek, odstraňování tabulek, přejmenování a změny tabulek. Následující příkazy DDL se běžně používají při práci s databázovým schématem.

`CREATE` - Používá se k vytvoření databáze nebo jejích objektů (jako je tabulka, index, funkce, pohledy, procedura ukládání a spouštěče).

`DROP` – Používá se k odstranění objektů z databáze.

`ALTER` - Používá se ke změně struktury databáze.

`ZKRÁTIT` – Používá se k odstranění všech záznamů z tabulky, včetně odstranění všech prostorů přidělených záznamům.

`KOMENTÁŘ` – Přidá komentáře do datového slovníku.

`RENAME` – Přejmenuje existující objekt v databázi.

## Příklad DDL

Následující příklad ukazuje příkaz DDL pro příkaz CREATE, který vytváří tabulku a definuje její pole.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Reference ##

* [DDL od Wikipedie](https://en.wikipedia.org/wiki/Data_definition_language)

