{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"NSF dosya formatı ve NSF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"NSF Dosya Biçimi - Lotus Notes Veritabanı Biçimi",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Bir NSF dosyası nedir?

.nsf (Notes Storage Facility) uzantılı bir dosya, daha önce Lotus Notes olarak bilinen [IBM Notes yazılımı](https://en.wikipedia.org/wiki/HCL_Domino) tarafından kullanılan bir veritabanı dosyası biçimidir. E-postalar, randevular, belgeler, formlar ve görünümler gibi farklı türden nesneleri depolamak için şemayı tanımlar. Tüm bu bilgiler, bir PST/OST dosyasına benzer şekilde ticari işbirliği için tek bir NSF dosyasında bulunur. NSF dosyalarını açabilen uygulamalardan bazıları IBM Lotus Notes ve IBM Domino'dur.

## NSF Dosya Biçimi Özellikleri

NSF dosyaları ikili yapıdadır ve özellikleri Joachim Metz tarafından [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database% adresinde mevcuttur) 20file%20format.asciidoc). Bu ayrıntılara göre, bir NSF dosyası aşağıdakilerden oluşur:

* Dosya Başlığı
* Veritabanı Başlığı

Ayrıca şunlardan oluşur:

* Süper blok
* Kova tanımlayıcı bloğu
* Bit eşlem
* Kayıt Relokasyon Vektörü kovası
* Özet kovaları
* Özet olmayan bölümler


### NSF Dosya Başlığı

NSF dosya başlığı, 6 bayt boyutundadır. Bu oluşmaktadır:

|Ofset|Boyut|Değer|Açıklama|
---|---|---|---|
0|2|0x1a 0x00|İmza|
2|4| |Veritabanı başlık boyutu|

### Veritabanı başlığı

NSD Veritabanı başlığı aşağıdaki onaylanmış değerleri içerir.

* Veritabanı Bilgileri
* Veritabanı tanımlayıcısı (DBID)
* Çoğaltma bilgileri
* Veritabanı bilgileri tampon bayrakları
* Başlık
* Kategoriler
* Sınıf
* Tasarım sınıfı (şablon adı)
* Özel not tanımlayıcıları
* Dolgu malzemesi
* Veritabanı bilgisi 2
* Veritabanı bilgisi 3
* Veritabanı bilgisi 4
* Veritabanı bilgisi 5
* Dolgu malzemesi
* Veritabanı örneği tanımlayıcısı (DBIID)
* Çoğaltma geçmişi

## Referanslar

* [NSF Biçimi - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

