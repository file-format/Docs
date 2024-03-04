{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMLX – Apple Mail failo formatas",
  "description": "Sužinokite apie EMLX failo formatą ir API, kurios gali kurti ir atidaryti EMLX failus.",
  "linktitle": "EMLX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-eml-ltx"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra EMLX failas?

EMLX failo formatą įdiegė ir sukūrė Apple. Apple Mail programa el. laiškams eksportuoti naudoja EMLX failo formatą. Taip pat yra kitų programų, kurios gali atidaryti EMLX failus ir konvertuoti juos į kitus failų formatus.

## Trumpa EMLX failo formato istorija

Mac OS X operacinė sistema priėmė esamą el. pašto programą NeXTMail, kurią NeXT sukūrė kaip NeXTSTEP operacinės sistemos dalį. Apple, įsigijusi NeXT, patobulino savo funkcijas ir tapo dabar Apple Mail el. pašto programa, naudojama kaip numatytoji pašto programa. El. laiškai, eksportuoti per Apple Mail, tiesiogiai išsaugomi kaip EMLX failai. Be to, tai yra numatytoji EMLX failų pašto programa, kai kas nors atidaro juos dukart spustelėdamas Mac OS.

## EMLX failo formatas

EMLx failai yra paprasti teksto failai, kuriuos galima atidaryti bet kuriame teksto rengyklėje, pvz., Notepad. EMLX failo struktūra susideda iš trijų dalių:

* Pranešimo baitų skaičius – paties pranešimo ilgis, parašytas ASCII dešimtainiu tikslumu, baigiamas 0x0a

* Pati žinutė

* Pranešimo metaduomenys XML plist forma


Tai gali būti geriau paaiškinta naudojant pavyzdinį el. laišką, ištrauktą iš Apple Mail kaip EMLX ir atidarius teksto rengyklėje.

### EMLX pavyzdys

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

Šiame pavyzdyje 875 rodo bendrą pranešimo ilgį. Pranešimo metaduomenys yra įtraukti į<plist> žymos ir vėliavėlės aprašytos taip:

|Laukas|Aprašymas|Vertė
---|---|---|
|0|skaityti|1 << 0
|1|ištrintas|1 << 1
|2|atsakė|1 << 2
|3|šifruota|1 << 3
|4|pažymėta|1 << 4
|5|naujausi|1 << 5
|6|juodraštis|1 << 6
|7|pradinis (nebenaudojamas)|1 << 7
|8|persiųsta|1 << 8
|9|peradresuota|1 << 9
|10–15|priedų skaičius|3F << 10 (6 bitai)
|16-22|prioriteto lygis|7F << 16 (7 bitai)
|23|pasirašytas|1 << 23
|24|yra šlamštas|1 << 24
|25|nėra šlamštas|1 << 25
|26–28|šrifto dydis delta|7 << 26 (3 bitai)
|29|užregistruotas šlamšto lygis|1 << 29
|30|paryškinti tekstą toc|1 << 30
|31|(nenaudota)|

## Taip pat žiūrėkite ##

* [EML](/email/eml/)

* [MSG](/email/msg/)


