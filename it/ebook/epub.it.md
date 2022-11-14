{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "file", "estensione", "formato", "E-Book", "Libro digitale" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file EPUB e le API che possono creare e aprire file EPUB.",
  "title" :"Cos'è un file EPUB?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Che cos'è un file EPUB?

I file con estensione .epub sono un formato di file di e-book che fornisce un formato di pubblicazione digitale standard per editori e consumatori. Il formato è ormai così comune da essere supportato da molti e-reader e applicazioni software. Ad esempio, su Mac OS, il software **Books** preinstallato fornisce il supporto per l'apertura di tali file. Inoltre, sono disponibili molti software compatibili per smartphone, tablet e computer. Gli standard dei file EPUB sono mantenuti dall'[International Digital Publishing Forum](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). La versione EPUB 3 è anche approvata dal Book Industry Study Group (BISG), una delle principali associazioni di categoria di libri per le migliori pratiche standardizzate, la ricerca, le informazioni e gli eventi, per il confezionamento dei contenuti.

## Breve storia del formato di file EPUB

* **Ottobre 2007** - Approvato EPUB 2.0
* **Settembre 2010** - È stato rilasciato l'aggiornamento di manutenzione
* **Ottobre 2011** - Le specifiche EPUB 3.0 sono entrate in vigore
* **Giugno 2014** - È stato rilasciato un aggiornamento di manutenzione minore per sostituire la versione 3.0
* **Gennaio 2017** - EPUB 3.1 è entrato in vigore

## Formato file EPUB

Il formato di file EPUB è un archivio che può essere rinominato con estensione [ZIP](/it/compression/zip/) e il suo contenuto può essere visualizzato estraendo l'archivio con qualsiasi estrattore di archivi. È un formato aperto basato su XML ed è costituito da file HTML, immagini, fogli di stile CSS e altri elementi. Può anche essere convertito in PDF, Mobi e molti altri formati di file tramite una serie di applicazioni software e API.

{{< figure src="../epub.png" alt="Formato file EPUB" >}}

**E-Book EPUB aperto con l'applicazione Libri Mac OS**

Il formato del file EPUB si basa sui seguenti tre standard aperti.

### Struttura pubblica aperta (OPS) ###

Un file EPUB 2.0 utilizza XHTML 1.1 per costruire il contenuto di una pubblicazione. In sostanza questo significa che un file EPUB è costituito da una o più pagine web. Anche se puoi includere l'intero contenuto di un libro o di un giornale in un'unica pagina, è meglio che tale file non superi i 300.000, sia per motivi di prestazioni che di compatibilità. Proprio come con le normali pagine Web, lo stile e il layout sono definiti utilizzando fogli di stile a cascata (CSS). Nei file EPUB è necessario utilizzare un sottoinsieme (serie limitata di comandi) di CSS2. Molte delle nuove funzionalità di CSS3, come riquadri arrotondati o ombre discendenti, non sono ancora disponibili. Per la compatibilità con le versioni precedenti, un creatore può anche utilizzare DTBook invece di XHTML per codificare il contenuto.

### Formato di imballaggio aperto (OPF) ###

Questa parte delle specifiche si occupa di informazioni strutturali come i metadati (chi è l'autore e l'editore, qual è il titolo,..), il manifest (un elenco di tutti i file all'interno di un file epub) e il sommario. Questi dati sono tutti incorporati utilizzando XML.

### Formato contenitore aperto (OCF) ###

Come le descrizioni precedenti avrebbero dovuto chiarire, un documento EPUB è costituito da una serie di file. Le specifiche OCF definiscono come tutti quei file finiscono per essere impacchettati in un unico file contenitore. Per questo viene utilizzata la compressione ZIP.

## Formati di file immagine supportati ##

Il formato di file EPUB supporta i seguenti formati di file di immagine.

* [GIF](/it/image/gif/)
* [JPG](/it/image/jpeg/)
* [PNG](/it/image/png/)
* [SVG](/it/page-description-language/svg/)

## Riferimenti ##

* [EPUB - Di Wikipedia](https://en.wikipedia.org/wiki/EPUB)

