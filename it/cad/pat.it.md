{
  "date" : "2020-03-16",
  "keywords" :[ "File PAT", "Formato", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file PAT e le API che possono creare e aprire file PAT.",
  "title" :"Formato file PAT",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## Che cos'è un file PAT?

Un file con estensione .pat è un file CAD utilizzato dal software AutoCAD. Le applicazioni che possono aprire file PAT utilizzano il modello di tratteggio memorizzato in questi file per ottenere informazioni sulla trama/riempimento di un'area. I modelli contenuti forniscono informazioni sull'aspetto del materiale agli oggetti disegnati. I file PAT possono essere aperti in applicazioni come Autodesk AutoCAD, CorelDRAW Graphics Suite e Ketron Software. I file PAT possono essere convertiti in diversi formati di immagine come JPG, PNG, BMP, ecc.

## Formato file PAT

I file PAT sono scritti in formato di testo normale e possono essere aperti in qualsiasi editor di testo. I modelli di tratteggio in questi file sono basati su vettori e seguono la sintassi delineata dalla documentazione di AutoCAD.

Tutti i modelli iniziano dal punto 0,0, il modello viene calcolato per coprire il confine di tratteggio.

### Definizione del modello

Tutte le definizioni del modello sono costituite dai seguenti campi:
* Un '\*' iniziale
* Un nome: il nome non può avere spazi, segni di punteggiatura, parentesi o barre.
* Una descrizione

Il formato standard per i modelli di tratteggio è `<\*><name> <, descrizione>`. Il nome e la descrizione sono separati da una virgola e le descrizioni non possono superare la lunghezza della riga di ottanta caratteri. I modelli di tratteggio sono definiti dopo queste informazioni.

### Esempi di modelli di tratteggio
Di seguito è riportato un esempio di motivo quadrato
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Un altro esempio che mostra il modello a parallelogramma è il seguente.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Riferimenti ##

* [Modelli hash di Autodesk](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/AutoCAD-LT/files/GUID-A6F2E6FF-1717- 44B6-A476-0CA817ADD77E-htm.html)

