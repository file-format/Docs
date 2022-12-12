{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Microsoft OneNote File Format",
  "description":"Další informace o formátu ONE souboru a rozhraních API, která mohou vytvářet a otevírat JEDEN soubory.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor .ONE? ##

Soubory reprezentované příponou .ONE jsou vytvořeny aplikací Microsoft OneNote. OneNote vám umožňuje shromažďovat informace pomocí aplikace, jako byste k psaní poznámek používali svůj koncept. Soubory OneNotu mohou obsahovat různé prvky, které lze umístit na nepevná místa na stránkách dokumentu. Tyto prvky mohou obsahovat text, digitalizovaný rukopis a objekty zkopírované z jiných aplikací, včetně obrázků, kreseb a multimediálních (audio/video) klipů. Microsoft nyní nabízí online verzi OneNotu jako součást Office365, kde lze poznámky sdílet s ostatními uživateli OneNotu přes internet.

## Specifikace formátu souboru .ONE ##

Formát souboru OneNote poskytuje efektivní způsob reprezentace digitálních poznámek jako hierarchických sad oddílů a stránek. Každá stránka obsahuje uživatelsky definovaný obsah ve specifické struktuře pro reprezentaci souborovým formátem Document Object Model (DOM). Datový model pro tento formát je znázorněn níže.

### Přehled struktury ###

Jak je znázorněno na datovém modelu pro formát souboru OneNote, dokument OneNotu se skládá z různých prvků.

#### Sekce ####

Sekce je nejvyšší kontejner v souboru OneNotu, který dále obsahuje různé prvky, například:

* Stránky
* Metadata
* Vlastnosti

Metadata a vlastnosti zahrnují název sekce, identifikaci stránek, které jsou v sekci obsaženy, a pořadí, ve kterém se tyto stránky zobrazují. Termín "sekce" se týká všech stránek, které jsou v sekci, a reprezentace těchto dat v souboru úložiště revizí OneNote®, který má příponu názvu souboru .one.

#### Stránka ####

Uživatelsky definovaný obsah v dokumentu OneNotu je obsažen na stránce. Informace o stránce zahrnují text, seznamy, tabulky, názvy stránek, obrázky a značky poznámek. Stránka se skládá z obrysových objektů, ke kterým je přidána většina obsažených objektů. Každé stránce lze přiřadit název pro smysluplnou reprezentaci a také lze na stránky přímo přidávat objekty. Stránka může dále obsahovat podstránky v hierarchickém systému.

#### Vlastnosti a sady vlastností ####

Obsah OneNotu se skládá z vlastností, sad vlastností a datových objektů souborů. Sada vlastností je kolekce vlastností, která představuje určitý typ obsahu. Datový objekt souboru je blok binárních dat, který obsahuje obrázky, vložené soubory nebo audio/video obsah.

#### OneNote Notebook ####

Poznámkový blok je kolekce souborů oddílů, které jsou uloženy ve stejném adresáři. Kolekce vlastností se používá k určení nastavení, jako je pořadí oddílů v poznámkovém bloku a barva poznámkového bloku.

### Struktura souboru ###

Soubor úložiště revizí MUSÍ začínat strukturou **Header**. Zbytek souboru je rozdělen do bloků bajtů, kde velikost a struktura každého bloku je určena polem, které na něj odkazuje. Blok je dosažitelný, pokud na něj odkazuje struktura **Header** nebo pokud na něj odkazuje pole v jiném dosažitelném bloku. Data mimo strukturu **Header** a jakékoli dosažitelné bloky MUSÍ být ignorovány.

Všechny struktury jsou zarovnány na 1bajtových hranicích. Všechna celá čísla jsou podepsána, pokud není uvedeno jinak. Všechna pole jsou [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), pokud není uvedeno jinak.

#### Záhlaví ####

Hlavička souboru .ONE se skládá z částí, které obsahují různá jedinečná ID a pole pro reprezentaci informací o souboru následovně:

`guidFileType (16 bajtů):` Identifikátor GUID, který určuje typ souboru úložiště revizí. MUSÍ být jedna z hodnot z následující tabulky.


|Formát souboru|Hodnota
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bajtů):` Identifikátor GUID, který určuje identitu tohoto souboru úložiště revizí. BY MĚL být celosvětově jedinečný.

`guidLegacyFileVersion (16 bajtů):` MUSÍ být „{00000000-0000-0000-0000-00000000000}“ a MUSÍ být ignorováno.

`guidFileFormat (16 bajtů):` Identifikátor GUID, který určuje, že soubor je soubor úložiště revizí. MUSÍ být "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

`ffvLastCodeThatWroteToThisFile (4 bajty):` Celé číslo bez znaménka. MUSÍ být jedna z hodnot v následující tabulce v závislosti na typu souboru.

|Formát souboru|Hodnota
--- | --- |
|.jedna|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 bajty):` Celé číslo bez znaménka. MUSÍ být jedna z hodnot v následující tabulce v závislosti na formátu souboru tohoto souboru.


