{
  "date" : "2021-07-30",
  "keywords" :[ "file dlg", "formato file dlg", "cos'è un file dlg", "file", "esempio dlg", "estensione file dlg", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - Formato dell'indice di forma dello shapefile",
  "description":"Scopri il formato di file DLG e le API che possono creare e aprire file DLG.",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## Che cos'è un file DLG?
Un file con estensione .dlg contiene il Digital Line Graph che è una caratteristica della mappa cartografica mostrata in forma vettoriale digitale che è amministrata dall'US Geological Survey (USGS). I file DLG sono disponibili in due diversi formati:
1. **Formato facoltativo**: un formato di semplice utilizzo che incorpora una lunghezza del record logico di 80 byte, il sistema di coordinate di terra UTM e i collegamenti della topologia contenuti negli elementi di linea, nodo e area.
2. **Formato Spatial Data Transfer Standard (SDTS)**: un formato che facilita il trasferimento di dati spaziali tra diversi sistemi informatici.

## Formato file DLG
Il formato di file DLG è progettato per le mappe USGS e viene trasmesso su scala grande, intermedia e piccola con un massimo di nove diverse categorie di funzioni. I file DLG sono disponibili in formati opzionali e Spatial Data Transfer Standard (SDTS) con struttura topologica per l'uso in applicazioni cartografiche e GIS.
### Specifiche del formato file DLG
I file DLG sono distribuiti su tre diverse scale:

1. **Grande scala** - normalmente corrispondono a:
- L'USGS 7,5- di 7,5 minuti
- Serie di mappe topografiche quadrangolari in scala 1:24.000 e 1:25.000
- Scala 1:63.360 per l'Alaska
- Scala 1:30.000 per Porto Rico
 

2. **Scala intermedia** - derivata dall'USGS:

- 30- per 60 minuti

- Serie di mappe in scala 1:100.000
3. **Piccola scala** - derivato dalle mappe in sezione in scala 1:2.000.000 dell'USGS dell'Atlante nazionale degli Stati Uniti
### Categorie di dati
Nove diverse categorie di livelli, o funzioni, sono disponibili nei file DLG:
1. Sistema pubblico di rilevamento del territorio (PLSS)
2. Confini (BD)
3. Trasporto (TR)
4. Idrografia (HY)
5. Ipsografia (HP)
6. Caratteristiche non vegetative (NV)
7. Controllo rilievo e marker (SM)

8. Caratteristiche artificiali (MS)

9. Copertura superficiale vegetativa (SC)

I file DLG su larga scala offrono tutti e nove i livelli, mentre quelli su scala intermedia offrono i cinque livelli di PLSS, BD, TR, HY e HP. I DLG su piccola scala offrono i cinque livelli di PLSS, BD, TR, HY e MS.

## Riferimenti

* [Grafico a linee digitali - di Wikipedia)](https://en.wikipedia.org/wiki/Digital_line_graph)


