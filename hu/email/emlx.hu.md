{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Apple Mail File Format",
  "description":"További információ az EMLX fájlformátumról és az API-król, amelyek EMLX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az EMLX fájl?

Az EMLX fájlformátumot az Apple valósította meg és fejlesztette ki. Az Apple Mail alkalmazás az EMLX fájlformátumot használja az e-mailek exportálásához. Vannak más alkalmazások is, amelyek megnyithatják az EMLX fájlokat, és konvertálhatják azokat más fájlformátumokba.

## Az EMLX fájlformátum rövid története

A Mac OS X operációs rendszer átvette a meglévő levelezőprogramot, a NeXTMail-t, amelyet a NeXT hozott létre a NeXTSTEP operációs rendszer részeként. Az Apple a NeXT megvásárlása után továbbfejlesztette szolgáltatásait, és ez lett az Apple Mail e-mail alkalmazás, amelyet alapértelmezett levelezőkliensként használnak. Az Apple Mail segítségével exportált e-maileket közvetlenül EMLX fájlként menti a rendszer. Ezenkívül ez az alapértelmezett levelezőkliens az EMLX-fájlokhoz, amikor valaki dupla kattintással nyitja meg ezeket a Mac OS rendszeren.

## EMLX fájlformátum

Az EMLx fájlok egyszerű szöveg alapú fájlok, amelyek bármely szövegszerkesztőben, például a Jegyzettömbben megnyithatók. Az EMLX fájlstruktúra három részből áll:

* Egy bájtszám az üzenethez – Az üzenet hossza, decimális ASCII-ben írva, 0x0a zárja le
* Maga az üzenet
* Üzenet metaadatok XML plist formájában

Ezeket jobban meg lehet magyarázni az alábbi minta e-mailek segítségével, amelyeket az Apple Mailből EMLX-ként kinyertünk és egy szövegszerkesztőben nyitunk meg.

### EMLX példa

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

Ebben a példában a 875 az üzenet teljes hosszát mutatja. Az üzenet metaadatait a<plist> a címkék és a zászlók leírása a következő:

|Mező|Leírás|Érték
---|---|---|
|0|olvasni|1 << 0
|1|törölt|1 << 1
|2|válaszolt|1 << 2
|3|titkosított|1 << 3
|4|megjelölve|1 << 4
|5|legutóbbi|1 << 5
|6|tervezet|1 << 6
|7|kezdeti (már nem használt)|1 << 7
|8|továbbküldve|1 << 8
|9|átirányítva|1 << 9
|10-15|mellékletek száma|3F << 10 (6 bit)
|16-22|prioritási szint|7F << 16 (7 bit)
|23|aláírva|1 << 23
|24|szemét|1 << 24
|25|nem szemét|1 << 25
|26-28|betűméret delta|7 << 26 (3 bit)
|29|levélszemét szint rögzítve|1 << 29
|30|szöveg kiemelése a toc-ban|1 << 30
|31|(nem használt)|

## Lásd még ##

* [EML](/hu/email/eml/)
* [MSG](/hu/email/msg/)

