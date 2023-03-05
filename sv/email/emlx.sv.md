{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Apple Mail File Format",
  "description":"Läs mer om EMLX-filformat och API:er som kan skapa och öppna EMLX-filer.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en EMLX fil?

EMLX-filformatet är implementerat och utvecklat av Apple. Apple Mail-applikationen använder EMLX-filformatet för att exportera e-postmeddelanden. Det finns också andra applikationer som kan öppna EMLX-filerna och konvertera dessa till andra filformat.

## Kort historia av EMLX-filformat

Mac OS X operativsystem antog det befintliga e-postprogrammet, NeXTMail, skapat av NeXT som en del av operativsystemet NeXTSTEP. Efter att Apple förvärvade NeXT lyfte det upp sina funktioner och det blev det nu Apple Mail e-postprogram som ska användas som standard e-postklient. E-postmeddelanden som exporteras via Apple Mail sparas direkt som EMLX-filer. Dessutom är det standardpostklienten för EMLX-filer när någon öppnar dessa genom att dubbelklicka på Mac OS.

## EMLX filformat

EMLx-filer är enkla textbaserade filer som kan öppnas i vilken textredigerare som helst som Anteckningar. EMLX-filstrukturen består av tre delar:

* En byte för meddelandet - Längden på själva meddelandet, skrivet i ASCII med decimaler, avslutat med 0x0a
* Själva meddelandet
* Meddelandemetadata i form av XML-plist

Dessa kan förklaras bättre med hjälp av följande exempel på e-post som extraherats från Apple Mail som EMLX och öppnas i en textredigerare.

### EMLX Exempel

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

I det här exemplet visar 875:an meddelandets totala längd. Meddelandets metadata bifogas i<plist> taggar och flaggorna är enligt följande:

|Fält|Beskrivning|Värde
---|---|---|
|0|läs|1 << 0
|1|raderad|1 << 1
|2|svarade|1 << 2
|3|krypterad|1 << 3
|4|flaggat|1 << 4
|5|senaste|1 << 5
|6|utkast|1 << 6
|7|initial (används inte längre)|1 << 7
|8|vidarebefordrad|1 << 8
|9|omdirigerad|1 << 9
|10-15|antal bilagor|3F << 10 (6 bitar)
|16-22|prioritetsnivå|7F << 16 (7 bitar)
|23|signerad|1 << 23
|24|är skräp|1 << 24
|25|är inte skräp|1 << 25
|26-28|teckenstorlek delta|7 << 26 (3 bitar)
|29|skräppostnivå registrerad|1 << 29
|30|markera text i toc|1 << 30
|31|(oanvänd)|

## Se även ##

* [EML](/sv/email/eml/)
* [MSG](/sv/email/msg/)

