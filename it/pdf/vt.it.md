{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file PDF/VT",
  "description":"Scopri il formato di file PDF/VT e le API che possono creare e aprire file PDF/VT.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Che cos'è PDF/VT? #

PDF/VT, pubblicato come [ISO 16612-2](https://www.iso.org/standard/46428.html) nell'agosto 2010 come standard, è progettato per consentire la stampa di documenti variabili (VDP) in una varietà di ambienti. Lo standard fa delle informazioni variabili e della stampa transazionale come base per lo standard. La stampa dei dati variabili viene utilizzata laddove una parte delle informazioni è diversa per ciascun destinatario del contenuto. La stampa transazionale include fatture, estratti conto e altri documenti che combinano informazioni di fatturazione con informazioni di marketing. Ciò si traduce in un mix di elaborazione migliorata di immagini, testo e altri tipi di contenuto. PDF/VT consente una gestione affidabile e dinamica delle pagine per i dati di stampa HVTO (High Volume Transactional Output) utilizzando il concetto di metadati delle parti del documento (DPM). I file PDF/VT possono essere aperti nel visualizzatore Adobe Acrobat senza la necessità di aggiungere altri componenti.

## Gerarchia delle parti del documento ##

La Gerarchia delle parti del documento (DPart) è come una struttura ad albero di nodi delle parti del documento basata su tutte le pagine del documento. Gli elementi di questo albero sono chiamati nodi DPart. Ogni nodo interno contiene altri nodi DPart e ogni nodo foglia specifica una o più pagine per un destinatario. In sostanza, la gerarchia DPart specifica la sequenza e la relazione di documenti o parti di documenti in un file PDF/VT. La struttura ad albero dei nodi DPart rappresenta facilmente il contenuto interno di un documento PDF/VT in quanto può contenere documenti secondari per molti destinatari e ogni parte del documento corrisponde alle pagine per un singolo destinatario. La gerarchia DPart è richiesta nei file PDF/VT.

## Metadati delle parti del documento (DPM) ##

I metadati delle parti del documento (DPM) sono associati a ciascun nodo nella gerarchia delle parti del documento e possono essere utilizzati per comunicare informazioni su un documento secondario di un particolare destinatario e le sue parti. In particolare, il DPM può contenere informazioni sulle proprietà o informazioni sui destinatari in forma codificata.

## Livelli di conformità ##

PDF/VT è conferito ai seguenti tre livelli di conformità. Questi sono tutti basati su [PDF](/it/pdf/) 1.6.

* `PDF/VT-1` - Si basa su PDF/X-4 e contiene tutte le risorse necessarie per il rendering di un documento PDF.
* `PDF/VT-2` - Progettati per lo scambio di più file, i documenti PDF/VT-2 possono fare riferimento a intenti di output esterni, contenuti esterni o entrambi. Un documento PDF/VT e tutti i suoi file PDF di riferimento e gli intenti di output esterni sono chiamati collettivamente set di file PDF/VT-2. Acrobat 9 e supporta questa funzione.
* `PDF/VT-2s` - Supporta lo streaming live PDF/VT-2. Ciò consente di elaborare sezioni di dati segmentate.

## Riferimenti ##

* [PDF/VT - Di Wikipedia](https://en.wikipedia.org/wiki/PDF/VT)
* [Tecnologia grafica ISO 16612-2](https://www.iso.org/standard/46428.html)

