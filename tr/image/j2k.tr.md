{
  "date" : "2019-10-11",
  "keywords" :[ "j2k dosyası", "j2k dosya biçimi", "j2k dosyası nedir", "dosya", "j2k örneği", "j2k dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2K",
  "description":"J2K dosya formatı ve J2K dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "J2K",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-03"
}

## J2K dosyası nedir?

**J2K** dosyası, DCT sıkıştırması yerine wavelet sıkıştırması kullanılarak sıkıştırılan bir görüntüdür. Bu dosya biçimi, Ortak Fotoğraf Uzmanları Grubu (JPEG) 2000 dosyaları tarafından kullanılır. J2K dosyaları, bu amaçla EXIF biçimini kullanan .jpeg veya .jpg'den farklı olarak, görüntü dosyasıyla ilgili meta veri bilgilerini XML'de depolar. J2K dosyaları 15 bit rengi, alfa saydamlığını ve kayıpsız sıkıştırmayı destekler. J2K-Codec gibi JPEG 2000 görüntülerinin kodunu çözmek için birkaç ticari API mevcuttur. Bir J2K dosyası, standart resim görüntüleyiciler kullanılarak Windows işletim sisteminde açılabilir.

## J2K Dosya Biçimi ##

J2K dosya biçimi, genellikle .jp2 ve .jpc olarak kaydedilen JPEG 2000 ile aynıdır. Bu, J2K dosyalarının, Exif etiketleri ve XML bileşenleri arasında bir referans olarak Standart 12234-1'in kullanıldığı XML biçimindeki meta verileri kodlama yaklaşımını izlemesini sağlar. Animasyon mekanizmasını ve kod akışı yapılandırmalarını tek bir görüntüde birleştiren JPEG 2000 part-2 uzantısı ile daha da geliştirilmiştir. Bu tür genişletilmiş dosya biçimi dosyaları .jpx olarak kaydedilir.

### Bir JPEG2000 Dosyasının Düzeni ###

JPEG2000, genişletilebilir dosya biçimlerine uygunluğu temel alan çeşitli uygulamaları destekler. En basit tür tek bir görüntü içerebilse de, daha karmaşık türler üst üste istiflenmiş veya zamana dayalı sıralanmış bir dizi görüntü içerebilir.

#### JP2 Kutusu ####
JP2 dosya biçiminin en üst düzey yapı taşıdır ve başlıkta bir tür ve uzunluk alanları ile bir veri bölümü içerir. En dikkate değer kutu tipi, bitişik kod akışı kutusudur. Bu kutu, veri bölümünde JPEG2000 kod akışını saklar.

#### JPEG2000 Kod Akışı ####

JPEG2000 CodeStream, JPEG2000 sıkıştırılmış görüntünün kodunu çözmek için gereken bir bayt dizisidir. Dosyanın bu kod akışından başka bir şeye sahip olmaması durumunda buna ham kod akışı dosyası denir. Genellikle bir JPEG kod akışı, tek yol olmasa da JPEG2000 sıkıştırma algoritmasının bir görüntüye uygulanmasıdır.

#### Fayans Parçaları ####

JPEG2000 kodlu bir görüntü, paket adı verilen bir veri birimleri koleksiyonudur. Bu paketler, kutucuk parçaları adı verilen paket gruplarının içindeki kod akışında tutulur. Bir görüntüyü kodlamadan önce, kodlayıcı görüntüyü, her bir döşemenin diğer döşemelerden bağımsız olarak ayrı ayrı kodlandığı, döşeme adı verilen dikdörtgen bir blok ızgarasına ayırır.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 Dosya Biçimi" >}}

## J2K Sıkıştırma ##
JPEG 2000, dalgacık sıkıştırma teknolojisini kullanır ve izleyicinin görüntüyü görüntülediği görünüm veya pencerede nispeten az sayıda pikselin gösterilmesi gerçeğine dayanarak onu hızlandırır. Bu, çok büyük boyutlu görüntüler için (gigabayt cinsinden) ekranda yalnızca birkaç megabayt pikselin görüneceği gerçeğiyle vurgulanabilir. Bu, görüntü verilerinin yalnızca ekran piksellerini doldurmak için gerekli olan kısmının hızlı bir şekilde getirilmesine ve oluşturulmasına yardımcı olur. Bu aynı zamanda anında gerekli görüntüleri oluşturmak için görüntü alma mekanizmasını hızlandırmak için yüksek hızlı açma teknolojisi gerektirir.

J2K, hızlı açma özelliğinden yararlanır ve görünür görüntülerin bir kısmını hızlı bir şekilde ekranlara işlemek için piksel verileri için yalnızca gerekli bilgileri getirir. J2K, öncelikle verileri düzenlemek için değil, görüntülemek için tasarlanmıştır.

## J2K Kimliği ##
JPEG 2000 dosyalarının imza baytları 6A 50 20 20'dir.

### Mim Türleri ###
JPEG 2000 dosyaları için Kayıtlı Mime Türleri şunları içerir:
* resim/jp2
* resim/jpx
* resim/jpm
* video/mj2

## JPEG standardına göre iyileştirmeler ##
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

