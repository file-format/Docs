{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "uzantı", "dosya", "biçim", "eKitap", "Kindle Dosya Biçimi", "AZW3 Dosya Yapısı"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"AZW3 dosya formatı ve AZW3 dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"AZW3 dosyası nedir?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## AZW3 dosyası nedir?

Kindle Format 8 (**KF8**) olarak da bilinen AZW3, Amazon Kindle cihazları için geliştirilmiş [AZW](/tr/ebook/azw/) e-kitap dijital dosya formatının değiştirilmiş versiyonudur. Biçim, eski AZW dosyalarına yönelik bir geliştirmedir ve Kindle Fire cihazlarında yalnızca ata dosya biçimi, yani [MOBI](/tr/ebook/mobi/) ve AZW için geriye dönük uyumlulukla kullanılır. Amazon, en son Kindle cihazlarında kullanılan KFX (KF sürüm 10) formatını KF8'den sonra tanıttı. AZW3 dosyalarında internet ortam türü application/vnd.amazon.mobi8-ebook bulunur. AZW3 dosyaları, [PDF](/tr/pdf/), [EPUB](/tr/ebook/epub/), [AZW](/tr/ebook/azw/), [DOCX](/tr/) gibi bir dizi başka dosya biçimine dönüştürülebilir. kelime işlemci/docx/) ve [RTF](/tr/kelime işlemci/rtf/).

## AZ3/KF8 Dosya Biçimi ##

KF8 dosyaları ikili yapıdadır ve MOBI dosya biçiminin yapısını PDB dosyası olarak korur. Daha önce belirtildiği gibi, bir KF8 dosyası hem bir MOBI'den hem de EPUB'un daha yeni bir KF8 sürümünden oluşabilir. Biçimin dahili ayrıntılarının kodu, nihai derlenmiş veritabanını ayrıştıran ve MOBI veya AZW kaynak dosyalarını buradan çıkaran bir Python betiği olan [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack) tarafından çözülmüştür. AZW3 (KF8) dosyaları, EPUB için de geriye dönük uyumluluğa sahip EPUB3 sürümünü hedefler. KF8, EPUB dosyalarını derler ve PDB dosya biçimine dayalı bir ikili yapı oluşturur.

## Referanslar ##

* [KF8 - Wikipedia'dan](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)

