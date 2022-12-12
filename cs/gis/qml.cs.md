{
  "date" : "2019-10-11",
  "keywords" :[ "soubor qml", "formát souboru qml", "co je soubor qml", "soubor", "příklad qml", "přípona souboru qml", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QML - formát souboru stylu QGIS",
  "description":"Další informace o formátu souborů QML a rozhraních API, která mohou vytvářet a otevírat soubory QML.",
  "linktitle" : "QML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Co je soubor QML?

Soubor s příponou .qml je soubor XML, který ukládá informace o stylu vrstev pro vrstvy QGIS. QGIS je open-source multiplatformní GIS aplikace používaná k zobrazování geoprostorových dat se schopností organizovat data ve formě vrstev. Soubory QML obsahují informace, které QGIS používá k vykreslování geometrií prvků včetně definic symbolů, velikostí a rotací, označení, krytí, režimu prolnutí a mnoha dalších. Na rozdíl od souborů QLR obsahují soubory QML samy o sobě všechny informace o stylu. Soubory QML lze otevřít v libovolném textovém editoru, jako je Notepad++.

## Formát souboru QML

QLR, podobně jako [QGS](/cs/gis/qgs/) a [QLR](/cs/gis/qlr/), je soubor XML, který obsahuje informace o stylu vrstev.

Obrázek níže ukazuje značky nejvyšší úrovně souboru QML (pouze renderer_v2 a rozbalenou značku symbolu).

{{< figure src="../qml.png" title="" >}}

## Reference

* [QGIS](https://www.qgis.org/en/site/)
* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

