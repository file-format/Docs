{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "FMW Dosyası - FME Workbench Dosya Formatı",
  "description":"FMW dosya formatı ve FMW dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "FMW",
  "menu" : {
    "docs" : {
      "identifier":"gis-fmw-tr",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## FMW dosyası nedir?

FMW dosyası, uzamsal veri dönüşümü için kullanılan FME Workbench yazılımı (FME Masaüstü paketinin bir parçası olarak gelir) ile oluşturulan bir proje dosyasıdır. Giriş veri setleri, çeviri özellikleri, projeksiyonlar ve çıkış ayarları gibi uzamsal veri manipülasyonu için kullanılan kullanıcı tanımlı ayarları içerir. Uzamsal veri işleme ayarları görsel bir düzen olarak saklanır ve düzenlenmesi ve yeniden kaydedilmesi kolaydır.

FMW dosyalarını [Safe Software FME Desktop](https://fme.safe.com/platform/) kullanarak açabilirsiniz.

## FMW Dosya Formatı - Daha Fazla Bilgi

FMW dosyaları diskte ikili dosyalar olarak saklanır ve yalnızca FME Masaüstü yazılımı kullanılarak okunabilir. Yazılım ayrıca bir dizi ilişkisel veritabanı formatındaki verileri okuyabilir ve ayrıca bir dizi veri formatını da destekler.

### FMW Kısa Bilgiler

|Gerçek|Değer|
---|---|
|Okuyucu/Yazar|Okuyucu|
|Lisanslama Düzeyi|Temel|
|Bağımlılıklar|Yok|
|Veri Kümesi Türü|Dosya|
|Özellik Türü|Sabit|
|Tipik Dosya Uzantıları|.fmw|
|Otomatik Çeviri Desteği|Evet|
|Kullanıcı Tanımlı Özellikler|Hayır|
|Koordinat Sistemi Desteği|Hayır|
|Genel Renk Desteği|Hayır|
|Uzaysal İndeks|Hayır|
|Şema Gerekli|Hayır|
|İşlem Desteği|Hayır|
|Geometri Türü Özniteliği|Yok|
|Kodlama Desteği|Hayır|

### FMW Geometri Desteği

|Geometri|Destekleniyor mu?|
---|---|
|toplam|hayır|
|daireler|hayır|
|dairesel yay|hayır|
|çörek çokgen|hayır|
|eliptik yay|hayır|
|elipsler|hayır|
|satır|hayır|
|yok|evet|
|nokta|hayır|
|çokgen|hayır|
|raster|hayır|
|katı|hayır|
|yüzey|hayır|
|metin|hayır|
|z değerleri|hayır|


## Referanslar

* [Güvenli Yazılım FME Masaüstü](https://fme.safe.com/platform/)
* [FMW Quick Facts](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_ReadersWriters/fmw/quick_facts_fmw.htm)
