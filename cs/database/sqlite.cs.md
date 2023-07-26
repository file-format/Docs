{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "rozšíření", "soubor", "formát souboru", "Typ souboru databáze", "Formát souboru databáze", "Soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů SQLITE a rozhraních API, která mohou vytvářet a otevírat soubory SQLITE.",
  "title" :"Formát souboru SQLite",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Co je soubor SQLite?

Soubor s příponou .sqlite je odlehčený databázový soubor SQL vytvořený pomocí softwaru [SQLite](https://www.sqlite.org/index.html). Jedná se o databázi v samotném souboru a implementuje samostatný, plně vybavený a vysoce spolehlivý databázový stroj [SQL](/cs/database/sql/). Databázové soubory SQLite lze použít ke sdílení bohatého obsahu mezi systémy jednoduchou výměnou těchto souborů po síti. Téměř všechny mobily a počítače používají SQLite pro ukládání a sdílení dat a je to volba formátu souboru pro multiplatformní aplikace. Vzhledem ke svému kompaktnímu použití a snadné použitelnosti je součástí jiných aplikací. SQLite vazby existují pro programovací jazyky jako C, [C#](/cs/programming/cs/), [C++](/cs/programming/cpp/), [Java](/cs/programming/java/), [PHP](/cs/programming/php/ ), a mnoho dalších.

## Formát souboru SQLite

SQLite je ve skutečnosti knihovna C-Language, která implementuje SQLite RDBMS pomocí formátu souboru SQLite. S vývojem nových zařízení každý den byl jeho formát souborů zpětně kompatibilní, aby vyhovoval starším zařízením. Formát souboru SQLite je považován za dlouhodobý archivační formát pro data.

### Soubor databáze

Databáze SQLite je plně udržována prostřednictvím dvou souborů.
* Soubor hlavní databáze - Obsahuje kompletní stav databáze SQLite
* Rollback Journal - Ukládá další informace do druhého souboru a používá se při provádění transakcí. V případě, že je SQLite v režimu WAL, je udržován soubor protokolu zapisovací hlavy.

#### Soubor deníku

Tento soubor je určen k uchování všech informací pro případ, že by poslední transakce nemohla být dokončena v případech, jako je například havárie počítače. Tento soubor se používá k obnovení souboru databáze do konzistentního stavu.

#### Stránky

Hlavní databázový soubor SQLite se skládá z jedné nebo více stránek. V každém okamžiku má každá stránka v hlavní databázi jedno použití, které je jedním z následujících:

* Stránka lock-byte
* Bezplatná stránka
* Freelist kmenová stránka
* Bezplatná listová stránka
* Stránka b-stromu
* Vnitřní stránka stolu B-strom
* Listová stránka tabulky B-strom
* Vnitřní stránka indexu b-stromu
* Indexová listová stránka b-stromu
* Stránka přetečení užitečného zatížení
* Stránka s ukazatelem mapy

Velikost databázových souborů SQLite se může pohybovat od několika kilobajtů do několika gigabajtů.

### Hlavička SQLite

Hlavička databáze SQLite se nachází v prvních 100 bytech databázového souboru. Každý platný databázový soubor SQLite začíná 16 bajty (v hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Podrobnosti polí záhlaví jsou jako v následující tabulce.

|Odsazení|Velikost|Popis|
---|---|---|
|0|16|Řetězec záhlaví: "formát SQLite 3\000"|
|16|2|Velikost stránky databáze v bajtech. Musí to být mocnina dvou mezi 512 a 32768 včetně nebo hodnota 1 představující velikost stránky 65536.|
|18|1|Verze zápisu formátu souboru. 1 pro dědictví; 2 pro WAL.|
|19|1|Čtená verze formátu souboru. 1 pro dědictví; 2 pro WAL.|
|20|1|Bajty nevyužitého "rezervovaného" prostoru na konci každé stránky. Obvykle 0.|
|21|1|Maximální podíl vloženého užitečného zatížení. Musí být 64.|
|22|1|Minimální podíl vloženého užitečného zatížení. Musí být 32.|
|23|1|Zlomek užitečného zatížení listu. Musí být 32.|
|24|4|Počítadlo změn souboru.|
|28|4|Velikost databázového souboru ve stránkách. "Velikost databáze v záhlaví".|
|32|4|Číslo první hlavní stránky freelistu.|
|36|4|Celkový počet stránek freelistu.|
|40|4|Soubor cookie schématu.|
|44|4|Číslo formátu schématu. Podporované formáty schématu jsou 1, 2, 3 a 4.|
|48|4|Výchozí velikost mezipaměti stránky.|
|52|4|Číslo stránky největší kořenové stránky b-stromu v režimu automatického vakua nebo přírůstkového vakua, jinak nula.|
|56|4|Kódování textu databáze. Hodnota 1 znamená UTF-8. Hodnota 2 znamená UTF-16le. Hodnota 3 znamená UTF-16be.|
|60|4|"Uživatelská verze" tak, jak ji čte a nastavuje pragma user_version.|
|64|4|Pravda (nenulová) pro režim přírůstkového vakua. False (nula) jinak.|
|68|4|"ID aplikace" nastavené PRAGMA application_id.|
|72|20|Vyhrazeno pro rozšíření. Musí být nula.|
|92|4|Číslo platné verze.|
|96|4|SQLITE_VERSION_NUMBER|

## Reference ##

* [Formát souboru SQLite – SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite – Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite – specifikace jazyka C](https://www.sqlite.org/c3ref/intro.html)

