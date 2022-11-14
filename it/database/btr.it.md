{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "Btrieve Database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file BTR e le API che possono creare e aprire file BTR.",
  "title" :"BTR - File di database Btrieve",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Che cos'è un file BTR?

Un file con estensione .btr è un file di database creato dall'applicazione di database transazionale [Btrieve](https://www.actian.com/). A differenza dei sistemi di gestione di database relazionali (RBMS), Btrieve si basa sul metodo di accesso sequenziale indicizzato (ISAM), che è un modo per archiviare i dati per un rapido recupero. Il file BTR memorizza una raccolta di record e viene utilizzato per generare report secondo i requisiti. I file BTR possono essere aperti utilizzando Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility e Legend Software BTRIEVE Viewer.

## Struttura del file BTR - Ulteriori informazioni

La struttura dei dati interni e l'allineamento di ciascun byte nella struttura di un file BTR non sono disponibili pubblicamente. Tuttavia, Btrieve
fornisce l'[API Btrieve](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) che può essere utilizzata per leggere le informazioni dai file BTR. È compatibile con i seguenti linguaggi di programmazione e ambienti di sviluppo.

* Embarcadero C/C++
* Embarcadero Delfi
* GNU C/C++
* Micro Focus COBOL
* Microsoft Visual Basic
* Microsoft Visual C++
* Watcom C/C++

Il recupero dei dati da un file BTR dipende dal file DDF associato con esso. Senza il DDF, non sarà facile recuperare le informazioni da un tale file.

## Riferimenti

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Introduzione alle API Btreive](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