|Formát souboru|Hodnota
--- | --- |
|.jedna|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bajty):` Celé číslo bez znaménka. MUSÍ být jedna z hodnot v následující tabulce v závislosti na formátu souboru tohoto souboru.

|Formát souboru|Hodnota
--- | --- |
|.jedna|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCode ThatMayReadThisFile (4 bajty):` Celé číslo bez znaménka. MUSÍ být jedna z hodnot v následující tabulce v závislosti na formátu souboru tohoto souboru.

|Formát souboru|Hodnota
--- | --- |
|.jedna|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 bajtů):` Struktura **FileChunkReference32**, která MUSÍ mít hodnotu "fcrZero".

`fcrLegacyTransactionLog (8 bajtů):` Struktura **FileChunkReference32**, která MUSÍ být "fcrNil".

`cTransactionsInLog (4 bajty):` Celé číslo bez znaménka, které určuje počet transakcí v protokolu transakcí. NESMÍ být nula.

`cbLegacyExpectedFileLength (4 bajty):` Celé číslo bez znaménka, které MUSÍ být nula a MUSÍ být ignorováno.

`rgbPlaceholder (8 bajtů):` Celé číslo bez znaménka, které MUSÍ být nula a MUSÍ být ignorováno.

`fcrLegacyFileNodeListRoot (8 bajtů):` Struktura **FileChunkReference32**, která MUSÍ být "fcrNil".

`cbLegacyFreeSpaceInFreeChunkList (4 bajty):` Celé číslo bez znaménka, které MUSÍ být nula a MUSÍ být ignorováno.

`fNeedsDefrag (1 byte):` MUSÍ být ignorován.

`fRepairedFile (1 byte):` MUSÍ být ignorován.

`fNeedsGarbageCollect (1 byte):` MUSÍ být ignorován.

`fHasNoEmbeddedFileObjects (1 byte):` Celé číslo bez znaménka, které MUSÍ být nula a MUSÍ být ignorováno.

`guidAcestor (16 bajtů):` GUID, který specifikuje pole **Header.guidFile** souboru s obsahem, dané následující tabulkou:


|Formát souboru s obsahem|Umístění souboru s obsahem
--- | --- |
|Soubor sekce - .One|Soubor s obsahem je umístěn ve stejném adresáři jako tento soubor.
|Soubor s obsahem - .onetoc2|Soubor s obsahem je umístěn v nadřazeném adresáři tohoto souboru.

Pokud je GUID {00000000-0000-0000-0000-000000000000}, toto pole neodkazuje na soubor s obsahem.

`crcName (4 bajty):` Celé číslo bez znaménka, které určuje hodnotu CRC názvu tohoto souboru úložiště revizí. Název je reprezentací Unicode názvu souboru s jeho příponou a dalším znakem null na konci. Toto CRC se vždy vypočítává pomocí algoritmu CRC pro soubor .one, bez ohledu na tento formát souboru úložiště revizí.

`fcrHashedChunkList (12 bajtů):` Struktura **FileChunkReference64x32**, která určuje odkaz na první **FileNodeListFragment** v seznamu hašovaných bloků. Pokud je hodnota struktury **FileChunkReference64x32** "fcrZero" nebo "fcrNil", hašovaný seznam bloků neexistuje.

`fcrTransactionLog (12 bajtů):` Struktura **FileChunkReference64x32**, která určuje odkaz na první strukturu **TransactionLogFragment** v protokolu transakcí. Hodnota pole **fcrTransactionLog** NESMÍ být "fcrZero" a NESMÍ být "fcrNil".

`fcrFileNodeListRoot (12 bajtů):` Struktura **FileChunkReference64x32**, která určuje odkaz na seznam uzlů kořenových souborů. Hodnota pole **fcrFileNodeListRoot** NESMÍ být "fcrZero" a NESMÍ být "fcrNil".

`fcrFreeChunkList (12 bajtů):` Struktura **FileChunkReference64x32**, která určuje odkaz na první strukturu **FreeChunkListFragment**. Pokud je hodnota struktury **FileChunkReference64x32** "fcrZero" nebo "fcrNil", pak seznam volných bloků neexistuje.

`cbExpectedFileLength (8 bajtů):` Celé číslo bez znaménka, které určuje velikost tohoto souboru úložiště revizí v bajtech.

`cbFreeSpaceInFreeChunkList (8 bajtů):` Celé číslo bez znaménka, které BY MĚLO určovat velikost v bajtech volného místa určeného seznamem volných bloků.

`guidFileVersion (16 bajtů):` GUID. Když se mění buď hodnota pole **cTransactionsInLog** nebo pole **guidDenyReadFileVersion**, MUSÍ být **guidFileVersion** změněn na nový GUID.

`nFileVersionGeneration (8 bajtů):` Celé číslo bez znaménka, které určuje, kolikrát se soubor změnil. MUSÍ být zvýšeno, když se změní pole **guidFileVersion**.

`guidDenyReadFileVersion (16 bajtů):` GUID. Když se mění stávající obsah souboru, s výjimkou struktury **Header** souboru a nepoužívaných bloků úložiště, MUSÍ být **guidDenyReadFileVersion** změněn na nový GUID.

`grfDebugLogFlags (4 bajty):` MUSÍ být nula. MUSÍ být ignorován.

`fcrDebugLog (12 bajtů):` Struktura **FileChunkReference64x32**, která MUSÍ mít hodnotu "fcrZero". MUSÍ být ignorován.

`fcrAllocVerificationFreeChunkList (12 bajtů):` Struktura **FileChunkReference64x32**, která MUSÍ být "fcrZero". MUSÍ být ignorován.

`bnCreated (4 bajty):` Celé číslo bez znaménka, které určuje číslo sestavení aplikace, která vytvořila tento soubor úložiště revizí. BY MĚLO být ignorováno.

`bnLastWroteToThisFile (4 bajty):` Celé číslo bez znaménka, které určuje číslo sestavení aplikace, která naposledy zapisovala do tohoto souboru úložiště revizí. BY MĚLO být ignorováno.

`bnOldestWritten (4 bajty):` Celé číslo bez znaménka, které určuje číslo sestavení nejstarší aplikace, která zapisovala do tohoto souboru úložiště revizí. BY MĚLO být ignorováno.

`bnNewestWritten (4 bajty):` Celé číslo bez znaménka, které určuje číslo sestavení nejnovější aplikace, která zapisovala do tohoto souboru úložiště revizí. BY MĚLO být ignorováno.

`rgbReserved (728 bajtů):` MUSÍ být nula. MUSÍ být ignorován.

## Reference ##

* [[MS-ONESTORE] – formát souboru OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote – Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

