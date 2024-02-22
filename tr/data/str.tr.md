{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "STR Dosyası - dBASE Yapı Listesi Nesne Dosyası - .str dosyası nedir ve nasıl açılır?",
  "description" : "STR dBASE Yapı Listesi Nesne Dosyası ve nasıl açılacağı hakkında bilgi edinin.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-tr",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## .STR dosyası nedir?

STR dosya formatı genellikle bir veritabanı yönetim sistemi olan dBASE ile ilişkilidir. dBASE'de bir .str dosyası genellikle bir yapı listesi nesne dosyasını temsil eder. Bu dosya, alanlar (sütunlar) ve bunların özellikleri hakkında bilgiler de dahil olmak üzere bir veritabanı tablosunun yapısını içerir.

Yapı listesi nesne dosyası (.str), alan adları, veri türleri, alan uzunlukları ve veritabanı tablosundaki her alanla ilişkili diğer özellikler gibi meta verileri içerir. Gerçek veri kayıtlarını içermeden veritabanı tablosunun yapısını tanımlamak için kullanılır.

dBASE gibi programlar veya diğer veritabanı yönetim araçları, bu dosyayı veritabanı tablosunun düzenini anlamak ve bu yapıya göre sorgulama, güncelleme veya yeni kayıt oluşturma gibi işlemleri gerçekleştirmek için kullanabilir.

Bir STR dosyasının neler içerebileceğine dair temel bir örnek:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Bu örnekte dört alan içeren bir tablo açıklanmaktadır: Kimlik, Ad, Yaş ve DOB ile ilgili veri türleri ve uzunlukları.

## STR dosyası nasıl açılır?

.str dosyalarını açmanın birincil yolu, özellikle Windows işletim sistemlerinde dBASE'in kendisini kullanmaktır. dBASE, bu dosyaların içeriğini okuma ve yorumlama yeteneğine sahip olup, kullanıcıların veritabanı yapısını görüntülemesine ve üzerinde çalışmasına olanak tanır.

.str dosyaları aslında veritabanının yapısı hakkında bilgi içeren düz metin dosyaları olduğundan, bunları bir metin düzenleyici kullanarak da açabilirsiniz. Metin düzenleyicilere örnek olarak Windows'ta Microsoft Notepad ve Mac'te Apple TextEdit verilebilir. Bir metin düzenleyicide açıldığında, alan adları, veri türleri ve diğer yapısal bilgiler de dahil olmak üzere dosyanın içeriğini insan tarafından okunabilir bir biçimde görebileceksiniz.

## Referanslar
* [dBase](https://en.wikipedia.org/wiki/DBase)


