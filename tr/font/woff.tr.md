{
  "date" : "2020-08-20",
  "keywords" :[ "woff dosyası", "woff dosya biçimi", "woff dosyası nedir", "dosya", "woff örneği", "woff dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Web Açık Dosya Biçimi",
  "description":"Bir WOFF dosyası, Web Açık Yazı Tipi Biçiminde oluşturulan açık bir yazı tipi biçimidir.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## .woff dosyası nedir?

.woff uzantılı bir dosya, Web Açık Yazı Tipi Formatına (WOFF) dayalı bir web yazı tipi dosyasıdır. TrueType (.TTF) veya OpenType (.OTT) yazı tipi türlerine dayalı biçime özel sıkıştırılmış kapsayıcıya sahiptir. WOFF, web yazı tiplerini masaüstü uygulamalarında kullanılan yazı tipi dosyalarından ayırmak amacıyla tanıtıldı. Ayrıca format, ağ üzerinden sunucudan istemcinin bilgisayarına yazı tiplerinin aktarımındaki gecikmeyi azaltmayı hedefledi. WOFF dosyalarını TTF'ye ve diğer yazı tipi dosyası biçimlerine dönüştürebilen çeşitli araçlar mevcuttur.

## **WOFF Dosya Biçimi**

WOFF yazı tipi formatı, TrueType, OpenType ve Open Yazı Tipi Formatı gibi farklı yazı tipi türlerinde kullanılan tablo tabanlı sfnt yapılarının yazı tipi veri tablolarını sıkıştırır. Bu yazı tipi türleri için bir kap gibidir ve ayrıca kapsayıcıya dahil edilecek yazı tipinin meta verilerini ve özel kullanım verilerini dahil etme odasına sahiptir. Dönüştürücüler, sfnt dosyalarını WOFF formatlı bir dosyaya kullanır ve kullanıcı aracıları, web belgesiyle kullanım için kodlanmış dosyayı geri yükler. Geri yüklenen yazı tipi verilerinin, tüm yönlerden giriş yazı tipi formatıyla tam olarak eşleştiğine dikkat edilmelidir.

WOFF dosyası Yardımcı programları genellikle glif alt kümesi, doğrulama veya yazı tipi özelliği eklemeleri gibi ek özellikler içerir, ancak bu gerekli değildir. Hem oluşturan hem de kullanan aracılar, altta yatan yazı tipi verilerinin geçerliliğinin korunmasını sağlamalıdır.

### WOFF Dosya Yapısı

WOFF dosya yapısı, sfnt yazı tiplerine benzer. Her yazı tipi veri tablosunun uzunluklarını ve uzaklıklarını içeren bir tablo dizinine dayanır. Bu ön bilgiden sonra tüm tablolar takip edilir. Dosya, orijinal yazı tipleriyle aynı olan yazı tipi veritabanını içerir. Tabloların sırası da aynıdır ancak her biri sıkıştırılabilir. WOFF tablo dizini, orijinal tablo dizininin yerini alır.

Bir WOFF dosyası aşağıdakilerden oluşur:

* WOFFHeader - Meta veriler ve özel veri blokları için ofsetlerle birlikte temel yazı tipi ve sürümüne sahip dosya başlığı.
* TableDirectory - WOFF dosyasındaki her tablonun orijinal boyutunu, sıkıştırılmış boyutunu ve konumunu gösteren yazı tipi tabloları dizini.
* FontTables - Giriş sfnt yazı tipinden gelen yazı tipi veri tabloları, bant genişliği gereksinimlerini azaltmak için sıkıştırılmıştır.
* ExtendedMetadata - XML biçiminde temsil edilen ve WOFF dosyasında depolamak için sıkıştırılmış, isteğe bağlı bir genişletilmiş meta veri bloğu.
* PrivateData- Yazı tipi tasarımcısı, dökümhane veya satıcının kullanması için isteğe bağlı bir özel veri bloğu.

### WOFF Başlığı
WOFF başlığı, dosyada bulunan veri türünü gösteren tanımlayıcı bir imzadan oluşur. Alanlarıyla birlikte WOFF başlığı aşağıdaki gibidir.

|Tür|Alan Adı|Açıklama|
---|---|---|
|UInt32|imza |0x774F4646 'wOFF' |
|UInt32| lezzet |Giriş yazı tipinin "sfnt versiyonu".|
|UInt32| uzunluk |WOFF dosyasının toplam boyutu.|
|UInt16| numTables |Yazı tipi tabloları dizinindeki giriş sayısı.|
|UInt16| ayrılmış |Ayrılmış; sıfıra ayarla.|
|UInt32| totalSfntSize |Sfnt başlığı, dizin ve yazı tipi tabloları (doldurma dahil) dahil olmak üzere sıkıştırılmamış yazı tipi verileri için gereken toplam boyut.|
|UInt16| majorVersion |WOFF dosyasının ana sürümü.|
|UInt16| minorVersion |WOFF dosyasının küçük versiyonu.|
|UInt32| metaOffset |WOFF dosyasının başından itibaren metadata bloğuna ofset.|
|UInt32| metaLength |Sıkıştırılmış meta veri bloğunun uzunluğu.|
|UInt32| metaOrigLength |Meta veri bloğunun sıkıştırılmamış boyutu.|
|UInt32| privOffset |WOFF dosyasının başından itibaren özel veri bloğuna ofset.|
|UInt32| privLength |Özel veri bloğunun uzunluğu.|


## **Referanslar**
* [w3 WOFF Dosya Biçimi](https://www.w3.org/TR/WOFF/)

