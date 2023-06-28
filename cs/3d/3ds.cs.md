{
  "date" : "2019-10-11",
  "keywords" :[ "3DS", "soubor", "formát", "typ souboru", "přípona", "co je soubor 3DS?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů 3DS a rozhraních API, která mohou otevírat a vytvářet soubory 3DS.",
  "title" :"Formát souboru 3DS",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor 3DS?

Soubor s příponou .3ds představuje formát mesh souboru 3D Sudio (DOS) používaný aplikací Autodesk 3D Studio. Autodesk 3D Studio je na trhu 3D formátů souborů od 90. let a nyní se vyvinulo na 3D Studio MAX pro práci s 3D modelováním, animacemi a renderováním. Soubor 3DS obsahuje data pro 3D reprezentaci scén a obrázků a je jedním z oblíbených formátů souborů pro import a export 3D dat. Bere v úvahu informace, jako jsou umístění kamer, data sítě, informace o osvětlení, konfigurace výřezů, data vyhlazovacích skupin, bitmapové odkazy a atributy, aby se vytvořily vrcholy a polygony pro vykreslení scény.

## Formát souboru 3DS – Další informace
3DS je ve své podstatě binární formát souborů a řídí se předem definovanou strukturou pro ukládání a získávání dat. Binární formát souboru umožňuje rychlejší menší formát souboru 3DS ve srovnání s textovými formáty souborů. Data uvnitř souboru 3DS jsou uložena ve formě kusů.

### 3DS kus

Každý blok v souboru 3DS je blok dat, který obsahuje ID, délku bloku pro umístění dalšího bloku a samotná data. ID bloku umožňuje čtenářům formátu souborů 3DS přeskočit bloky, které nerozpoznají. Pomáhá také v rozšiřitelnosti formátu. Každý blok ukládá informace související s tvary, osvětlením a informacemi o zobrazení, které společně vykreslují scénu. Bloky jsou uspořádány v hierarchické struktuře v souboru 3DS a v reprezentaci připomínají strom objektů dokumentu XML.

**ID bloku:** První dva bajty bloku představují identifikátor bloku, který umožňuje čtečce souboru rozhodnout, zda jej má vzít v úvahu při čtení, nebo jej přeskočit.

**Délka bloku:** Za ID bloku následuje 4bajtové celé číslo (v little-endian), které představuje délku bloku. Tato délka zahrnuje také délku dat, délku jejich dílčích bloků a 6bajtovou hlavičku.

**Payload:** Po délce bloku následují skutečné bajty dat pro blok, za nimiž následují jeho dílčí bloky ve stejné hierarchické struktuře, kterou lze rozšířit na několik úrovní.

### Struktura kusu

Hierarchická struktura jednoduchého bloku je uvedena níže:

**Kousek**

|začátek|konec|velikost|název
--- | --- | --- | ---
|0|1|2|ID bloku
|2|5|4|Další blok

Bloky mají hierarchii, která je identifikována jejich ID. Soubor 3ds má primární ID bloku 4D4Dh. Toto je vždy první část souboru. V primární části jsou hlavní části.

**Hlavní kousky**

|id|Popis
--- | ---
|3D3D|Začátek dat sítě objektů.
|B000|Začátek dat klíčového snímku.

Ukazatel dalšího bloku za blokem ID ukazuje na další hlavní blok.
Přímo za hlavním chunkem je další chunk. Může se jednat o jakýkoli jiný typ chunku přípustný v rámci jeho rozsahu hlavních chunků.
Pro popis sítě (3D3D) mohou být libovolné násobky.

**Podčásti 3D3D – síťový blok**


|id|Popis
--- | ---
|1100|neznámý
|1200|Barva pozadí.
|1201|neznámý
|1300|neznámý
|1400|neznámý
|1420|neznámý
|1450|neznámý
|1500|neznámý
|2100|Blok okolních barev
|2200|mlha?
|2201|mlha?
|2210|mlha?
|2300|neznámý
|3000|neznámý
|4000|Blok objektů
|7001|neznámý
|AFFF|neznámý

**Podčásti 4000 – blok popisu objektu**
První položkou Subchunk 4000 je řetězec ASCIIZ názvu objektu.
Pamatujte, že objektem může být síť, světlo nebo kamera.

|id|Popis
--- | ---
|4010|neznámý
|4012|stín?
|4100|Trojúhelníkový polygonový objekt
|4600|Světlo
|4700|Fotoaparát

## Reference

* [Formáty geometrických souborů – Autodesk](https://help.autodesk.com/view/3DSMAX/2015/ENU/?guid=GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32)
* [3DS – z Wikipedie](https://en.wikipedia.org/wiki/.3ds)
