{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AGI Dosyası - Asterisk Gateway Arayüzü Dosya Biçimi",
  "description":"AGI dosya biçiminin ne olduğunu örnekle ve AGI dosyalarını oluşturabilen ve açabilen API'lerle öğrenin.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## AGI dosyası nedir?

Bir AGI dosyası, açık kaynaklı telefon sistemi Asterisk tarafından kullanılan bir komut dosyasıdır. İşlemleri ve Yıldız işareti çevirme planını otomatikleştirmek için kullanılabilecek bilgileri içerir. AGI betik dosyaları kullanılarak, PostgreSQL veya MySQL gibi ilişkisel veritabanlarıyla bağlantılar kurulabilir. Ek olarak, diğer harici kaynaklara erişmek için AGI betikleri de kullanılabilir. AGI betikleri, arama planının kontrolünü harici bir AGI betiğine devrederek Asterisk'in karmaşık görevleri gerçekleştirmesini sağlayabilir.

## AGI Dosya Biçimi - Daha Fazla Bilgi

AGI betik dosyaları, metin dosyaları olarak kaydedilir ve değişiklik yapmak için herhangi bir metin düzenleyicide açılabilir.

### AGI İletişiminin Standart Modeli

AGI betiği, kendisine Asterisk ile gönderilen değişkenleri ve değerlerini yükler. Bu değişkenlerin ortak bir görünümü aşağıdaki gibidir.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Bu değişkenleri, Asterisk tarafından gönderilen boş bir satır takip eder ve bu, AGI betiğinin arama planının kontrolünü artık ele geçirebileceğini gösterir.

### AGI Komut Dosyaları için programlama dili

AGI betikleri genellikle Perl, [PHP](/tr/programming/php/), [C](/tr/programming/c/), Pascal veya Bourne Shell'de yazılabilir.

## Referanslar

* [Yıldız AGI Komut Dosyası](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

