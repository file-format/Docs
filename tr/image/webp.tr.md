{
  "date" : "2019-10-11",
  "keywords" :[ "webp dosyası", "webp dosya biçimi", "webp dosyası nedir", "dosya", "webp örneği", "webp dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP - Google Raster Resim Dosyası Formatı",
  "description":"WEBP dosya formatı ve WEBP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## WEBP dosyası nedir?

Google tarafından tanıtılan WebP, kayıpsız ve kayıplı sıkıştırmaya dayalı modern bir raster web görüntü dosyası biçimidir. Görüntü boyutunu önemli ölçüde azaltırken aynı görüntü kalitesini sağlar. Web sayfalarının çoğu verilerin etkili temsili olarak görüntüleri kullandığından, web sayfalarında WebP görüntülerinin kullanılması web sayfalarının daha hızlı yüklenmesiyle sonuçlanır. Google'a göre, WebP kayıpsız görüntüleri [PNG'ler](/tr/image/png/) ile karşılaştırıldığında boyut olarak %26 daha küçüktür, WebP kayıplı görüntüler ise karşılaştırılabilir [JPEG](/tr/image/jpeg/) görüntülerden %25-34 daha küçüktür. Görüntüler, WebP ve diğer görüntü dosyası formatları arasındaki Yapısal Benzerlik (SSIM) indeksine göre karşılaştırılır. WebP, [WebM](https://en.wikipedia.org/wiki/WebM) multimedya kapsayıcı biçiminin kardeş projesidir.

## WebP Özelliklerine Genel Bakış ##

WebP görüntüleri, çevreleyen bloklardan piksellerin tahminine dayalı sıkıştırma işlemini kullanır ve piksellerin tek bir dosyada birden çok kez kullanılmasıyla sonuçlanır. Animasyonlu görüntüleri destekler ve gelecekte daha fazla özelliği desteklemesi beklenir. Google, gerektiğinde kullanılmak üzere kodlayıcısı ve kod çözücüsü için [çevrimiçi](https://developers.google.com/speed/webp/download) kaynak kodunu kullanıma sunmuştur. WebP görüntüsü aşağıdakiler için destek sağlar:

* **Kayıplı sıkıştırma:** Kayıplı sıkıştırma, [VP8](http://en.wikipedia.org/wiki/VP8) anahtar çerçeve kodlamasına dayalıdır. VP8, On2 Technologies tarafından VP6 ve VP7 biçimlerinin halefi olarak oluşturulan bir video sıkıştırma biçimidir.
* **Kayıpsız sıkıştırma:** Kayıpsız sıkıştırma biçimi, WebP ekibi tarafından geliştirilmiştir.
* **Şeffaflık:** 8 bit alfa kanalı, grafik görüntüler için kullanışlıdır. Alfa kanalı, şu anda başka hiçbir formatta bulunmayan bir özellik olan kayıplı RGB ile birlikte kullanılabilir.
* **Animasyon:** Gerçek renkli animasyonlu görüntüleri destekler.
* **Meta veriler:** EXIF ve XMP meta verilerine sahip olabilir (örneğin kameralar tarafından kullanılır).
* **Renk Profili:** Gömülü bir ICC profiline sahip olabilir.

Kayıplı WebP sıkıştırması, bir görüntüyü kodlamak için tahmine dayalı kodlamayı kullanır; bu, videolardaki ana kareleri sıkıştırmak için VP8 video codec bileşeni tarafından kullanılan yöntemin aynısıdır. Tahmine dayalı kodlama, bir bloktaki değerleri tahmin etmek için komşu piksel bloklarındaki değerleri kullanır ve ardından yalnızca farkı kodlar.

Kayıpsız WebP sıkıştırması, yeni pikselleri tam olarak yeniden oluşturmak için halihazırda görülen görüntü parçalarını kullanır. İlginç bir eşleşme bulunamazsa yerel bir palet de kullanabilir.

## Dosya formatı ##

WebP dosya biçimi, RIFF (kaynak değişim dosyası biçimi) belge biçimini temel alır. WebP kapsayıcısı, yalnızca bir VP8 anahtar çerçevesi olarak kodlanmış tek bir görüntüyü içerenden daha fazla özellik için destek sağlar. Bir RIFF dosyasının temel öğesi aşağıdakilerden oluşan bir öbektir:


|Alan|Açıklama
---|---|
|Chunk FourCC: 32 bit|Öbek tanımlaması için kullanılan ASCII dört karakterli kod
|Yığın Boyutu: 32 bit (uint32)|Yığın boyutu, bu alan, yığın tanımlayıcı veya dolgu dahil değildir
|Yığın Yükü: Yığın Boyutu baytları|Veri yükü. Yığın Boyutu tek ise, 0 ~-~- olması gereken tek bir doldurma baytı ~-~- eklenir
|ChunkHeader ('ABCD')|Tek tek parçaların FourCC ve Chunk Size başlığını tanımlamak için kullanılır; burada 'ABCD', yığın için FourCC'dir. Bu öğenin boyutu 8 bayttır.

### WebP Başlığı ###

Bir WebP dosya başlığı aşağıdaki gibidir:

* RIFF Başlığı - ASCII karakterlerini temsil eden 32 bit 'R' 'I' 'F' 'F'
* Dosya Boyutu - 32 bit (uint32), 8 konumundan başlayan bayt cinsinden dosyanın boyutunu temsil eder. Bu alanın maksimum değeri 2^32 eksi 10 bayttır ve dolayısıyla tüm dosyanın boyutu en fazla 4GiB eksi 2 bayttır. .
* 'WEBP' - ASCII karakterlerini temsil eden 32 bit 'W' 'E' 'B' 'P'

### Kayıplı Dosya Biçimi ###

WebP görüntüleri, görüntü kayıplı kodlamaya dayalıysa ve saydamlık, canlandırma, alfa vb. herhangi bir gelişmiş/genişletilmiş özellik gerektirmiyorsa kayıplı dosya biçimini kullanır. Kayıplı görüntüler daha küçüktür ve eski uygulamalar tarafından da desteklenir.

Bu durumda WebP dosyası şunlardan oluşur:

* 12 bayt WebP dosya başlığı
* VP8 Parçası

[VP8 Veri Formatı ve Kod Çözme Kılavuzu](https://tools.ietf.org/html/rfc6386), VP8 bit akışı format özelliklerini gösterir.

### Kayıpsız Dosya Biçimi ###

Bu düzen, görüntü kayıpsız kodlamaya dayalı olduğunda ve harici biçimin sağladığı gelişmiş özelliklere gerek olmadığında kullanılır. Ancak daha eski uygulamalar bu tür dosyaları okuyamayabilir.

Bu durumda WebP dosyası şunlardan oluşur:

* 12 bayt WebP dosya başlığı
* VP8L Yığın

## Referanslar ##

* [WebP Geliştirici Referansı - Google Tarafından](https://developers.google.com/speed/webp/)
* [WebP Dosya Biçimi - Wikipedia Tarafından](https://en.wikipedia.org/wiki/WebP)

