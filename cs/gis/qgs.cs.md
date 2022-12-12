{
  "date" : "2019-10-11",
  "keywords" :[ "soubor qgs", "formát souboru qgs", "co je soubor qgs", "soubor", "příklad qgs", "přípona souboru qgs", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - Formát souboru projektu QGIS",
  "description":"Další informace o formátu souborů QGS a rozhraních API, která mohou vytvářet a otevírat soubory QGS.",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor QGS?

Soubor s příponou .qgs je soubor projektu vytvořený pomocí [QGIS](https://www.qgis.org/en/site/), což je open-source multiplatformní GIS aplikace. Všechna nastavení projektu, jako jsou vlastnosti hladiny a pomocná data pro projekt. Vytvoří se při uložení mapového projektu na disk. Je to vlastně konfigurační soubor, který uchovává informace, jako jsou ukazatele na data GIS, informace o stylu vrstev a název projektu. Soubory QGS lze otevřít pomocí softwaru QGIS, který je volně ke stažení.

## Formát souboru QGS

Soubory QGS jsou ve formátu [XML](/cs/web/xml/) a ukládají data projektů jako XML tagy. Soubor QGS obsahuje informace jako:

* Název projektu
* projekt CRS
* strom vrstev
* nastavení přichycení
* vztahy
* rozsah mapového plátna
* modely projektů
* legenda
* doky mapview (2D a 3D)
* vrstvy s odkazy na základní datové sady (zdroje dat) a další vlastnosti vrstvy včetně rozsahu, SRS, spojení, stylů, rendereru, režimu prolnutí, krytí a dalších.
* vlastnosti projektu

### Značky XML nejvyšší úrovně QGS

{{< figure src="../qgstoplevel.png" title="" >}}

### Rozšířené značky nejvyšší úrovně projektu

{{< figure src="../qgstoplevel.png" title="" >}}

## Reference

* [QGIS](https://www.qgis.org/en/site/)

