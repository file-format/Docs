{
  "date" : "2019-10-11",
  "keywords" :[ "file wmf", "formato file wmf", "cos'è un file wmf", "file", "esempio wmf", "estensione file wmf", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Formato metafile di Microsoft Windows",
  "description":"Scopri il formato di file WMF e le API che possono creare e aprire file WMF.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file WMF?

I file con estensione WMF rappresentano il metafile di Microsoft Windows (WMF) per la memorizzazione di dati di immagini in formato bitmap e vettoriali. Per essere più precisi, WMF appartiene alla categoria del formato di file vettoriale dei formati di file grafici che è indipendente dal dispositivo. Windows Graphical Device Interface (GDI) utilizza le funzioni memorizzate in un file WMF per visualizzare un'immagine sullo schermo. Successivamente è stata pubblicata una versione più avanzata di WMF, nota come Enhanced Meta Files (EMF), che rende il formato più ricco di funzionalità. In pratica, WMF sono simili a SVG.

## Specifiche del formato file WMF ##

Un file WMF si riferiva al formato di file a 16 bit al momento del suo avvio con Windows 3.0. Il formato del file è costituito da una serie di record a lunghezza variabile che contengono comandi di disegno grafico, definizioni di oggetti e proprietà. Poiché i file WMF si basano su comandi resi al GDI per disegnare l'immagine, è anche noto come registrazione digitale dell'immagine che può essere riprodotta per riprodurre quell'immagine. Le specifiche complete del formato di file di WMF sono disponibili online e dovrebbero essere consultate per lo sviluppo di applicazioni per lavorare con i file WMF. Un file WMF è organizzato in:

* Record di intestazione WMF
* Record WMF
* Record di fine file WMF

### Record di intestazione WMF ###

Il **MEMA_HEADER Record** contiene informazioni che definiscono le caratteristiche del metafile, tra cui:

* Il tipo di metafile
* La versione del metafile
* La dimensione del metafile
* Il numero di oggetti definiti nel metafile
* La dimensione del record singolo più grande nel metafile

### Record di intestazione posizionabile WMF ###

Il **Meta_PLACEABLE Record** contiene informazioni estese relative all'immagine, tra cui:

* Un rettangolo di delimitazione
* Dimensione dell'unità logica, per il ridimensionamento
* Un checksum, per la convalida

### Record WMF ###

I record WMF hanno un formato generico, specificato nel documento delle specifiche. Ogni record WMF contiene le seguenti informazioni:

* La dimensione del record
* La funzione di registrazione
* Parametri, se presenti, per la funzione di registrazione

## Riferimenti ##

* [[MS-WMF]: formato metafile di Windows](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

