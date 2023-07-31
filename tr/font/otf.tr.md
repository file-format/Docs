{
  "date" : "2020-08-20",
  "keywords" :[ "otf dosyası", "otf dosya biçimi", "otf dosyası nedir", "dosya", "otf örneği", "otf dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - TrueType Yazı Tipi Dosya Biçimi",
  "description":"OTF dosya formatı ve OTF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## OTF dosyası nedir?

.otf uzantılı bir dosya, OpenType yazı tipi biçimini ifade eder. OTF yazı tipi biçimi daha ölçeklenebilirdir ve dijital tipografi için [TTF](/tr/font/ttf/) biçimlerinin mevcut özelliklerini genişletir. Microsoft ve Adobe tarafından geliştirilen OTF, PostScript ve TrueType yazı tipi biçimlerinin özelliklerini birleştirir. Bu, OTF biçimini çoğunluk yazma sistemlerini barındırmak için yapar ve bu nedenle büyük bilgisayar platformlarında tek tip olarak kullanılır. OpenType yazı tipi formatı, Mac OS X ve Windows 2000 ve sonrası tarafından desteklenir.

## Kısa Tarihçe

OpenType yazı tiplerinin gerekliliği, ince tipografiyi işleyebilecek daha anlamlı bir yazı tipi formatı için bir gereklilik olarak ortaya çıktı. Ayrıca dünyadaki birçok yazı sisteminin karmaşık davranış gereksinimlerini karşılaması amaçlandı. Microsoft, 1990'ların başında Apple'ın GX Tipografi olarak bilinen gelişmiş tipografi teknolojisini lisanslamaya çalıştı. Bu pek iyi gitmedi ve sonuç olarak Microsoft, 1994 yılında kendi TrueType yazı tipi teknolojisini geliştirmeye başladı. Adobe'nin Tip 1 (PostScript) yazı tipi biçimlerinin özelliklerini de karşılayan daha uygun bir yazı tipi biçimini tanıtmak için değişiklikler de dahil edildi.

Adobe, 1996'da, hem Apple'ın TrueType hem de kendi Tip 1 yazı tipi biçimlerinin yerini alma çabalarında Microsoft'a katıldı. Bu, sınırlamaların üstesinden gelmek ve yeni uzantılar eklemek için her iki temel yazı tipi biçiminin birleşimiyle sonuçlandı. Bu yeni teknoloji aynı yıl **OpenType** adıyla tanıtıldı.

## OTF Dosya Biçimi Özellikleri

OTF spesifikasyonları, Microsoft tarafından genel olarak mevcuttur ve geliştiricinin bakış açısından atıfta bulunulabilir. TTF gibi, aynı 'sfnt' kapsayıcı yapısını kullanır ve TrueType belirtimleriyle uyumludur. Bir OpenType yazı tipi dosyasının içindeki veriler, metin düzenini hesaplama, glifleri TrueType veya Kompakt Yazı Tipi Biçimi (CFF) ana hatları olarak tanımlama, alternatif glif açıklamaları olarak tek renkli veya renkli bit eşlemler veya SVG belgeleri sağlama ve meta veri bilgileri gibi farklı amaçlar için kullanılır.

### OTF Veri Türleri
OTF dosyaları, tümü Big Endian'da bulunan aşağıdaki veri türlerini kullanır.

|Veri Türü| Açıklama|
---|---|
|uint8| 8-bit işaretsiz tamsayı.|
|int8| 8-bit işaretli tamsayı.|
|uint16| 16-bit işaretsiz tamsayı.|
|int16| 16-bit işaretli tamsayı.|
|uint24| 24-bit işaretsiz tamsayı.|
|uint32| 32-bit işaretsiz tamsayı.|
|int32| 32-bit işaretli tamsayı.|
|Sabit| 32-bit imzalı sabit noktalı sayı (16.16)|
|ÖN SÖZCÜK| yazı tipi tasarım birimlerinde bir miktarı açıklayan int16.|
|UFKELİME| yazı tipi tasarım birimlerinde bir miktarı açıklayan uint16.|
|F2DOT14| Düşük 14 bitlik kesir (2.14) ile 16-bit işaretli sabit sayı.|
|UZUN TARİH SÜRESİ| Tarih ve saat, 1 Ocak 1904, UTC, 12:00 gece yarısından bu yana saniye olarak gösterilir. Değer, işaretli 64 bitlik bir tamsayı olarak temsil edilir.|
|Etiket| Bir tabloyu, tasarım varyasyon eksenini, komut dosyasını, dil sistemini, özelliği veya temel çizgiyi tanımlamak için kullanılan dört uint8 dizisi (uzunluk = 32 bit)|
|Ofset16| uint16 ile aynı, NULL ofset = 0x0000|
|Ofset32| Bir tabloya uzun uzaklık, uint32 ile aynı, NULL uzaklık = 0x00000000|
|Sürüm16Nokta16| Ana ve küçük sürüm numaralarıyla paketlenmiş 32 bitlik değer. (Bkz. Versiyon Numaraları Tablosu.)|

### OTF Tabloları Dizini

Bir OTF dosyası bir tablo dizini ile başlar. Bu dizin, yazı tipi dosyasındaki tabloların en üst düzey koleksiyonudur. Bir dosyadaki yazı tipi sayısına bağlı olarak, tablo dizini dosyanın farklı yerlerinde bulunabilir. Örneğin, yazı tipi dosyasının yalnızca bir yazı tipi olması durumunda, tablo dizini dosyanın bayt 0'ında başlar. Birden çok OpenType Yazı Tipi koleksiyonu olması durumunda,
tablo dizini başlangıcı TTHeader'da belirtilir.

|Tür |Ad |Açıklama|
---|---|---|
|uint32 |sfntSürüm| 0x00010000 veya 0x4F54544F ('OTTO')|
|uint16| numTables |Tablo sayısı.|
|uint16| searchRange |2'nin maksimum kuvveti numTables'tan küçük veya eşittir, çarpı 16 ((2\**floor(log2(numTables))) * 16, burada “**” bir üs operatörüdür).|
|uint16 |entrySelector Log2 maksimum gücü 2 olan numTables'den (log2(searchRange/16) eşit veya daha az, bu da floor(log2(numTables)))'a eşittir.|
|uint16 |rangeShift |numTables çarpı 16, eksi searchRange ((numTables * 16) - searchRange).|
|tablo Kaydı| tableRecords[numTables] |Tablo kayıtları dizisi—yazı tipindeki her üst düzey tablo için bir tane|


### Tablo Kaydı

Fonttaki her üst düzey tablo için aşağıdaki alanlardan oluşan bir Tablo Kaydı vardır.

|Tür| Ad| Açıklama|
---|---|---|
|Etiket| tabloEtiket| Tablo tanımlayıcı.|
|uint32| sağlama toplamı| Bu tablo için sağlama toplamı.|
|Ofset32| ofset| Yazı tipi dosyasının başından itibaren ofset.|
|uint32| uzunluk Bu tablonun uzunluğu.|

OpenType yazı tipi dosyasındaki her tablo, tablo etiketleri olarak bilinen adlarla temsil edilir. Dizideki tüm kayıtların etikete göre artan sırada sıralanması zorunludur.

## Referanslar
* [Microsoft'tan OpenType Yazı Tipi Özellikleri](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [TrueType'a Genel Bakış](https://learn.microsoft.com/en-us/typography/truetype/)

