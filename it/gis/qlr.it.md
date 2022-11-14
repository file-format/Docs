{
  "date" : "2019-10-11",
  "keywords" :[ "file qlr", "formato file qlr", "cos'è un file qlr", "file", "esempio qlr", "estensione file qlr", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - File di definizione del livello QGIS",
  "description":"Scopri il formato di file QLR e le API che possono creare e aprire file QLR.",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Che cos'è un file QLR?

Un file con .qlr è un file di definizione del livello che contiene un puntatore all'origine dati del livello. Questo è in aggiunta alle informazioni sullo stile [QGIS](https://www.qgis.org/en/site/) per il livello. Avendo riferimenti a tutti gli stili correlati, questo file viene utilizzato come un'unica fonte di dati da utilizzare per ottenere le informazioni sullo stile. Utilizzando i file QLR, le informazioni sulle origini dati possono essere inserite in questo singolo file che può essere letto da altre applicazioni per caricare le informazioni sullo stile. I file QLR possono essere aperti con qualsiasi editor di testo come Notepad ++.

## Formato file QLR

QLR, simile a [QGS](/it/gis/qgs/), è un file XML che contiene puntatori a un'origine dati a strati sotto forma di tag XML. È simile al file .lyr di ArcGIS. I tag di livello superiore di un file QML sono mostrati nell'immagine seguente.

{{< figure src="../qlr.png" title="" >}}

## Riferimenti

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

