{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Apple Mail-bestandsindeling",
  "description":"Meer informatie over EMLX-bestandsindelingen en API's die EMLX-bestanden kunnen maken en openen.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een EMLX-bestand?

Het EMLX-bestandsformaat is geïmplementeerd en ontwikkeld door Apple. De Apple Mail-applicatie gebruikt het EMLX-bestandsformaat voor het exporteren van de e-mails. Er zijn ook andere toepassingen die de EMLX-bestanden kunnen openen en converteren naar andere bestandsindelingen.

## Korte geschiedenis van het EMLX-bestandsformaat

Het Mac OS X-besturingssysteem heeft het bestaande e-mailprogramma NeXTMail overgenomen, dat door NeXT is gemaakt als onderdeel van het NeXTSTEP-besturingssysteem. Apple heeft na de overname van NeXT zijn functies verbeterd en het werd de nu Apple Mail-e-mailtoepassing die als standaard e-mailclient moet worden gebruikt. E-mails die zijn geëxporteerd via Apple Mail worden direct opgeslagen als EMLX-bestanden. Bovendien is het de standaard e-mailclient voor EMLX-bestanden wanneer iemand deze opent door te dubbelklikken op Mac OS.

## EMLX-bestandsindeling

EMLx-bestanden zijn eenvoudige op tekst gebaseerde bestanden die in elke teksteditor zoals Kladblok kunnen worden geopend. De EMLX-bestandsstructuur bestaat uit drie delen:

* Een bytetelling voor het bericht - Lengte van het bericht zelf, geschreven in ASCII in decimaal, afgesloten met 0x0a
* Het bericht zelf
* Metadata van berichten in de vorm van XML-plist

Deze kunnen beter worden uitgelegd met behulp van het volgen van voorbeeld-e-mail die is geëxtraheerd uit Apple Mail als EMLX en wordt geopend in een teksteditor.

### EMLX Voorbeeld

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

In dit voorbeeld toont de 875 de totale lengte van het bericht. De metadata van het bericht is ingesloten in de<plist> tags en de vlaggen zijn als volgt beschreven:

|Veld|Beschrijving|Waarde
---|---|---|
|0|lezen|1 << 0
|1|verwijderd|1 << 1
|2|beantwoord|1 << 2
|3|gecodeerd|1 << 3
|4|gemarkeerd|1 << 4
|5|recent|1 << 5
|6|concept|1 << 6
|7|eerste (niet meer gebruikt)|1 << 7
|8|doorgestuurd|1 << 8
|9|doorverwezen|1 << 9
|10-15|aantal bijlagen|3F << 10 (6 bits)
|16-22|prioriteitniveau|7F << 16 (7 bits)
|23|ondertekend|1 << 23
|24|is rommel|1 << 24
|25|is geen rommel|1 << 25
|26-28|lettergrootte delta|7 << 26 (3 bits)
|29|ongewenst mailniveau geregistreerd|1 << 29
|30|markeer tekst in toc|1 << 30
|31|(ongebruikt)|

## Zie ook ##

* [EML](/nl/e-mail/eml/)
* [MSG](/nl/e-mail/bericht/)

