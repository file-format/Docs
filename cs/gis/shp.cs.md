{
  "date" : "2019-10-11",
  "keywords" :[ "soubor shp", "formát souboru shp", "co je soubor shp", "soubor", "příklad shp", "přípona souboru shp", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - ESRI Shapefile",
  "description":"Další informace o formátu souborů SHP a rozhraních API, která mohou vytvářet a otevírat soubory SHP.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor SHP?

SHP je přípona souboru pro jeden z primárních typů souborů používaných pro reprezentaci ESRI Shapefile. Představuje geoprostorové informace ve formě vektorových dat pro použití v aplikacích geografických informačních systémů (GIS). Formát byl vyvinut jako otevřené specifikace za účelem usnadnění interoperability mezi ESRI a dalšími softwarovými produkty.

## Reprezentace dat

Jak již bylo zmíněno, formát shapefile popisuje geoprostorové informace datové sady jako vektorové prvky. Mezi tyto vektorové vlastnosti patří:

* body
* čáry
* polygony

Tyto prvky v kombinaci mohou představovat téměř jakýkoli typ tvarů, jako jsou vodní studny, hranice zemí, prostorové body, tok řek, jezera atd. Každý vektorový prvek může mít atributy, které ve skutečnosti definují účel tohoto prvku. Například soubor shapefile obsahující města Los Angeles může mít název města a teplotu jako atributy, které poskytují smysluplnou reprezentaci prostorových dat.

## Přidružené soubory

Samostatný soubor shp nelze použít v softwarových aplikacích k tomu, aby určovaly význam dat, která obsahuje. Aby bylo možné porozumět informacím obsaženým v takovém souboru, shapefile využívá následující dodatečné povinné soubory.

* shx soubor - indexový soubor
* soubor dbf – soubor dBASE, který ukládá všechny atributy tvarů v hlavním souboru
* soubor prj - ukládá informace o projektu souboru

Mohou existovat i další volitelné soubory, které mají stejný název jako hlavní soubor.

## Specifikace formátu souboru SHP

Otevřené specifikace shapefile jsou k dispozici online od ESRI ve formě [Technical Description] (http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) a podrobně rozvádí celkovou strukturu souboru. Informace v hlavním souboru .shp se skládají z hlaviček a záznamů. Po hlavičce souboru s pevnou délkou následují záznamy s proměnnou délkou, kde každý záznam je tvořen hlavičkou záznamu s pevnou délkou následovanou obsahem záznamu s proměnnou délkou.

### Hlavní záhlaví souboru SHP

Hlavní záhlaví souboru začíná od začátku souboru a je dlouhé 100 bajtů. Organizace této hlavičky hlavního souboru spolu s pozicí bajtů, hodnotou, typem a pořadím bajtů je uvedena v následující tabulce.


|Bajty|Pole|Hodnota|Typ|Pořadí bajtů
---|---|---|---|---|
|0-3|Kód souboru|9994|Celé číslo|Big Endian
|4-23|Nepoužité|0|Celé číslo|Big Endian
|24-27|Délka souboru|Délka souboru|Celé číslo|Big Endian
|28-31|Verze|1000|Celé číslo|Little Endian
|32-35|Typ tvaru|Typ tvaru|Celé číslo|Little Endian
|36-67|Minimální ohraničující obdélník|Xmin, Ymin, Xmax a Ymax|double|Little Endian
|68-83|Bounding Box|Zmin, Zmax|double|Little Endian
|84-99|Vymezovací rámeček|Mmin, Mmax|dvojitý|

Je třeba poznamenat, že hodnota délky souboru je celková délka souboru v 16bitových slovech, která také zahrnuje padesát 16bitových slov tvořících hlavičku.

#### Typy tvarů

Hodnoty polí typů tvarů ve výše uvedené tabulce jsou následující:


|Hodnota|Typ tvaru
---|---|
|0|Nulový tvar
|1|Bod
|3|Křivka
|5|Mnohoúhelník
|8|MultiPoint
|11|BodZ
|13|PolyLineZ
|15|PolygonZ
|18|MultiPointZ
|21|BodM
|23|PolyLineM
|25|MnohoúhelníkM
|28|MultiPointM
|31|MultiPatch

### Záznamy dat ###

Za hlavičkou hlavního souboru následují záznamy s proměnnou délkou, kde každý záznam se skládá z hlavičky záznamu s pevnou délkou následované obsahem záznamu s proměnnou délkou.

#### Záhlaví záznamu ####

Hlavička záznamu obsahuje informaci o čísle záznamu a délce obsahu záznamu v pevné délce 8 bajtů. Organizace záhlaví záznamu je následující:


|Bajty|Pole|Hodnota|Typ|Pořadí bajtů
---|---|---|---|---|
|0-3|Číslo záznamu|Číslo záznamu|Celé číslo|Velké
|4-7|Délka záznamu|Délka záznamu|Celé číslo|Velká

#### Obsah záznamu ####

Obsah záznamu shapefile se skládá z typu tvaru následovaného geometrickými daty pro tento tvar. Typ tvaru 0 představuje nulový tvar, který nemá pro tvar žádná geometrická data. Délka obsahu záznamu je odrazem tvarových částí a vrcholů. Vezměme si příklad typu Bodový tvar, abychom vysvětlili, jak záznam obsahuje informace o takovém typu tvaru.

Bod představuje určitou geografickou polohu v pořadí X,Y, kde každá souřadnice je reprezentována hodnotou s dvojnásobnou přesností. Následující tabulka ukazuje uspořádání typu tvaru Bod.


|Bajty|Typ tvaru|Hodnota|Typ|Číslo|Pořadí bajtů
---|---|---|---|---|---|
|0-3|Typ tvaru|1|Celé číslo|1|Malý
|4-11|X|X|double|1|Malý
|12-19|Y|Y|double|1|Malý

Příklady dalších typů tvarů lze nalézt v dokumentu technického popisu ESRI.

## Reference ##

* [Technický popis ESRI Shapefile] (http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) od ESRI

