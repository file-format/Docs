{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "Sqlite-databas för QGIS-projektet", "tillägg", "format", "QGIS", "Auxilary Database", "Vad är en QGD-fil"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - SQLite Database of the QGIS Project",
  "description":"Lär dig mer om QGD som är en SQLite-databas över QGIS-projektet och API:er som kan skapa och öppna QGD-filer.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Vad är en QGD fil?

Filen med filändelsen .QGD-filen är faktiskt den associerade SQLite-databasen för **QGIS**-projektet som rymmer extradata för projektet. QGD-filen förblir tom om det inte finns några extra data för projektet.

## Detaljer om QGD-filformat

I klassiskt läge sparas den extra databasen som en fil med filtillägget .qgd längs xml-filen. **Auxiliary Database**-systemet tillåter att läsa och skriva data i systemet som ett alternativt sätt. När du skapar QGZ, som är en zippad behållare, ingår .qgd-filen i .qgz.

## Vad är Auxilary Database?
Auxiliary-databasen är faktiskt ett standby-db-system som skapas som ett svar på dupliceringen av måldatabasen. Den extra databasen är faktiskt ett fall av en duplicerad databas skulle vara databasen du duplicerar till. Om du t.ex. ställer in en standby-databas med dubblettdatabas, kommer källdatabasen att vara målet och standby-databasen kommer att kallas auxiliary.


## Referenser

* [QGZ – Ett nytt standardprojektfilformat för QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS-filformat](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

