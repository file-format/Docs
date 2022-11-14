{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - File casella di posta elettronica",
  "description":"Scopri il formato di file MBOX e le API che possono creare e aprire file MBOX.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file MBOX?

Il formato file MBox è un termine generico che rappresenta un contenitore per la raccolta di messaggi di posta elettronica. I messaggi vengono archiviati all'interno del contenitore insieme ai relativi allegati. I messaggi di un'intera cartella vengono salvati in un unico file di database e i nuovi messaggi vengono aggiunti alla fine del file. Numerose applicazioni e API forniscono supporto per il formato di file MBox come Apple Mail e Mozilla Thunderbird.

## Formato file MBOX ##

Il formato del file MBox è rimasto non standardizzato per un periodo piuttosto lungo fino al 2005, quando l'applicazione/mbox è stata standardizzata come [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Messaggi, in formato RFC 2822 , sono concatenati all'interno del formato di file MBox uno dopo l'altro. Ciascun messaggio inizia con una riga di separazione che identifica il mittente del messaggio e identifica anche la data e l'ora in cui il messaggio è stato ricevuto dal destinatario finale (il sistema dell'ultimo salto nel percorso di trasferimento o il sistema che funge da negozio di posta). Ogni messaggio è in genere terminato da una riga vuota. La fine del database viene solitamente riconosciuta dall'assenza di dati aggiuntivi o dalla presenza di un esplicito marker di fine file.

## Lettura di un messaggio dal file MBox ##

Un lettore esegue la scansione di un file mbox cercando From_lines. Qualsiasi riga From_ contrassegna l'inizio di un messaggio. Il lettore non dovrebbe tentare di trarre vantaggio dal fatto che ogni riga From_ (oltre l'inizio del file) è vuota. Una volta che il lettore trova un messaggio, estrae un mittente della busta (possibilmente danneggiato) e la data di consegna dalla riga From_. Quindi legge fino alla riga From_ successiva o alla fine del file, a seconda dell'evento che si verifica per primo. Elimina la riga vuota finale ed elimina le virgolette di >Da_ righe e >>Da_ righe e così via. Il risultato è un messaggio RFC 822.

## Considerazioni sulla codifica ##

Il contenuto di un file MBox può essere irreversibilmente mescolato quando un'e-mail ricevuta contiene un file Mbox come allegato e viene salvata in un altro file Mbox. Per evitare ciò, i sistemi di messaggistica devono codificare un database mbox con una codifica di trasferimento non trasparente (come BASE64 o Quoted-Printable) ogni volta che un tale oggetto viene trasferito tramite protocolli di messaggistica. Gli implementatori dovrebbero anche essere preparati a codificare i dati mbox in locale se vengono ricevuti dati non conformi.

## Riferimenti ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)

