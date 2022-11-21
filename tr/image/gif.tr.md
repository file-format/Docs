{
  "date" : "2019-10-11",
  "keywords" :[ "gif dosyası", "gif dosya formatı", "gif dosyası nedir", "dosya", "gif örneği", "gif dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Resim Dosyası Biçimi",
  "description":"GIF dosya formatı ve GIF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## GIF dosyası nedir? ##

GIF veya Grafik Değişim Biçimi, yüksek oranda sıkıştırılmış bir görüntü türüdür. Unisys'e ait GIF, görüntü kalitesini düşürmeyen LZW sıkıştırma algoritmasını kullanır. Her görüntü için GIF tipik olarak piksel başına 8 bit'e kadar izin verir ve görüntü genelinde 256'ya kadar renge izin verilir. 16 milyon renge kadar görüntüleyebilen ve insan gözünün sınırlarını oldukça aşan bir [JPEG](/tr/image/jpeg/) görüntüsünün aksine. İnternet ortaya çıktığında, GIF'ler en iyi seçenek olmaya devam etti çünkü düşük bant genişliği gerektiriyorlar ve katı renk alanlarını tüketen grafikler için uyumlulardı. Animasyonlu bir GIF, çok sayıda görüntüyü veya kareyi tek bir dosyada birleştirir ve animasyonlu bir klip veya kısa bir video oluşturmak için bunları sırayla görüntüler. Renk sınırlamaları, her kare için 256'ya kadardır ve renk gradyanlı diğer resimlerin ve fotoğrafların çoğaltılması için muhtemelen en az uygun olanlardır.

## GIF Dosya Biçimi ##

Kavramsal olarak, GIF dosyalarının sıfır veya daha fazla resimle dolu sabit boyutlu bir grafik alanı vardır. Bazı GIF dosyaları, sabit boyutlu grafik alanı veya blokları, animasyonlu GIF durumunda animasyonlu çerçeveler olarak işlev görebilen alt görüntülere böler. GIF formatı, bitmap verilerini depolamak için 1 ila 8 bit arasındaki piksel derinliklerini kullanır. Görüntüleri depolamak için her zaman RGB renk modeli ve palet verileri kullanılır. Sürüme bağlı olarak, sabit uzunlukta bir başlık ("GIF87a" veya "GIF89a") tipik bir GIF dosyasının başlangıcını tanımlar.

Şu anda GIF'in iki versiyonu mevcuttur: 87a ve 89a. İlki orijinal GIF formatıdır, ikincisi ise yeni GIF formatıdır. Bu dosya biçiminde, blokların özellikleri ve piksel boyutları sabit uzunlukta bir Mantıksal Ekran Tanımlayıcısında belirtilir. Global Renk Tablosunun varlığı ve boyutu, varsa daha fazla ayrıntıyı izleyen ekran tanımlayıcı tarafından belirtilebilir. Fragman, tek bir ASCII noktalı virgül baytı tutan dosyanın son baytıdır. Tipik bir GIF87a dosya düzeni aşağıdaki gibidir:

### Başlık ###

Başlık altı bayt tutar ve dosya türünü GIF olarak belirtmek için kullanılır. Mantıksal Ekran Tanımlayıcı gerçek başlıktan ayrılmış olsa da bazen ikinci başlık olarak kabul edilir. Başlığı saklamak için kullanılan aynı yapı, Mantıksal Ekran Açıklayıcısını saklayabilir. Tüm GIF dosyaları 3 baytlık imzayla başlar ve tanımlayıcı olarak "GIF" karakterlerini kullanır. Sürüm ayrıca üç bayt boyutundadır ve GIF dosyasının sürümünü bildirir.

### Mantıksal Ekran Açıklayıcı ###

Sabit uzunlukta bir Görüntü Tanımlayıcı, GIF görüntüsünü oluşturmak için gerekli ekran ve renk bilgilerini belirtir. Yükseklik ve Genişlik alanları, görüntü verilerini göstermek için zorunlu olan en küçük ekran çözünürlüğü değerini içerir. Görüntüleme cihazı belirtilen çözünürlüğü görüntüleyemiyorsa, görüntüyü uygun şekilde görüntülemek için ölçeklendirme gerekecektir. Ekran ve Renk Haritası Bilgileri, aşağıdaki tablonun dört alt alanında görüntülenir (oysa 0 biti en önemsiz bittir):


|Bit|Alt alanlar
---|---|
|0-2|Global Renk Tablosunun Boyutu
|3|Renk Tablosu Sıralama İşareti
|4-6|Renk Çözünürlüğü
|7|Küresel Renk Tablosu Bayrağı

#### Küresel Renk Tablosu ####

Mantıksal Ekran Tanımlayıcının hemen sonrasına isteğe bağlı bir Global Renk Tablosu yerleştirilir. Bu tablo, görüntü verilerinin içindeki piksel renk verilerini indekslemek için eşlenmiştir. Genel Renk Tablosunun olmaması durumunda, GIF dosyasındaki her görüntü kendi Yerel Rengini kullanır. Hem Global hem de Yerel Renk Tablosu eksikse varsayılan bir renk tablosu sağlamak daha iyidir. Bir dizi üç baytlık üçlü, renk tablosunun öğelerini oluşturur. Her bayt, bir RGB renk değerini karakterize eder. Kırmızı, yeşil ve mavi renkler, her bir renk tablosu öğesinin değerleri olarak kullanılır. Global Renk Tablosundaki girişler maksimum 256 girişe ulaşır ve her zaman ikinin kuvvetini temsil eder.

#### Görüntü Verileri ####

Görüntü verisi, kodlanmamış sembollerin bir baytını ve ardından LZW ile kodlanmış verilerin bağlantılı alt listesini depolar.

#### Tanıtım videosu ####

Fragman, dosyadaki son karakter olan tek baytlık veriyi temsil eder. Bu baytın değeri kalıcı olarak 3Bh'dir ve veri akışının sonunu belirtir. Her GIF dosyası, her dosyanın sonunda fragmana sahip olmalıdır.

## Referanslar ##

* [GIF dosya formatı](https://en.wikipedia.org/wiki/GIF)

