{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Formato file di posta Apple",
  "description":"Scopri il formato di file EMLX e le API che possono creare e aprire file EMLX.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file EMLX?

Il formato di file EMLX è implementato e sviluppato da Apple. L'applicazione Apple Mail utilizza il formato di file EMLX per esportare le e-mail. Esistono anche altre applicazioni che possono aprire i file EMLX e convertirli in altri formati di file.

## Breve storia del formato di file EMLX

Il sistema operativo Mac OS X ha adottato il programma di posta elettronica esistente, NeXTMail, creato da NeXT come parte del sistema operativo NeXTSTEP. Apple dopo l'acquisizione di NeXT ha migliorato le sue funzionalità ed è diventata l'applicazione di posta elettronica di Apple Mail da utilizzare come client di posta predefinito. Le e-mail esportate tramite Apple Mail vengono salvate direttamente come file EMLX. Inoltre, è il client di posta predefinito per i file EMLX quando qualcuno li apre facendo doppio clic su Mac OS.

## Formato file EMLX

I file EMLx sono semplici file di testo che possono essere aperti in qualsiasi editor di testo come Blocco note. La struttura del file EMLX è composta da tre parti:

* Un byte count per il messaggio - Lunghezza del messaggio stesso, scritto in ASCII in decimale, terminato con 0x0a
* Il messaggio stesso
* Metadati del messaggio sotto forma di plist XML

Questi possono essere spiegati meglio con l'aiuto di seguenti email di esempio estratte da Apple Mail come EMLX e aperte in un editor di testo.

### Esempio EMLX

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1](******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

In questo esempio, l'875 mostra la lunghezza totale del messaggio. I metadati del messaggio sono racchiusi nel file<plist> i tag e i flag sono descritti come segue:

|Campo|Descrizione|Valore
---|---|---|
|0|leggi|1 << 0
|1|eliminato|1 << 1
|2|risposta|1 << 2
|3|crittografato|1 << 3
|4|contrassegnato|1 << 4
|5|recenti|1 << 5
|6|bozza|1 << 6
|7|iniziale (non più utilizzato)|1 << 7
|8|inoltrato|1 << 8
|9|reindirizzato|1 << 9
|10-15|conteggio allegati|3F << 10 (6 bit)
|16-22|livello di priorità|7F << 16 (7 bit)
|23|firmato|1 << 23
|24|è spazzatura|1 << 24
|25|non è spazzatura|1 << 25
|26-28|delta dimensione carattere|7 << 26 (3 bit)
|29|Livello di posta indesiderata registrato|1 << 29
|30|evidenzia il testo in toc|1 << 30
|31|(non utilizzato)|

## Guarda anche ##

* [EML](/it/email/eml/)
* [MSG](/it/email/msg/)

