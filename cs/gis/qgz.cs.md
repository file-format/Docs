{
  "date" : "2021-03-18",
  "keywords" :[ "soubor qgz", "formát souboru qgz", "co je soubor qgz", "soubor", "příklad qgz", "přípona souboru qgz", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Quantum GIS Compressed Project",
  "description":"Další informace o formátu souboru QGZ, který je pouze komprimovaným QGS a rozhraními API, která mohou vytvářet a otevírat soubory QGZ.",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Co je soubor QGZ?

Formát souboru **QGZ** je komprimovaný archiv obsahující soubor [QGS](https://docs.fileformat.com/gis/qgs/) a soubor QGD. Zatímco soubor QGD je databáze sqlite projektu qgis, která se skládá z pomocných dat pro projekt. Pokud neexistují žádná pomocná data, soubor QGD zůstane prázdný.

## Podrobnosti o formátu souboru QGZ

QGZ byl představen jako nová varianta **formátu souboru projektu QGIS 3**. Tento formát je zazipovaný kontejner pro soubor QGS xml. Pokud uživatelé zvolí QGD, což je volitelný formát, je v tomto případě kontejner výhodný pro uložení databáze pomocného úložiště.

V klasickém režimu je pomocná databáze uložena jako soubor s příponou .qgd spolu se souborem xml. Při výběru zazipovaného kontejneru je soubor .qgd součástí .qgz, což uživatelům bez problémů usnadňuje, uživatelé jej nemohou smazat nebo zapomenout zkopírovat při sdílení souborů projektu!


## Reference

* [QGZ – nový výchozí formát souboru projektu pro QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Formáty souborů QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

