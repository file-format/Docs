{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru EDB - soubor databáze pošty Exchange",
  "description":"Další informace o formátu souboru EDB a rozhraních API, která mohou vytvářet a otevírat soubory EDB.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## Co je soubor EDB?

Soubor s příponou .edb je databáze poštovních schránek vytvořená serverem Microsoft Exchange Server k ukládání dat souvisejících s poštou. EDB, databáze Exchange, ukládá zprávy, které jsou v procesu a nejsou SMTP. EDB jsou také známé jako soubory databáze Extensible Storage Engine (ESE) a ukládají soubory pomocí struktury b-stromu. Jako úložné soubory lze soubory EDB převést do jiných formátů souborů pro ukládání pošty, jako je [PST](/cs/email/pst/) a [OST](/cs/email/ost/).

## Formát souboru EDB

Nejsou k dispozici žádné oficiální/otevřené specifikace formátu souboru EDB, na které lze odkazovat. Určitého pokroku bylo dosaženo v oblasti zpětného inženýrství formátu souboru, což vedlo k částečnému dekódování specifikací. Podle nich se soubor EDB skládá z:
* Záhlaví souboru - Obsahuje informace o záhlaví souboru databáze
* Stránky s pevnou velikostí - Obsahuje databázi, která se skládá z tabulek a indexů

### Záhlaví souboru databáze
Záhlaví souboru databáze se nachází na první stránce databáze a má alespoň 668 bajtů. Záhlaví souboru obsahuje kromě jiných polí také `File Format Version` a `File Type`.

#### Typy souborů
|Typ|Popis
---|---|
|0| Databáze|
|1| Streamování|

`Poznámka:` Identifikátory pro tyto typy nejsou známy.

#### Verze formátu souboru
Původní formát EDB začal v dubnu 1997 a dále se vyvíjel kvůli změnám.

|Datum revize|Verze|Revize|popis
---|---|---|---|
|dubna 1997| 0x00000620|0x00000000| Původní verze operačního systému Beta.|
|květen 1997 |0x00000620|0x00000001| Přidejte do katalogu sloupce pro podmíněné indexování a STARÉ.|
|Červen 1997|0x00000620|0x00000002|Přidat příznak fLocalizedText do IDB.|
|Oct 1997|0x00000620|0x00000003|Přidat SPLIT_BUFFER do kořenových stránek stromu prostoru.|
|Leden 1998|0x00000620|0x00000002|Vraťte revizi, aby ESE97 zůstala dopředně kompatibilní.|
||0x00000620|0x00000003|Přidat do katalogu nové označené sloupce ("CallbackData" a "CallbackDependencies").|
|Květen 1998|0x00000620|0x00000004|Podpora super dlouhé hodnoty (SLV): signSLV, fSLVEexistuje v dbheader.|
|Květen 1998|0x00000620|0x00000005|Nový vesmírný strom SLV.|
|říjen 1998|0x00000620|0x00000006|Mapa prostoru SLV.|
|Prosinec 1998|0x00000620|0x00000007|4bajtový IDXSEG.|
|Leden 1999|0x00000620|0x00000008|Nový formát sloupce šablony.|
|Červen 1999|0x00000620|0x00000009|Seřazené sloupce šablony. Používá se ve Windows XP SP3|
||0x00000620|0x0000000b|Obsahuje záhlaví stránky s kontrolním součtem ECCUsed in Exchange|
||0x00000620|0x0000000c|Používá se ve Windows Vista (SP0)|
||0x00000620|0x00000011|Podpora stránek o velikosti 2 kB, 16 kB a 32 kB.Rozšířené záhlaví stránky s dalšími kontrolními součty ECC.Komprese sloupců.Nápovědy k mezerám.Použito ve Windows 7 (SP0)|
|Květen 1999|0x00000623|0x00000000|Nový manažer vesmíru.|

### Soubory databáze

Databázový soubor EDB obsahuje schéma pro všechny tabulky v databázi. Kromě toho také obsahuje záznamy pro všechny databázové tabulky a indexy pro tabulky. Jeho umístění je určeno následujícími identifikátory.

* JetCreateDatabase
* JetCreateDatabase2
* Databáze JetAttach
* JetAttachDatabase2

Na jejich základě lze hodnotit stav databáze následovně.

|Hodnota|Identifikátor|Popis
---|---|---|
|1|JET_dbstateJustCreated|Databáze byla právě vytvořena.|
|2|JET_dbstateDirtyShutdown|K tomu, aby byla databáze použitelná nebo přenosná, vyžaduje spuštění tvrdé nebo měkké obnovy. Člověk by se neměl pokoušet přesouvat databáze v tomto stavu.|
|3|JET_dbstateCleanShutdown|Databáze je v čistém stavu. Databázi lze připojit bez jakýchkoliv souborů protokolu.|
|4|JET_dbstateBeingConverted|Probíhá aktualizace databáze.|
|5|JET_dbstateForceDetachInternal|Tato hodnota je zavedena ve WindowsXP|
 

## Reference
* [Specifikace databázového souboru (EDB) Extensible Storage Engine (ESE)](https://github.com/libyal/libesedb/tree/main/documentation)

