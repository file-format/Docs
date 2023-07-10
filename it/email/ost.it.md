{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Formato file di archiviazione di Outlook",
  "description":"Scopri il formato di file OST e le API che possono creare e aprire file OST.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file OST?

OST o File di archiviazione offline rappresentano i dati della casella di posta dell'utente in modalità offline sul computer locale al momento della registrazione con Exchange Server tramite Microsoft Outlook. Viene creato automaticamente al primo utilizzo di Microsoft Outlook al momento della connettività con il server. Una volta creato il file, i dati vengono sincronizzati con il server di posta in modo che siano disponibili offline anche in caso di disconnessione dal server di posta. I file OST possono utilizzare elementi della casella di posta come e-mail, contatti, informazioni sul calendario, note, attività e altri dati simili. Gli utenti possono creare e-mail e altri dati in file OST anche in assenza di connessione al server, ma questi non verranno sincronizzati con il server. Una volta stabilita la connessione, il file locale viene nuovamente sincronizzato con il server in modo che sia il server che la copia locale siano allo stesso livello di informazioni.

## Formato file OST

Il formato di file OST (Offline Storage Table) e [PST](/it/email/pst/) (Personal Storage Table) è costituito dal formato PFF (Personal Folder File) che corrisponde alla memorizzazione di email, contatti e appuntamenti dell'utente. I dati in un file PFF vengono archiviati in little-endian con tutte le date e gli orari rappresentati come FILETIME in UTC. [MS-PST] definisce due tipi di PFF:

* Formato ANSI a 32 bit
* Formato Unicode a 64 bit

Il formato file PST [specifiche](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), come disponibile da Microsoft, è applicabile anche al formato file OST come gratuito e licenza di brevetto irrevocabile attraverso la Open Specification Promise. Si compone dei seguenti elementi distinguibili:

* Intestazione Fle
* Dati di intestazione del file
* Nodo di diramazione dell'indice
* Nodo foglia indice
* Indice di offset (file).
* Indice del descrittore (elemento).
* Descrittori locali
* Tipo di tabella articolo

### Informazioni sull'intestazione

La struttura HEADER del file OST si trova proprio all'inizio del file a 0 offset. Contiene informazioni sui metadati sul file OST e le informazioni ROOT per accedere alle strutture di dati del livello NDB descritte sopra. La struttura HEADER differisce per le versioni Unicode e ANSI del formato file OST.

L'intestazione inizia con una parola magica di 4 byte **!BDN** rappresentata da byte (0x21, 0x42, 0x44, 0x4E). Un altro numero magico di 2 byte, **SM** (0x53, 0x4D), si trova all'offset 8 dall'inizio del file. Le informazioni sulla versione (ANSI o Unicode) si trovano a un offset di 10 dall'inizio del file. Il valore esadecimale (0x17) specifica il file OST Unicode mentre 0x0E o 0x0F rappresenta il formato di file ANSI.

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
|rgnid[](128 byte)|Un array fisso di 32 NID, ciascuno corrispondente a uno dei 32 possibili NID_TYPE (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_TYPE_ASSOC_MESSAGE)
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

## Riferimenti

* [Formato file delle cartelle personali di Outlook (.ost)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Specifiche del formato del file della cartella personale](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

