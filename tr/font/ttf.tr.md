{
  "date" : "2020-08-20",
  "keywords" :[ "ttf dosyası", "ttf dosya formatı", "ttf dosyası nedir", "dosya", "ttf örneği", "ttf dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - TrueType Yazı Tipi Dosya Biçimi",
  "description":"TrueType yazı tipleri (TTF), başlangıçta Apple, Inc. tarafından tasarlanan dijital yazı tipi teknolojisi özelliklerine dayanmaktadır. Hem Apple hem de Microsoft, Mac ve Windows İşletim sistemlerinde TTF kullanmıştır.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## .tf dosyası nedir?

.ttf uzantılı bir dosya, TrueType belirtimleri yazı tipi teknolojisine dayalı yazı tipi dosyalarını temsil eder. Başlangıçta Apple Computer, Inc. tarafından Mac OS için tasarlanmış ve başlatılmıştır ve daha sonra Microsoft tarafından Windows OS için benimsenmiştir. TrueType yazı tipleri, bilgisayar ekranlarında ve yazıcılarda çözünürlüğe bağlı olmaksızın en yüksek kalitede görüntü sağlar. Yazı tiplerini kullanan tüm modern uygulamalar, TTF dosyalarıyla çalışabilir. TTF yazı tipi dosyaları internet üzerinden ücretsiz olarak temin edilebilir ve ayrıca OTF ve WOFF gibi diğer yazı tipi dosya biçimlerine dönüştürülebilir.

## Kısa Tarihçe

1980'lerde Apply Computer, Inc tarafından MacOS için tasarlanan TTF yazı tipi formatı, Adobe'nin Type 1 formatıyla bazı teknik sınırlamaları çözmeyi amaçlıyordu. Apple, 1991'de Mac'te TrueType yazı tiplerini desteklemeye başladı. TTF yazı tiplerinin arkasındaki tasarım hedefi, depolama ve işlemede verimlilik ve genişletilebilirlikti. Bu genişletilebilirliğe bağlı olarak, mevcut yazı tipleri TrueType biçimine dönüştürülebilir.

Microsoft, TrueType yazı tiplerini Windows 3.1'de ilk olarak Nisan 1992'de Apple'ın TrueType'ı Microsoft'a lisanslamayı kabul etmesinden sonra kullandı. Rasterleştirme mekanizmasını geliştirdi ve verimliliğini ve performansını iyileştirdi.

## True Type Dosya Biçimi Özellikleri

TrueType yazı tipi dosyası, bir dizi birleştirilmiş tablodan oluşan bir ikili dosyadır. Her tablo bir sözcük dizisidir ve "Etiket" olarak bilinen bir adı vardır. Her etiket uint32 veri tipindedir ve dört karakterden oluşur. Dosyadaki ilk tablo, yazı tipi dosyasındaki diğer tablolara erişim sağlayan yazı tipi dizini. Yazı tipi verileri, yazı tipi dizini tablosundan sonra gelen diğer tablolarda bulunur. Her tabloya kendi etiketiyle erişilebildiğinden, tablolar dosyada herhangi bir sırada görünebilir.

Gerekli tablolar ve etiket adları aşağıdaki tabloda gösterilmektedir.

|**Etiket**|**Tablo**|
---|---|
|'cmmap'| karakterden glif eşleme|
|'glif'| glif verileri|
|'kafa'| yazı başlığı |
|'hee'| yatay başlık|
|'hmtx'| yatay metrikler|
|'yer'| konum dizini|
|'maksimum'| maksimum profil|
|'isim'| adlandırma|
|'yayın'| PostScript|

### Veri tipleri
TrueType yazı tipleri, aşağıdaki tabloda listelenen standart tamsayı ve ek veri türlerini kullanır.

|**Veri Türü** | **Açıklama** |
---|---|
|kısaFrac| 16 bit işaretli kesir |
|Sabit| 16.16-bit işaretli sabit noktalı sayı|
|FKelime| em uzayda ölçülebilir en küçük mesafe olan FUnit cinsinden bir miktarı tanımlayan 16 bitlik işaretli tamsayı.|
|uFKelime| em uzayda ölçülebilir en küçük mesafe olan FUnit cinsinden bir miktarı tanımlayan 16 bitlik işaretsiz tamsayı.|
|F2Nokta14| Düşük 14 bit kesri temsil eden 16-bit işaretli sabit sayı.|
|uzunTarihZaman| 1 Ocak 1904, gece yarısı 12:00'den bu yana bir tarihin saniye cinsinden uzun dahili biçimi. İşaretli 64 bitlik bir tamsayı olarak temsil edilir.|

### Yazı Dizini

TrueType yazı tipindeki ilk tablo, diğer tablolardaki verilere erişmek için gerekli bilgilere erişimi sağlayan yazı dizinidir. Ayrıca şunlardan oluşur:

* 'Ofset alt tablosu' - yazı tipindeki tabloların kaydını tutar ve dizindeki her tabloya erişmek için ofset bilgileri sağlar
* `Tablo Dizini` - Yazı tipindeki her tablo için girişler içerir

#### Ofset Alt Tablosu
Ofset alt tablosu aşağıda gösterilmiştir.

|**Tür**|**Ad**|**Açıklama**|
---|---|---|
|uint32| ölçekleyici tipi| Bu yazı tipini rasterleştirmek için kullanılacak OFA ölçekleyiciyi belirten bir etiket; daha fazla bilgi için aşağıdaki ölçekleyici türüyle ilgili nota bakın.|
|uint16| sayıTablolar| masa sayısı|
|uint16| arama Aralığı| (maksimum güç 2 <= numTables)*16|
|uint16| giriş Seçici| log2(maksimum güç 2 <= numTables)|
|uint16| menzil Kaydırma| numTables*16-arama Aralığı|

#### Tablo dizini
Tablo dizini, ofset alt tablosundan hemen sonra gelir. Yapısı aşağıdaki tabloda gösterildiği gibidir.

|**Tür**|**Ad**|**Açıklama**|
---|---|---|
|uint32| etiket| 4 bayt tanımlayıcı|
|uint32| kontrol toplamı| bu tablo için sağlama toplamı|
|uint32| ofset| sfnt'nin başından itibaren uzaklık|
|uint32| uzunluk| bu tablonun bayt cinsinden uzunluğu (gerçek uzunluk dolgulu uzunluk değil)|

Font dosyasındaki her tablonun kendi tablo dizini girişi olmalıdır. Bir tablodaki girişler, etikete göre artan düzende sıralanmalıdır.


## Referanslar
* [TrueType Yazı Tipi Referans Kılavuzu](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [TrueType'a Genel Bakış](https://docs.microsoft.com/en-us/typography/truetype/)

