{
  "date" : "2019-10-11",
  "keywords" :[ "XSLFO", "Oggetti di formattazione XSL", "File", "Estensione", "Formato file", "Linguaggio del foglio di stile estensibile"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"Scopri il formato di file XSLFO e le API che possono creare e aprire file XSLFO.",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Che cos'è un file XSL-FO? ##

XSL-FO (XSL Formatting Objects) è un potente linguaggio di fogli di stile per la formattazione di documenti XML. La semantica della forma delimitata di carta e stampa è espressa da XSL-FO quando le dimensioni sono fisse. In contrasto con HTML, che rappresenta la semantica della forma illimitata di una finestra del browser con dimensioni variabili. I documenti XML formattati da XSL-FO vengono utilizzati principalmente per generare file PDF. XSL (Extensible Stylesheet Language) è un insieme di tecnologie W3C complete di funzionalità destinate alla progettazione per la formattazione e lo scambio di documenti XML e parti XSL-FO di questo linguaggio. XSLT e XPath sono anche altre parti di XSL.

Si propone di trasformare prima i documenti XML in XSL-FO, PDF è un esempio di questo criterio. In PDF, i risultati vengono visualizzati utilizzando prima XSLT e poi il formattatore XSL-FO. In questo modo, i documenti XML possono essere formattati in modo casuale. Sebbene XSL-FO sfrutti il vantaggio di utilizzare le proprietà CSS (Cascading Style Sheet) e di estenderle ove necessario per il formato reale, ospita la fornitura di modelli di pagina chiamati page master nella terminologia di XSL-FO. XSL-FO fornisce anche la formattazione per documenti abbastanza sofisticati e supporta la generazione di indici.

## Storia e concetti di base ##

Nel gennaio 2012 il Working Draft di XSL-FO è stato aggiornato l'ultima volta e nel novembre 2013 il suo gruppo di lavoro è stato chiuso. Un foglio di stile XSL specifica la presentazione di una classe di documenti XML descrivendo come un'istanza della classe viene trasformata in un documento XML che utilizza il vocabolario di formattazione. XSL-FO è un linguaggio di presentazione integrato e non ha markup semantici utilizzati in HTML. Inoltre, questo linguaggio memorizza tutti i dati del documento al suo interno, contrariamente ai CSS che alterano le impostazioni predefinite di un documento HTML o XML esterno.

Il criterio generale per l'utilizzo di XSL-FO è che l'utente scriva un documento in un linguaggio XML anziché in FO. Successivamente, si verifica una trasformazione XSLT. Questa trasformazione XSLT è responsabile della conversione di XML in XSL-FO. Non appena il documento XSL-FO viene generato, viene quindi consegnato a un'applicazione chiamata processore FO. I processori FO sono responsabili della trasformazione di questo documento in un documento leggibile e stampabile. I file PDF o PS sono esempi dell'output più comune di XSL-FO. Ma ciò non significa che il processore FO possa produrre solo questi due tipi di formato come output. Alcuni processori FO possono emettere file RTF o anche una finestra può apparire nella GUI dell'utente, questa finestra mostra la sequenza della pagina e il loro contenuto.

Un documento XSL-FO è diverso da un PDF o un PS nel senso che non definisce in definitiva il layout del testo su pagine diverse. Forse, modella le pagine e determina i luoghi in cui visualizzare i contenuti. Inoltre, un elaboratore FO organizza il testo entro i limiti specificati dal documento FO. Questa specifica consente anche a diversi processori FO di comportarsi di conseguenza alle pagine risultanti create. Un esempio di tale comportamento è la sillabazione, pochi processori FO possono sillabare le parole per risparmiare spazio quando una riga si interrompe, mentre alcuni processori non selezionano questa opzione. Dipende dai processori scegliere diversi algoritmi di sillabazione che soddisfino i loro requisiti. Questi algoritmi di sillabazione possono essere molto semplici o forse più complessi. In alcune situazioni, la specifica XSL-FO sanziona esplicitamente i processori FO, un certo grado di scelta nel contesto del layout.

Questa variazione tra i processori FO genera risultati variabili, di cui i processori spesso rimangono indifferenti. Perché l'obiettivo generale di XSL-FO è produrre documenti impaginati/stampati. I documenti XSL-FO stessi in genere fungono da intermediari, la loro funzione principale è quella di generare file PDF o un documento che può essere stampato come output da distribuire. In HTML/CSS o XSL-FO, la distribuzione del PDF come risultato finale anziché l'immissione del linguaggio di formattazione indica che i ricevitori rimangono inalterati dalla versatilità risultante che viene prodotta a causa delle differenze tra gli interpreti del linguaggio di formattazione. D'altra parte, è evidente che non esiste un modo semplice, che un documento possa soddisfare le diverse esigenze dei destinatari, ad es. dimensione pagina variabile o dimensione del carattere desiderata, o personalizzazione della pagina o della stampa.

## Formato file XSLFO ##

I documenti SL-FO sono fondamentalmente documenti XML, ma non seguono alcuno schema. Al suo posto, i documenti SL-FO seguono la sintassi definita nella specificazione della propria lingua. Ci sono due sezioni richieste in ogni documento XSL-FO:

1. Una sezione che specifica un elenco di layout di pagina etichettati.
1. Una sezione con tutti i dettagli dei dati del documento, con markup, che determina la visualizzazione dei contenuti su pagine diverse attraverso diversi layout di pagina.

Le proprietà della pagina sono menzionate nei layout di pagina, che possono definire l'organizzazione del testo, per rispettare le convenzioni per la lingua specifica. Inoltre, la dimensione della pagina, i suoi margini e le sequenze di pagine (che sancisce proprietà diverse per le pagine pari e dispari) sono anche definiti dai layout di pagina.

La porzione di dati del documento è suddivisa in una serie di flussi, in cui ogni flusso è collegato a un layout di pagina. I flussi racchiudono un elenco di blocchi al loro interno. Questo elenco di blocchi può contenere funzionalità di markup in linea o un elenco di dati di testo, o forse entrambi contemporaneamente. I margini del documento possono anche visualizzare i numeri di pagina o le intestazioni dei capitoli. La funzionalità di entrambi i blocchi e degli elementi inline rimane la stessa del CSS, tuttavia alcune regole di riempimento e margine sono diverse tra FO e CSS.

La direzione di orientamento della pagina è interamente specificata per l'estensione di blocchi e inline, rendendo così i documenti FO eseguiti in lingue diverse dall'inglese. Il linguaggio della specifica FO utilizza le parole inizio e fine anziché sinistra e destra per la descrizione delle direzioni. Il markup del contenuto di base di XSL-FO e le regole a cascata sono presi dai CSS. Il linguaggio di XSL-FO è conforme alle seguenti specifiche.

## Più colonne ##

Una pagina può avere più colonne e blocchi e può estendersi da una colonna all'altra per impostazione predefinita. Più pagine possono avere larghezze e numeri di colonne diversi. Tutte le caratteristiche FO seguono i limiti di una pagina a più colonne.

### Elenchi ###

Un elenco XSL-FO è stabilito da due serie di blocchi disposti guancia per guancia. Concettualmente, in un elenco, un blocco a sinistra indica un numero, un punto elenco o una stringa di testo, mentre il blocco a destra può funzionare come previsto. La numerazione degli elenchi XSL-FO viene solitamente eseguita dall'XSLT.

### Tabelle ###

Una tabella FO è simile a una tabella HTML/CSS. L'utente può selezionare le righe di dati, le informazioni sullo stile, il colore di sfondo per ogni singola cella. Utilizzando informazioni di stile distinte, l'utente ha il privilegio di selezionare la prima riga come riga di intestazione della tabella. Il processore FO può essere informato in modo esplicito sulla specifica dello spazio di ciascuna colonna o per adattare automaticamente il testo nella tabella.

### Indicizzazione ###

XSL-FO 1.1 ha funzionalità che aiutano a generare un indice facendo riferimento a elementi correttamente contrassegnati.

### Benefici ###

* Appropriato per la pubblicazione basata sui contenuti
* Facilità d'uso
* A basso costo

## Riferimenti ##

* [Cos'è XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [Oggetti di formattazione XSL](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

