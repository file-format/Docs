{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Formato e-mail di Microsoft Outlook",
  "description":"Scopri il formato di file MSG e le API che possono creare e aprire file MSG.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file MSG?

MSG è un formato di file utilizzato da [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) ed Exchange per archiviare i messaggi di posta elettronica , contatto, appuntamento o altre attività. Tali messaggi possono contenere uno o più campi di posta elettronica, con il mittente, il destinatario, l'oggetto, la data e il corpo del messaggio, oppure le informazioni di contatto, i dettagli dell'appuntamento e una o più specifiche dell'attività. Le proprietà che costituiscono l'oggetto Message, incluso, fanno anche parte del file MSG. Il file MSG ha intestazioni, corpo del messaggio principale e collegamenti ipertestuali come testo ASCII semplice. I file MSG sono adatti anche con i programmi che richiedono MAPI (Messaging Applications Programming Interface) di Microsoft.

## Struttura del file MSG

Il formato CFB_3 è la base del file MSG. Il paradigma si basa sui concetti di storage e stream, abbastanza vicini a directory e file. Pertanto, una delle principali differenze nel primo è l'intera gerarchia, impacchettata in un file distinto, chiamato file composto. Gli oggetti costituiscono i file di messaggio e sono costituiti da una singola proprietà o dalle sue raccolte. Questa capacità consente alle applicazioni di archiviare dati complessi e strutturati in un unico file. Questo formato specifica anche più archivi, ogni archivio rappresenta l'oggetto Messaggio come un componente principale. Questi archivi contengono un numero di flussi che rappresentano una proprietà di quel componente. È anche possibile l'annidamento dell'archiviazione.

## Proprietà Mapi

Al livello superiore del file .msg, gli archivi contengono flussi che archiviano le proprietà al loro interno. Le proprietà possono essere classificate come segue:

* Proprietà di lunghezza fissa
* Proprietà di lunghezza variabile
* Proprietà a più valori

Indipendentemente dalla categoria, una proprietà può essere contrassegnata o denominata. Tuttavia, sono necessarie informazioni di mappatura adeguate per le proprietà denominate, come specificato dalla loro memoria di mappatura.

## Magazzini

Gli archivi costituiscono i componenti chiave dell'oggetto Messaggio. Il formato di file MSG indica i seguenti archivi:

## Struttura di primo livello

L'oggetto messaggio rappresenta l'intero livello superiore del formato di file MSG. A seconda del tipo, delle proprietà, del numero di destinatari e degli oggetti Allegato, un oggetto messaggio può avere diverse memorie di flusso nel file .MSG corrispondente.

### Relazione con altre strutture

Il formato del file Msg ha le seguenti relazioni con altre strutture:

* La base di .msg è il formato file binario file composto.
* Le proprietà utilizzate da Message and Attachment Object Protocol vengono utilizzate da questo formato.

## Scenari per evitare i formati MSG

L'oggetto messaggio può essere condiviso tra client o archivi di messaggi che utilizzano il file system .msg. Ci sono alcune circostanze in cui la memorizzazione di un oggetto messaggio nel formato di file con estensione msg non sarebbe appropriato. Per esempio:

* In caso di gestione di un archivio autonomo di grandi dimensioni, è preferibile utilizzare un formato completo in cui le viste possono essere visualizzate in modo più preciso.
* Se il destinatario è sconosciuto, è possibile che il formato non sia supportato dal destinatario e che venga consegnato privato o irrilevante.

## Esempio di file MSG

Per avere un'idea di come appare un file MSG, puoi scaricare un [file MSG di esempio](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) e aprirlo sul tuo computer per visualizzarne il contenuto.

## Riferimenti

* [[MS-OXMSG]: Formato file MSG di Outlook](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

