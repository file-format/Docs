{
  "date" : "2019-12-10",
  "keywords" :[ "XLSB", "file", "estensione", "formato file", "File foglio di calcolo binario Excel"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"La tua guida al formato dei file per sapere cos'è un file XLSB e le API che possono crearli e aprirli.",
  "title" :"Cos'è un file XLSB?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Che cos'è un file XLSB?

Il formato file XLSB specifica il formato file binario di Excel, che è una raccolta di record e strutture che specificano il contenuto della cartella di lavoro di Excel. Il contenuto può includere tabelle di numeri non strutturate o semi-strutturate, testo o sia numeri che testo, formule, connessioni dati esterne, grafici e immagini. A differenza di [XLSX](/it/spreadsheet/xlsx/) (che si basa sul formato di file Open XML), XLSB rappresenta il file binario della cartella di lavoro di Excel. I file XLSB possono essere letti e scritti più velocemente, il che li rende utili per lavorare con file di grandi dimensioni. XLSB viene utilizzato raramente per archiviare cartelle di lavoro poiché XLSX (e in precedenza [XLS](/it/spreadsheet/xls/)) sono i formati di file selezionati dall'utente più comuni per il salvataggio delle cartelle di lavoro. Può essere aperto da Microsoft Office 2007 e versioni successive.

## Specifiche del formato file XLSB ##

Le specifiche del formato file per il formato file XLSB sono state rese pubbliche nel 2008 come versione 1.0. Da allora, le specifiche sono state riviste più volte e l'ultima versione delle specifiche (v 10.0) è stata pubblicata nell'aprile 2018. Le specifiche sono disponibili pubblicamente da Microsoft come [[MS-XLSB] - Specifiche del formato file binario di Excel](https:/ /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) e dovrebbe essere consultato da chiunque per leggere o scrivere file in formato XLSB.

## Struttura del file XLSB ##

Un file XLSB è un pacchetto che consiste in una raccolta di parti. Queste parti contengono informazioni sul contenuto di una cartella di lavoro, inclusi i dati della cartella di lavoro e la struttura del pacchetto. Alcune parti contengono informazioni archiviate utilizzando record binari, alcune come XML, mentre altre contengono informazioni archiviate come flusso binario di byte. Ogni record binario contiene zero o più campi strutturati che contengono i dati della cartella di lavoro.

#### Pacchetto ####

Un pacchetto XLSB è un archivio [ZIP](/it/compression/zip/) che deve contenere esattamente una parte della cartella di lavoro. Questa parte deve essere la destinazione di una relazione in questa parte della relazione di pacchetto. La parte della cartella di lavoro è la parte iniziale del documento XLSB.

#### Parte ####

Una parte è un flusso di byte a cui è associato un tipo di contenuto che specifica la natura e il tipo di contenuto archiviato nella parte. Alcune parti memorizzano le informazioni in formato binario mentre altre memorizzano le informazioni come XML. La sezione [enumerazione delle parti](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) del documento delle specifiche elenca le parti valide, i tipi di contenuto e le relazioni obbligatorie/facoltative tra tutte le parti in un pacchetto.

#### Relazione ####

Una fonte e una risorsa di destinazione sono collegate da una relazione. Una relazione può essere:

**Rapporto pacchetto:** dove la destinazione è una parte e l'origine è il pacchetto nel suo insieme

**Relazione da parte a parte:** dove la destinazione è una parte e l'origine è una parte del pacchetto

**Relazione esplicita:** dove si fa riferimento a una risorsa dal contenuto di una parte di origine facendo riferimento al valore dell'attributo ID di un elemento di relazione

**relazione implicita** è una relazione non esplicita

**Relazione interna:** dove il target fa parte del pacchetto

**Relazione esterna:** dove la destinazione è una risorsa esterna non nel pacchetto

#### Disco ####

Un record è l'elemento costitutivo di base utilizzato per archiviare informazioni sulle funzionalità in una cartella di lavoro. Ogni record binario è una sequenza di byte di lunghezza variabile. Un record binario è costituito da tre componenti:

* un tipo di record
* una dimensione record, e
* i dati del record specifici per quel tipo di record.

**Tipo di record:** Il tipo di record mostra il tipo di record specificato dal record. Specifica inoltre la struttura dei dati del record specifici per questo record. I tipi di record validi sono elencati nella sezione [enumerazione record](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) del documento delle specifiche. Il tipo di record deve essere uno o due byte e deve essere maggiore o uguale a 128 e minore di 16384.

**Record Size:** La dimensione del record specifica il conteggio dei byte che specifica la dimensione totale dei dati del record. Questo valore DEVE essere da uno a quattro byte. Questo valore DEVE essere un byte se il bit alto nel byte basso è uguale a 0; in caso contrario, questo valore DEVE essere maggiore di un byte. Se il conteggio dei byte è maggiore di un byte, il bit alto in ogni byte successivo specifica se viene utilizzato un byte aggiuntivo. Se il bit alto del secondo byte è uguale a 1, allora questo valore DEVE utilizzare un terzo byte aggiuntivo. Se il bit alto del terzo byte è uguale a 1, allora questo valore DEVE utilizzare un ulteriore quarto byte. Il bit alto del quarto byte DEVE essere ignorato. Il valore è costituito dai sette bit bassi di ciascun byte combinati. I bit bassi e meno significativi sono contenuti nel primo byte e ogni byte successivo contiene bit di ordine superiore rispetto al byte precedente.

**Dati del record:** Il componente dei dati del record contiene campi che corrispondono a un particolare tipo di record e comprendono il resto del record. L'ordine e la struttura dei campi per un determinato tipo di record elencato in Record Enumeration sono specificati nella sezione corrispondente per quel tipo di record in Records. La dimensione totale del componente di dati del record DEVE essere uguale alla dimensione del record. I campi nel componente dei dati del record possono contenere valori semplici, matrici di valori, strutture di diversi campi, matrici di campi e matrici di strutture.

#### Esempio di registrazione XLSB ####

Il tipo di record e la dimensione del record seguenti specificano un record **BrtCommentText** con una dimensione di 200 byte:

11111101 00000100 11001000 00000001 [Campi record]

Il primo byte è 11111101, che specifica un valore basso di 125 e che il tipo di record richiede un secondo byte. Il secondo byte è 00000100, che specifica un valore alto di 4 * 128, che equivale a 512. Il valore del tipo di record è 125 + 512 o 637, che corrisponde a un tipo di record **BrtCommentText**. Il byte successivo è 11001000, che specifica un valore basso di 72 e che la dimensione del record richiede un secondo byte. Il secondo byte è 00000001, che specifica un valore maggiore di 1 * 128 e che la dimensione del record non richiede un byte aggiuntivo. La dimensione del record è 72 + 128, o 200, che specifica la dimensione totale, in byte, del componente dei dati del record. I campi nel componente dei dati del record sono specificati da **BrtCommentText**.

## Riferimenti ##

* [[MS-XLSB] - Formato file binario Excel (.xlsb)](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)

