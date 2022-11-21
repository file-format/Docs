{
  "date" : "2019-11-25",
  "keywords" :[ "jpeg dosyası", "jpeg dosya biçimi", "jpeg dosyası nedir", "dosya", "jpeg örneği", "jpeg dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - Görüntü Dosyası Biçimi",
  "description":"JPEG dosya formatı ve JPEG dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## JPEG dosyası nedir? ##

JPEG, kayıplı sıkıştırma yöntemi kullanılarak kaydedilen bir görüntü biçimi türüdür. Çıktı görüntüsü, sıkıştırmanın bir sonucu olarak, depolama boyutu ile görüntü kalitesi arasında bir değiş tokuştur. Kullanıcılar, depolama boyutunu küçültürken aynı zamanda istenen kalite düzeyine ulaşmak için sıkıştırma düzeyini ayarlayabilir. Görüntüye 10:1 sıkıştırma uygulanırsa görüntü kalitesi ihmal edilebilir düzeyde etkilenir. Sıkıştırma değeri ne kadar yüksek olursa, görüntü kalitesindeki bozulma da o kadar yüksek olur.

## Dosya Biçimi Özellikleri ##

JPEG görüntü dosyası formatı, Ortak Fotoğraf Uzmanları Grubu ve dolayısıyla JPEG adı tarafından standartlaştırıldı. Biçim, fotoğrafik görüntülerin web üzerinde saklanması ve iletilmesi seçimi olmuştur. Hemen hemen tüm İşletim sistemlerinde artık, genellikle JPG uzantısıyla da depolanan JPEG görüntülerin görselleştirilmesini destekleyen görüntüleyiciler var. Web tarayıcıları bile JPEG görüntülerin görselleştirilmesini destekler. JPEG dosya formatı özelliklerine girmeden önce, JPEG oluşturmada yer alan adımların genel sürecinden bahsetmek gerekir.

### JPEG Sıkıştırma Adımları ###

**Dönüşüm:** Renkli görüntüler RGB'den bir parlaklık/renkli görüntüye dönüştürülür (Göz renkliliğe değil parlaklığa duyarlıdır, bu nedenle renkli kısım çok fazla veri kaybedebilir ve bu nedenle yüksek oranda sıkıştırılabilir.

**Aşağı Örnekleme:** Aşağı örnekleme, renkli bileşen için yapılır, parlaklık bileşeni için yapılmaz. Aşağı örnekleme, yatay olarak 2:1 ve dikey olarak 1:1 oranında (2h 1 V) yapılır. Böylece 'y' bileşenine dokunulmadığı için görüntünün boyutu küçülür, görüntü kalitesinde gözle görülür bir kayıp olmaz.

**Gruplarda Düzenleme:** Satır veya sütun sayısı 8'in katı değilse, her bir renk bileşeninin pikselleri “veri birimleri” adı verilen 8×2 piksellik gruplar halinde düzenlenir, en alttaki satır ve en sağdaki sütunlar çoğaltılır.

**Ayrık Kosinüs Dönüşümü:** Daha sonra dönüştürülmüş bileşenlerin 8×8 haritasını oluşturmak için her veri birimine Ayrık Kosinüs Dönüşümü (DCT) uygulanır. DCT, bilgisayar aritmetiğinin sınırlı kesinliği nedeniyle bir miktar bilgi kaybına neden olur. Bu, harita olmasa bile görüntü kalitesinde bir miktar kayıp olacağı, ancak normalde küçük olduğu anlamına gelir.

**Kuantizasyon:** Veri birimindeki dönüştürülmüş 64 bileşenin her biri, "Kuantizasyon Katsayısı (QC)" adı verilen ayrı bir sayıya bölünür ve ardından bir tamsayıya yuvarlanır. Bilginin geri alınamayacak şekilde kaybolduğu yer burasıdır, Büyük KK daha fazla kayba neden olur. Genel olarak, çoğu JPEG uygulaması, JPEG standardı tarafından önerilen QC tablolarının kullanılmasına izin verir.

**Kodlama:** Her bir veri biriminin 64 nicelleştirilmiş dönüştürülmüş katsayıları (artık tam sayılardır), RLE ve Huffman kodlamasının bir kombinasyonu kullanılarak kodlanır.

**Başlık Ekleme:** Son adım, başlığı ve kullanılan tüm JPEG parametrelerini ekler ve sonucu verir.

JPEG kod çözücü, sıkıştırılmış görüntüden orijinal görüntüyü oluşturmak için ters adımları kullanır.

### Dosya Yapısı ###

Bir JPEG görüntüsü, her bölümün bir işaretleyici ile başladığı bir dizi bölüm olarak temsil edilir. Her işaretçi, 0xFF baytı ile başlar ve ardından işaretçinin türünü temsil eden işaretçi bayrağı gelir. İşaretçi tarafından takip edilen yük, işaretçi türüne göre farklıdır. Yaygın JPEG işaretleyici türleri aşağıda listelenmiştir:

|Kısa Ad|Bayt|Yük|Ad|Yorumlar
---|---|---|---|---|
|SOI|0xFF, 0xD8|yok|Görüntünün Başlangıcı|
|S0F0|0xFF, 0xC0|değişken boyut|Çerçevenin Başlangıcı|
|S0F2|0xFF, 0xC2|değişken boyut|Çerçeve için Başlangıç|
|DHT|0xFF, 0xC4|değişken boyut|Huffman Tablolarını Tanımlayın|
|DQT|0xFF, 0xDB|değişken boyut|Kuantizasyon Tablolarını Tanımlayın|
|DRI|0xFF, 0xDD|4 bayt|Yeniden Başlatma Aralığını Tanımla|
|SOS|0xFF, 0xDA|değişken boyut|Taramanın Başlangıcı|
|RSTn|0xFF, 0xD//n//(/tr//n//#0..7)|yok|Yeniden Başlat|
|APPn|0xFF, 0xE//n//|değişken boyut|Uygulamaya özel|
|COM|0xFF, 0xFE|değişken boyut|Yorum|
|EOI|0xFF, 0xD9|yok|Görüntünün Sonu|

Entropi kodlu verilerde, herhangi bir 0xFF baytından sonra, kodlayıcı tarafından bir sonraki bayttan önce bir 0x00 baytı eklenir, böylece hiçbirinin amaçlanmadığı yerde bir işaretçi görünmez ve çerçeveleme hatalarını önler. Kod çözücüler bu 0x00 baytı atlamalıdır. [Byte doldurma](https://en.wikipedia.org/wiki/Byte_stuffing) olarak adlandırılan bu teknik (bkz. JPEG spesifikasyonu bölüm F.1.2.3), yalnızca entropi kodlu verilere uygulanır, işaretleyici yük verilerine uygulanmaz . Bununla birlikte, entropi kodlu verilerin kendine ait birkaç belirteci olduğunu unutmayın; özellikle paralel kod çözmeye izin vermek için bağımsız entropi kodlu veri parçalarını izole etmek için kullanılan Sıfırlama işaretçileri (0xD0 ila 0xD7) ve kodlayıcılar bu Sıfırlama işaretlerini düzenli aralıklarla eklemekte özgürdür (ancak bunu tüm kodlayıcılar yapmaz).

