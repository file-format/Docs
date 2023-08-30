{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "přípona", "soubor", "formát souboru", "Typ souboru databáze", "Formát souboru databáze", "Soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru MDF a rozhraních API, která mohou vytvářet a otevírat soubory NDF.",
  "title" :"Formát souboru NDF - soubor hlavní databáze serveru SQL",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Co je soubor NDF?

Soubor s příponou .ndf je sekundární databázový soubor používaný [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) k ukládání uživatelských dat. NDF je sekundární úložný soubor, protože SQL server ukládá uživatelsky specifikovaná data v primárním úložném souboru známém jako [MDF](/cs/database/mdf/). Datový soubor NDF je volitelný a je uživatelsky definovaný pro správu úložiště dat v případě, že primární soubor MDF využívá veškerý přidělený prostor. Obvykle je uložen na samostatném disku a může se rozšířit na více úložných zařízení. Přítomnost souborů MDF je nezbytná pro otevření souborů NDF.

## Formát souboru NDF

Formát souboru NDF se neliší od [MDF](/cs/database/mdf/) a používá stránky jako základní jednotku pro ukládání dat. každá stránka začíná 96 bajtovým záhlavím, které obsahuje:

* ID stránky
* Typ struktury
* Počet záznamů na stránkách
* Ukazatele na předchozí a následující stránky

### Struktura souborů NDF

Soubor MDF má následující datovou strukturu.

* Strana 0: Záhlaví
* Strana 1: První PFS
* Strana 2: První GAM
* Strana 3: První SGAM
* Strana 4: Nepoužité
* Strana 5: Nepoužité
* Strana 6: První DCM
* Strana 7: První BCM

#### Záhlaví souboru NDF

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

## Stránka datového souboru

Stránky v datovém souboru SQL Server začínají od nuly (0) a postupně se zvyšují. Každý soubor je rozpoznán jedinečným ID souboru. Dvojice ID souboru a čísla stránky jednoznačně identifikuje stránku v databázi. Příklad zobrazující čísla stránek v databázi je jako na následujícím obrázku.

{{< figure src="../ndf.png" alt="Formát souboru databáze NDF" >}}

Tento příklad ukazuje čísla stránek v databázi, která má 4 MB primární datový soubor a 1 MB sekundární datový soubor.

## Reference

* [Databázové soubory a skupiny souborů](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver16)
* [Odpojit a připojit databázi – SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Analýza anatomie datového souboru SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

