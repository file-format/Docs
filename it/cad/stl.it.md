{
  "date" : "2020-03-16",
  "keywords" :[ "File STL", "Formato", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file STL e le API che possono creare e aprire file STL.",
  "title" :"Formato file STL",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è il file STL?

STL, abbreviazione di stereolitografia, è un formato di file intercambiabile che rappresenta la geometria della superficie tridimensionale. Il formato di file trova il suo utilizzo in diversi campi come la prototipazione rapida, la stampa 3D e la produzione assistita da computer. Rappresenta una superficie come una serie di piccoli triangoli, noti come sfaccettature, in cui ogni sfaccettatura è descritta da una direzione perpendicolare e tre punti che rappresentano i vertici del triangolo. I dati risultanti vengono utilizzati dalle applicazioni per determinare la sezione trasversale della forma 3D che deve essere costruita dal fabber. Non sono disponibili informazioni nel formato di file STL per la rappresentazione di colori, texture o altri attributi comuni del modello [CAD](/it/cad/).

## Breve storia ##

Lo sviluppo del formato di file STL risale al 1987. È stato sviluppato da 3D Systems per il suo utilizzo nelle stampanti 3D commerciali. Una versione rivista del formato di file STL, nota come STL 2.0, è stata proposta nel 2009 con aggiornamenti al formato di file.

## Specifiche del formato file ##

Un file STL rappresenta una geometria di superficie utilizzando le sfaccettature. Le sfaccettature definiscono la superficie di un oggetto 3D ed è identificata in modo univoco da una normale unitaria, che è una linea perpendicolare al triangolo con lunghezza di 1,0, e da tre vertici. Ci sono un totale di 12 numeri memorizzati per ogni faccetta come Normale e ogni vertice è specificato da tre coordinate ciascuno. Il file StL non contiene alcuna informazione sulla scala; le coordinate sono in unità arbitrarie.

Le specifiche del formato di file STL possono essere esaminate dai seguenti due aspetti.

### Orientamento delle sfaccettature ###

L'orientamento di una sfaccettatura è determinato dalla direzione della normale unitaria e dall'ordine in cui sono elencati i vertici. L'orientamento delle faccette è specificato in due modi come segue:

* La direzione della normale è verso l'esterno
* I vertici sono elencati in senso antiorario dall'esterno, obbedendo alla regola della mano destra.

### Regola da vertice a vertice ###

Secondo questa regola, ogni triangolo condivide due vertici con ciascuno dei suoi triangoli adiacenti. Pertanto, un vertice di un triangolo non può giacere sul lato di un altro triangolo.

## Formati file ##

STL è disponibile in ASCII e in rappresentazioni binarie per il formato file compatto.

### Formato ASCII STL ###

La versione ASCII del formato di file STL è scritta in ASCII semplice. Tuttavia, a causa delle sue grandi dimensioni, il formato del file non è selezionato come formato preferibile per l'utilizzo. La sintassi di un file ASCII STL è la seguente:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
Le parole in grassetto rappresentano le parole chiave che dovrebbero essere sempre minuscole. I simboli in corsivo sono variabili che devono essere sostituite con valori specificati dall'utente. I dati numerici nelle righe **facet normal** e **vertex** sono float a precisione singola, ad esempio 1.23456E+789. Una coordinata **normale della faccetta** può avere un segno meno iniziale; una coordinata **vertice** potrebbe non esserlo.

### Formato binario STL ###

Il formato binario utilizza la rappresentazione numerica intera IEEE e virgola mobile. Il formato del file è rappresentato come segue:

|Campo|Informazioni|
---|---|
|Intestazione|80 caratteri|
|Numero di triangoli|Intero senza segno little endian a 4 byte|
|Dati per ogni triangolo|12 numeri in virgola mobile a 32 bit|

Una vista più elaborata del formato del file è quella mostrata di seguito.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Riferimenti ##

* [Il formato STL](http://www.fabbers.com/tech/STL_Format)
* [STL - di Wikipedia](https://en.wikipedia.org/wiki/STL_(file_format))

