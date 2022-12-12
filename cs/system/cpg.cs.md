{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru CPG - soubor kódové stránky ESRI",
  "description":"Další informace o formátu souboru CPG a rozhraních API, která mohou vytvářet a otevírat soubory CPG.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## Co je soubor CPG?

Soubor CPG je volitelný soubor, který vyžaduje ESRI Shapefile, který se používá k určení kódové stránky pro identifikaci znakové sady, která má být použita. Ty jsou uloženy ve formátu prostého textového souboru a obsahují informace o kódování použitém pro vytvoření souboru shapefile. V případě, že soubor CPG není k dispozici, použije soubor shapefile výchozí systémové kódování. Soubor CPG, pokud existuje, musí mít stejnou předponu jako soubor [SHP](/cs/gis/shp/), například roads.shp, roads.cpg.

Soubory CPG lze otevřít pomocí ESRI ArcGIS Pro.

### Formát souboru CPG – Další informace

Při prohlížení souboru shapefile v ArcCatalog nebo jakékoli jiné aplikaci ArcGIS vidíte pouze soubor shapefile. Ve skutečnosti však shapefile používá další přidružené soubory, které se čtou vedle hlavního souboru shape. Soubor CPG je také jedním z nich, pokud je přítomen vedle hlavního souboru SHP.

## Reference

* [Přípony souborů Shapefile
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

