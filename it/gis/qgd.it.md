{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "Database Sqlite del progetto QGIS", "estensione", "format", "QGIS", "Database ausiliario", "Cos'è un file QGD"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - Database Sqlite del Progetto QGIS",
  "description":"Scopri QGD che è un database sqlite del progetto QGIS e delle API che possono creare e aprire file QGD.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Che cos'è un file QGD?

Il file con estensione .QGD è in realtà il database sqlite associato del progetto **QGIS** che contiene i dati ausiliari per il progetto. Il file QGD rimarrà vuoto, se non ci saranno dati ausiliari per il progetto.

## Dettagli sul formato file QGD

In modalità classica, il database ausiliario viene salvato come file con estensione .qgd lungo il file xml. Il sistema **Database Ausiliario** consente di leggere e scrivere i dati nel sistema in modo alternativo. Quando si crea il QGZ che è un contenitore zippato, il file .qgd viene incluso nel file .qgz.

## Cos'è il database ausiliario?
Il database ausiliario è in realtà un sistema db standby che viene creato in risposta alla duplicazione del database di destinazione. Il database ausiliario è in realtà un caso di database duplicato sarebbe il database in cui stai duplicando. Ad esempio, se si configura un database in standby utilizzando un database duplicato, il database di origine sarà la destinazione e il database in standby sarà noto come ausiliario.


## Riferimenti

* [QGZ – Un nuovo formato di file di progetto predefinito per QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Formati file QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

