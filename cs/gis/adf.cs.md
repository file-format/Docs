{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - formát binární mřížky ESRI ArcInfo",
  "description":"Další informace o formátu souboru ADF a rozhraních API, která mohou vytvářet a otevírat soubory ADF.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Co je soubor ADF?

Soubor s příponou .adf je formát rastrových dat používaný softwarovými aplikacemi ESRI, jako jsou ArcGIS, ArcView a ArcInfo. Prostorová data jsou uložena jako binární mřížka, která je nativní pro ESRI. Mřížka se skládá z řádků a sloupců buněk, které mohou být celočíselné i s plovoucí desetinnou čárkou. Celočíselné mřížky v souboru ADF představují diskrétní data a mřížky s plovoucí desetinnou čárkou představují spojitá data. Dalším oblíbeným formátem souboru ESRI je soubor [SHP](/cs/gis/shp/), který představuje geoprostorové informace ve formě vektorových dat pro použití v aplikacích geografických informačních systémů (GIS).

## Formát souboru ADF – Další informace

Soubory ADF se ukládají jako binární soubory na disk v binární mřížce. Celočíselné mřížky mají atributy, které jsou uloženy v tabulce atributů hodnot (VAT). Každá jedinečná hodnota v mřížce má jeden záznam v DPH, kde záznam ukládá jedinečnou hodnotu a počet buněk v mřížce je reprezentován touto hodnotou.

Mřížky s plovoucí desetinnou čárkou nemají DPH.

### Struktura mřížky

Uvnitř souboru ADF jsou mřížky implementovány pomocí dlaždicové rastrové datové struktury. Základní jednotkou uvnitř této rastrové datové struktury je obdélníkový blok buněk. Každý blok je uložen na disku a komprimován do struktury souborů s proměnnou délkou, nazývané dlaždice. Každý blok je uložen jako jeden záznam s proměnnou délkou.

Rastry GRID jsou uloženy v pracovních prostorech, kde pracovní prostor obsahuje jeden podadresář info a podadresář pro každý GRID. Existuje několik souborů s geografickou polohou a atributem dat pro odpovídající mřížku. Podadresář Info obsahuje několik souborů, které uchovávají určité informace o GRID a dalších datových sadách, jako jsou pokrytí, v pracovním prostoru.

## Reference ##

* [Formát mřížky ESRI](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)


