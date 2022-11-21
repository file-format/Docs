{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"KEY dosya formatı ve ANAHTAR dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"KEY Dosya Biçimi - Gizlilik Açısından Geliştirilmiş Posta Özel Anahtar Dosyası",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## ANAHTAR dosyası nedir?

ANAHTAR dosyası, bir güvenlik mekanizmasının Privacy-Enhanced Mal (PEM) dosya biçiminde diske kaydedilen özel parçasıdır. Bir web tarayıcısı ile tarama isteklerine hizmet eden web sunucusu arasında değiş tokuş edilen bilgilerin şifresini çözmek için kullanılır. Bir ANAHTAR dosyası, insan gözü için yararsız olan ancak web sunucularındaki SSL sertifikasının bir parçası olarak bilgi alışverişini şifrelemenin/şifresini çözmenin özü olan kodlanmış dizeler içerir. ANAHTAR dosyaları otomatik olarak oluşturulur ve istemci tarafında kurulur.

**KEY** dosyalarını Microsoft Notepad (Windows), Apple TextEdit (Mac) veya GitHub Atom (çapraz platform) gibi herhangi bir metin düzenleyiciyle açabilirsiniz. ANAHTAR dosyaları, [CRT](/tr/web/crt/) ve [CER](/tr/web/cer/) dosya biçimlerine benzer.

## ANAHTAR Dosya Biçimi - Daha Fazla Bilgi

ANAHTAR dosyaları diskte düz metin dosyaları olarak depolanır, ancak okunması kolay olmayan kodlanmış dizelerdir. Pratik olarak, kullanıcılar bir metin düzenleyicide açıldığında dizeleri sıfır olarak anlarlar. Özel anahtar sertifikası gizlidir ve kimseyle paylaşılmamalıdır. İnternet üzerinden bilgi alışverişini güvence altına alma sürecinin tamamı şunları içerir:

* **Genel Anahtar** - tarayıcı ve web sunucuları arasında veri alışverişi için kullanıcı bilgilerini şifrelemek için kullanılır
* **Özel Anahtar** - web sunucusu tarafından alınan bilgilerin şifresini çözmek için kullanılır

X.509 sertifikaları olarak da bilinen SSL sertifikaları, her web sitesi için benzersizdir. KEY dosyaları aşağıdaki söz dizimini kullanır:

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### ANAHTAR Dosya Örneği

Aşağıda özel Anahtar dosyası örneği verilmiştir.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referanslar

* [Genel Anahtarlar, Özel Anahtarlar ve Sertifikalar](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

