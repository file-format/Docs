{
  "date" : "2021-08-09",
  "keywords" :[ "cso dosyası", "cso dosya biçimi", "cso dosyası nedir", "dosya", "cso örneği", "cso dosya uzantısı","uzantı", "biçim", "iso", "DAX sıkıştırması "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"CSO dosya formatı ve CSO dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"CSO - Sıkıştırılmış ISO Disk Görüntüsü",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## .cso dosyası nedir?

.cso uzantılı bir dosya, sıkıştırılmış bir ISO görüntü dosyasıdır. CSO, DAX sıkıştırma yöntemine bir alternatiftir; CISO olarak da bilinir; [ISO](/tr/compression/iso/) dosyalarını sıkıştırmak için ilk yöntemdi ve genellikle PlayStation Portable öğelerini arşivlemek için tercih edilen bir yöntemdir. Bu biçim, dokuz adede kadar sıkıştırma katmanı içerebilen Söndürme sıkıştırmasını kullanır. Görüntüleri oluşturmak için Prometheus ve YACC gibi yazılımlar kullanılır.

## CSO dosya formatı

CSO dosya biçimi, daha fazla bellek alanı kazanmak için ISO için ilk sıkıştırma yöntemiydi. Geliştirmeler, daha iyi sıkıştırma için zaman zaman yapılmıştır. CSO, dokuz ön ayar seviyesine sahip Söndürme sıkıştırmasını kullanıyor, genellikle her seviye 2 KiB bloğunu ayrı ayrı işleyebilir. En yüksek sıkıştırma seviyeleri, büyük ölçüde disk akışına bağlı olan yazılımlarda yükleme sürelerini yavaşlatabilir ve uzatabilirken, daha düşük seviyeler de önemli sıkıştırma gerçekleştirebilir.

### CSO dosya yapısı

CSO dosya biçimi 24 baytlık bir başlık, veri blokları ve bir dizin tablosu içerir. Little-endian, bir bayttan büyük alanlar için varsayılır. PlayStation Portable'ın mimari özellikleri aşağıda verilmiştir.

#### Başlık

| Ofset (bayt) | Ad | Boyut (bayt) | amaç |
----------|----------|--------------|---------|
| 0x0 | Büyü | 4 | 32 bit tamsayı olarak okunduğunda her zaman CISO veya 0x4F534943. Bu alan bir CSO dosyasını tanımlamak için kullanılır. Bu alanın CSO'nun diğer türevleri için farklı olabileceğini unutmayın, örneğin ZSO, ZISO sihirli kodunu kullandı. |
| 0x4 | Başlık boyutu | 4 | Orijinal CSO "v1" dosya biçimi için bu alan yoksayılır ve bu nedenle doğru olması gerekmez. Ancak "v2" ve ZSO biçimi, bu alanın her zaman 0x18 (24 bayt) olmasını gerektirir. |
| 0x8 | Sıkıştırılmamış boyut | 8 | Orijinal sıkıştırılmamış ISO'nun bayt cinsinden boyutu. |
| 0x10 | blok boyutu | 4 | Sıkıştırmadan önce her veri bloğunun bayt cinsinden boyutu. Genellikle 2048 bayt, her bir ISO 9660 sektörünün boyutuyla aynı. |
| 0x14 | Sürüm | 1 | Kullanılan dosya biçiminin sürümü. "v1" biçimi için değer 0 veya 1 olabilir. "v2" biçimi için bu 2 olmalıdır. Ayrıca, ZSO biçimi bunun 1 olmasını gerektirir. |
| 0x15 | Dizin hizalaması | 1 | Bit cinsinden belirtilen her bir dizin girişinin hizalaması. |
| 0x16 | Ayrılmış | 2 | Bu alan kullanılmamaktadır. "v1" biçiminde bu alan yoksayılır ve isteğe bağlı değerler içerebilir. "v2" formatında bu alan sıfır olmalıdır. |

#### Dizin tablosu

İndeks tablosu, her veri bloğunun konumunu gösteren birkaç 4 baytlık giriş ve dosyanın sonunu gösteren ek, son bir giriş içerir.
Her girişin içeriği aşağıdaki gibidir:
| Bit | Uzunluk | Maske | İsim | amaç |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFFF | pozisyon | Bu alan, başlıkta verilen indeks hizalaması ile sola kaydırıldığında veri bloğunun başladığı konumu verir. |
| 31 | 1 | 0x80000000 | Sıkıştırma türü | ZSO biçimi benzer semantiklere sahiptir, yalnızca 0, Söndür yerine LZ4'ü temsil eder. "v2" formatında. Blok boyutu, dosya başlığında belirtilen blok boyutuna eşit veya daha büyükse, blok dolaylı olarak sıkıştırılmamış olarak kabul edilir. |

#### Veri blokları

Veri blokları, sıkıştırılmamış veya sıkıştırılmış verilerden oluşur. Bir bloğun boyutu, konumu alınarak ve sonraki bloğun konumundan çıkarılarak hesaplanır. Dizin hizalaması sıfırdan büyükse, blok boyutunun tuttuğu verilerden büyük olması muhtemeldir.


## Referanslar

* [CSO - Wikipedia'dan](https://en.wikipedia.org/wiki/.CSO)


