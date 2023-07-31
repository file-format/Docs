{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "přípona", "soubor", "formát souboru", "Typ souboru databáze", "Formát souboru databáze", "Soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru ACCDT a rozhraních API, která mohou vytvářet a otevírat soubory ACCDT.",
  "title" :"ACCDT - Formát souboru šablony databáze Microsoft Access 2007",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Co je soubor ACCDT?

Soubor s příponou .accdt je soubor šablony databáze Microsoft Access, který obsahuje předdefinované prvky databáze. Tyto prvky jsou kolekcí struktur, které definují databázové aplikace, jako jsou databázová schémata pro ukládání dat, popis rozvržení pro pohledy na data a metadata popisující databázi. Jako soubory šablon lze soubory ACCDT použít k vytváření databází na základě nastavení šablon, které jsou v nich k dispozici. Výsledné databázové soubory jsou uloženy jako soubory [ACCDB](/cs/database/accdb/) a naplněny daty v tabulkách. Microsoft Access 2007 a novější mohou otevírat soubory ACCDT.

## Formát souboru ACCDT

Soubory šablon ACCDT jsou založeny na specifikacích Office Open XML a všechna data jsou obsažena v balíčku ZIP. Informace o struktuře a obsahu databáze jsou obsaženy v souborech [XML](/cs/web/xml/) a textových souborech a jsou vzájemně propojeny prostřednictvím vztahů. Soubor ACCDT můžete přejmenovat na příponu [.zip](/cs/compression/zip/) a použít jakýkoli komprimační software k extrahování obsahu archivu ZIP.

### Struktura souboru

Soubory ACCDT jsou balíčky, které obsahují kolekci souvisejících částí. Každá **část** ukládá informace o obsahu databázové aplikace pomocí XML, textových a binárních formátů, které zahrnují:

* Databázové objekty
* Přidružená metadata
* Struktura balíčku

#### Balíček

Balíček je archiv [ZIP](/cs/compression/zip/), který obsahuje více částí a odpovídá konvencím Open Packaging uvedeným v [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html). Soubory ACCDT musí obsahovat alespoň jednu část metadat šablony, která by měla být cílem vztahu. Tato metadata šablony jsou počáteční částí souboru ACCDT.

#### Část

Část je proud bajtů, který má přidružený typ pro určení povahy a typu obsahu, který je v něm uložen. Výčet částí určuje platné části, platné typy obsahu a požadované vztahy mezi všemi částmi v balíčku.

#### Vztah

`Package Relationship` - kde cíl je část a zdroj je balíček jako celek.

`Part-to-Part Relationship` - kde cíl je součástí a zdroj je součástí balíčku.

`Explicitní vztah` – kde je zdroj odkazován z obsahu zdrojové části odkazem na prvek vztahu hodnotou jeho atributu ID.

„Implicitní vztah“ – vztah, který není explicitní.

`Interní vztah` - kde cíl je součástí balíčku.

`Externí vztah` - kde cíl je externí zdroj, který není v balíčku.

## Reference ##

* [Formát souboru šablony přístupu](https://learn.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

