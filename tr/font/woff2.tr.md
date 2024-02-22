{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF2 Dosyası - Web Açık Yazı Tipi Formatı 2.0 Dosyası",
  "description": "WOFF2 dosyasının ne olduğunu ve WOFF2 dosyasını oluşturup açabilen API'leri öğrenin.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-tr2"
}
},
  "lastmod": "2023-01-10"
}

## WOFF2 dosyası nedir?

WOFF2, Web Açık Yazı Tipi Formatının (WOFF) daha sıkıştırılmış bir versiyonu olan bir yazı tipi dosyası formatıdır. Web yazı tiplerinin dosya boyutunu küçülterek bunların daha hızlı yüklenmesini ve daha az bant genişliği kullanmasını sağlamak için geliştirildi. WOFF2, yazı tipi verilerini sıkıştırmak için Brotli adı verilen bir sıkıştırma algoritması kullanır; bu, dosya boyutlarının eşdeğer [WOFF](/font/woff/) yazı tiplerinden önemli ölçüde daha küçük olmasına neden olabilir. Bu biçim, Chrome, Firefox, Safari, Opera ve Edge (sürüm 14'ten itibaren) dahil olmak üzere çoğu modern web tarayıcısı tarafından desteklenir.

## WOFF2 Dosya Formatı - Daha Fazla Bilgi

WOFF2 yazı tipi dosyasının dahili dosya yapısı, başlık, meta veriler, tablo dizini ve yazı tipi verilerinin kendisi de dahil olmak üzere birkaç farklı bölümden oluşur.

 1. Başlık, sürüm numarası ve dosyada bulunan tabloların sayısı da dahil olmak üzere dosyanın genel formatı hakkında bilgi içerir.

 1. Meta veriler bölümü yazı tipi adı, telif hakkı ve yazı tipiyle ilgili diğer bilgiler gibi bilgileri içerir.

 1. Tablo dizini, yazı tipini oluşturan farklı tablolar hakkında, dosyadaki konumları ve uzunlukları da dahil olmak üzere bilgiler içerir.

 1. Yazı tipi verilerinin kendisi, her biri yazı tipi hakkında karakterler ve bunlara karşılık gelen glifler gibi belirli bilgileri içeren birkaç farklı tabloya bölünmüştür. Bu tablolar şunları içerebilir:

 * Glyf' tablosu, her karakterin şekli ve boyutu da dahil olmak üzere gerçek yazı tipi ana hatlarını içerir.
 * Başlık' tablosu yazı tipi hakkında sürüm numarası, tasarım boyutu vb. gibi genel bilgileri içerir.
 * Hmtx' tablosu, karakterlerin genişlikleri ve konumları da dahil olmak üzere yazı tipinin ölçümleri hakkında bilgi içerir.
 * Her tablo, kodlama işlemi tamamlandıktan sonra sıkıştırılır ve WOFF2 dosya formatında saklanır.

Genel olarak yapı, hızlı ayrıştırma ve kod çözmeye izin verecek şekilde tasarlanmıştır; böylece web tarayıcıları, yazı tipini hızlı ve verimli bir şekilde yükleyebilir ve bir web sitesinde görüntüleyebilir.

### WOFF2 Başlığı
WOFF başlığı, dosyada yer alan veri türünü belirten tanımlayıcı bir imzadan oluşur. WOFF başlığı alanlarıyla birlikte aşağıdaki gibidir.

|Tür|Alan Adı|Açıklama|
---|---|---|
|UInt32|imza |0x774F4632 'wOF2' |
|UInt32| lezzet |Giriş yazı tipinin sfnt sürümü.|
|UInt32| uzunluk |WOFF dosyasının toplam boyutu.|
|UInt16| numTables |Yazı tipi tabloları dizinindeki girişlerin sayısı.|
|UInt16| ayrılmış |Ayrılmış; sıfıra ayarlandı.|
|UInt32| totalSfntSize |Sfnt başlığı, dizin ve yazı tipi tabloları (dolgu dahil) dahil olmak üzere sıkıştırılmamış yazı tipi verileri için gereken toplam boyut.|
|UInt32| totalCompressedSize Sıkıştırılmış veri bloğunun toplam uzunluğu.|
|UInt16| majorVersion |WOFF dosyasının ana sürümü.|
|UInt16| minörVersiyon |WOFF dosyasının küçük versiyonu.|
|UInt32| metaOffset |WOFF dosyasının başlangıcından meta veri bloğuna uzaklık.|
|UInt32| metaLength |Sıkıştırılmış meta veri bloğunun uzunluğu.|
|UInt32| metaOrigLength |Meta veri bloğunun sıkıştırılmamış boyutu.|
|UInt32| privOffset |WOFF dosyasının başından itibaren özel veri bloğuna ofset.|
|UInt32| privLength |Özel veri bloğunun uzunluğu.|


## Referanslar
 * [w3 WOFF2 Dosya Formatı](https://www.w3.org/TR/WOFF2/)

