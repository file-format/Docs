{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "dosya", "uzantı", "format", "amr dosyası nedir", "müzik", "amr dosya biçimi", "amr dosyası","amr dosyasını şuraya dönüştür: mp3", "amr dosyasını çal" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"AMR dosya formatı ve AMR dosyalarını oluşturabilen, dönüştürebilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"AMR - Adaptive Multi-Rate Codec Dosyası",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## AMR dosyası nedir?
.amr uzantılı dosya, **Adaptive Multi-Rate** ses kodekiyle ilgili bir ses verisi biçimidir; 7,4 kbit/s'den başlayan ücretli konuşma kalitesiyle 4,75-12,2 kbit/s bit hızında dar bant sinyalleri kodlayan çok oranlı bir dar bant konuşma codec bileşeninden oluşur; tabanlı sekiz farklı bit hızından birini seçmek için bağlantı uyarlamasını kullanır.

## AMR Dosya Biçimi
AMR dosya formatı birçok kodlama tekniği kullanır, ACELP (Cebirsel Kod Uyarılmış Doğrusal Tahmin) algoritması en iyi tekniklerden biridir; insan konuşma sesini daha verimli bir şekilde sıkıştırmak için tasarlanmıştır. AMR, 1999 yılında 3GPP tarafından standart ses veya konuşma codec'i olarak belirlendi. AMR dosya formatı, birçok akıllı telefon tarafından kaydedilenleri depolamak için kullanılan **Adaptive Multi-Rate** ses codec'i kullanılarak konuşulan sesi depolamak için de kullanılır. konuşmalar

### Dosya biçimi yapısı
AMR (Adaptive Multi-Rate) bir ses formatıdır; çeşitli mobil uygulamalarda ve cihazlarda, tipik olarak ses çalar/kaydedicide veya VoIP türü uygulamalarda yaygın olarak kullanılır. AMR ayrıca şu şekilde sınıflandırılabilir:

1. AMR-NB(Dar Bant)
2. AMR-WB(Geniş Bant)

Genellikle AMR, AMR-NB'yi ifade eder. AMR dosya formatı aşağıdaki yapıya sahiptir:

Her AMR dosyası, dosyayı bir AMR sesi olarak tanıyan 6 baytlık bir başlık içerir. Bu başlık her zaman şu şekilde ayarlanır:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Bu genellikle tüm AMR-NB dosyalarında benzerdir. Başlık bir standardı takip ediyorsa, muhtemelen dosya bozuktur ve kullanılmamalıdır. AMR dosyası, çok sayıda paketlenmiş ses karesinden oluşur. Bu çerçevelerin her biri 20ms ses oluşturur. Her çerçeve, geçerli AMR-NB modlarından herhangi biri kullanılarak kodlanabilir (DTX modunda 0-7, 8 SID). Çerçeveler farklı bit hızlarında kodlanabildiğinden, bu tipik yönteme Uyarlanabilir Çoklu Hız (AMR) adı verilir.
#### AMR modları
Aşağıdakiler, farklı AMR modları ve bunlara karşılık gelen bit hızlarıdır:

|MOD| BİT ORANLARI|
---|---|
|0| AMR 4.75 - 4.75kbit/sn'de kodlar |
|1 | AMR 5.15 - 5.15kbit/s'de kodlar |
|2 | AMR 5.9 - 5.9kbit/sn'de kodlar |
|3 | AMR 6.7 - 6.7kbit/sn'de kodlar |
|4 | AMR 7.4 - 7.4kbit/s'de kodlar |
|5 | AMR 7.95 - 7.95kbit/s'de kodlar |
|6 | AMR 10.2 - 10.2kbit/s'de kodlar |
|7 | AMR 12.2 - 12.2kbit/sn'de kodlar |

Bayt cinsinden (başlık baytı dahil) AMR modlarının çerçeve boyutu aşağıda verilmiştir:

|CMR |MOD |ÇERÇEVE BOYUTU( bayt cinsinden )|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7,95 |21|

## Referanslar ##

* [Uyarlanabilir Çoklu Hız ses codec'i - Wikipedia'dan](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [AMR ve AMR-WB Ses codec'leri için RTP Yük Biçimi ve Dosya Depolama Biçimi](https://tools.ietf.org/html/rfc4867#page-35)

