{
  "date" : "2019-10-11",
  "keywords" :[ "file emf", "formato file emf", "cos'è un file emf", "file", "esempio emf", "estensione file emf", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - Formato metafile avanzato",
  "description":"Scopri il formato di file EMF e le API che possono creare e aprire file EMF.",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file EMF?

**Enhanced Metafile Format (EMF)** memorizza le immagini grafiche indipendentemente dal dispositivo. I metafile di EMF comprendono record di lunghezza variabile in ordine cronologico che possono eseguire il rendering dell'immagine archiviata dopo l'analisi su qualsiasi dispositivo di output. Questi record a lunghezza variabile possono essere definizioni di oggetti racchiusi, comandi per il disegno e proprietà grafiche fondamentali per il rendering accurato dell'immagine. Quando un dispositivo apre un metafile EMF utilizzando il proprio ambiente grafico, le proporzioni, le dimensioni, i colori e altre proprietà grafiche dell'immagine originale rimangono le stesse indipendentemente dalla piattaforma del dispositivo di apertura.

## Breve storia ##

Nel 1990, Microsoft ha progettato un formato di file immagine Windows Metafile ([WMF](/it/image/wmf/)) per Microsoft Windows. I metafile di Windows sono un formato a 16 bit che può contenere alcuni componenti bitmap. WMF può essere costituito da grafica vettoriale ed è destinato a mantenersi portabile tra diverse applicazioni. Nel 1993, Win32/GDI ha annunciato l'Enhanced Metafile (EMF), una versione più recente con maggiore flessibilità e scalabilità. EMF utilizzato anche come comandi del linguaggio grafico per eseguire i driver della stampante. Microsoft consiglia ora il formato di metafile avanzato (EMF) sul formato Windows (WMF). Quando è stato introdotto Windows XP, è stata rilasciata la versione Enhanced Metafile Format Plus (EMF+). Questa versione più recente trova la sua strada serializzando le chiamate API GDI+ allo stesso modo WMF/EMF registra le chiamate a GDI. Esiste una versione compressa gzip di EMF nota come EMZ.

## Formato metafile EMF ##

Di seguito sono riportati gli elementi essenziali del formato metafile avanzato:

* Un EMR_HEADER (versione, dimensione, risoluzione dell'immagine al momento della creazione)
* Una tabella per gli oggetti GDI
* Una tavolozza riservata (opzionale)
* Record di metafile disposti in una struttura di matrice (impostazioni delle proprietà, oggetti definiti, comandi di disegno)
* Record EMR_EOF (ultimo record nel metafile EMF)

## Versioni EMF ##
* **Originale**: la versione originale specifica il record necessario per mantenere l'immagine originale e mantenere il suo dispositivo indipendente. Supporta inoltre il record contenente oggetti grafici e comandi per il disegno.
* **Versione 1**: la seconda versione di EMF ha migliorato la flessibilità e l'indipendenza dal dispositivo aggiungendo il record per il formato pixel e la disposizione per utilizzare il comando OpenGL.
* **Versione 2**: la terza versione ha migliorato la precisione aggiungendo il sistema Metric per misurare le distanze della superficie del dispositivo, lasciando il record più scalabile.

## Record di metafile migliorati ##

I record di metafile sono organizzati sotto forma di array. Questi record hanno struttura ENHMETARECORD e lunghezza variabile. ENHMETARECORD specifica i dati che definiscono le funzioni GDI per creare un'immagine utilizzando un formato metafile avanzato. La struttura **ENHMETAHEADER** è sempre il primo record in questo formato. Questa intestazione EMF contiene le seguenti informazioni.

Ogni record di metafile avanzato ha due membri di EMR (fornisce la struttura di base) all'inizio. Il primo membro riconosce la funzione GDI (i parametri vengono utilizzati nel record) che determina il tipo di record ed è noto come iType. L'altro membro nSize definisce la dimensione di ogni record. Parametri rimanenti (se presenti) e dati aggiuntivi disposti immediatamente sotto nSize. Immediatamente dopo l'intestazione potrebbe essere presente una descrizione testuale opzionale. Il nome dell'immagine e dell'autore è registrato in quella descrizione testuale. La tavolozza la cui presenza è un'opzione specifica i colori utilizzati nella creazione avanzata di metafile. Gli altri record utilizzati per specificare la funzione GDI che è essenziale nella creazione di immagini.

Almeno un record EMF dovrebbe essere presente in ogni metafile. Le informazioni di attraversamento da un record all'altro dipendono dai record EMF, quindi questi record devono essere disposti adiacenti. In qualsiasi dato record nel metafile eccetto EOF_record, la lunghezza di quel particolare record definisce per passare al record successivo.

## Creazione di metafile migliorata ##

La funzione **CreateEnhMetaFile** viene utilizzata per creare un metafile avanzato. Gli argomenti di questa funzione vengono utilizzati per le dimensioni e la memorizzazione dell'immagine su disco/memoria. Inoltre, questa funzione richiede la dimensione del dispositivo in cui l'immagine è apparsa per prima (dispositivo di riferimento) e il contesto del dispositivo di riferimento (DC). Quindi gli argomenti per gestire questo controller di dominio devono fornire quando si chiama la funzione **CreateEnhMetaFile**. La sintassi della funzione è la seguente:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** gestisce un dispositivo di riferimento.

**lptoFilename:** Un puntatore al nome del file.

**lprc:** Il puntatore alla struttura ovale specifica le dimensioni dell'immagine in mm.

**lpDesc:** un puntatore a una stringa per il titolo dell'immagine e il nome dell'applicazione che ha creato l'immagine.

## Operazioni avanzate sui metafile ##

Di seguito sono riportati i lavori che possono essere eseguiti utilizzando l'handle in un metafile avanzato.

* Visualizza e modifica per l'immagine memorizzata.
* Produci copie di metafile avanzate.
* Recupera la copia di un'intestazione EMF, la descrizione facoltativa e la versione binaria di un metafile avanzato
* Ricapitola i colori nella tavolozza.

## Oggetti grafici ##

Nelle operazioni di disegno e pittura, gli oggetti grafici possono essere creati dai record di creazione degli oggetti e possono essere salvati per un ulteriore utilizzo. Un record `EMR_SELECTOBJECT` può recuperare questi oggetti grafici utilizzando il contesto del dispositivo di riproduzione. Penne, tavolozze, pennelli, spazi colore, caratteri e oggetti stock sono alcuni tipi di oggetti riutilizzabili.

## Ordinamento byte ##

Il formato little-endian viene utilizzato per archiviare i dati nei record di metafile.

## Versione ##

Il formato del file EMF è stato rivisto due volte. Le versioni modificate sono originale, estensione 1 ed estensione 2. Le versioni estese prevedono record OpenGL e un descrittore opzionale per il formato pixel interno. Per le dimensioni visualizzate viene aggiunta una funzione di misurazione in millilitri.

## Riferimenti ##

* [Metafile in formato avanzato | Microsoft Docs](https://learn.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Formato e specifica del metafile migliorati](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

