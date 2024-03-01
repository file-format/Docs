{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMLX - Apple Mail -tiedostomuoto",
  "description": "Opi EMLX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata EMLX-tiedostoja.",
  "linktitle": "EMLX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-eml-fix"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on EMLX-tiedosto?

EMLX-tiedostomuodon on toteuttanut ja kehittänyt Apple. Apple Mail -sovellus käyttää EMLX-tiedostomuotoa sähköpostien viemiseen. On myös muita sovelluksia, jotka voivat avata EMLX-tiedostoja ja muuntaa ne muihin tiedostomuotoihin.

## EMLX-tiedostomuodon lyhyt historia

Mac OS X -käyttöjärjestelmä otti käyttöön olemassa olevan sähköpostiohjelman NeXTMail, jonka NeXT loi osaksi NeXTSTEP-käyttöjärjestelmää. NeXT:n hankinnan jälkeen Apple paransi ominaisuuksiaan ja siitä tuli nyt Apple Mail -sähköpostisovellus, jota käytetään oletussähköpostiohjelmana. Apple Mailin kautta viedyt sähköpostit tallennetaan suoraan EMLX-tiedostoina. Lisäksi se on oletussähköpostiohjelma EMLX-tiedostoille, kun joku avaa ne kaksoisnapsauttamalla Mac OS:ää.

## EMLX-tiedostomuoto

EMLx-tiedostot ovat yksinkertaisia tekstipohjaisia tiedostoja, jotka voidaan avata missä tahansa tekstieditorissa, kuten Notepadissa. EMLX-tiedostorakenne koostuu kolmesta osasta:

* Viestin tavumäärä - Itse viestin pituus, kirjoitettu ASCII-muodossa desimaaleina, päättyy numeroon 0x0a

* Itse viesti

* Viestin metatiedot XML-muodossa


Nämä voidaan selittää paremmin seuraavan Apple Mailista EMLX-muodossa poimitun ja tekstieditorissa avatun mallisähköpostin avulla.

### EMLX-esimerkki

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

Tässä esimerkissä 875 näyttää viestin kokonaispituuden. Viestin metatiedot ovat mukana<plist> tunnisteet ja liput ovat seuraavat:

|Kenttä|Kuvaus|Arvo
---|---|---|
|0|lue|1 << 0
|1|poistettu|1 << 1
|2|vastasi|1 << 2
|3|salattu|1 << 3
|4|merkitty|1 << 4
|5|äskettäin|1 << 5
|6|luonnos|1 << 6
|7|alkuperäinen (ei enää käytössä)|1 << 7
|8|edelleen|1 << 8
|9|uudelleenohjattu|1 << 9
|10-15|liitteiden määrä|3F << 10 (6 bittiä)
|16-22|prioriteettitaso|7F << 16 (7 bittiä)
|23|allekirjoitettu|1 << 23
|24|on roskaa|1 << 24
|25|ei ole roskaa|1 << 25
|26-28|fonttikoko delta|7 << 26 (3 bittiä)
|29|roskapostitaso tallennettu|1 << 29
|30|korosta teksti tocissa|1 << 30
|31|(käyttämätön)|

## Katso myös ##

* [EML](/email/eml/)

* [MSG](/email/msg/)


