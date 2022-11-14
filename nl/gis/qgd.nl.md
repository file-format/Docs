{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "Sqlite Database of the QGIS Project", "extension", "format", "QGIS", "Auxilary Database", "Wat is een QGD-bestand"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - Sqlite Database van het QGIS Project",
  "description":"Meer informatie over QGD, wat een sqlite-database is van het QGIS-project en API's die QGD-bestanden kunnen maken en openen.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Wat is een QGD-bestand?

Het bestand met de extensie .QGD is in feite de bijbehorende sqlite-database van het project **QGIS** dat de hulpgegevens voor het project bevat. Het QGD-bestand blijft leeg als er geen hulpgegevens voor het project zijn.

## Details over QGD-bestandsindeling

In de klassieke modus wordt de hulpdatabase opgeslagen als een bestand met de extensie .qgd naast het xml-bestand. Met het **Auxiliary Database**-systeem kunnen op een alternatieve manier gegevens in het systeem worden gelezen en geschreven. Bij het maken van de QGZ die een gecomprimeerde container is, wordt het .qgd-bestand opgenomen in de .qgz.

## Wat is een hulpdatabase?
De Auxiliary Database is eigenlijk een stand-by db-systeem dat is gemaakt als reactie op de duplicatie van de doeldatabase. De hulpdatabase is eigenlijk een geval van een dubbele database, de database waarnaar u dupliceert. Als u bijvoorbeeld een standby-database instelt met een dubbele database, is de brondatabase het doel en staat de standby-database bekend als de hulpdatabase.


## Referenties

* [QGZ – Een nieuw standaard projectbestandsformaat voor QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Bestandsindelingen van QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

