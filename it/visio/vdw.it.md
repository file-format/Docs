{
  "date" : "2019-10-11",
  "keywords" :[ "vdw","file vdw", "formato file vdw", "tipo di file vdw", "file", "tipo", "cos'è un file vdw" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - Formato file del servizio di grafica di Visio",
  "description":"Scopri il formato di file VDW e le API che possono creare e aprire file VDW.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## Che cos'è un file VDW?

VDW è il formato di file di Visio Graphics Service che specifica i flussi e gli archivi necessari per il rendering di un disegno Web. Un disegno Web è una raccolta di pagine di disegno, forme, caratteri, immagini, connessioni dati e informazioni sull'aggiornamento del diagramma che possono essere renderizzate come un disegno vettoriale o raster. I file VDW possono essere aperti anche in Microsoft Visio, ma vengono salvati principalmente per l'uso sul Web. Microsoft Visio offre la possibilità di convertire i file Visio in diversi formati di file, inclusi [PNG](/it/Image/PNG/), [BMP](/it/Image/BMP/), [PDF](/it/pdf/) e altri.

## **VDW** Formato file

Le specifiche tecniche del formato di file VDW sono disponibili online da [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) e possono essere consultate dagli sviluppatori per la creazione applicazioni. Il documento tecnico descrive i dati contenuti in un file composto che contiene archivi e flussi. La rappresentazione di un Web Drawing è resa possibile attraverso un flusso, denominato VisioServerData, tramite un archivio ZIP. Una parte ShapGraphic XML nell'archivio descrive gli elementi grafici visualizzati nel disegno Web e sono espressi in Extensible Application Markup Language (XAML). Una raccolta di parti XML nell'archivio ZIP descrive la connessione dati del disegno Web, informazioni sulla sua forma e la logica di aggiornamento del diagramma. Queste parti sono espresse come XML. La parte DataGraphic XML descrive le proprietà ricalcolate che devono essere valutate dopo che i dati nel disegno Web sono stati aggiornati dall'origine dati. Gli elementi aggiuntivi nell'archivio ZIP contengono informazioni per i caratteri e le immagini utilizzate nel disegno Web.

|![Possibile implementazione di un file](/it/web/vdw.png "Possibile implementazione di un file")

## Riferimenti

* [[MS-VGSFF]: Formato file Visio Graphics Service (.vdw)](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

