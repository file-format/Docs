{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMLX - Apple Mail Fayl Format",
  "description": "EMLX faylları yarada və aça bilən EMLX fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "EMLX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-eml-azx"
}
},
  "lastmod": "2019-09-10"
}

## EMLX faylı nədir?

EMLX fayl formatı Apple tərəfindən həyata keçirilir və hazırlanır. Apple Mail proqramı e-poçtları ixrac etmək üçün EMLX fayl formatından istifadə edir. EMLX fayllarını aça və digər fayl formatlarına çevirə bilən başqa proqramlar da var.

## EMLX Fayl Formatının Qısa Tarixi

Mac OS X əməliyyat sistemi NeXT tərəfindən NeXTSTEP əməliyyat sisteminin bir hissəsi kimi yaradılmış NeXTMail adlı mövcud e-poçt proqramını qəbul etdi. NeXT-i əldə etdikdən sonra Apple öz xüsusiyyətlərini artırdı və o, standart poçt müştərisi kimi istifadə olunan indi Apple Mail e-poçt proqramı oldu. Apple Mail vasitəsilə ixrac edilən e-poçtlar birbaşa EMLX faylları kimi saxlanılır. Bundan əlavə, kimsə Mac OS-də iki dəfə klikləməklə onları açdıqda EMLX faylları üçün standart poçt müştərisidir.

## EMLX Fayl Format

EMLx faylları Notepad kimi istənilən mətn redaktorunda açıla bilən sadə mətn əsaslı fayllardır. EMLX fayl strukturu üç hissədən ibarətdir:

* Mesaj üçün bayt sayı - Mesajın özünün uzunluğu, ASCII-də onluqda yazılmış, 0x0a ilə bitir

* Mesajın özü

* XML plist şəklində mesaj metaməlumatları


Bunları EMLX kimi Apple Mail-dən çıxarılmış və mətn redaktorunda açılan aşağıdakı nümunə e-poçtun köməyi ilə daha yaxşı izah etmək olar.

### EMLX Nümunəsi

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

Bu nümunədə 875 mesajın ümumi uzunluğunu göstərir. Mesaj metadatası əlavə olunur<plist> etiketlər və bayraqlar aşağıdakı kimi təsvir edilmişdir:

|Sahə|Təsvir|Dəyər
---|---|---|
|0|oxumaq|1 << 0
|1|silindi|1 << 1
|2|cavab verdi|1 << 2
|3|şifrələnmiş|1 << 3
|4|bayraqlı|1 << 4
|5|son|1 << 5
|6|qaralama|1 << 6
|7|ilkin (artıq istifadə olunmur)|1 << 7
|8|yönləndirilmiş|1 << 8
|9|yönləndirilmiş|1 << 9
|10-15|qoşma sayı|3F << 10 (6 bit)
|16-22|prioritet səviyyəsi|7F << 16 (7 bit)
|23|imzalı|1 << 23
|24|zibildir|1 << 24
|25|zibil deyil|1 << 25
|26-28|şrift ölçüsü delta|7 << 26 (3 bit)
|29|qeyd edilmiş lazımsız poçt səviyyəsi|1 << 29
|30|toc-da mətni vurğulayın|1 << 30
|31|(istifadə olunmamış)|

## Həmçinin bax ##

* [EML](/email/eml/)

* [MSG](/email/msg/)


