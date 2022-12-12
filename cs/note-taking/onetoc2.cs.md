{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Microsoft OneNote File Format",
  "description":"Další informace o formátu souboru ONETOC2 a rozhraních API, která mohou vytvářet a otevírat soubory ONETOC2.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Co je ONETOC2? ##

Ti, kteří pracovali s aplikací [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app), si mohli všimnout přítomnosti souborů .onetoc2 ve složce notebooku. Microsoft OneNote vytvoří binární soubor .onetoc2 jako obsah pro uchování rejstříku o řazení různých oddílů pro psaní poznámek v poznámkovém bloku. Poznámkový blok je kolekce souborů oddílů, které jsou uloženy ve stejném adresáři. Soubor .onetoc2 používá kolekci vlastností k určení nastavení, jako je pořadí oddílů v poznámkovém bloku a barva poznámkového bloku.

Když vytvoříte poznámkový blok ve OneNotu 2016, automaticky se uloží v novém formátu souboru 2010–2016. Tento formát budete potřebovat, pokud chcete, aby všechny funkce ve OneNotu 2016, jako jsou matematické rovnice a propojené poznámky, fungovaly správně.

## Formát souboru ONETOC2 ##

Formát souboru .onetoc2 je reprezentován jako OneNote Revision Store File Format a je sbírkou struktur, které určují úložiště revizí uspořádané do prostorů objektů s křížovými odkazy, obsahující objekty se sadami vlastností a obsahující transakční protokol pro zajištění integrity souboru napříč asynchronními píše. Kompletní specifikace pro formát souboru .onetoc2 jsou k dispozici [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) a lze je použít pro vývoj aplikací .

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

`guidLegacyFileVersion (16 bajtů):` MUSÍ být „{00000000-0000-0000-0000-000000000000}“ a MUSÍ být ignorováno.

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
:


|Formát souboru|Hodnota
--- | --- |
|.jedna|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCode ThatMayReadThisFile (4 bajty):` Celé číslo bez znaménka. MUSÍ být jedna z hodnot v následující tabulce v závislosti na formátu souboru tohoto souboru.


|Formát souboru|Hodnota
--- | --- |
|.jedna|0x0000002A
|.onetoc2|0x0000001B

## Reference ##

* [[MS-ONESTORE] – formát souboru OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote – Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

