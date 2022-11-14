{
  "date" : "2019-10-11",
  "keywords" :[ "file obj", "formato file obj", "cos'è un file obj", "file", "esempio obj", "estensione file obj", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file OBJ",
  "description":"Scopri il formato di file OBJ e le API che possono aprire e creare file OBJ.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file OBJ?

**I file OBJ** vengono utilizzati dall'applicazione Advanced Visualizer di Wavefront per definire e memorizzare gli oggetti geometrici. La trasmissione avanti e indietro di dati geometrici è resa possibile tramite file OBJ. Sia la geometria poligonale come punti, linee, vertici di texture, facce e geometria a forma libera (curve e superfici) sono supportate dal formato OBJ. Questo formato non supporta l'animazione o le informazioni relative alla luce e alla posizione delle scene.

Un file OBJ è solitamente un prodotto finale del processo di modellazione 3D generato da un CAD (Computer Aided Design). L'ordine predefinito per memorizzare i vertici è in senso antiorario, evitando la dichiarazione esplicita delle normali delle facce. Sebbene i file OBJ dichiarino informazioni sulla scala in una riga di commento, non sono state dichiarate unità per le coordinate OBJ.

## Storia del formato 3D OBJ

Wavefront Technologies ha creato il formato file OBJ per la sua applicazione Advanced Visualizer per memorizzare oggetti geometrici e dati 3D. La sua versione 2.11 è stata sostituita da una versione 3 recentemente documentata. Il formato del file è aperto ed è stato implementato da altri fornitori per le loro applicazioni di grafica 3D. Wavefront Technologies ha mantenuto questo formato di file open source e neutrale.

## Formato file OBJ

Negli oggetti 3D, la codifica della geometria della superficie è un lavoro impegnativo che il formato di file OBJ ha svolto molto bene. Questo formato è abbastanza versatile in quanto offre una serie di scelte per codificare la geometria della superficie. Di seguito sono riportati tre formati consentiti con i propri vantaggi e svantaggi:

### Tassellatura con facce poligonali

Il formato di file OBJ facilita all'utente la tassellatura di una superficie del modello 3D utilizzando forme geometriche semplici o complesse. Per la codifica della geometria della superficie di un modello, un file memorizza i vertici e la normale a ciascun poligono. Sebbene la tassellatura aumenti la ruvidezza del modello, tuttavia è necessario scoprire il corretto equilibrio tra le dimensioni di un file e la sua qualità di stampa.

### Curva a forma libera

Il formato file OBJ consente alle curve di superficie a forma libera definite dall'utente di specificare la geometria della superficie di un modello. Poiché le curve a forma libera sono più complesse delle facce poligonali poiché, con pochi parametri matematici, le linee curve possono essere definite al meglio da curve a forma libera. Pertanto, con un minor numero di dati rispetto alle tassellazioni poligonali, le curve a forma libera sono utilizzate per generare una codifica di alta qualità di qualsiasi modello 3D senza espandere le dimensioni del file.

### Superfici a forma libera

Il formato file OBJ specifica anche la piastrellatura della geometria della superficie con patch di superficie a forma libera. Questo tipo di patch di superficie a forma libera (NURBS) è molto adatto per superfici senza dimensioni radiali rigide come la carrozzeria di un camion, le ali di un elicottero o lo scafo di una barca. L'uso di superfici a forma libera è molto vantaggioso in quanto sono più precise per mantenere le dimensioni dei file più piccole con una maggiore precisione. Queste superfici sono una parte essenziale dell'industria aerospaziale e automobilistica, dove la bassa precisione non perdona.

Le seguenti parole chiave sono organizzate per tipo di dati per definire la geometria della superficie.


|Elementi|Dichiarazioni di curve/corpo di superficie in forma libera|Attributi di curve/superfici in forma libera
---|---|---|
|p|Punto|parm|Valori parametro|gradi|Grado
|l|Linea|trim|Anello di taglio esterno|bmat|Matrice di base
|f|Viso|foro|Anello di rifinitura interno|passo|Dimensione del passo
|curv|Curva|scrv|Curva speciale|cstype|Tipo di curva o superficie
|curv2|Curva 2D|sp|Punto speciale|**Connettività e Raggruppamento di superfici**
|surf|Superficie|fine|Dichiarazione finale|con|connetti
|**Visualizza/renderizza attributi**|g|Nome del gruppo
|smusso|Interpolazione smusso|shadow_obj|Fusione ombra|s|Gruppo levigante
|lod|Livello di dettaglio|trace_obj|Ray-tracing|mg|Gruppo di fusione
|d_interp|Interpolazione dissolvi|ctech|Tecnica di approssimazione della curva|o|Nome dell'oggetto
|c_interp|Interpolazione del colore|stech|Tecnica di approssimazione della superficie|
|usemtl|Nome materiale|mtllib|Libreria materiali|
|**Vertici geometrici**|
|v|Vertici geometrici|vn|Normali ai vertici|
|vt|Vertici della trama|vp|Vertici dello spazio parametrico|

### Colore e consistenza

Il file OBJ consente di memorizzare le informazioni sul colore e sulla trama in un formato di file associato chiamato Material Template Library (MTL). I modelli geometrici multicolori vengono renderizzati utilizzando questi due file insieme. I file MTL sono basati su ASCII e facilitano il rendering al computer descrivendo le proprietà di riflessione della luce di una superficie utilizzando il modello di riflessione Phong. Lo standard è stato adottato da un gran numero di fornitori di software che ne sfruttano l'interscambio di materiali. Il formato MTL è leggermente obsoleto per non avere supporto nelle ultime tecnologie come mappe speculari e parallasse.

## Riferimenti

* [File Wavefront .obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

