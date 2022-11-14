{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file PS",
  "description":"Scopri il formato di file PS e le API che possono creare e aprire file PS.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file .PS? ##

PostScript (PS) è un linguaggio di descrizione di pagina generico utilizzato nel business del desktop e dell'editoria elettronica. L'obiettivo principale di PostScript (PS) è facilitare la progettazione grafica bidimensionale. La maggior parte dei linguaggi richiede una fase di compilazione distinta prima dell'esecuzione del codice, mentre il formato Post Script (PS) supporta un'interpretazione diretta di runtime. La sua prima versione definisce le forme grafiche, i diversi aspetti del testo e le immagini modellate sulle pagine stampate o visualizzate, seguendo le regole del modello di imaging Adobe. Un programma di PS è in grado di intercomunicare una descrizione del documento tra una composizione e un sistema di stampa mantenendo il dispositivo indipendente e di alto livello. Inoltre questo programma è anche in grado di governare l'aspetto del testo e della grafica su un display.

La descrizione della pagina PostScript può essere renderizzata, visualizzata su stampante e altro dispositivo di output con l'aiuto dell'interprete PostScript del dispositivo. Poiché i comandi per stampare caratteri, forme grafiche e immagini vengono eseguiti dall'interprete, per quel dispositivo specifico, la descrizione PostScript di alto livello viene convertita nel formato di dati raster di basso livello. In genere, diverse applicazioni come illustratori, sistemi di composizione di documenti e progettazione assistita da computer (CAD) vengono automatizzate per generare descrizioni di pagina PostScript. Generalmente i programmatori devono scrivere programmi PostScript al momento della creazione di nuove applicazioni. Tuttavia, un programmatore può sfruttare le capacità del linguaggio PostScript che non sono accessibili in nessuna applicazione scrivendo un programma PS per quella situazione speciale.

## Breve storia ##

Il concetto di linguaggio PostScript è stato introdotto per la prima volta da John Warnock. Nel 1966 stava lavorando a un progetto del porto di New York. Stava cercando di sviluppare un interprete per una grande grafica tridimensionale per il database di quel progetto. Per elaborare queste grafiche, John Warnock ha concepito il linguaggio Design System. Nel frattempo Xerox PARC stava cercando un mezzo standard per definire le immagini delle pagine per la sua prima stampante laser. Sebbene Bob Sproull e William Newman nel 1975-76 abbiano sviluppato il formato Press (formato dati) per guidare le stampanti laser, tuttavia era necessario un linguaggio per una maggiore flessibilità. Nel 1978 Warnock si unì a Martin Newell in Xerox PARC e riscrisse il linguaggio interpretativo, JaM, che in seguito fu ampliato ed esteso al linguaggio Interpress. Warnock ha fondato Adobe Systems nel dicembre 1982 con Chuck Geschke, Doug Brotz, Ed Taft e Bill Paxton. Hanno iniziato a lavorare su un linguaggio più semplice chiamato PostScript simile a Interpress, che è stato rilasciato in commercio nel 1984. Steve Jobs di Apple li ha visitati e ha consigliato loro di adattare PostScript per guidare le stampanti laser.

Nel marzo 1985, la prima stampante con un interprete PostScript incorporato è stata LaserWriter di Apple, che ha rivoluzionato il desktop publishing (DTP). La solidità tecnica e l'ampia disponibilità hanno reso PostScript un linguaggio d'elezione per il desktop e l'editoria elettronica. Nel corso del 1990, un interprete per il linguaggio PostScript è stato una parte essenziale delle stampanti laser.

## Caratteristiche principali ##

Le capacità del linguaggio PostScript di gestire la grafica interattiva e la descrizione delle pagine possiedono le seguenti caratteristiche:

**Forme:** di natura arbitraria, possono comprendere linee rette, curve, quadrati e curve cubiche che possono essere sia autotraversanti che disconnesse (nelle sezioni e nei fori).

**Operatori di pittura:** consentono il contorno della forma di qualsiasi spessore, colore, riempimento o consentono di disegnare la forma come ritaglio per consentire il ritaglio di qualsiasi altro elemento grafico.

**Colori:** hanno la diversità come scala di grigi, RGB, CMYK e CIE. Tipi speciali di colori sono modellati come caratteristiche diverse: tinte piatte, mappatura dei colori, ombreggiatura uniforme e motivi ripetuti.

**Testo:** completamente integrato con la grafica. Inoltre, il modello di imaging di Adobe consente di visualizzare i caratteri di testo come forme grafiche che possono essere gestite da qualsiasi normale operatore grafico.

**Immagini campionate**: estratte da fonti originali (fotografie digitalizzate) o possono essere prodotte sinteticamente. Il linguaggio PostScript offre diversi mezzi per rigenerare le immagini a qualsiasi risoluzione e in base a diversi modelli di colore su un dispositivo di output.

Un linguaggio di programmazione generico può sfruttare le capacità grafiche del linguaggio PostScript incorporando Ps nel suo framework. I tipi di dati primitivi, come numeri, caratteri, array e stringhe; primitive di controllo, come loop, procedure e condizionali; e alcune funzionalità non convenzionali, come i dizionari, sono specificate nella lingua. Queste caratteristiche facilitano ai programmatori la scrittura di comandi per invocare operazioni di livello superiore. Queste operazioni di alto livello soddisfano le esigenze di applicazioni complesse. Tale pratica è più compatta ed efficiente piuttosto che utilizzare un insieme fisso di operazioni di base.

I programmi scritti in PostScript possono essere prodotti, comunicati e interpretati sotto forma di testo sorgente ASCII. L'intera lingua può essere definita sotto forma di caratteri stampabili e spazi bianchi. Questa rappresentazione supporta i programmatori per creare, manipolare e comprendere facilmente il linguaggio. Inoltre, l'archiviazione e la trasmissione di file tra diversi computer e sistemi operativi sono state mantenute convenienti grazie all'indipendenza dalla macchina.

Sono possibili forme codificate binarie del linguaggio, quando al programma è garantito un percorso di comunicazione completamente trasparente con l'interprete PostScript. Adobe consiglia una stretta coesione alla rappresentazione ASCII dei programmi PS per lo scambio di documenti o l'archiviazione di archivi.

## Versioni ##

PS(.ps) è l'estensione del file per un documento PostScript. Gli archivi nazionali del Regno Unito classificano cinque versioni cronologiche del file PostScript, definito nella versione DSC: versioni 1.0, 2.0, 2.1, 3.0, 3.1. Ogni versione definisce importanti commenti di strutturazione. Encapsulated PostScript File (EPS) è un sottotipo speciale di file PostScript che utilizza il linguaggio per specificare un'immagine rettangolare. Il manuale di riferimento del linguaggio PostScript descrive un EPS come "Un file PostScript (EPS) incapsulato è un programma PostScript che descrive al massimo una singola pagina in un formato che può essere importato da altre applicazioni per incorporarlo in un documento contenitore". Un file di documento PostScript può incapsularvi un file EPS. Un ulteriore uso di PostScript è menzionato come Display PostScript (DPS). DPS genera grafica su schermo tramite un motore grafico che utilizza il modello e il linguaggio di imaging PostScript.

## Riferimenti ##

* [Famiglia di formati PostScript](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

