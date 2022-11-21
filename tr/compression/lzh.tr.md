{
  "date" : "2021-06-16",
  "keywords" :[ "LZH", "Sıkıştırılmış", "Dosya", "Uzantı", "Dosya Biçimi", "Lempel-Ziv", "Haruyasu", "LHA"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZH Dosya Biçimi",
  "description":"LZH dosya formatı ve LZH dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## LZH dosyası nedir? ##

.lzh ve .lha uzantılı bir dosya genellikle arşiv sıkıştırma dosyası biçimiyle ilgilidir. Bu dosya formatı, [ZIP](/tr/compression/zip/), [RAR](/tr/compression/rar/), vb. gibi diğer dosya sıkıştırma formatlarıyla aynıdır. Bu dosya formatlarının temel amacı, dosya boyutunu küçültmektir. kolayca göndermek ve sıkıştırılmış formda bir arada tutmak için format. Diğer batılı şirketlerle karşılaştırıldığında LZH dosyaları Japonya'da çok popülerdir ve genellikle video oyunu verilerini sıkıştırmak için kullanılır. Windows 7 için LZH eklentisi, Windows 7'nin Japonca sürümünde yerleşiktir. Microsoft, Windows XP'nin Japonca sürümü için ilk olarak Microsoft Sıkıştırılmış (LZH) Klasör Eklentisini yayımladı. Bu dosya formatı, Lempel-Ziv ve Haruyasu algoritması tarafından kullanılan sıkıştırma hükümleri ve özellikleri ile uygulanmaktadır.

## LZH Spesifikasyonu ##

Bir LZH arşivinin sıkıştırma yöntemi, -lz1- gibi beş baytlık bir metin dizisi olarak gösterilir. Bunlar, sıkıştırılmış dosyadaki üçüncü ila yedinci baytlardır.

|Özellikler|Açıklama|
---|---|
|Uzantı | .lzh, .lha|
|Medya Türü| uygulama/x-lzh-sıkıştırılmış|
|Kod yazın| "LHA_" (LHA-UZAY)|
|UTI| public.archive.lha|
|Geliştiren| Haruyasu Yoshizaki (Yoshi)|
|Tür| Sıkıştırma|
|Genişletilmiş| LArc|

## Bir LZH dosyasını açma sorunları ##

Aşağıda, LZH dosya biçiminin kötü çalışmasına neden olabilecek birkaç sorun bulunmaktadır:
  

* Dosya bozuk olabilir. Bu sorunu çözmek için dosyayı yeniden indirin veya gönderenden dosyayı yeniden göndermesini isteyin
* İkinci neden virüslü dosyadır bu durumda dosyayı düzgün bir şekilde tarayın
* LZH dosyasına uygun olmayan bağlantılar
* LZH açıklamasının kaldırılması
* Yeterli donanım kaynağı yok
* Ekipmanın güncel olmayan sürücüleri

## Referanslar ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
