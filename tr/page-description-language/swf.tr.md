{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :[ "SWF", "dosya", "uzantı", "format", "video formatı", "SWF dosyası nedir", "swf dosya formatı", "swf dosya oynatıcısı", "swf dosyası nasıl açılır"] ,
  "title" :"SWF Dosyası - Shockwave Flash Film Dosyası Formatı",
  "description":"SWF dosyasının ne olduğunu ve oluşturabilen API'leri öğrenin ve SWF dosyasının nasıl açılacağını gösterin.",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## SWF dosyası nedir?

SWF dosyası, Adobe Flash ile oluşturulan bir animasyon dosyasıdır. Animasyonu oluşturmak için metin, vektör görüntüleri, raster görüntüler, actionscripts gibi farklı türde öğeler, daireler, çizgiler, kareler ve dikdörtgen gibi nesneler içerebilir. SWF dosyaları, bu multimedya öğelerini saniyede farklı karelerde (fps) oynatılabilen kareler halinde düzenler. SWF, Kısa Web Dosyası anlamına gelir ancak Shockwave Formatına sahip olduğu da bilinir.

*SWF dosyalarını açabilen** uygulamalar arasında Adobe Flash Player (artık üretilmiyor) ve Eltima Elmedia Player yer alıyor.

## SWF Dosya Biçimi - Daha Fazla Bilgi

SWF dosyaları, diske ikili dosyalar olarak saklanmak için kullanıldı. SWF dosya formatı, web sitelerine gömülebilen ve bağımsız olarak da oynanabilen animasyonlar ve oyunlar geliştirmek için kullanıldı. Ayrıca, geliştiricilere etkileşimli multimedya uygulamaları oluşturmak için birçok seçenek sunan videoları ve sesleri de destekledi. SWF dosyaları, Adobe Shockwave'in kurulu olduğu web tarayıcılarında oynatılabilir. Adobe Flash, eksiklikleri ve güvenlik sorunları nedeniyle Aralık 2020'de kullanımdan kaldırıldı.

## SWF Dosya Biçiminin Kısa Tarihi

SWF dosya formatı, orijinal olarak FutureWave Software tarafından, dosya boyutunu küçük tutarken, daha yavaş ağ bağlantılarına sahip herhangi bir sistemde bir oynatıcı yazılımında çalıştırma niyetiyle animasyonları görüntülemek üzere tasarlanmıştır. Aralık 1996'da Macromedia, FutureWave'in sahibi oldu ve Macromedia Flash 1.0'a dönüştürüldü.

2005'te Macromedia, 2008'de açık kaynak projesinin bir parçası olarak SWF'yi duyuran Adobe tarafından satın alındı. Aynı yıl içinde Adobe, SWF dosyalarının taranmasını ve dizine eklenmesini sağlamak için dünyanın popüler web motorlarına kod yayınladı. Bununla birlikte, SWF dosyaları internette Flash içeriği yayınlamak için standart bir biçim haline geldiği için, SWF, Küçük Web Biçimi anlamına gelecek şekilde revize edilmiştir.

## SWF Dosya Yapısı

Yol, basit çizgilerden Bezier eğrilerine kadar değişen temel öğelerin bölümleri dizisi olan SWF'deki temel grafik öğedir. Bu basit öğeler ayrıca küpler, elipsler ve hatta metinler gibi diğer ek ilkel öğeleri oluşturmaya yardımcı olur. SWF'deki grafik ilkel öğeler, SVG ve MPEG-4 BIFS gibi diğer biçimlerin grafik öğeleriyle benzerlik gösterir.

Biçim, görüntüleme listelerine ve önceden tanımlanmış öğelerin yeniden kullanılmasına/yeniden adlandırılmasına da izin verir. SWF'nin ikili akış formatı, etiket, boyut ve yük açısından benzer olan QuickTime atomlarıyla karşılaştırılabilir. İkili akış biçimi, eski oynatıcıların desteklenmeyen içerikleri atlamasına olanak tanır. SWF'nin orijinal sürümleri vektör grafikleri ve görüntüleri sunmakla sınırlı olsa da, bu nedenle yeni sürümler ses ve video içeriklerine de izin verir.

Flash Player'ın "Stage3D" adlı yeni, düşük seviyeli bir 3D API'si sürüm 11'de tanıtıldı. Bu API'nin OpenGL veya Direct3D'nin muadili olduğu tasavvur edildi. Stage3D, renkleri Adobe Graphics Assembly Language (AGAL) adı verilen düşük seviyeli bir dilde tanımlar. Aşağıda, SWF dosya biçiminin birkaç temel veri türü bulunmaktadır.

### Koordinatlar

SWF dosya biçimindeki XY koordinatları, tamsayılar olarak saklanır ve twip adı verilen bir birimde ölçülür. Bir twip, mantıksal pikselin 1/20'sinden oluşur. Dosya %100'de ölçeklenmeden oynatıldığında mantıksal piksel ve ekran pikseli aynıdır.

### Tamsayı Türleri ve Bayt Sırası

SWF dosya biçiminde 8, 16, 32 ve 64 bitlik işaretli ve işaretsiz tamsayı türlerine izin verilir. Little-endian bayt sırası, tamsayı değerleri depolamak için kullanılır. Bayt içinde olsa da, bit sırası big-endian'da saklanır. Tüm tamsayı değerleri bayt hizalı olmalıdır. İşaretli tamsayılar, geleneksel 2'nin -tümleyen bit kalıpları kullanılarak temsil edilir.

### Sabit Noktalı Sayılar

SWF dosya biçimi tarafından iki tür sabit noktalı sayı desteklenir, yani 32 ve 16 bit.

### Kayan nokta sayıları

SWF 8 ve sonraki sürüm, kayan nokta türlerinin IEEE Standardı 754 ile uyumlu olan üç tür kayan noktalı sayı (FLOAT, FLOAT 16, DOUBLE) kullanır.

### Kodlanmış Tam Sayılar

Bir tür kodlanmış tamsayı, değişken bayt sayısıyla SWF 9 ve sonraki sürümleri tarafından desteklenir.

## Referanslar

* [SWF dosya biçimi](https://en.wikipedia.org/wiki/Swf)

