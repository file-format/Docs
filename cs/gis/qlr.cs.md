{
  "date" : "2019-10-11",
  "keywords" :[ "soubor qlr", "formát souboru qlr", "co je soubor qlr", "soubor", "příklad qlr", "přípona souboru qlr", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - QGIS Layer Definition File",
  "description":"Další informace o formátu souborů QLR a rozhraních API, která mohou vytvářet a otevírat soubory QLR.",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Co je soubor QLR?

Soubor s příponou .qlr je soubor s definicí vrstvy, který obsahuje ukazatel na zdroj dat vrstvy. Toto je doplněk k informacím o stylu [QGIS](https://www.qgis.org/en/site/) pro vrstvu. Tento soubor, který obsahuje odkazy na všechny související styly, se používá jako jediný zdroj dat pro získání informací o stylu. Pomocí souborů QLR lze informace o zdrojích dat vložit do tohoto jediného souboru, který lze číst jinými aplikacemi a načíst informace o stylu. Soubory QLR lze otevřít pomocí libovolného textového editoru, jako je Notepad++.

## Formát souboru QLR

QLR, podobně jako [QGS](/cs/gis/qgs/), je soubor XML, který obsahuje ukazatele na zdroj dat vrstvy ve formě značek XML. Je podobný souboru ArcGIS .lyr. Značky nejvyšší úrovně souboru QML jsou znázorněny na obrázku níže.

{{< figure src="../qlr.png" title="" >}}

## Reference

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

