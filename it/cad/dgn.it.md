{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "File", "Formato", "Apri", "Leggi", "API", "MicroStation", "Sistema di progettazione grafica interattiva Intergraph" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - Formato file di progettazione CAD MicroStation",
  "description" :"Scopri il formato di file DGN e le API che possono creare e aprire file DGN.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## Che cos'è un file DGN?

Un file con estensione .dgn (Design) è un file di disegno creato e supportato da applicazioni CAD come MicroStation e Intergraph Interactive Graphics Design System. Viene utilizzato per creare e salvare progetti per progetti di costruzione come autostrade, ponti ed edifici. Il formato è simile al formato di file [DWG](/it/cad/dwg/) di Autodesk ed è considerato un suo concorrente. I file DNG possono essere salvati come Intergraph Standard File Format o V8 DGN. DGN può essere convertito in molti altri formati come DWG, [BMP](/it/image/bmp/), [JPEG](/it/image/jpeg/), [PDF](/it/pdf/), [GIF](/it/image/ gif/) e altri. Può essere aperto con Autodesk AutoCAD, Bentley View e Bentley Systems MicroStation oltre ad altre applicazioni software come le versioni Corel PaintShop Photo Pro e IMSI TurboCAD Deluxe.

## Formato file DGN V8

Un file DGN di MicroStation V8 è composto da uno o più modelli. Un modello è un contenitore di elementi. Il DGN V8 rimuove tutti i vincoli basati sul formato file che erano presenti nelle versioni precedenti di MicroStation. Di seguito è riportato un elenco di miglioramenti nel formato di file DGN.

* Il limite al numero di livelli in un file DGN è stato rimosso e ogni livello è nominato e memorizzato come elemento.
* La dimensione fisica massima del file DGN non ha alcuna limitazione ed è limitata solo dal sistema operativo (ad esempio il limite NT è 4 GB)
* La dimensione massima di un singolo elemento è 128 KB.
* Non c'è limite alla dimensione massima di una cella.
* I nomi delle celle sono limitati a circa 500 caratteri.
* Non c'è limite al numero di riferimenti che possono essere allegati a un file DGN.
* Una stringa di linea, una forma o una curva puntuale possono avere fino a 5000 vertici.
* Non c'è limite al numero di componenti in una catena complessa o in una forma complessa.
* Non c'è limite al numero di gruppi grafici in un file DGN.
* La recinzione è parallela alla vista in cui è posizionata.
* Una singola riga di testo può contenere 65.535 caratteri.
* Non c'è limite alla dimensione massima di un nodo di testo.
* Non c'è limite al numero di nodi di testo in un file DGN.
* Ogni elemento ha un identificatore univoco a 64 bit che non cambia durante il ciclo di vita dell'elemento.
* Ogni elemento ha un timestamp che indica l'ora della modifica più recente.

## Riferimenti

* [DNG - Di Wikipedia](https://en.wikipedia.org/wiki/DGN)
* [OpenDNG](http://www.bentley.com/opendgn)
* [Formato file DGN di MicroStation V8](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

