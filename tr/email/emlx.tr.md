{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Apple Mail Dosya Biçimi",
  "description":"EMLX dosya formatı ve EMLX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## EMLX dosyası nedir?

EMLX dosya formatı Apple tarafından uygulanır ve geliştirilir. Apple Mail uygulaması, e-postaları dışa aktarmak için EMLX dosya biçimini kullanır. EMLX dosyalarını açabilen ve bunları başka dosya biçimlerine dönüştürebilen başka uygulamalar da vardır.

## EMLX Dosya Formatının Kısa Tarihi

Mac OS X işletim sistemi, NeXTSTEP işletim sisteminin bir parçası olarak NeXT tarafından oluşturulan mevcut e-posta programı NeXTMail'i benimsemiştir. Apple, NeXT'yi satın aldıktan sonra özelliklerini yükseltti ve artık varsayılan posta istemcisi olarak kullanılacak Apple Mail e-posta uygulaması oldu. Apple Mail aracılığıyla dışa aktarılan e-postalar doğrudan EMLX dosyaları olarak kaydedilir. Ayrıca, birisi Mac OS'de çift tıklayarak açtığında, EMLX dosyaları için varsayılan posta istemcisidir.

## EMLX Dosya Biçimi

EMLx dosyaları, Notepad gibi herhangi bir metin düzenleyicide açılabilen basit metin tabanlı dosyalardır. EMLX dosya yapısı üç bölümden oluşur:

* Mesaj için bir bayt sayısı - ASCII'de ondalık olarak yazılmış, 0x0a ile sonlandırılan mesajın kendisinin uzunluğu
* Mesajın kendisi
* XML plist biçimindeki Mesaj Meta Verileri

Bunlar, Apple Mail'den EMLX olarak çıkarılan ve bir metin düzenleyicide açılan aşağıdaki örnek e-postanın yardımıyla daha iyi açıklanabilir.

### EMLX Örneği

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

Bu örnekte, 875 mesajın toplam uzunluğunu gösterir. Mesaj meta verileri,<plist> etiketler ve bayraklar aşağıda açıklandığı gibidir:

|Alan|Açıklama|Değer
---|---|---|
|0|oku|1 << 0
|1|silindi|1 << 1
|2|cevap|1 << 2
|3|şifreli|1 << 3
|4|işaretlendi|1 << 4
|5|en son|1 << 5
|6|taslak|1 << 6
|7|başlangıç (artık kullanılmıyor)|1 << 7
|8|iletildi|1 << 8
|9|yönlendirildi|1 << 9
|10-15|ek sayısı|3F << 10 (6 bit)
|16-22|öncelik düzeyi|7F << 16 (7 bit)
|23|imza|1 << 23
|24|önemsiz|1 << 24
|25|önemsiz değil|1 << 25
|26-28|yazı boyutu delta|7 << 26 (3 bit)
|29|önemsiz posta düzeyi kaydedildi|1 << 29
|30|tc'de metni vurgula|1 << 30
|31|(kullanılmamış)|

## Ayrıca bakınız ##

* [EML](/tr/email/eml/)
* [MSG](/tr/email/msg/)

