{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - File modello e-mail di Microsoft Outlook",
  "description":"Scopri il formato di file OFT e le API che possono creare e aprire file OFT.",
  "linktitle" : "OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file OFT?

I file con estensione .oft sono file modello creati utilizzando Microsoft Outlook. Il layout preformattato impostato per i modelli di messaggio viene quindi utilizzato per inviare e-mail con informazioni comuni per risparmiare tempo. Tali file possono essere generati creando una nuova e-mail, aggiungendo le informazioni necessarie e quindi utilizzando il menu a discesa Salva come modello di Office (.oft) da Microsoft Outlook. Gli utenti possono aprire i file OFT facendo doppio clic su di esso e si aprirà nell'applicazione associata su quel particolare sistema.

## Struttura del file OFT ##

Il formato file .OFT utilizza il formato file [MSG](/it/email/msg/) alla base. L'unica differenza è che i file OFT hanno CLSID_TemplateMessage ({0006F046-0000-0000-C000-000000000046}) come classe di archiviazione (WriteClassStg), mentre i file MSG utilizzano CLSID_MailMessage ({00020D0B-0000-0000-C000-000000000046}).

Il formato CFB_3 è la base del file MSG. Il paradigma si basa sui concetti di storage e stream, abbastanza vicini a directory e file. Pertanto, una delle principali differenze nel primo è l'intera gerarchia, impacchettata in un file distinto, chiamato file composto. Gli oggetti costituiscono i file di messaggio e sono costituiti da una singola proprietà o dalle sue raccolte. Questa capacità consente alle applicazioni di archiviare dati complessi e strutturati in un unico file. Questo formato specifica anche più archivi, ogni archivio rappresenta l'oggetto Messaggio come un componente principale. Questi archivi contengono un numero di flussi che rappresentano una proprietà di quel componente. È anche possibile l'annidamento dell'archiviazione.

### Proprietà OFT

Al livello superiore del file .msg, gli archivi contengono flussi che memorizzano le proprietà al loro interno. Le proprietà possono essere classificate come segue:

* Proprietà di lunghezza fissa
* Proprietà di lunghezza variabile
* Proprietà a più valori

Indipendentemente dalla categoria, una proprietà può essere contrassegnata o denominata. Tuttavia, sono necessarie informazioni di mappatura adeguate per le proprietà denominate, come specificato dalla loro memoria di mappatura.

### depositi OFT

Gli archivi costituiscono i componenti chiave dell'oggetto Messaggio. Il formato di file MSG indica i seguenti archivi:

### Struttura di primo livello

L'oggetto messaggio rappresenta l'intero livello superiore del formato di file Msg. A seconda del tipo, delle proprietà, del numero di destinatari e degli oggetti Allegato, un oggetto messaggio può avere diverse memorie di flusso nel file .MSG corrispondente.

#### Relazione con altre strutture

Il formato di file MSG/OFT ha le seguenti relazioni con altre strutture:

* La base di .msg è il formato file binario file composto.
* Le proprietà utilizzate da Message and Attachment Object Protocol vengono utilizzate da questo formato.

## Riferimenti

* [[MS-OXMSG]: Formato file MSG di Outlook](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

