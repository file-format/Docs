{
  "date" : "2019-10-11",
  "keywords" :[ "gz dosyası", "gz dosya biçimi", "gz dosyası nedir", "dosya", "gz örneği", "gz dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GZ Dosya Biçimi - GNU Sıkıştırılmış Arşiv Dosyası",
  "description":"GZ dosyasının ne olduğu ve GZ dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## .gz dosyası nedir?

Bir GZ dosyası, standart [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) sıkıştırma algoritması kullanılarak oluşturulan sıkıştırılmış bir arşivdir. Birden çok sıkıştırılmış dosya, dizin ve dosya koçanı içerebilir. Bu format başlangıçta UNIX sistemlerindeki sıkıştırma formatlarının yerini almak için geliştirilmiştir. ve hala Linux sistemlerindeki en yaygın arşiv türlerinden biridir. [WinZip](https://www.winzip.com/en/) gibi uygulamalar, içeriğini hem Windows hem de MacOS'ta görüntülemek için GZ dosyalarını açabilir.

## GZ Dosya Formatı - Daha Fazla Bilgi

Gzip, arşivi sıkıştırmak için [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) algoritmasını kullanır ve sıkıştırma algoritmasını tüm arşive uygulama açısından [ZIP](/tr/compression/zip/) arşiv biçiminden farklıdır. bireysel dosyalar yerine. Internet Engineering Task Force (IETF) tarafından yayınlanan GZIP dosya biçimi belirtimleri sürüm 4.3, dosya biçimi hakkında ayrıntılı bilgiler içerir. Dosya biçimi şunlardan oluşur:

* Dosya Başlığı
* İsteğe Bağlı Başlıklar
* Sıkıştırılmış Veri
* Dosya Altbilgisi

## GZ Dosya Başlığı ##

GZ dosya başlığı aşağıdaki gibi 10 bayttan oluşur:

|Ofset|Boyut|Değer|Açıklama
---|---|---|---|
|0|2|0x1f 0x8b|Dosya türünü tanımlayan sihirli sayı
|2|1| |Sıkıştırma Metodu * 0-7 (Ayrılmış) * 8 (Söndür)
|3|1| |Dosya Bayrakları
|4|4| |32-bit zaman damgası
|8|1| |Sıkıştırma bayrakları
|9|1| |İşletim sistemi kimliği

### Dosya Bayrakları ###

|Değer|Tanımlayıcı|Açıklama
---|---|---|
|0x01|FTEXT|Ayarlanırsa, sıkıştırılmamış verinin ikili veri yerine metin olarak ele alınması gerekir. Bu bayrak, platformlar arası metin dosyaları için satır sonu dönüştürmeyi ima eder, ancak bunu zorlamaz.
|0x02|FHCRC|Dosya bir başlık sağlama toplamı içeriyor (CRC-16)
|0x04|FEXTRA|Dosya fazladan alanlar içeriyor
|0x08|FNAME|Dosya, orijinal bir dosya adı dizesi içeriyor
|0x10|FCOMMENT|Dosya yorum içeriyor
|0x20| |Ayrılmış
|0x40| |Ayrılmış
|0x80| |Ayrılmış

### İşletim sistemi ###

|Değer|Açıklama
---|---|
|0|FAT dosya sistemi (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (veya OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari Hizmet Şartları
|6|HPFS dosya sistemi (OS/2, NT)
|7|Macintosh
|8|Z-Sistemi
|9|CP/M
|10|ÜST-20
|11|NTFS dosya sistemi (NT)
|12|QDOS
|13|Palamut RISCOS
|255|bilinmiyor

## GZ İsteğe Bağlı Başlıklar ##

İsteğe bağlı ekstra başlıklar, dosya bayraklarıyla gösterilenlerdir ve orijinal dosya adı, ekstra alanlar, yorumlar ve başlık sağlama toplamı gibi bilgileri içerir.

## Sıkıştırılmış Veri ##

Bu bölüm, DEFLATE sıkıştırma algoritması kullanılarak sıkıştırılmış verileri içerir.

## GZ Dosya Altbilgisi ##

Dosya altbilgisi 8 bayt boyutundadır ve aşağıdaki bilgileri içerir.

|Ofset|Boyut|Açıklama
---|---|---|
|0|4|Sağlama toplamı (CRC-32)
|4|4|Bayt cinsinden sıkıştırılmamış veri boyutu değeri

## Referanslar ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: GZIP dosya biçimi belirtimi](http://tools.ietf.org/html/rfc1952), IETF tarafından.

