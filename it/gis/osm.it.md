{
  "date" : "2019-10-11",
  "keywords" :[ "file osm", "che cos'è un file osm", "file", "esempio osm", "estensione file osm", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM - Formato file OpenStreetMap",
  "description":"Scopri il formato di file OSM e le API che possono creare e aprire file OSM.",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file OSM?

OpenStreetMap (OSM) è una vasta raccolta di archivi di informazioni geografiche volontari in diversi tipi di file, che utilizzano diversi schemi di codifica per convertire questi dati in bit e byte. OSM è uno sforzo collaborativo verso la creazione di una mappa del mondo modificabile gratuitamente. L'output principale di questo sforzo di collaborazione sono i dati geografici piuttosto che la mappa stessa. I vincoli all'uso o alla disponibilità delle informazioni geografiche in gran parte del mondo fanno scattare la necessità di creare un OSM. I dati disponibili da OSM sono pronti per sostituire Google Maps per le applicazioni classiche (Facebook, Craigslist ecc.) e i dati predefiniti per le applicazioni dei ricevitori GPS.^^ ^^Sebbene la qualità dei dati sia diversa in tutto il mondo, i dati di OpenStreetMap possono essere convenientemente confrontati con i brevetti Origine dei dati.

## Breve storia ##

Ispirato dal successo di Wikipedia, nel 2004, Steve Coast, un imprenditore britannico, ha creato questo progetto di mappatura del mondo basato sulla comunità nel Regno Unito. Inizialmente si è concentrato sulla mappatura del Regno Unito. OpenStreetMap Foundation è stata fondata nell'aprile 2006 per supportare l'evoluzione, l'espansione e la circolazione del geospaziale gratuito per chiunque. Nel dicembre 2006, Yahoo ha aiutato OpenStreetMap con la sua fotografia aerea per la produzione di mappe. I dati stradali completi per i Paesi Bassi e i dati sulle strade principali per India e Cina sono stati forniti a OSM nell'aprile 2007 da Automotive Navigation Data (AND). Nel dicembre 2007, l'Università di Oxford è stata l'organizzazione più importante che ha integrato i dati di OpenStreetMap all'interno del proprio sito Web principale. Da allora, oltre 2 milioni di utenti registrati contribuiscono con i dati a questo progetto utilizzando dispositivi GPS, fotografie aeree e rilievi manuali. Questi dati forniti dalla comunità sono resi disponibili sotto la licenza Open Database. Un'organizzazione senza scopo di lucro registrata in Inghilterra OpenStreetMap Foundation ha gestito il sito OSM.

## Formato file OSM ##

Esistono molti modi e formati di file per archiviare i dati geografici, ma il formato di file **OSM** è limitato a OpenStreetMap. OSM è un formato standard appositamente progettato per essere trasportato facilmente attraverso Internet. Un formato ordinato strutturato, codificato in XML costituisce un file .osm. In OpenStreetMap ci sono quattro elementi pivot per memorizzare la struttura dei dati topologici:

{{< figure src="../OSM.png" alt="Formato file OSM" >}}


|Nodi|Modi|Relazioni|Tag
---|---|---|---|
|<ul><li> Rappresenta la posizione geografica memorizzata come coppie di latitudine e longitudine.</li><li> Utilizzato per rappresentare le caratteristiche della mappa senza una dimensione, come le cime delle montagne.</li></ul> |<ul><li> Elenchi ordinati di nodi, che indicano una polilinea o un poligono</li><li> Rappresentano elementi lineari come strade e fiumi e zone, come aree di parcheggio, giungle e parchi.</li></ul> |<ul><li> Elenchi ordinati di nodi e strade rappresentano la loro relazione come barriere e svolte su strade, autostrade attraversano diverse strade esistenti e aree con buche.</li></ul> |<ul><li> Memorizza i metadati sugli oggetti della mappa.* Sempre collegati a qualsiasi nodo, via o relazione</li></ul>


I tag vengono utilizzati per caratterizzare le caratteristiche fisiche del terreno (edifici e strade, ecc.) in OpenStreetMap. Ciascun tag mette in relazione una caratteristica geografica della caratteristica rappresentata da quel nodo o relazione specifica. In questo sistema di tagging gratuito, per descrivere una caratteristica, è possibile includere in una mappa un numero illimitato di attributi. Specifiche combinazioni di valori e chiavi approvate dagli utenti registrati fungono da standard informali per i tag utilizzati di frequente. Tuttavia, è possibile creare nuovi tag ogni volta che nuovi aspetti richiedono l'analisi di attributi delle caratteristiche precedentemente non mappati. La maggior parte delle funzioni utilizza solo un numero limitato di tag per la descrizione.

Tre tipi di file vengono utilizzati da OSM per memorizzare i suoi dati principali.

OSM gestisce tutti questi file con le informazioni sui loro dettagli di formattazione. Ma gli stessi oggetti interni sono prodotti da questi file. Per i file di dati il flag visibile sugli oggetti OSM è sempre vero, il che non è il caso per i file di cronologia e modifiche.

Nell'uso comune, c'è una diversità nei formati di file OSM. I formati di file definiscono la codifica del contenuto su disco o cavo in bit e byte. OSM è in grado di leggere e scrivere il massimo di questi formati.

**XML**

Il formato OSM originale è basato su XML. I dati di ritorno dell'API del database OSM principale sono in formato XML.

**PBF**

La codifica dei buffer di protocollo si basa sul formato binario e uno dei formati più compatti.

**O5M/O5C**

Formato più semplice basato su formato binario ma relativamente meno utilizzato. OSM può leggere ma non può scrivere questo formato.

**OPL**

Un formato semplice proposto per l'uso con gli strumenti a riga di comando UNIX standard. Vicino ai file CSV, consente un'entità OSM su una riga.

**DEBUG**

Un formato basato su testo destinato a creare per il debug. L'OSM può scrivere questo formato ma non può leggere.

**BUCO NERO**

Un formato fittizio che elimina tutti i dati. L'OSM può scrivere questo formato ma non può leggere.

## Archiviazione dati OSM ##

Il database principale **PostgreSQL** di OSM conserva la copia principale dei dati OSM con estensione PostGIS. Per ogni primitiva di dati, il database principale mantiene una tabella le cui righe memorizzano i singoli oggetti. Tutte le modifiche aggiornano questo database e tutti gli altri formati vengono formati utilizzando questo database. Vengono creati numerosi pool di database scaricabili per trasferire i dati da un luogo all'altro. Due formati, uno che utilizza XML e l'altro che utilizza Protocol Buffer Binary Format (PBF) definiscono questi pool. I dati completi sono memorizzati in un file chiamato planet.osm

## Compressione nei file OSM ##

I formati basati su testo (XML, OPL e Debug) utilizzano la compressione gzip o bzip2 opzionalmente.

## Riferimenti ##

* [Manuale dei formati di file OSM](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [Impara OSM](https://learnosm.org/en/osm-data/getting-data/)

