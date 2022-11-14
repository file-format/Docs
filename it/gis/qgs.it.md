{
  "date" : "2019-10-11",
  "keywords" :[ "file qgs", "formato file qgs", "cos'è un file qgs", "file", "esempio qgs", "estensione file qgs", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - Formato file progetto QGIS",
  "description":"Scopri il formato di file QGS e le API che possono creare e aprire file QGS.",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file QGS?

Un file con estensione .qgs è un file di progetto creato con [QGIS](https://www.qgis.org/en/site/), che è un'applicazione GIS multipiattaforma open source. Tutte le impostazioni del progetto come le proprietà del livello e i dati ausiliari per il progetto. Viene creato quando un progetto di mappa viene salvato su disco. In realtà è un file di configurazione che conserva informazioni come puntatori ai dati GIS, informazioni sullo stile dei livelli e titolo del progetto. I file QGS possono essere aperti con il software QGIS che è disponibile gratuitamente per il download.

## Formato file QGS

I file QGS sono in formato [XML](/it/web/xml/) e memorizzano i dati dei progetti come tag XML. Un file QGS contiene informazioni come:

* titolo del progetto
* progetto CRS
* l'albero dei livelli
* impostazioni di scatto
* relazioni
* l'estensione della tela della mappa
* modelli di progetto
* legenda
* Dock di visualizzazione mappa (2D e 3D)
* i livelli con collegamenti ai set di dati sottostanti (sorgenti dati) e altre proprietà dei livelli tra cui extent, SRS, join, stili, renderer, modalità di fusione, opacità e altro.
* proprietà del progetto

### Tag XML di livello superiore QGS

{{< figure src="../qgstoplevel.png" title="" >}}

### Tag del livello di progetto di livello superiore estesi

{{< figure src="../qgstoplevel.png" title="" >}}

## Riferimenti

* [QGIS](https://www.qgis.org/en/site/)

