{
  "date" : "2019-10-11",
  "keywords" :[ "file qml", "formato file qml", "cos'è un file qml", "file", "esempio qml", "estensione file qml", "estensione", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QML - Il formato di file di stile QGIS",
  "description":"Scopri il formato di file QML e le API che possono creare e aprire file QML.",
  "linktitle" : "QML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Che cos'è un file QML?

Un file con estensione .qml è un file XML che memorizza le informazioni sullo stile dei livelli per i livelli QGIS. QGIS è un'applicazione GIS multipiattaforma open source utilizzata per visualizzare dati geospaziali con la capacità di organizzare i dati sotto forma di livelli. I file QML contengono informazioni che vengono utilizzate da QGIS per eseguire il rendering delle geometrie delle caratteristiche, comprese le definizioni dei simboli, le dimensioni e le rotazioni, l'etichettatura, l'opacità, la modalità di fusione e molto altro. A differenza dei file QLR, i file QML contengono tutte le informazioni sullo stile in sé. I file QML possono essere aperti in qualsiasi editor di testo come Notepad++.

## Formato file QML

QLR, simile a [QGS](/it/gis/qgs/) e [QLR](/it/gis/qlr/), è un file XML che contiene informazioni di stile per i livelli.

La figura seguente mostra i tag di livello superiore di un file QML (con solo renderer_v2 e il relativo tag simbolo espansi).

{{< figure src="../qml.png" title="" >}}

## Riferimenti

* [QGIS](https://www.qgis.org/en/site/)
* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

