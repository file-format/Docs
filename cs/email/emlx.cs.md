{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Apple Mail File Format",
  "description":"Další informace o formátu souboru EMLX a rozhraních API, která mohou vytvářet a otevírat soubory EMLX.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor EMLX?

Formát souboru EMLX je implementován a vyvinut společností Apple. Aplikace Apple Mail používá pro export e-mailů souborový formát EMLX. Existují i další aplikace, které mohou otevřít soubory EMLX a převést je do jiných formátů souborů.

## Stručná historie formátu souborů EMLX

Operační systém Mac OS X přijal stávající e-mailový program NeXTMail vytvořený společností NeXT jako součást operačního systému NeXTSTEP. Apple po akvizici NeXT pozvedl své funkce a stal se nyní e-mailovou aplikací Apple Mail, která se používá jako výchozí poštovní klient. E-maily exportované prostřednictvím Apple Mail se přímo ukládají jako soubory EMLX. Navíc je to výchozí poštovní klient pro soubory EMLX, když je někdo otevře poklepáním na Mac OS.

## Formát souboru EMLX

Soubory EMLx jsou jednoduché textové soubory, které lze otevřít v libovolném textovém editoru, jako je Poznámkový blok. Struktura souboru EMLX se skládá ze tří částí:

* Počet bajtů pro zprávu - Délka samotné zprávy, zapsaná v ASCII v desítkové soustavě, ukončená 0x0a
* Samotná zpráva
* Metadata zprávy ve formě XML plist

Ty lze lépe vysvětlit pomocí následujícího vzorového e-mailu extrahovaného z Apple Mail jako EMLX a otevřením v textovém editoru.

### Příklad EMLX

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

V tomto příkladu 875 ukazuje celkovou délku zprávy. Metadata zprávy jsou uzavřena v<plist> značky a příznaky jsou popsány následovně:

|Pole|Popis|Hodnota
---|---|---|
|0|číst|1 << 0
|1|smazáno|1 << 1
|2|odpovězeno|1 << 2
|3|šifrované|1 << 3
|4|označeno|1 << 4
|5|nedávno|1 << 5
|6|návrh|1 << 6
|7|počáteční (již se nepoužívá)|1 << 7
|8|předáno|1 << 8
|9|přesměrováno|1 << 9
|10-15|počet příloh|3F << 10 (6 bitů)
|16-22|úroveň priority|7F << 16 (7 bitů)
|23|podepsán|1 << 23
|24|je nevyžádaná|1 << 24
|25|není odpad|1 << 25
|26-28|velikost písma delta|7 << 26 (3 bity)
|29|zaznamenána úroveň nevyžádané pošty|1 << 29
|30|zvýraznění textu v obsahu|1 << 30
|31|(nepoužité)|

## Viz také ##

* [EML](/cs/e-mail/eml/)
* [MSG](/cs/e-mail/msg/)

