{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Format fișier Apple Mail",
  "description":"Aflați despre formatul de fișier EMLX și despre API-urile care pot crea și deschide fișiere EMLX.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier EMLX?

Formatul de fișier EMLX este implementat și dezvoltat de Apple. Aplicația Apple Mail folosește formatul de fișier EMLX pentru exportul e-mailurilor. Există și alte aplicații care pot deschide fișierele EMLX și le pot converti în alte formate de fișiere.

## Scurt istoric al formatului de fișier EMLX

Sistemul de operare Mac OS X a adoptat programul de e-mail existent, NeXTMail, creat de NeXT ca parte a sistemului de operare NeXTSTEP. După ce a achiziționat NeXT, Apple și-a îmbunătățit funcțiile și a devenit aplicația de e-mail Apple Mail pentru a fi folosită ca client de e-mail implicit. E-mailurile exportate prin Apple Mail sunt salvate direct ca fișiere EMLX. În plus, este clientul de e-mail implicit pentru fișierele EMLX atunci când cineva le deschide făcând dublu clic pe Mac OS.

## Format de fișier EMLX

Fișierele EMLx sunt fișiere simple bazate pe text care pot fi deschise în orice editor de text, cum ar fi Notepad. Structura fișierului EMLX constă din trei părți:

* Un număr de octeți pentru mesaj - Lungimea mesajului în sine, scrisă în ASCII în zecimală, terminată cu 0x0a
* Mesajul în sine
* Metadatele mesajelor sub formă de XML plist

Acestea pot fi explicate mai bine cu ajutorul următorului exemplu de e-mail extras din Apple Mail ca EMLX și care se deschide într-un editor de text.

### Exemplu EMLX

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1] (******.*********.*** [***.**.**.**])
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

În acest exemplu, 875 arată lungimea totală a mesajului. Metadatele mesajului sunt incluse în<plist> etichetele și steagurile sunt descrise după cum urmează:

|Câmp|Descriere|Valoare
---|---|---|
|0|citește|1 << 0
|1|șters|1 << 1
|2|a răspuns|1 << 2
|3|criptat|1 << 3
|4|marcat|1 << 4
|5|recent|1 << 5
|6|schiță|1 << 6
|7|inițial (nu mai este folosit)|1 << 7
|8|redirecționat|1 << 8
|9|redirecționat|1 << 9
|10-15|număr de atașamente|3F << 10 (6 biți)
|16-22|nivel de prioritate|7F << 16 (7 biți)
|23|semnat|1 << 23
|24|este junk|1 << 24
|25|nu este nedorit|1 << 25
|26-28|dimensiunea fontului delta|7 << 26 (3 biți)
|29|nivel de mesaje nedorite înregistrate|1 << 29
|30|evidențiați textul în toc|1 << 30
|31|(nefolosit)|

## Vezi si ##

* [EML](/ro/email/eml/)
* [MSG](/ro/email/msg/)

