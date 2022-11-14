{
  "date" : "2019-10-11",
  "keywords" :[ "file shp", "formato file shp", "cos'è un file shp", "file", "esempio shp", "estensione file shp", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - File di forma ESRI",
  "description":"Scopri il formato di file SHP e le API che possono creare e aprire file SHP.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file SHP?

SHP è l'estensione di file per uno dei tipi di file principali utilizzati per la rappresentazione di ESRI Shapefile. Rappresenta le informazioni geospaziali sotto forma di dati vettoriali che devono essere utilizzati dalle applicazioni GIS (Geographic Information Systems). Il formato è stato sviluppato come specifiche aperte al fine di facilitare l'interoperabilità tra ESRI e altri prodotti software.

## Rappresentazione dei dati

Come accennato, un formato shapefile descrive le informazioni geospaziali di un set di dati come caratteristiche vettoriali. Queste caratteristiche vettoriali includono:

* punti
* linee
* poligoni

Queste caratteristiche in combinazione possono rappresentare quasi tutti i tipi di forme come pozzi d'acqua, confini di paesi, punti spaziali, flussi di fiumi, laghi, ecc. Ogni caratteristica vettoriale può avere attributi che definiscono effettivamente lo scopo di quella caratteristica. Ad esempio, uno shapefile contenente le città di Los Angeles può avere il nome della città e la temperatura come attributi che forniscono una rappresentazione significativa dei dati spaziali.

## File associati

Un file shp autonomo non può essere utilizzato dalle applicazioni software per dare un significato ai dati che contiene. Per dare un senso alle informazioni contenute in tale file, uno shapefile fa uso dei seguenti file obbligatori aggiuntivi.

* file shx - file di indice
* file dbf - un file dBASE che memorizza tutti gli attributi delle forme nel file principale
* prj file - memorizza le informazioni sul progetto del file

Possono esserci anche altri file facoltativi che condividono lo stesso nome del file principale.

## Specifiche del formato file SHP

Le specifiche aperte di shapefile sono disponibili online da ESRI sotto forma di [Descrizione tecnica](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) ed elabora in dettaglio la struttura generale del file. Le informazioni nel file .shp principale sono costituite da intestazioni e record. L'intestazione del file a lunghezza fissa è seguita da record a lunghezza variabile in cui ogni record è costituito da un'intestazione di record a lunghezza fissa seguita da contenuti di record a lunghezza variabile.

### Intestazione del file SHP principale

L'intestazione del file principale inizia dall'inizio del file ed è lunga 100 byte. L'organizzazione di questa intestazione del file principale insieme alla posizione dei byte, al valore, al tipo e all'ordine dei byte è mostrata nella tabella seguente.


|Byte|Campo|Valore|Tipo|Ordine byte
---|---|---|---|---|
|0-3|Codice file|9994|Numero intero|Big Endian
|4-23|Non utilizzato|0|Numero intero|Big Endian
|24-27|Lunghezza file|Lunghezza file|Intero|Big Endian
|28-31|Versione|1000|Numero intero|Little Endian
|32-35|Tipo di forma|Tipo di forma|Intero|Little Endian
|36-67|Rettangolo di delimitazione minimo|Xmin, Ymin, Xmax e Ymax|doppio|Little Endian
|68-83|Riquadro di delimitazione|Zmin, Zmax|doppio|Little Endian
|84-99|Riquadro di delimitazione|Mmin, Mmax|doppio|

Va notato che il valore della lunghezza del file è la lunghezza totale del file in parole a 16 bit che include anche le cinquanta parole a 16 bit che compongono l'intestazione.

#### Tipi di forme

I valori del campo dei tipi di forma nella tabella sopra sono i seguenti:


|Valore|Tipo di forma
---|---|
|0|Forma nulla
|1|Punto
|3|Polilinea
|5|Poligono
|8|Multipunto
|11|PuntoZ
|13|PolyLineZ
|15|PoligonoZ
|18|MultipuntoZ
|21|PuntoM
|23|PolyLineM
|25|PoligonoM
|28|MultipuntoM
|31|Multipatch

### Record di dati ###

L'intestazione del file principale è seguita da record a lunghezza variabile in cui ogni record è costituito da un'intestazione di record a lunghezza fissa seguita da contenuti di record a lunghezza variabile.

#### Intestazione del record ####

L'intestazione del record contiene informazioni sul numero del record e sulla lunghezza del contenuto del record in una lunghezza fissa di 8 byte. L'organizzazione dell'intestazione del record è la seguente:


|Byte|Campo|Valore|Tipo|Ordine byte
---|---|---|---|---|
|0-3|Numero record|Numero record|Intero|Grande
|4-7|Lunghezza record|Lunghezza record|Intero|Grande

#### Registra contenuto ####

Il contenuto di un record di shapefile consiste in un tipo di forma seguito dai dati geometrici per quella forma. Un tipo di forma 0 rappresenta una forma nulla che non ha dati geometrici per la forma. La lunghezza del contenuto del record riflette le parti e i vertici della forma. Prendiamo un esempio di tipo Point Shape per elaborare come un record contiene informazioni su tale tipo di forma.

Un punto rappresenta una determinata posizione geografica nell'ordine X,Y in cui ciascuna coordinata è rappresentata da un valore a doppia precisione. La tabella seguente mostra la disposizione di un tipo di forma Punto.


|Byte|Tipo forma|Valore|Tipo|Numero|Ordine byte
---|---|---|---|---|---|
|0-3|Tipo di forma|1|Intero|1|Piccolo
|4-11|X|X|doppio|1|Piccolo
|12-19|Y|Y|doppio|1|Piccolo

Esempi di altri tipi di forma possono essere trovati nel documento di descrizione tecnica ESRI.

## Riferimenti ##

* [Descrizione tecnica di ESRI Shapefile](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) di ESRI

