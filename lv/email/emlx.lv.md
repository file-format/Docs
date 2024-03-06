{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMLX — Apple Mail faila formāts",
  "description": "Uzziniet par EMLX failu formātu un API, kas var izveidot un atvērt EMLX failus.",
  "linktitle": "EMLX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-eml-lvx"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir EMLX fails?

EMLX faila formātu ir ieviesis un izstrādājis Apple. Lietojumprogramma Apple Mail e-pasta eksportēšanai izmanto EMLX faila formātu. Ir arī citas lietojumprogrammas, kas var atvērt EMLX failus un pārvērst tos citos failu formātos.

## Īsa EMLX faila formāta vēsture

Operētājsistēma Mac OS X pieņēma esošo e-pasta programmu NeXTMail, ko NeXT izveidoja kā daļu no operētājsistēmas NeXTSTEP. Apple pēc NeXT iegādes uzlaboja savas funkcijas, un tā kļuva par tagad Apple Mail e-pasta lietojumprogrammu, kas tiks izmantota kā noklusējuma pasta klients. E-pasta ziņojumi, kas eksportēti, izmantojot Apple Mail, tiek tieši saglabāti kā EMLX faili. Turklāt tas ir noklusējuma pasta klients EMLX failiem, kad kāds tos atver, veicot dubultklikšķi uz Mac OS.

## EMLX faila formāts

EMLx faili ir vienkārši teksta faili, kurus var atvērt jebkurā teksta redaktorā, piemēram, Notepad. EMLX faila struktūra sastāv no trim daļām:

* Ziņojuma baitu skaits — paša ziņojuma garums, rakstīts ASCII ar decimāldaļu, beidzas ar 0x0a

* Pati ziņa

* Ziņojuma metadati XML plist formātā


Tos var labāk izskaidrot, izmantojot šādu e-pasta paraugu, kas iegūts no Apple Mail kā EMLX un atvērts teksta redaktorā.

### EMLX piemērs

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

Šajā piemērā 875 parāda kopējo ziņojuma garumu. Ziņojuma metadati ir iekļauti<plist> atzīmes un karodziņi ir šādi:

|Lauks|Apraksts|Vērtība
---|---|---|
|0|lasīt|1 << 0
|1|dzēsts|1 << 1
|2|atbildēja|1 << 2
|3|šifrēts|1 << 3
|4|atzīmēts|1 << 4
|5|nesen|1 << 5
|6|melnraksts|1 << 6
|7|sākotnējais (vairs netiek izmantots)|1 << 7
|8|pārsūtīts|1 << 8
|9|novirzīts|1 << 9
|10-15|pielikumu skaits|3F << 10 (6 biti)
|16-22|prioritātes līmenis|7F << 16 (7 biti)
|23|parakstīts|1 << 23
|24|ir nevēlams|1 << 24
|25|nav atkritumi|1 << 25
|26-28|fonta lielums delta|7 << 26 (3 biti)
|29|reģistrēts nevēlamā pasta līmenis|1 << 29
|30|izcelt tekstu kopā|1 << 30
|31|(nelietots)|

## Skatīt arī ##

* [EML](/email/eml/)

* [MSG](/email/msg/)


