{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX — format pliku Apple Mail",
  "description":"Poznaj format pliku EMLX i interfejsy API, które mogą tworzyć i otwierać pliki EMLX.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik EMLX?

Format pliku EMLX jest wdrażany i rozwijany przez firmę Apple. Aplikacja Apple Mail używa formatu pliku EMLX do eksportowania wiadomości e-mail. Istnieją również inne aplikacje, które mogą otwierać pliki EMLX i konwertować je do innych formatów plików.

## Krótka historia formatu pliku EMLX

System operacyjny Mac OS X przyjął istniejący program pocztowy NeXTMail, stworzony przez firmę NeXT jako część systemu operacyjnego NeXTSTEP. Apple po przejęciu NeXT ulepszyło swoje funkcje i stało się teraz aplikacją e-mail Apple Mail, która ma być używana jako domyślny klient poczty. E-maile eksportowane przez Apple Mail są zapisywane bezpośrednio jako pliki EMLX. Ponadto jest to domyślny klient poczty dla plików EMLX, gdy ktoś otwiera je, klikając dwukrotnie system Mac OS.

## Format pliku EMLX

Pliki EMLx to proste pliki tekstowe, które można otwierać w dowolnym edytorze tekstu, takim jak Notatnik. Struktura plików EMLX składa się z trzech części:

* Liczba bajtów dla wiadomości - Długość samej wiadomości, zapisana w ASCII w systemie dziesiętnym, zakończona przez 0x0a
* Sama wiadomość
* Metadane wiadomości w postaci plist XML

Można to lepiej wyjaśnić za pomocą następującego przykładowego e-maila wyodrębnionego z Apple Mail jako EMLX i otwieranego w edytorze tekstu.

### EMLX Przykład

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

W tym przykładzie 875 pokazuje całkowitą długość wiadomości. Metadane wiadomości są zawarte w pliku<plist> tagi i flagi są opisane w następujący sposób:

|Pole|Opis|Wartość
---|---|---|
|0|czytaj|1 << 0
|1|usunięto|1 << 1
|2|odpowiedział|1 << 2
|3|szyfrowane|1 << 3
|4|oflagowane|1 << 4
|5|ostatnie|1 << 5
|6|projekt|1 << 6
|7|inicjał (już nie używany)|1 << 7
|8|przesłane|1 << 8
|9|przekierowany|1 << 9
|10-15|liczba załączników|3F << 10 (6 bitów)
|16-22|poziom priorytetu|7F << 16 (7 bitów)
|23|podpisano|1 << 23
|24|jest śmieciem|1 << 24
|25|nie jest śmieciem|1 << 25
|26-28|rozmiar czcionki|7 << 26 (3 bity)
|29|zarejestrowano poziom wiadomości-śmieci|1 << 29
|30|podświetl tekst w toc|1 << 30
|31|(nieużywane)|

## Zobacz też ##

* [EML](/pl/e-mail/eml/)
* [MSG](/pl/e-mail/msg/)

