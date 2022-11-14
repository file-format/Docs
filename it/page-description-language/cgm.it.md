{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Metafile di grafica per computer", "File", "Estensione", "Formato file", "Grafica vettoriale", "Descrittore metafile"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file CGM",
  "description":"Scopri il formato di file CGM e le API che possono creare e aprire file CGM.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Che cos'è un file CGM? ##

Computer Graphics Metafile (CGM) è un formato metafile standard internazionale gratuito, indipendente dalla piattaforma per l'archiviazione e lo scambio di grafica vettoriale (2D), grafica raster e testo. CGM utilizza un approccio orientato agli oggetti e molte disposizioni di funzioni per la produzione di immagini. CGM utilizza queste caratteristiche orientate agli oggetti per rimodellare elementi grafici per il rendering di un'immagine. Un metafile contiene le informazioni necessarie che definiscono altri file. In CGM, un file sorgente basato su testo contiene tutti gli elementi grafici che possono essere successivamente compilati in un file binario. Fondamentalmente, CGM è un modo per facilitare lo scambio di dati grafici 2D, indipendentemente da qualsiasi piattaforma o dispositivo particolare.

Il formato CGM fornisce diversi elementi per eseguire funzioni e significare oggetti per regolare le primitive geometriche e le informazioni grafiche. Sebbene CGM sia stato sostituito da altri formati per visualizzare le arti grafiche su pagine Web in quanto non ben supportato dalle pagine Web, è ancora molto popolare tra le applicazioni industriali, aeronautiche e altre applicazioni tecniche. Sebbene il World Wide Web Consortium abbia sviluppato WebCGM, un approccio alternativo per l'uso del CGM sul Web. L'implementazione CGM principale era un'illustrazione della sequenza delle operazioni di base del Graphical Kernel System (GKS). Non è stato molto adottato nei progetti professionali, ma è stato ampiamente soppiantato da altri formati come DXF e SVG.

## Storia ##

CGM si è rivelato essere uno standard internazionale nel 1987 (ISO 8632-1987) ed è stato adottato anche come standard nazionale nel Regno Unito da BSI e negli Stati Uniti da ANSI. Dopo una serie di modifiche nel 1991, uno standard rivisto di CGM è stato rilasciato nel 1992 (ISO 8632:1992). Nel 2001, il World Wide Web Consortium ha sviluppato WebCGM con capacità avanzate per essere utilizzato con le pagine Web. Nel 2007 è stata rilasciata la seconda versione di WebCGM e la terza versione è stata rilasciata nel 2010 con funzionalità avanzate.

## Formato file CGM ##

I metafile di computer grafica sono fondamentalmente database per informazioni grafiche e forniscono i mezzi per l'acquisizione, l'archiviazione e la trasmissione di dati grafici. Di conseguenza, deve essere presente un componente di sistema grafico per la creazione simultanea del database insieme all'esecuzione di un'applicazione in un formato metafile. Nella maggior parte dei casi, questo componente è il generatore di Metafile. Inoltre, è necessario un altro componente in grado di recuperare, interpretare e rendere i dati grafici in un metafile. Questa esigenza è soddisfatta dalla presenza di un interprete di metafile. La figura seguente rappresenta l'ambiente di lavoro grafico del metafile.

La relazione di CGM con altri componenti di un tipico sistema grafico è illustrata nella figura sopra. È anche evidente dalla figura che la funzionalità del metafile non dipende dall'output del dispositivo finale.

In genere, ci sono due categorie di metafile: **acquisizione sezione** e **acquisizione immagine**. La funzionalità principale del metafile di acquisizione delle immagini è l'acquisizione di definizioni di immagini multiple indipendenti dal dispositivo. Mentre i metafile di acquisizione della sessione utilizzano l'interfaccia di sistema per acquisire il dialogo di output in un sistema grafico. CGM appartiene alla categoria dei metafile di acquisizione di immagini statiche. CGM fornisce una disposizione ben organizzata dei componenti con una struttura a due livelli.

1. Descrittore di metafile
1. Un pool di immagini logicamente indipendenti

Ogni immagine è una raccolta di descrittori dell'immagine e un corpo dell'immagine che include una definizione dell'immagine. il descrittore di metafile definisce le informazioni descrittive che si applicano ugualmente a tutte le immagini di quel metafile. Queste informazioni consentono all'interprete di analizzare correttamente un metafile e riconoscere le risorse necessarie per il corretto rendering di un'immagine. Sebbene il descrittore dell'immagine racchiuda anche le informazioni descrittive, tuttavia può riconoscere solo l'immagine in cui risiede il descrittore. In questo formato di file, ogni definizione di immagine è autonoma e logicamente sovrana. Sono indipendenti da tutte le altre definizioni di immagine in un file. Subito dopo l'interpretazione del meta-descrittore, è possibile accedere alle immagini e interpretarle in modo casuale. Il cambiamento nello stato delle immagini precedenti non ha alcun effetto sui loro successori. Questa indipendenza dall'immagine è un'altra caratteristica importante di CGM.CGM consiste nello spazio delle coordinate che sono coordinate cartesiane 2D chiamate coordinate del dispositivo virtuale e possono essere rappresentate tramite numero o precisione che rappresentano l'intervallo e la granularità. CGM specifica sia la selezione diretta dei colori che la selezione basata su indici. Nel primo, l'identificatore di colore è costituito da una tripla RGB mentre in seguito, l'identificatore di colore indica un indice in una tabella di colori.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
