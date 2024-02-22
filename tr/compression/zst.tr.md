{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ZST Dosyası - Zstandard Sıkıştırılmış Dosya Formatı",
  "description":"ZST dosyalarını oluşturabilen ve açabilen ZST dosya formatı ve API'ler hakkında bilgi edinin.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-tr",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## .ZST dosyası nedir?

ZST dosyası, Zstandard (zstd) sıkıştırma algoritmasıyla oluşturulan sıkıştırılmış bir dosyadır. Algoritma tarafından kayıpsız sıkıştırmayla oluşturulan sıkıştırılmış bir dosyadır. ZST dosyaları veritabanları, dosya sistemleri, ağlar ve oyunlar gibi farklı dosya türlerini sıkıştırmak için kullanılabilir. Zstandardı, genel sıkıştırma mekanizmasını, medya türünü ve içerik kodlamasını açıklayan [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) tarafından yönetilir.

## ZST Dosya Formatı

ZST dosyaları sıkıştırılmış dosya formatında diske kaydedilir. Sıkıştırma mekanizması, RFC 8478'i geçersiz kılan RFC 8878 tarafından açıklandığı gibidir.

## ZST Çerçeveleri

Bir ZST dosyası bir veya daha fazla çerçeveden oluşur. Her kare bir Z standart karesi veya atlanabilir bir kare olabilir. Bir Zstandard çerçevesi sıkıştırılmış verileri içerirken, atlanabilir bir çerçeve özel kullanıcı meta verilerini içerir.

### Zstandart Çerçeve

Bir Zstandard çerçevesi aşağıdaki yapıya sahiptir.

|Alan|Bayt Cinsinden Boyut|
---|---|
|Magic_Number |4 bayt|
|Frame_Header |2-14 bayt|
|Data_Block |n bayt|
|[Daha Fazla Veri_Bloğu] ||
|[Content_Checksum] |4 bayt|

### Atlanabilir Çerçeve

Atlanabilir bir çerçeve, kullanıcı tanımlı meta verilerin birleştirilmiş çerçeveler akışına eklenmesine olanak tanır. Atlanabilir çerçevenin yapısı aşağıdaki gibidir.

|Sihirli_Numara |Frame_Size |Kullanıcı_Verileri|
---|---|---|
|4 bayt |4 bayt |n bayt|

## Referanslar ##

* [RFC 8878 Zstandart Sıkıştırma](https://www.rfc-editor.org/rfc/rfc8878)


