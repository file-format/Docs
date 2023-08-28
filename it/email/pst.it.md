{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Formato file archivio informazioni personali di Outlook",
  "description":"Scopri il formato di file PST e le API che possono creare e aprire file PST.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file PST?

I file con estensione .pst rappresentano i file di archiviazione personale di Outlook (chiamati anche tabella di archiviazione personale) che archiviano una varietà di informazioni sull'utente. Le informazioni sull'utente sono archiviate in cartelle di diversi tipi che includono e-mail, elementi del calendario, note, contatti e molti altri formati di file. I file PST vengono utilizzati per archiviare i dati di invio di posta elettronica offline che possono essere successivamente caricati e visualizzati in varie applicazioni.

## Specifiche del formato file PST

Il formato file PST [specifiche](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) è disponibile da Microsoft come licenza di brevetto gratuita e irrevocabile tramite Open Specification Promise .

### Tipo di formati PST

I formati di file PST sono classificati in due tipi in base alla codifica del tipo di file. I file PST con codifica ANSI sono formati di file meno recenti e sono supportati solo da Outlook 2002 e versioni precedenti. Tali file hanno un limite di dimensione massima di 2 GB (2^^31^^ Byte) e non supportano Unicode. Un tipo di formato file più moderno, basato sulla codifica Unicode, rimuove la limitazione della dimensione del file e può raggiungere una dimensione massima dei dati di 50 GB.

### Organizzazione logica del formato file PST

Alla base del formato di file PST si trova B-Tree che mantiene i dati ordinati e consente ricerche, accessi sequenziali, inserimenti, eliminazioni ecc. in tempo logaritmico. La struttura complessiva di un file PST è organizzata in tre livelli.

![Logical layers of a PST file](/it/email/PST-1.png "Logical layers of a PST file")

"Livello database dei nodi (NDB)" - Il livello del database dei nodi si trova al livello inferiore di un file PST e include il database dei nodi. Questi nodi rappresentano in realtà strutture di archiviazione di livello inferiore del formato di file PST. Il livello NDB comprende header, informazioni sull'allocazione dei file, blocchi e BTree (Node BTree e Block BTree) dal punto di vista dell'archiviazione. I nodi e i blocchi del livello NDB sono collegati tramite Data BID, che è una delle quattro proprietà di riferimento del nodo, ovvero NID (Node ID), Parent NID, Data BID (Block BID) e SubNode BID.

Livello `Liste, tabelle e proprietà -` Il livello LTP fornisce la comprensione logica di concetti di livello superiore oltre a NDB. Oltre ad altri elementi, il livello LTP comprende principalmente Property Context (PC) e Table Context (TC). PC è una raccolta di proprietà, mentre TC rappresenta una matrice bidimensionale di raccolta di proprietà rispetto alla presenza di queste. Implementazione efficiente di PC e TC, il livello LTP utilizza i seguenti due tipi di strutture dati in cima al nodo NDB:

* Heap On Node (HN): consente di sotto-allocare il flusso di dati di un nodo in piccoli frammenti di dimensioni variabili.
* BTree on Heap (BTH) - BTH fornisce un modo comodo e pratico di ricerca attraverso PC dati, descritti sopra, sono implementati come BTH ed è per questo che viene implementato costruendo all'interno di una struttura HN.

`Livello di messaggistica -` Le regole di livello superiore e la logica aziendale per lavorare con i file PST sono implementate a questo livello. L'output logico di questo livello risulta come oggetti cartella, oggetti messaggio, oggetti allegato e proprietà che è reso possibile dalla combinazione di livelli LTP e NDB. Regole e requisiti, che devono essere seguiti durante la modifica dei contenuti PST, sono definiti anche a questo livello.

### Organizzazione fisica del formato file PST

L'alto livello di organizzazione dei file del file PST è mostrato nella figura seguente. Questa è solo una panoramica di concetti diversi dagli elementi logici del file PST.

![Physical organization of the PST file format](/it/email/PST-2.png "Physical organization of the PST file format")


#### Informazioni sull'intestazione PST

La struttura HEADER del file PST si trova proprio all'inizio del file a 0 offset. Contiene informazioni sui metadati sul file PST e le informazioni ROOT per accedere alle strutture di dati del livello NDB descritte sopra. La struttura HEADER differisce per le versioni Unicode e ANSI del formato file PST.

L'intestazione inizia con una parola magica di 4 byte **!BDN** rappresentata da byte (0x21, 0x42, 0x44, 0x4E). Un altro numero magico di 2 byte, **SM** (0x53, 0x4D), si trova all'offset 8 dall'inizio del file. Le informazioni sulla versione (ANSI o Unicode) si trovano a un offset di 10 dall'inizio del file. Il valore esadecimale (0x17) specifica il file PST Unicode mentre 0x0E o 0x0F rappresenta il formato di file ANSI.

|Campo|Descrizione
---|---|
|dwMagic (4 byte)|DEVE essere "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 byte)|Il valore CRC a 32 bit dei 471 byte di dati a partire da wMagicClient (0ffset 0x0008)
|wMagicClient (2 byte)|DEVE essere "{ 0x53, 0x4D }".
|wVer (2 byte)|Versione formato file. Questo valore DEVE essere 14 o 15 se il file è un file PST ANSI e DEVE essere 23 se il file è un file PST Unicode.
|wVerClient (2 byte)|Versione del formato del file client. La versione che corrisponde al formato descritto in questo documento è 19. I creatori di un nuovo file PST basato su questo documento DEVONO inizializzare questo valore a 19.
|bPlatformCreate (1 byte)|Questo valore DEVE essere impostato su 0x01.
|bPlatformAccess (1 byte)|Questo valore DEVE essere impostato su 0x01.
|dwRiservato (8 byte)|
|bidUnused (solo Unicode a 8 byte)|Padding non utilizzato aggiunto quando è stato creato il formato di file PST Unicode.
|bidNextP (Unicode: 8 byte; ANSI: 4 byte)|Pagina successiva BID. Le pagine hanno un contatore speciale per l'allocazione dei valori bidIndex. Il valore di bidIndex per BID per le pagine viene allocato da questo contatore.
|bidNextB (solo ANSI 4 byte): |BID successivo. Questo valore è il contatore monotono che indica il BID da assegnare per il prossimo blocco allocato. I valori BID avanzano con incrementi di 4. Per maggiori dettagli, vedere la sezione 2.2.2.2.
|dwUnique (4 byte)|Questo è un valore monotonicamente crescente che viene modificato ogni volta che viene modificata la struttura HEADER del file PST. La funzione di questo valore è fornire un valore univoco e garantire che i CRC HEADER siano diversi dopo ogni modifica dell'intestazione.
|rgnid[]   (128 byte)|Un array fisso di 32 NID, ciascuno corrispondente a uno dei 32 possibili NID_TYPE (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_TYPE_ASSOC_MESSAGE)
|qwUnused (8 byte)|Spazio inutilizzato; DEVE essere impostato a zero. Solo formato di file PST Unicode.
|root (Unicode: 72 byte; ANSI: 40 byte)|Una struttura ROOT (sezione 2.2.2.5).
|dwAlign (4 byte)|Byte di allineamento non utilizzati; DEVE essere impostato a zero. Solo formato di file PST Unicode.
|rgbFM (128 byte)|FMap obsoleto. Questo non è più utilizzato e DEVE essere riempito con 0xFF. I lettori DOVREBBE ignorare il valore di questi byte.
|rgbFP (128 byte)|FPMap obsoleto. Questo non è più utilizzato e DEVE essere riempito con 0xFF. I lettori DOVREBBE ignorare il valore di questi byte.
|bSentinel (1 byte)|DEVE essere impostato su 0x80.
|bCryptMethod (1 byte)|Indica come vengono codificati i dati all'interno del file PST. DEVE essere impostato su uno dei valori predefiniti (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbRiservato (2 byte)| Riservato; DEVE essere impostato a zero.
|bidNextB (8 byte)|Indica il successivo valore BID disponibile. Solo formato di file PST Unicode.
|bidNextB (SOLO Unicode: 8 byte)|BID successivo. Questo valore è il contatore monotono che indica il BID da assegnare per il prossimo blocco allocato. I valori BID avanzano con incrementi di 4. Per maggiori dettagli, vedere la sezione 2.2.2.2.
|dwCRCFull (4 byte)|Il valore CRC a 32 bit dei 516 byte di dati a partire da wMagicClient fino a bidNextB, inclusi. Solo formato di file PST Unicode.
|ullRiservato (8 byte)|Riservato; DEVE essere impostato a zero. Solo formato di file PST ANSI.
|dwRiservato (4 byte)|Riservato; DEVE essere impostato a zero. Solo formato di file PST ANSI.
|rgbRiservato2 (3 byte)|
|bRiservato (1 byte) |
|rgbRiservato3 (32 byte) |

### Protezione dati ###

Per motivi di sicurezza, i file PST possono anche essere protetti da password, il che richiede all'applicazione di caricamento di applicare la password prima che possano essere visualizzati. La password applicata al file PST viene archiviata nell'archivio messaggi. Tuttavia, ciò non fornisce una protezione dei dati efficace poiché la password può essere rimossa dagli strumenti disponibili. Inoltre, la password specificata dall'utente non viene utilizzata come parte della chiave per la codifica e la decodifica degli algoritmi di crittografia. Pertanto, non vi è alcun vantaggio nel proteggere i dati a cui accedono le parti non autorizzate. L'archiviazione della password come hash CRC-32 della stringa originale lo rende anche un metodo debole per la sicurezza dei dati contro l'approccio della forza bruta.

## Riferimenti ##

* [Formato file delle cartelle personali di Outlook (.pst)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Specifiche del formato del file della cartella personale](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

