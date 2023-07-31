{
  "date" : "2020-08-20",
  "keywords" :[ "soubor ttf", "formát souboru ttf", "co je soubor ttf", "soubor", "příklad ttf", "přípona souboru ttf", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - TrueType Font File Format",
  "description":"Písma TrueType (TTF) jsou založena na specifikacích technologie digitálních písem původně navržených společností Apple, Inc. Apple i Microsoft používaly TTF na operačních systémech Mac a Windows.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Co je soubor TTF?

Soubor s příponou .ttf představuje soubory písem založené na technologii písem specifikace TrueType. Původně byl navržen a spuštěn společností Apple Computer, Inc pro Mac OS a později byl přijat společností Microsoft pro OS Windows. Písma TrueType poskytují nejvyšší kvalitu zobrazení na obrazovkách počítačů a tiskáren bez jakékoli závislosti na rozlišení. Všechny moderní aplikace využívající fonty jsou schopny pracovat se soubory TTF. Soubory písem TTF jsou volně dostupné přes internet a lze je také převést do jiných formátů souborů písem, jako jsou OTF a WOFF.

## Stručná historie

Formát písma TTF, navržený společností Apply Computer, Inc v 80. letech pro MacOS, byl zaměřen na vyřešení některých technických omezení formátu Type 1 společnosti Adobe. Apple začlenil podporu TrueType písem do Mac v roce 1991. Cílem designu za písmy TTF byla efektivita při ukládání a zpracování a rozšiřitelnost. Na základě této rozšiřitelnosti lze existující písma převést do formátu TrueType.

Microsoft poprvé použil písma TrueType ve Windows 3.1 v dubnu 1992 poté, co Apple souhlasil s licencí TrueType společnosti Microsoft. Vylepšila mechanismus rasterizace a zlepšila jeho účinnost a výkon.

## Specifikace formátu souborů True Type

Soubor písem TrueType je binární soubor, který se skládá ze sekvence zřetězených tabulek. Každá tabulka je posloupnost slov a má název známý jako „Tag“. Každá značka je datového typu uint32 a skládá se ze čtyř znaků. První tabulka v souboru je adresář písem, který umožňuje přístup k dalším tabulkám v souboru písem. Data písem jsou obsažena v dalších tabulkách za tabulkou adresáře písem. Vzhledem k tomu, že každá tabulka je přístupná pomocí své značky, mohou se tabulky v souboru objevit v libovolném pořadí.

Požadované tabulky a jejich názvy značek jsou uvedeny v následující tabulce.

|**Značka**|**Tabulka**|
---|---|
|'cmap'| mapování znaků na glyfy|
|'glyf'| glyfové údaje|
|'hlava'| záhlaví písma|
|'hhea'| horizontální záhlaví|
|'hmtx'| horizontální metriky|
|'loca'| index k umístění|
|'maxp'| maximální profil|
|'jméno'| pojmenování|
|'příspěvek'| PostScript|

### Typy dat
Písma TrueType používají standardní celé číslo a další datové typy uvedené v následující tabulce.

|**Typ dat** | **Popis** |
---|---|
|shortFrac| 16bitový zlomek se znaménkem|
|Opraveno| 16,16bitové číslo s pevnou řádovou čárkou se znaménkem|
|FWord| 16bitové celé číslo se znaménkem, které popisuje veličinu v jednotkách FJ, nejmenší měřitelnou vzdálenost v em prostoru.|
|uFWord| 16bitové celé číslo bez znaménka, které popisuje veličinu v jednotkách FJ, nejmenší měřitelnou vzdálenost v em prostoru.|
|F2Dot14| 16bitové pevné číslo se znaménkem, přičemž spodních 14 bitů představuje zlomek.|
|longDateTime| Dlouhý vnitřní formát data v sekundách od půlnoci 12:00, 1. ledna 1904. Je reprezentován jako 64bitové celé číslo se znaménkem.|

### Adresář písem

První tabulka v písmu TrueType je adresář písem, který poskytuje přístup k informacím potřebným pro přístup k datům v jiných tabulkách. Dále se skládá z:

* `Offset subtable` - uchovává záznamy o tabulkách ve fontu a poskytuje informace o offsetu pro přístup ke každé tabulce v adresáři
* `Table Directory` - Obsahuje položky pro každou tabulku ve fontu

#### Offsetová podtabulka
Podtabulka offsetu je uvedena níže.

|**Typ**|**Název**|**Popis**|
---|---|---|
|uint32| typ scaleru| Značka označující škálovač OFA, který se má použít k rastrování tohoto písma; více informací naleznete v poznámce k typu scaleru níže.|
|uint16| numTables| počet stolů|
|uint16| rozsah hledání| (maximální výkon 2 <= numTables)*16|
|uint16| entrySelector| log2(maximální výkon 2 <= numTables)|
|uint16| rangeShift| numTables*16-searchRange|

#### Adresář tabulky
Adresář tabulky následuje hned za offsetovou podtabulkou. Jeho struktura je uvedena v následující tabulce.

|**Typ**|**Název**|**Popis**|
---|---|---|
|uint32| tag| 4bajtový identifikátor|
|uint32| kontrolní součet| kontrolní součet pro tuto tabulku|
|uint32| offset| posun od začátku sfnt|
|uint32| délka| délka této tabulky v bytech (skutečná délka bez vycpávky)|

Každá tabulka v souboru písem musí mít svůj vlastní záznam v adresáři tabulky. Záznamy v tabulce musí být seřazeny vzestupně podle značky.


## Reference
* [Referenční příručka písem TrueType](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [Přehled TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

