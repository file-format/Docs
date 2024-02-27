{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMLX - Apple Mail-filformat",
  "description": "Lær om EMLX filformat og API'er, der kan oprette og åbne EMLX filer.",
  "linktitle": "EMLX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-eml-dax"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en EMLX fil?

EMLX-filformatet er implementeret og udviklet af Apple. Apple Mail-applikationen bruger EMLX-filformatet til at eksportere e-mails. Der er også andre applikationer, der kan åbne EMLX-filerne og konvertere disse til andre filformater.

## Kort historie om EMLX-filformat

Mac OS X-operativsystemet adopterede det eksisterende e-mail-program, NeXTMail, skabt af NeXT som en del af NeXTSTEP-operativsystemet. Efter erhvervelsen af NeXT løftede Apple sine funktioner, og det blev det nu Apple Mail-e-mail-program, der skal bruges som standard-mailklient. E-mails, der eksporteres via Apple Mail, gemmes direkte som EMLX-filer. Derudover er det standardmail-klienten for EMLX-filer, når nogen åbner disse ved at dobbeltklikke på Mac OS.

## EMLX filformat

EMLx-filer er simple tekstbaserede filer, der kan åbnes i enhver teksteditor som Notesblok. EMLX-filstrukturen består af tre dele:

* Et byteantal for meddelelsen - Længden af selve meddelelsen, skrevet i ASCII i decimal, afsluttet med 0x0a

* Selve beskeden

* Besked Metadata i form af XML plist


Disse kan bedre forklares ved hjælp af følgende eksempel-e-mail uddraget fra Apple Mail som EMLX og åbne i en teksteditor.

### EMLX Eksempel

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

I dette eksempel viser 875 meddelelsens samlede længde. Meddelelsens metadata er indeholdt i<plist> tags og flag er som beskrevet som følger:

|Felt|Beskrivelse|Værdi
---|---|---|
|0|læst|1 << 0
|1|slettet|1 << 1
|2|besvarede|1 << 2
|3|krypteret|1 << 3
|4|markeret|1 << 4
|5|seneste|1 << 5
|6|udkast|1 << 6
|7|initial (bruges ikke længere)|1 << 7
|8|videresendt|1 << 8
|9|omdirigeret|1 << 9
|10-15|antal vedhæftede filer|3F << 10 (6 bit)
|16-22|prioritetsniveau|7F << 16 (7 bit)
|23|signeret|1 << 23
|24|er junk|1 << 24
|25|er ikke uønsket|1 << 25
|26-28|skriftstørrelse delta|7 << 26 (3 bit)
|29|junk mail niveau registreret|1 << 29
|30|fremhæv tekst i toc|1 << 30
|31|(ubrugt)|

## Se også ##

* [EML](/email/eml/)

* [MSG](/email/msg/)


