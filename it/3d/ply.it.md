{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "file", "estensione", "formato", "formato file 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file PLY e le API che possono creare e aprire file PLY.",
  "title" :"PLY - Formato file 3D poligonale",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file PLY?

PLY, Polygon File Format, rappresenta il formato di file 3D che memorizza oggetti grafici descritti come una raccolta di poligoni. Lo scopo di questo formato di file era quello di stabilire un tipo di file semplice e facile che fosse abbastanza generale da essere utile per un'ampia gamma di modelli. Il formato di file PLY è disponibile sia in formato ASCII che in formato binario per l'archiviazione compatta e per il salvataggio e il caricamento rapidi. Il formato del file è utilizzato da diverse applicazioni che forniscono supporto per la lettura di file 3D.

Gli oggetti in un formato PLY sono descritti da una raccolta di vertici, facce e altri elementi, insieme a proprietà come il colore e la direzione normale che possono essere associate a questi elementi. Altre proprietà che possono anche essere memorizzate con l'oggetto includono:

* Normali di superficie
* coordinate della trama
* trasparenza
* affidabilità dei dati dell'intervallo
* proprietà per la parte anteriore e posteriore di un poligono

Un oggetto rappresentato dal formato PLY può essere il risultato di varie fonti come oggetti digitalizzati a mano, oggetti poligonali da applicazioni di modellazione, dati di portata, triangoli da cubi in marcia, dati di terain e modelli di radiosità.

## Breve storia

Il formato PLY è stato sviluppato negli anni '90 da Greg Turk e altri nel laboratorio di grafica di Stanford ed è per questo che è anche conosciuto come Stanford Triangle Format. Da allora il formato del file ha la versione 1.0 e non sono state apportate ulteriori modifiche.

## Formato file PLY

Un semplice oggetto PLY consiste in una raccolta di elementi per la rappresentazione dell'oggetto. Consiste in un elenco di (x,y,z) triple di vertici e un elenco di facce che sono effettivamente indici nell'elenco dei vertici. Vertici e facce sono due esempi di elementi e la maggior parte del file PLY è costituita da questi due elementi. Nuove proprietà possono anche essere create e allegate agli elementi di un oggetto, ma queste dovrebbero essere aggiunte in modo tale che i vecchi programmi non si interrompano quando si incontrano queste nuove proprietà. Tali proprietà possono essere eliminate anche leggendo le applicazioni. Inoltre, è possibile creare nuovi elementi e definire proprietà anche con questo elemento.

### Struttura del file

La struttura del file di un formato di file PLY è la seguente:

|Campo
---|
|Intestazione del file
|Elenco dei vertici
|Elenco facce
|Elenco di altri elementi

#### Esempio di struttura

Useremo il seguente esempio di seguito nella nostra discussione successiva per varie parti di un formato di file PLY.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Intestazione del file

L'intestazione del formato file PLY è costituita da testo ASCII sia per il formato ASCII che per il formato binario. L'inizio e la fine della sezione dell'intestazione è identificata dalle parole chiave ply e end-header. L'inizio dell'intestazione ha la parola magica ply che viene utilizzata per il riconoscimento del formato di file PLY dai lettori. La riga successiva mostra il numero di versione per questo file. I commenti in un formato di file PLY iniziano con la parola chiave comment all'inizio di ogni riga di commento.

#### Parola chiave elemento

La parola chiave element dice quindi cosa c'è all'interno del file. È seguito dalle proprietà per quel tipo di elemento specifico in cui ogni proprietà ha il tipo e l'ordine di proprietà specificati come mostrato di seguito:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

In questo particolare esempio, l'elemento vertex specifico ha 3 proprietà di tipo float con il loro ordine specificato.

#### Tipi di tipi di dati

Esistono due tipi di tipi di dati che possono avere una proprietà.

`Scalare`: i tipi di dati scalari sono mostrati di seguito:

|#Nome|#Tipo|#Numero di byte
|carattere|carattere|1
|uchar|carattere senza segno|1
|breve|corto intero|2
|ushort|intero breve senza segno|2
|int|Intero|4
|uint|Intero senza segno|4
|float|float a precisione singola|4
|doppia|doppia precisione float|8

`Lista`: esiste una forma speciale di definizioni di proprietà che utilizza il tipo di dati elenco. Un esempio di questo è dal file cubo sopra:

`lista proprietà uchar int vertex_index`

Ciò significa che la proprietà "vertex_index" contiene prima un carattere senza segno che indica quanti indici contiene la proprietà, seguito da un elenco contenente quel numero di interi. Ogni numero intero in questo elenco a lunghezza variabile è un indice di un vertice.

## Riferimenti ##

* [Formato file PLY](http://paulbourke.net/dataformats/ply/)
* [PLY - Di Wikipedia](https://en.wikipedia.org/wiki/PLY_(file_format))

