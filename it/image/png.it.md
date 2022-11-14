{
  "date" : "2019-10-11",
  "keywords" :[ "file png", "formato file png", "cos'è un file png", "file", "esempio png", "estensione file png", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file PNG - File immagine raster",
  "description":"Scopri il formato di file PNG e le API che possono creare e aprire file PNG.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file PNG?

Un file **PNG** (Portable Network Graphics) è un formato di file di immagine raster che utilizza la compressione senza perdita di dati. Questo formato di file è stato creato in sostituzione del Graphics Interchange Format ([GIF](/it/image/gif/)) e non ha limiti di copyright. Tuttavia, il formato di file PNG non supporta le animazioni. Il formato di file PNG supporta la compressione delle immagini senza perdita di dati che lo rende popolare tra i suoi utenti. Con il passare del tempo, PNG si è evoluto come uno dei formati di file immagine ampiamente utilizzati.

## Breve storia del formato di file PNG

Il motivo principale alla base della creazione del formato di file PNG è stato l'algoritmo di compressione brevettato, Lempel-Ziv-Welch, utilizzato nel formato di file GIF. Questo, insieme ad altre limitazioni GIF, ha creato la necessità di sostituire il formato di file [**GIF**](/it/image/gif/). La prima proposta e il nome per il formato di file PNG sono arrivati nel gennaio 1995. Gli eventi chiave relativi ai formati di file PNG sono elencati di seguito:

* Ottobre 1996: le specifiche PNG Versione 1.0 sono state rilasciate e successivamente sono apparse come [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. La stessa è diventata una Raccomandazione del W3C nell'ottobre 1996.
* Dicembre 1998: è stata rilasciata la versione 1.1, con alcune piccole modifiche e l'aggiunta di tre nuovi blocchi.
* Agosto 1999: è stata rilasciata la versione 1.2, con l'aggiunta di un pezzo in più.
* Novembre 2003: PNG è diventato uno standard internazionale (ISO/IEC 15948:2003). Questa versione di PNG differisce solo leggermente dalla versione 1.2 e non aggiunge nuovi blocchi.
* Marzo 2004: ISO/IEC 15948:2004

## Confronto funzionale di GIF e PNG

Il formato di file PNG è stato progettato per essere semplice e portatile, legalmente libero, intercambiabile, flessibile e robusto. La tabella seguente elenca le funzionalità GIF ereditate dal formato di file PNG oltre alle nuove funzionalità.

|Caratteristica|GIF|PNG|
---|---|---|
|Indicizza immagini a colori fino a 256 colori|Sì|Sì|
|Supporto per lo streaming|Sì|Sì|
|Trasparenza|Sì|Sì|
|Informazioni accessorie|Sì|Sì|
|Indipendenza da hardware e piattaforma|Sì|Sì|
|Efficace|Sì|Sì|
|Immagini a colori fino a 48 bit per pixel|No|Sì|
|Immagini in scala di grigi fino a 16 bit per pixel|No|Sì|
|Canale alfa completo (maschere di trasparenza generali)|No|Sì|
|Informazioni sulla gamma di immagini|No|Sì|
|Affidabilità|No|Sì|
|Presentazione iniziale più rapida|No|Sì|

## Struttura del file PNG

Quasi tutti i sistemi operativi supportano l'apertura di file PNG. Ad esempio, il visualizzatore di Microsoft Windows ha la capacità di aprire file PNG poiché il sistema operativo ha per impostazione predefinita il supporto disponibile come parte dell'installazione. Un file PNG è costituito da una `firma` PNG seguita da una serie di //blocchi//.

### Intestazione del file PNG

I primi otto byte di un file PNG contengono sempre i seguenti valori (decimali):

{{{137 80 78 71 13 10 26 10 }}}

Questa firma indica che il resto del file contiene una singola immagine PNG, costituita da una serie di blocchi che iniziano con un blocco IHDR e terminano con un blocco IEND.

### Pezzi ###

Ogni pezzo è composto da quattro parti:

**Length:** Un intero senza segno di 4 byte che fornisce il numero di byte nel campo dati del blocco. La lunghezza conta solo il campo dati, non se stesso, il codice del tipo di blocco o il CRC. Zero è una lunghezza valida. Sebbene codificatori e decodificatori debbano considerare la lunghezza come senza segno, il suo valore non deve superare i 231 byte.

**Tipo Chunk:** Un codice di tipo Chunk a 4 byte. Per comodità nella descrizione e nell'esame dei file PNG, i codici di tipo sono limitati a essere costituiti da lettere ASCII maiuscole e minuscole (AZ e az, o 65-90 e 97-122 decimale). Tuttavia, codificatori e decodificatori devono trattare i codici come valori binari fissi, non come stringhe di caratteri. Ad esempio, non sarebbe corretto rappresentare il codice del tipo IDAT con gli equivalenti EBCDIC di quelle lettere. Ulteriori convenzioni di denominazione per i tipi di blocchi sono discusse nella sezione successiva.

**Dati Chunk:** I byte di dati appropriati al tipo di chunk, se presenti. Questo campo può essere di lunghezza zero.

**CRC:** Un CRC (Cyclic Redundancy Check) a 4 byte calcolato sui byte precedenti nel blocco, inclusi il codice del tipo di blocco e i campi dei dati del blocco, ma escluso il campo della lunghezza. Il CRC è sempre presente, anche per i blocchi che non contengono dati.

La lunghezza dei dati del blocco può essere un qualsiasi numero di byte fino al massimo; pertanto, gli implementatori non possono presumere che i blocchi siano allineati su limiti più grandi dei byte.

I blocchi possono apparire in qualsiasi ordine, fatte salve le restrizioni imposte a ciascun tipo di blocco. (Una restrizione notevole è che IHDR deve apparire per primo e IEND deve apparire per ultimo; quindi il blocco IEND funge da indicatore di fine file.) Possono apparire più blocchi dello stesso tipo, ma solo se specificamente consentito per quel tipo.

#### Tipi di pezzi

I tipi Chunk sono classificati in blocchi **Critical** e **Ancillary** in base al valore ASCII di 4 byte con distinzione tra maiuscole e minuscole assegnato al tipo Chunk. Tutte le implementazioni devono comprendere ed eseguire correttamente il rendering dei blocchi critici standard. Un'immagine PNG valida deve contenere un blocco IHDR, uno o più blocchi IDAT e un blocco IEND.

### Compressione

Il metodo di compressione PNG 0 (l'unico metodo di compressione attualmente definito per PNG) specifica la compressione/gonfia con una finestra scorrevole di al massimo 32768 byte. Deflate compression è un derivato LZ77 utilizzato in zip, gzip, pkzip e programmi correlati. Sono state condotte ricerche approfondite a sostegno del suo status di brevetto. I dati compressi all'interno del flusso di dati zlib vengono archiviati come una serie di blocchi, ognuno dei quali può rappresentare dati grezzi (non compressi), dati compressi LZ77 codificati con codici Huffman fissi o dati compressi LZ77 codificati con codici Huffman personalizzati. Un bit marker nel blocco finale lo identifica come l'ultimo blocco, consentendo al decoder di riconoscere la fine del flusso di dati compresso.

#### Filtraggio di precompressione

I filtri di precompressione vengono applicati per preparare i dati dell'immagine per una compressione ottimale. Il metodo di filtro PNG definisce cinque tipi di filtro di base come segue:

|Tipo filtro|Nome|Valore previsto|
---|---|---|
|0|Nessuno|La linea di scansione viene trasmessa non modificata|
|1|Sub|Trasmette la differenza tra ogni byte e il valore del byte corrispondente del pixel precedente.|
|2|Su|Il filtro Su() è proprio come il filtro Sub() tranne per il fatto che il pixel immediatamente sopra il pixel corrente, anziché solo alla sua sinistra, viene utilizzato come predittore.|
|3|Media|Il filtro Media() utilizza la media dei due pixel adiacenti (a sinistra e sopra) per prevedere il valore di un pixel.|
|4|Paeth|Il filtro Paeth() calcola una semplice funzione lineare dei tre pixel adiacenti (a sinistra, in alto, in alto a sinistra), quindi sceglie come predittore il pixel vicino più vicino al valore calcolato.|

Gli algoritmi di filtraggio vengono applicati ai "byte", non ai pixel, indipendentemente dalla profondità di bit o dal tipo di colore dell'immagine. Gli algoritmi di filtraggio lavorano sulla sequenza di byte formata da una scanline. Se l'immagine include un canale alfa, i dati alfa vengono filtrati allo stesso modo dei dati dell'immagine.

Quando l'immagine è interlacciata, ogni passaggio del motivo interlacciato viene trattato come un'immagine indipendente a scopo di filtraggio. I filtri lavorano sulle sequenze di byte formate dai pixel effettivamente trasmessi durante un passaggio, e la "linea di scansione precedente" è quella trasmessa in precedenza nello stesso passaggio, non quella adiacente nell'immagine completa. Si noti che l'immagine secondaria trasmessa in ogni passaggio è sempre rettangolare, ma è di larghezza e/o altezza inferiori rispetto all'immagine completa. Il filtro non viene applicato quando questa immagine secondaria è vuota.

## Riferimenti ##

* [PNG - Pagina iniziale](http://www.libpng.org/pub/png/)

