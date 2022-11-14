{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"Scopri il formato di file TNEF e le API che possono creare e aprire file TNEF.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file TNEF?

Transport Neutral Encapsulation Format (TNEF) è un proprietario Microsoft per l'incapsulamento di allegati di posta elettronica basati su Messaging Application Programming Interface (**MAPI**). Microsoft Outlook e Microsoft Exchange Server supportano interamente TNEF mentre in seguito decodifica TNEF in MAPI e visualizza i messaggi di posta formattati. Un allegato e-mail con codifica TNEF ha un tipo MIME di MS-TNEF e viene archiviato come winmail/win.dat. L'allegato in winmail .dat racchiude le seguenti informazioni:


|Messaggio|Oggetti OLE|Caratteristiche di Outlook
---|---|---|
|<ul><li> Allegati messaggi originali</li><li> Versione formattata originale</li><li> caratteri, dimensioni del testo e colori del testo</li></ul> |<ul><li> immagini incorporate</li><li> documenti di Office incorporati</li></ul> |<ul><li> moduli personalizzati</li><li> pulsanti di voto</li><li> richieste di incontro</li></ul>


Altri servizi di posta elettronica che non supportano TNEF, presentano testo normale per i messaggi formattati TNEF. Outlook incorpora un formato avanzato del messaggio nei file TNEF (OLE) o in particolari funzionalità di Outlook (moduli, pulsanti di polling e richieste di conferenza). Non è possibile sanzionare la codifica TNEF esplicita all'interno del client di posta elettronica di Outlook, tuttavia, l'opzione del formato RTF per l'invio di un messaggio di posta elettronica facilita implicitamente la codifica TNEF.

## Formato file TNEF

L'algoritmo dei dati TNEF stabilisce una struttura appiattita dalle proprietà del messaggio gerarchiche avanzate. Queste strutture appiattite vengono quindi utilizzate per rappresentare un flusso di dati seriale composto da proprietà particolari.

In alcune situazioni, in cui le proprietà si verificano in gruppi o hanno più valori, il flusso potrebbe includere conteggi e riempimenti per imporre specifici allineamenti di dati. Una situazione particolare in cui l'uso di questo algoritmo è vantaggioso è in un ambiente di messaggistica non di supporto. In tali ambienti, una proprietà di messaggi avanzati viene codificata in un flusso di dati seriali da un writer TNEF. Inoltre, le proprietà che non appartengono al TNEF sottostante possono essere incapsulate durante la trasmissione. Queste proprietà incapsulate sono quindi rese disponibili dalla decodifica tramite un TNEF per garantire la disponibilità di tutte le proprietà del messaggio originale all'applicazione client.

In TNEF tutti i tipi di dati numerici sono little-endian e le loro dimensioni sono maggiori di un byte. La gestione di questi valori numerici su piattaforme non little-endian richiede di eseguire le trasformazioni appropriate per ottenere valori corretti. I valori di stringa sono rappresentati in formato Augmented Backus-Naur Form (ABNF) secondo le specifiche [RFC5234]. Quando la stringa termina con un carattere nullo, viene anche inclusa; ad esempio, "lavoratore@campione.com" %x00.

{{< figure src="../TNEF.png" alt="Formato file TNEF" >}}

## Attributi TNEF e regole di elaborazione ##

Il flusso di dati in TNEF inizia con un numero di versione legacy, una firma, un valore di chiave primitiva e un attributo rappresentano una tabella codici. Questa tabella codici viene generata quando il codificatore registra gli attributi e le proprietà ANSI. Successivamente, il flusso è diventato una serie di attributi in cui gli attributi del messaggio sono stati prima allineati e poi seguiti dagli attributi degli allegati. Diverse caratteristiche di messaggi e allegati sono contenute in attributi speciali come attMsgProps, attAttachment e attRecipTable. Gli attributi che appaiono nel flusso TNEF, contengono la struttura, le proprietà del messaggio e le conversioni necessarie per impegnarli con le proprietà del messaggio. Ogni attributo è costituito da un ID, dimensione e dati dell'attributo, un checksum e un livello in base alla sua applicazione.

## Relazione con protocolli e altri algoritmi ##

I sistemi che hanno un meccanismo scadente per visualizzare un formato di messaggio avanzato richiedono in modo nativo l'algoritmo di dati TNEF per il trasporto. Utilizzando il tipo di supporto ms-TNEF, l'output dell'algoritmo è costituito da un file allegato (winmail.dat) e una parte del corpo del MIME specificato in [RFC2045]. Il corpo del messaggio di testo normale viene trasmesso utilizzando UUENCODE secondo la specifica [MSDN-UAF] e questo corpo del messaggio o un metodo equivalente decodificato all'estremità del destinatario. Inoltre, TNEF può trasmettere i dati dei messaggi utilizzando diversi protocolli Internet come SMTP, POP3, IMAP4 e quelli integrati MIME secondo lo standard RFC2045.

## Dichiarazione di applicabilità ##

Oltre alla semplice trasmissione di messaggi, l'applicazione originale di TNEF doveva essere creata per utilizzare classi di messaggi e supportare funzionalità aggiuntive che non hanno supporto originale nel protocollo di trasporto. Questa applicazione è stata ulteriormente perfezionata per la trasmissione di proprietà di messaggi avanzati e proprietà denominate che i moderni client di messaggistica utilizzano oggigiorno. Per la conformità con l'implementazione originale, viene mantenuta la sintassi dell'attributo originale e un attributo speciale mantiene le nuove proprietà del messaggio separatamente.

## Riferimenti

* [Transport Neutral Encapsulation Format](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Indirizzi e-mail e rubriche in Exchange Server](https://docs.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: Transport Neutral Encapsulation Format (TNEF) Data Algorithm](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

