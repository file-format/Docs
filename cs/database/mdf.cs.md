{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "přípona", "soubor", "formát souboru", "Typ databázového souboru", "Formát databázového souboru", "Soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru MDF a rozhraních API, která mohou vytvářet a otevírat soubory MDF.",
  "title" :"Formát souboru MDF - soubor hlavní databáze serveru SQL",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Co je soubor MDF?

Soubor s příponou .mdf je hlavní databázový soubor používaný [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) k ukládání uživatelských dat. Je to velmi důležité, protože všechna data jsou uložena v tomto souboru. Soubor MDF ukládá uživatelská data v relačních databázích ve formulářových sloupcích, řádcích, polích, indexech, pohledech a tabulkách. SQL Server umožňuje nastavit autogrow a autoshrink nastavení tak, aby mělo pozitivní dopad na výkon databáze. Soubory MDF lze načíst a připojit k databázi pomocí Microsoft SQL Server. Soubory MDF mají typ MIME Application/octet-stream.

## Formát souboru MDF

Základní jednotkou ukládání dat na serveru SQL Server je stránka. Stránka úložiště přiřazená k databázi je rozdělena na logické stránky s číslováním od 0 do n. Jedna stránka začíná 96bajtovým záhlavím, které obsahuje ID stránky, typ struktury, ke které stránka patří, počet záznamů na stránce a ukazatele na předchozí a následující stránky.

### Struktura souboru

Soubor MDF má následující datovou strukturu.

* Strana 0: Záhlaví
* Strana 1: První PFS
* Strana 2: První GAM
* Strana 3: První SGAM
* Strana 4: Nepoužité
* Strana 5: Nepoužité
* Strana 6: První DCM
* Strana 7: První BCM

#### Záhlaví souboru

Číslo stránky 0 všech souborů obsahuje záhlaví, které ukládá metadata o souboru.

#### Místo volného místa (PFS)
PFS identifikuje stav přidělení a určuje množství volného místa.

* Bit 1: Označuje, zda je stránka přidělena nebo ne.
* Bit 2: Označuje, zda je stránka smíšeného rozsahu.
* Bit 3: Označuje, že tato stránka je stránkou IAM.
* Bit 4: Označuje, že tato stránka obsahuje falešné záznamy
* Bity 5 až 7: Kombinovaná tříbitová hodnota, která označuje zaplnění stránky následovně:
* 0: Stránka je prázdná
* 1: Stránka je zaplněna z 1–50 %.
* 2: Stránka je zaplněna z 51–80 %.
* 3: Stránka je zaplněna z 81–95 %.
* 4: Stránka je zaplněna z 96–100 %.

## Reference

* [Databázové soubory a skupiny souborů](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Odpojit a připojit databázi – SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [Analýza anatomie datového souboru SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

