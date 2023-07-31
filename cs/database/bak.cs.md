{
  "date" : "2020-11-11",
  "keywords" :[ "BAK", "přípona", "soubor", "formát souboru", "typ souboru BAK", "přípona souboru BAK", "typ souboru databáze", "formát souboru databáze", "soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů BAK a rozhraních API, která mohou vytvářet a otevírat soubory BAK.",
  "title" :"Formát souboru BAK - soubor zálohy databáze",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## Co je soubor BAK?

Soubor s příponou .bak je obvykle záložní soubor, který používají různé softwarové nástroje k ukládání záloh dat. Z pohledu databáze je soubor BAK používán Microsoft SQL Serverem pro ukládání obsahu databáze. Všechna data a soubory spojené s databází jsou uloženy v tomto formátu souboru, aby mohly být načteny v případě, že by se databáze z jakéhokoli důvodu mohla poškodit nebo zneplatnit. Záložní soubory mohou být z bezpečnostních důvodů uloženy a indexovány na jiných serverech. Soubory BAK může vytvářet několik aplikací, například SQL Server Management Studio, Transact-SQL a Windows PowerShell.

## Formát souboru BAK

Interní podrobnosti souboru BAK nejsou známy, ale obecně se předpokládá, že je založen na formátu Microsoft Tape Format (MTF). Specifikace MTF jsou k dispozici a lze na ně odkazovat pro pochopení struktury souboru. Dokument poskytuje podrobnosti o úložišti MTF pro každého, kdo má obecné znalosti o operacích správy úložiště, páskových jednotkách a souborových systémech.

### Soubory dat

Datová sada je kolekce objektů zapsaných na paměťové médium (páska, optický disk atd.) během zálohování nebo obnovy dat. V případě velkého objemu dat se datové sady skládají z více médií.

### Základní prvky MTF

Soubor MTF se skládá z některých základních prvků, které tvoří jeho stavební bloky. Tyto prvky jsou:

#### Deskriptorové bloky

Deskriptorové bloky (DBLK) se používají pro řízení formátu a tvoří primární základy souboru MTF. Jeden soubor MTF definuje více DBLK pro každou jedinečnou roli. Každý DBLK je blok dat s proměnnou délkou, který je rozdělen do následujících čtyř částí:

* `Common Block Header` - Struktura pevné délky, která je společná pro všechny DBLK. Toto je jediné záhlaví bloku, které je vyžadováno.
* `DBLK Type Information` - Blok s pevnou délkou specifický pro typ DBLK, který je definován
* `Data operačního systému` - Specifická data, která jsou definována na základě typu DBLK a operačních systémů
* `DBLK Information` - Specifické informace DBLK s proměnnou délkou, které nelze uložit s informacemi DBLK s pevnou délkou.

 {{< figure src="../bak.png" alt="Záložní formát souboru Microsoft SQL" >}}

#### Datový tok

Datové toky v souboru MTF se používají pro zapouzdření a zarovnání dat. Skládá se z hlavičky proudu, po které následují data proudu. Záhlaví proudu může zapouzdřit pouze jeden typ dat proudu.

{{< figure src="../bak_datastream.png" alt="Záložní formát souboru Microsoft SQL" >}}

#### FileMarks

Filemark se používá pro logické oddělení a rychlý přístup v rámci média. Souborové značky jsou emulovány ovladačem zařízení nebo použitím bloku Soft Filemark Descriptor v případě, že používané zařízení neposkytuje souborové značky.

## Reference ##

* [[MS-BCP]: Formát hromadného kopírování](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5?redirectedfrom=MSDN)

