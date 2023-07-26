{
  "date" : "2021-07-29",
  "keywords" :[ "soubor shx", "formát souboru shx", "co je soubor shx", "soubor", "příklad shx", "přípona souboru shx", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - Formát indexu tvaru souboru Shapefile",
  "description":"Další informace o formátu souboru SHX a rozhraních API, která mohou vytvářet a otevírat soubory SHX.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Co je soubor SHX?
Soubor SHX patří do formátu indexu tvaru, což je poziční index geometrie prvku, který umožňuje rychlé vyhledávání vpřed a vzad. SHX je offsetový soubor s přímým přístupem. V tomto souboru nejsou žádná data, pouze duplikovaná kopie prvních sto bajtů, číslo záznamu a offset na počáteční bajt tohoto záznamu v shp. Vezměte prosím na vědomí, že soubor s příponou .shx nesouvisí s [SHP](/cs/gis/shp/) a [DBF](/cs/database/dbf).

## Formát souboru SHX
Formát SHX obsahuje poziční index geometrie prvku a 100bajtové záhlaví podobné souboru SHP, za nímž následuje libovolný počet 8bajtových záznamů pevné délky, které obsahují následující dvě pole:
| Bajty | Typ | Endianness | Použití |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | velký | Offset záznamu (v 16bitových slovech) |
| 4–7 | int32 | velký | Délka záznamu (v 16bitových slovech) |

Tento index umožňuje zpětné vyhledávání v souboru shapefile nejprve zpětným vyhledáváním v indexu tvaru a poté čtením offsetu záznamu. Tento posun lze použít k vyhledání správné pozice v souboru SHP. Můžete také hledat dopředu; libovolný počet záznamů pomocí stejné metody. Je sice možné vygenerovat kompletní index spolu se souborem SHP, ale může to zvýšit pravděpodobnost rychlého poškození souboru SHP.


## Reference

* [Shapefile – od Wikipedie)](https://en.wikipedia.org/wiki/Shapefile)


