{
  "date" : "2019-10-11",
  "keywords" :[ "j2c dosyası", "j2c dosya biçimi", "j2c dosyası nedir", "dosya", "j2c örneği", "j2c dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"J2C dosya formatı ve J2C dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## J2C dosyası nedir?

.j2c uzantılı bir dosya, JPEG dosya biçiminin bir çeşididir ve dalgacık sıkıştırmasıyla sıkıştırılır. JPEG 2000 dosya formatıyla neredeyse aynı işaretçi ve segment sistemine sahiptir. J2C dosya formatı, hem kayıplı hem de kayıpsız sıkıştırmayı destekleyen JPEG 2000 standının 1. Bölümünde tanımlandığı gibidir. JPEG 2000 kod akışı, kendi başına bir dosyada görünebilmesine rağmen, [JP2](/tr/image/jp2/) veya başka bir dosya biçimine gömülmek üzere tasarlanmıştır. J2C dosyası Adobe Photoshop 2020, Adobe Illustrator 2020 ve Corel Paintshop Pro kullanılarak açılabilir.

## J2C Dosya Biçimi

J2C dosya biçimi, genellikle .jp2 ve .jpc olarak kaydedilen JPEG 2000 ile aynıdır. Bu, J2C dosyalarının, Exif etiketleri ve XML bileşenleri arasında bir referans olarak Standart 12234-1'in kullanıldığı, XML formatındaki meta verileri kodlama yaklaşımını izlemesini sağlar. Animasyon mekanizmasını ve kod akışı yapılandırmalarını tek bir görüntüde birleştiren JPEG 2000 part-2 uzantısı ile daha da geliştirilmiştir. Bu tür genişletilmiş dosya biçimli dosyalar [.jpx](/tr/image/jpx/) olarak kaydedilir.

### Bir JPEG2000 Dosyasının Düzeni

JPEG2000, genişletilebilir dosya biçimlerine uygunluğu temel alan çeşitli uygulamaları destekler. En basit tür tek bir görüntü içerebilse de, daha karmaşık türler üst üste istiflenmiş veya zamana dayalı sıralanmış bir dizi görüntü içerebilir.

#### JP2 Kutusu
JP2 dosya biçiminin en üst düzey yapı taşıdır ve başlıkta bir tür ve uzunluk alanları ile bir veri bölümü içerir. En dikkate değer kutu tipi, bitişik kod akışı kutusudur. Bu kutu, veri bölümünde JPEG2000 kod akışını saklar.

#### JPEG2000 Kod Akışı

JPEG2000 CodeStream, JPEG2000 sıkıştırılmış görüntünün kodunu çözmek için gereken bir bayt dizisidir. Dosyanın bu kod akışından başka bir şeye sahip olmaması durumunda buna ham kod akışı dosyası denir. Genellikle bir JPEG kod akışı, tek yol olmasa da JPEG2000 sıkıştırma algoritmasının bir görüntüye uygulanmasıdır.

#### Fayans Parçaları ####

JPEG2000 kodlu bir görüntü, paket adı verilen bir veri birimleri koleksiyonudur. Bu paketler, kutucuk parçaları adı verilen paket gruplarının içindeki kod akışında tutulur. Bir görüntüyü kodlamadan önce, kodlayıcı görüntüyü, her bir döşemenin diğer döşemelerden bağımsız olarak ayrı ayrı kodlandığı, döşeme adı verilen dikdörtgen bir blok ızgarasına ayırır.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 Dosya Biçimi" >}}

## J2C Sıkıştırma
JPEG 2000, dalgacık sıkıştırma teknolojisini kullanır ve izleyicinin görüntüyü görüntülediği görünüm veya pencerede nispeten az sayıda pikselin gösterilmesi gerçeğine dayanarak onu hızlandırır. Bu, çok büyük boyutlu görüntüler için (gigabayt cinsinden) ekranda yalnızca birkaç megabayt pikselin görüneceği gerçeğiyle vurgulanabilir. Bu, görüntü verilerinin yalnızca ekran piksellerini doldurmak için gerekli olan kısmının hızlı bir şekilde getirilmesine ve oluşturulmasına yardımcı olur. Bu aynı zamanda anında gerekli görüntüleri oluşturmak için görüntü alma mekanizmasını hızlandırmak için yüksek hızlı açma teknolojisi gerektirir.

J2C, hızlı açmanın avantajlarından yararlanır ve görünür görüntülerin bir kısmını hızlı bir şekilde ekranlara işlemek için piksel verileri için yalnızca gerekli bilgileri getirir. J2C, öncelikle verileri düzenlemek için değil, görüntülemek için tasarlanmıştır.

## J2C Kimliği
JPEG 2000 dosyaları 'FF 4F FF 51' imza baytlarına sahiptir.

### Mim Türleri
JPEG 2000 dosyaları için Kayıtlı Mime Türleri şunları içerir:
* resim/j2c
* resim/jpx
* resim/jpm
* video/mj2

## JPEG standardına göre iyileştirmeler
JPEG standardı üzerindeki iyileştirmeler şunları içerir:
* Üstün sıkıştırma performansı
* Çoklu çözünürlük gösterimi
* Piksel ve çözünürlük doğruluğu ile aşamalı iletim
* Kayıpsız veya kayıplı sıkıştırma seçimi
* Hata direnci, Esnek dosya formatı
* Yüksek dinamik aralık desteği
* Yan kanal mekansal bilgileri

## Referanslar ##
* [Taubman, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

