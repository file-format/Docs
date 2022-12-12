{
  "date" : "2020-08-20",
  "keywords" :[ "soubor otf", "formát souboru otf", "co je soubor otf", "soubor", "příklad otf", "přípona souboru otf", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - TrueType Font File Format",
  "description":"Další informace o formátu souboru OTF a rozhraních API, která mohou vytvářet a otevírat soubory OTF.",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Co je soubor OTF?

Soubor s příponou .otf označuje formát písma OpenType. Formát písma OTF je škálovatelnější a rozšiřuje stávající funkce formátů [TTF](/cs/font/ttf/) pro digitální typografii. OTF, vyvinutý společnostmi Microsoft a Adobe, kombinuje funkce formátů písem PostScript a TrueType. Díky tomu je formát OTF vhodný pro většinu systémů zápisu, a proto je jednotně používán na hlavních počítačových platformách. Formát písma OpenType podporují Mac OS X a Windows 2000 a novější.

## Stručná historie

Požadavek písem OpenType vznikl jako požadavek na výraznější formát písma, který by zvládal jemnou typografii. Kromě toho byl zaměřen na splnění požadavků na komplexní chování mnoha světových psacích systémů. Microsoft se na počátku 90. let pokusil licencovat pokročilou typografickou technologii Applu, známou jako GX Typography. To se nepovedlo a v důsledku toho začal Microsoft v roce 1994 vylepšovat svou vlastní technologii písem TrueType. Úpravy zahrnovaly také zavedení vhodnějšího formátu písem, který také splňuje vlastnosti formátů písem Type 1 (PostScript) Adobe.

Společnost Adobe se v roce 1996 připojila k Microsoftu ve snaze nahradit jak TrueType od Apple, tak vlastní formáty písem Type 1. Výsledkem byla kombinace obou základních formátů písem, která překonala omezení a přidala nová rozšíření. Tato nová technologie byla představena ve stejném roce pod názvem **OpenType**.

## Specifikace formátu souboru OTF

Specifikace OTF jsou veřejně dostupné společností Microsoft a lze na ně odkazovat z pohledu vývojáře. Stejně jako TTF používá stejnou strukturu kontejneru „sfnt“ a je kompatibilní se specifikacemi TrueType. Data uvnitř souboru písem OpenType se používají pro různé účely, jako je výpočet rozvržení textu, definování glyfů jako obrysů TrueType nebo Compact Font Format (CFF), poskytování monochromatických nebo barevných bitmap nebo dokumentů SVG jako alternativních popisů glyfů a metadatové informace.

### Datové typy OTF
Soubory OTF používají následující datové typy, které jsou všechny v Big Endian.

|Typ dat| Popis|
---|---|
|uint8| 8bitové celé číslo bez znaménka.|
|int8| 8bitové celé číslo se znaménkem.|
|uint16| 16bitové celé číslo bez znaménka.|
|int16| 16bitové celé číslo se znaménkem.|
|uint24| 24bitové celé číslo bez znaménka.|
|uint32| 32bitové celé číslo bez znaménka.|
|int32| 32bitové celé číslo se znaménkem.|
|Opraveno| 32bitové číslo s pevnou řádovou čárkou se znaménkem (16.16)|
|FWORD| int16, který popisuje množství v jednotkách návrhu písma.|
|UFWORD| uint16, který popisuje množství v jednotkách návrhu písma.|
|F2DOT14| 16bitové pevné číslo se znaménkem s nejnižšími 14 bity zlomku (2,14).|
|LONGDATETIME| Datum a čas v sekundách od půlnoci 12:00, 1. ledna 1904, UTC. Hodnota je reprezentována jako 64bitové celé číslo se znaménkem.|
|Značka| Pole čtyř uint8 (délka = 32 bitů) používané k identifikaci tabulky, osy variace návrhu, skriptu, jazykového systému, funkce nebo základní linie|
|Offset16| Krátký offset na tabulku, stejně jako uint16, NULL offset = 0x0000|
|Offset32| Dlouhý offset k tabulce, stejně jako uint32, NULL offset = 0x00000000|
|Verze16Dot16| Zabalená 32bitová hodnota s čísly hlavních a vedlejších verzí. (Viz Čísla verzí tabulky.)|

### Adresář tabulek OTF

Soubor OTF začíná adresářem tabulky. Tento adresář je kolekce nejvyšší úrovně tabulek v souboru písem. V závislosti na počtu písem v souboru může být adresář tabulky umístěn na jiném místě v souboru. Například v případě, že soubor s písmem obsahuje pouze jedno písmo, adresář tabulky začíná na bajtu 0 souboru. V případě více kolekce písem OpenType,
začátek adresáře tabulky je uveden v TTCHeader.

|Typ |Název |Popis|
---|---|---|
|uint32 |sfntVersion| 0x00010000 nebo 0x4F54544F ('OTTO')|
|uint16| numTables |Počet tabulek.|
|uint16| searchRange |Maximální mocnina 2 menší nebo rovno numTables, krát 16 ((2\**podlaží(log2(numTables))) * 16, kde „**“ je operátor umocnění.|
|uint16 |entrySelector Log2 maximálního výkonu 2 menšího nebo rovného numTables (log2(searchRange/16), což je rovno floor(log2(numTables))).|
|uint16 |rangeShift |numTables krát 16, mínus searchRange ((numTables * 16) - searchRange).|
|tableRecord| tableRecords[numTables] |Pole záznamů tabulek—jeden pro každou tabulku nejvyšší úrovně ve fontu|


### Záznam tabulky

Pro každou tabulku nejvyšší úrovně v písmu existuje záznam tabulky, který se skládá z následujících polí.

|Typ| Jméno| Popis|
---|---|---|
|Značka| tableTag| Identifikátor tabulky.|
|uint32| kontrolní součet| Kontrolní součet pro tuto tabulku.|
|Offset32| offset| Odsazení od začátku souboru písma.|
|uint32| délka Délka tohoto stolu.|

Každá tabulka v souboru písem OpenType je reprezentována názvy známými jako značky tabulky. Je nutné, aby všechny záznamy v poli byly seřazeny vzestupně podle značky.

## Reference
* [Specifikace písem OpenType od společnosti Microsoft](https://docs.microsoft.com/en-us/typography/opentype/spec/overview)
* [Přehled TrueType](https://docs.microsoft.com/en-us/typography/truetype/)

