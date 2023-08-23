{
  "date" : "2021-03-18",
  "keywords" :[ "file qgz", "formato file qgz", "cos'è un file qgz", "file", "esempio qgz", "estensione file qgz", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Progetto compresso GIS quantistico",
  "description":"Scopri il formato di file QGZ che è solo un QGS compresso e API in grado di creare e aprire file QGZ.",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Che cos'è un file QGZ?

Il formato file **QGZ** è un archivio compresso contenente un file [QGS](/gis/qgs/) e un file QGD. Considerando che il file QGD è il database sqlite del progetto qgis che consiste in dati ausiliari per il progetto. Se non ci sono dati ausiliari, il file QGD rimarrà vuoto.

## Dettagli sul formato file QGZ

Il QGZ è stato introdotto come una nuova variante del **formato di file di progetto QGIS 3**. Questo formato è un contenitore zippato per il file xml QGS. Se gli utenti scelgono QGD che è un formato opzionale, in questo caso il contenitore è utile per archiviare il database di archiviazione ausiliario.

In modalità classica, il database ausiliario viene salvato come file con estensione .qgd lungo il file xml. Quando si sceglie il contenitore zippato, il file .qgd include nel .qgz, facilita semplicemente gli utenti senza alcun problema, gli utenti non possono eliminarlo o dimenticarsi di copiarlo quando condividono i file di progetto!


## Riferimenti

* [QGZ – Un nuovo formato di file di progetto predefinito per QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Formati file QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

