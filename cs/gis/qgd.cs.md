{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "Databáze Sqlite projektu QGIS", "rozšíření", "formát", "QGIS", "Pomocná databáze", "Co je soubor QGD"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - databáze Sqlite projektu QGIS",
  "description":"Další informace o QGD, což je sqlite databáze projektu QGIS a rozhraní API, která mohou vytvářet a otevírat soubory QGD.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Co je soubor QGD?

Soubor s příponou .QGD file je ve skutečnosti přidružená databáze sqlite projektu **QGIS**, která obsahuje pomocná data pro projekt. Soubor QGD zůstane prázdný, pokud nebudou k dispozici žádná pomocná data pro projekt.

## Podrobnosti o formátu souboru QGD

V klasickém režimu je pomocná databáze uložena jako soubor s příponou .qgd spolu se souborem xml. Systém **Auxiliary Database** umožňuje alternativním způsobem číst a zapisovat data v systému. Při vytváření QGZ, což je zazipovaný kontejner, soubor .qgd zahrnuje do .qgz.

## Co je pomocná databáze?
Auxiliary Database je vlastně záložní db systém, který vzniká jako odpověď na duplikaci cílové databáze. Pomocná databáze je ve skutečnosti případ, kdy duplicitní databáze by byla databáze, do které duplikujete. Např. pokud nastavíte záložní databázi pomocí duplicitní databáze, zdrojová databáze bude cílová a záložní databáze bude známá jako pomocná.


## Reference

* [QGZ – nový výchozí formát souboru projektu pro QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Formáty souborů QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

