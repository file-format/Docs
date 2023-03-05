{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "přípona", "soubor cdb", "formát souboru cdb", "Typ souboru databáze", "Formát souboru databáze", "co je soubor cdb" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů CDB a rozhraních API, která mohou vytvářet a otevírat soubory CDB.",
  "title" :"CDB - konstantní databázový soubor",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## Co je soubor CDB?
Soubory CDB se používají v kritických aplikacích, jako je e-mail. CDB je zkratka pro "konstantní databáze", rychlý, spolehlivý a jednoduchý balíček pro vytváření nebo čtení konstantních databází. Výměna databáze je bezpečná proti zhroucení systému. Uživatelé se nemusí během přepisování pozastavovat. CDB funguje jako asociativní pole (na disku), mapuje klíče na hodnoty a umožňuje uložení více hodnot do jednoho klíče.

## Formát souboru CDB
Formát souboru CDB ukládá čísla, offsety, délky a hodnoty hash ve formátu little endian jako 32bitová celá čísla bez znaménka. Klíče a data jsou považovány za neprůhledné bajtové řetězce bez zvláštního zacházení. Na začátku databáze představuje hlavička s pevnou velikostí 256 hašovacích tabulek s uvedením jejich pozice v souboru a jejich délky ve slotech. Obvykle jsou data uložena jako sekvence záznamů, každý záznam ukládá délku klíče, délku dat, klíč a data. Neexistují žádná pravidla pro třídění nebo zarovnání. Po záznamech následuje sada 256 hash tabulek různé délky. Protože nula je platná délka, může být v databázi fyzicky uloženo méně než 256 hašovacích tabulek, ale za 256 tabulek se nic nepovažuje. Hashovací tabulky se skládají ze série slotů, z nichž každý obsahuje hodnotu hash a offset záznamu. "Prázdné sloty" mají offset nula.

### Struktura
Databáze CDB se skládá z celé datové sady v jediném počítačovém souboru. Obsahuje tři části:
- Hlavička pevné velikosti
- Data
- Sada hašovacích tabulek.

Vyhledávání jsou dostupná pouze pro přesné klíče. Vyhledávání se provádí pomocí následujícího algoritmu:

- Hash klíč.
- Určete, ve které hashovací tabulce a slotu by měl být tento záznam umístěn.
- Otestujte uvedený slot v hashovací tabulce.

Pro vyhledávání klíčů s více než jednou hodnotou lze další hodnoty najít jednoduchým obnovením vyhledávání v dalším slotu.

#### Funkce

Struktura databáze CDB poskytuje několik funkcí:

##### Rychlé vyhledávání
Úspěšné vyhledávání v rozsáhlé databázi obvykle vyžaduje pouze dva přístupy na disk a neúspěšné vyhledávání pouze jeden.
##### Nízká režie
Databáze používá 2048 bajtů, 24 bajtů na záznam a prostor pro klíče a data.
##### Žádné náhodné limity
CDB může spravovat jakoukoli databázi až do velikosti 4 GB. Vzhledem k tomu, že neexistují žádná další omezení, záznamy se ani nemusí vejít do paměti. Databáze jsou uloženy ve formátu nezávislém na stroji.
##### Rychlé nahrazení atomové databáze
Příkaz **cdbmake** dokáže přepsat celou databázi do dvou řádů, rychleji než jiné hashovací balíčky.
##### Rychlé výpisy z databáze
**cdbdump** umí vytisknout obsah databáze ve formátu kompatibilním s cdbmake.


## Reference ##

* [cdb (software) – Wikipedie](https://en.wikipedia.org/wiki/Cdb_(software))
* [Specifikace CDB](http://cr.yp.to/cdb.html)

