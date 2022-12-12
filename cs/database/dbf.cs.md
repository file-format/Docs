{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "přípona", "soubor dbf", "formát souboru dbf", "Typ souboru databáze", "Formát souboru databáze", "co je soubor dbf", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů DBF a rozhraních API, která mohou vytvářet a otevírat soubory DBF.",
  "title" :"DBF - soubor databáze dBase",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## Co je soubor DBF?
Soubor s příponou .dbf je databázový soubor používaný aplikací systému správy databází s názvem **dBASE**. Zpočátku byla databáze dBASE pojmenována jako Project Vulcan; založil **Wayne Ratliff** v roce 1978. Typ souboru DBF byl představen s dBASE II v roce 1983. Uspořádává více datových záznamů s poli typu Array. Databázový software **xBase**, který je okázalý díky své kompatibilitě s širokou škálou formátů souborů; podporuje také soubory DBF.

## Formát souboru DBF
Formát souboru DBF patří do systému správy databází dBASE, ale může být kompatibilní s xBase nebo jiným DBMS softwarem. Počáteční verze souboru dbf sestávala z jednoduché tabulky, do které bylo možné přidávat, upravovat, mazat nebo tisknout data pomocí sady znaků ASCII. S postupem času byl .dbf vylepšen a byly přidány další soubory pro zvýšení funkcí a schopností databázového systému.

V moderním dBASE se soubor DBF skládá ze záhlaví, datových záznamů a značky EOF (End of File).

- Hlavička obsahuje informace o souboru, jako je počet záznamů a počet typů polí použitých v záznamech.
- Záznamy obsahují aktuální údaje.
- Konec souboru je označen jedním bajtem s hodnotou 0x1A.

### Záhlaví souboru
Rozložení hlavičky souboru v dBase je uvedeno v následující tabulce:

| Byte | Obsah | Význam |
---|---|---|
| 0 | 1 bajt | Platné dBASE pro soubor DOS; bity 0–2 označují číslo verze, bit 3 indikují přítomnost souboru poznámky dBASE pro DOS, bity 4–6 indikují přítomnost tabulky SQL, bit 7 označuje přítomnost libovolného souboru poznámky (buď dBASE m PLUS nebo dBASE pro DOS) |
| 1–3 | 3 bajty | Datum poslední aktualizace; ve formátu RRMMDD |
| 4–7 | 32bitové číslo | Počet záznamů v souboru databáze |
| 8–9 | 16bitové číslo | Počet bajtů v záhlaví |
| 10–11 | 16bitové číslo | Počet bajtů v záznamu |
| 12–13 | 2 bajty | Rezervováno; vyplnit 0 |
| 14 | 1 bajt | Vlajka označující nedokončenou transakci[poznámka 1] |
| 15 | 1 bajt | Příznak šifrování[poznámka 2] |
| 16–27 | 12 bajtů | Vyhrazeno pro dBASE pro DOS ve víceuživatelském prostředí |
| 28 | 1 bajt | Příznak produkčního souboru .mdx; 1, pokud existuje produkční soubor .mdx, 0, pokud není |
| 29 | 1 bajt | ID ovladače jazyka |
| 30–31 | 2 bajty | Rezervováno; vyplnit 0 |
| 32–n [pozn. 3][pozn. 4] | 32 bajtů každý | pole deskriptorů polí (rozvržení deskriptorů viz níže) |
| n + 1 | 1 bajt | 0x0D jako terminátor pole deskriptoru pole |

- Funkce ISMARKEDO kontroluje tento příznak (BEGIN TRANSACTION jej nastaví na 1, END TRANSACTION a ROLLBACK jej nastaví na 0).
- Pokud je tento příznak nastaven na 1, zobrazí se zpráva Databáze šifrována.
- Maximální počet polí je 255.
- n znamená poslední bajt v poli deskriptorů pole.

### Pole deskriptorů pole
Rozložení deskriptorů polí v dBASE:

| Byte | Obsah | Význam |
---|---|---|
| 0–10 | 11 bajtů | Název pole v ASCII (vyplněno nulou) |
| 11 | 1 bajt | Typ pole. Povolené hodnoty: C, D, F, L, M nebo N (významy viz následující tabulka) |
| 12–15 | 4 bajty | Rezervováno |
| 16 | 1 bajt | Délka pole v binární podobě (maximálně 254 (0xFE)). |
| 17 | 1 bajt | Počet desetinných míst pole v binárním systému |
| 18–19 | 2 bajty | ID pracovní oblasti |
| 20 | 1 bajt | Příklad |
| 21–30 | 10 bajtů | Rezervováno |
| 31 | 1 bajt | Příznak produkčního pole MDX; 1, pokud má pole indexovou značku v produkčním souboru MDX, 0, pokud ne |

### Záznamy v databázi
Každý záznam začíná příznakem odstranění (1 bajt). Pole jsou zabalena do záznamů bez oddělovačů polí. Všechna data pole jsou ASCII. V závislosti na typu pole aplikace ukládá další omezení. Zde jsou typy polí v dBase:

| Typ pole | Mnemotechnická pomůcka | Co přijímá |
-------|-----|----|
| C | Postava | Libovolný text ASCII (vyplněný mezerami až do délky pole) |
| D | Datum | Čísla a znak pro oddělení měsíce, dne a roku (interně uloženo jako 8 číslic ve formátu RRRRMMDD) |
| F | Plovoucí desetinná čárka | -, ., 0–9 (zarovnáno vpravo, doplněno mezerami) |
| L | Logické | Y, y, N, n, T, t, F, f nebo ? (při neinicializaci) |
| M | Poznámka | Libovolný text ASCII (interně uložený jako 10 číslic představujících číslo bloku .dbt, zarovnaný vpravo, doplněný mezerami) |
| N | Číselné | -, ., 0–9 (zarovnáno vpravo, doplněno mezerami) |









## Reference ##

* [.dbf – Wikipedia](https://en.wikipedia.org/wiki/.dbf)

