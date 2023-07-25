{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Formato scambio materiale",
  "keywords" :[ "MXF", "video matroska", "formato mkv", "come riprodurre file MXF", "SMPTE", "multimedia", "video" ],
  "description":"Scopri il formato di file MXF e le API che possono creare e aprire file MXF.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## Che cos'è un file MXF?

Un file con estensione .mxf è un formato contenitore multimediale che contiene supporti audio e video digitali insieme a informazioni sui metadati sul file. Segue lo standard SMPTE (Society of Motion Picture and Television Engineers), un'associazione globale di professionisti dell'ingegneria, della tecnologia e dei dirigenti che lavorano nel settore dei media e dell'intrattenimento. I file MXF possono essere convertiti in altri formati di file come [AVI](/it/video/avi/) o [MOV](/it/video/mov/).

## Formato file MXF

I file MXF sono infatti file binari costituiti da una sequenza di byte in un formato definito. Le applicazioni di decodifica devono essere conformi a questo formato per comprenderlo ed estrarne informazioni. Il formato consente di aggiungere nuovi elementi senza interrompere la compatibilità con le versioni precedenti utilizzando la codifica KLV descritta di seguito.

* Chiave: l'identificatore dell'elemento, un'etichetta universale SMPTE (UL)
* Lunghezza: la lunghezza dei dati che è la codifica a lunghezza variabile utilizzata per ridurre la quantità di spazio richiesta per questo elemento
* Valore: il valore effettivo dell'elemento.

### Specifiche del formato SMPTE

Il formato file MXF è stato definito dalle seguenti specifiche SMPTE.

* SMPTE ST 377-1:2011. Televisione — Formato scambio materiale (MXF) — Specifica formato file
* SMPTE ST 377-2 (lavori in corso da gennaio 2012). Sintassi dell'estensione codificata KLV per MXF.
* SMPTE ST 378:2004 (Archiviato nel 2010). Televisione — Material Exchange Format (MXF) — Modello operativo 1a (articolo singolo, pacchetto singolo)
* SMPTE ST 379-1:2009. Material Exchange Format (MXF) — Contenitore generico MXF
* SMPTE ST 379-2:2010. Material Exchange Format (MXF) -- Contenitore generico vincolato MXF
* SMPTE ST 380:2004. Televisione — Material Exchange Format (MXF) — Descriptive Metadata Scheme-1 (Standard, Dynamic)
* SMPTE ST 381-1:2005. Televisione — Material Exchange Format (MXF) — Mappatura dei flussi MPEG nel contenitore generico MXF (dinamico)
* SMPTE ST 381-2:2011. Material Exchange Format (MXF): mappatura dei flussi MPEG nel contenitore generico vincolato MXF
* SMPTE ST 382:2007. Material Exchange Format (MXF): mappatura di flussi AES3 e Broadcast Wave Audio al contenitore generico MXF
* SMPTE ST 383:2008. Televisione — Material Exchange Format (MXF) — Mappatura dei dati DV-DIF sul contenitore generico MXF
* SMPTE ST 384:2005. Televisione — Material Exchange Format (MXF) — Mappatura di immagini non compresse nel contenitore generico MXF
* SMPTE ST 385:2004. Televisione — Material Exchange Format (MXF) — Mappatura dell'essenza e dei metadati SDTI-CP nel contenitore generico MXF
* SMPTE ST 386:2004 (Archiviato nel 2010). Televisione — Material Exchange Format (MXF) — Mappatura dei dati dell'essenza di tipo D-10 sul contenitore generico MXF
* SMPTE ST 387:2004 (Archiviato nel 2010). Televisione — Material Exchange Format (MXF) — Mappatura dei dati dell'essenza di tipo D-11 sul contenitore generico MXF
* SMPTE ST 388:2004 (Archiviato 2010). Televisione — Material Exchange Format (MXF) — Mappatura dell'audio codificato di legge A nel contenitore generico MXF
* SMPTE ST 389:2005. Televisione — Material Exchange Format (MXF) — MXF Generic Container Reverse Play System Element
* SMPTE ST 390:2011. Televisione — Material Exchange Format (MXF) — Modello operativo specializzato "Atom" (rappresentazione semplificata di un singolo elemento)
* SMPTE ST 391:2004 (Archiviato nel 2010). Televisione — Material Exchange Format (MXF) — Operational Pattern 1b (Single Item, Ganged Packages)
* SMPTE ST 392:2004. Televisione — Material Exchange Format (MXF) — Operational Pattern 2a (Play-list Items, Single Package)
* SMPTE ST 393:2004. Televisione — Material Exchange Format (MXF) — Operational Pattern 2b (Play-list Items, Ganged Packages)
* SMPTE ST 394:2006. Televisione — Material Exchange Format (MXF) — Schema di sistema 1 per il contenitore generico MXF
* SMPTE ST 405:2006. Televisione — Material Exchange Format (MXF) — Elementi ed elementi di dati individuali per lo schema 1 del sistema di container generici MXF
* SMPTE ST 407:2006. Televisione — MXF — Schemi operativi 3a e 3b
* SMPTE ST 408:2006. Televisione — MXF — Schemi operativi 1c, 2c e 3c
* SMPTE ST 410: 2008. Formato di scambio di materiali - Partizione di flusso generica.
* SMPTE ST 422:2006. Formato di scambio materiale: mappatura dei flussi di codice JPEG2000 nel contenitore generico MXF
* SMPTE ST 429.4:2006. Imballaggio D-Cinema — Applicazione MXF JPEG 2000
* SMPTE ST 429.5:2006. Packaging D-Cinema — File di tracce di testo a tempo
* SMPTE ST 429.6:2006. D-Cinema Packaging: crittografia MXF Track File Essence
* SMPTE ST 434:2006. Material Exchange Format: codifica XML per metadati e informazioni sulla struttura dei file
* SMPTE ST 436:2006. Televisione: mappature MXF per linee VBI e pacchetti di dati ausiliari
* SMPTE ST 2019-4:2009. Mappatura delle unità di codifica VC-3 nel contenitore generico MXF
* SMPTE ST 2037:2009. Mappatura di VC-1 nel contenitore generico MXF
* SMPTE RP 2008:2008. Formato di scambio materiale: mappatura dei flussi AVC nel contenitore generico MXF
* SMPTE RP 2057:2011. Trasporto di metadati testuali in MXF
* SMPTE EG 41:2004. Material Exchange Format (MXF) — Linee guida ingegneristiche. Nota: questo documento non era più elencato nel sito Web SMPTE quando consultato nel gennaio 2012.
* SMPTE EG 42:2004. Material Exchange Format (MXF) — Metadati descrittivi MXF
* SMPTE RDD 3:2008. Specifiche di interoperabilità e-VTR MXF
* SMPTE RDD 9-2009. Specifiche di interoperabilità MXF dei prodotti Sony MPEG Long GOP
* Menu del foglio di calcolo del registro dei metadati SMPTE.

### Metadati strutturali MXF

I metadati strutturali sono fondamentali in un file MXF in quanto contengono informazioni utili sul contenuto del file. I metadati MXF contengono informazioni come frequenza fotogrammi, dimensione fotogramma, data di creazione del file e data di modifica personalizzata. I metadati strutturali descrivono la struttura e le capacità di un file MXF che include la descrizione tecnica dei vari componenti essenziali e il modo in cui è composta la sequenza temporale di output.

## Riferimenti

* [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - Rapporto sullo stato di avanzamento](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [Libreria C++ OpenSource per MXF](http://www.freemxf.org/)

