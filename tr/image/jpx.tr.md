{
  "date" : "2021-02-10",
  "keywords" :[ "jpx dosyası", "jpx dosya biçimi", "jpx dosyası nedir", "dosya", "jpx örneği", "jpx dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX - Görüntü Dosyası Biçimi",
  "description":"JPX dosya formatı ve JPX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## JPX dosyası nedir? ##

.jpx uzantılı bir dosya, JPEG 2000 dosya biçiminin bir uzantısıdır. Öncelikle JPEG 2000 sıkıştırmasını kullanır ve ayrıca bir görüntü için çoklu katmanlar, çeşitli renk alanları, opaklık ve parçalanmış kod akışları gibi gelişmiş özellikler sağlar. JPX, JPEG 2000 sıkıştırmasına ek olarak JBIG, CCITT Group3, CCITT Group4 vb. gibi diğer sıkıştırmalara da izin verir. JPX dosya formatı [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html) standardı olarak onaylandı, ancak [JPEG'in yoğun kullanımı nedeniyle sıcak bir karşılama alamadı. ](/tr/image/jpeg/) dosya biçimi. JPX dosyalarını açabilen uygulamalar arasında Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 ve CorelDraw Graphics Suite 2020 bulunur.

## Kısa Tarihçe

2000 yılında, Ortak Fotoğraf Uzmanları Grubu komitesi, bu yeni dalgacık tabanlı yöntemle kendi ayrık kosinüs dönüşümü tabanlı JPEG standardını geliştirmek amacıyla JP2'yi tasarladı. JPEG komitesi, temel yöntemlerini lisans ücretlerinden muaf tutmayı amaçladı. 20 şirket arasındaki JP2 lisans kazanma yarışmasını farkla kazandılar. JPEG 2000, bir ISO standardı olarak ilan edildi, ancak çoğu web tarayıcısı 2017'den beri JPEG 2000'e yardım etmeye hazır değil. 2004'te, ISO/IEC 15444-2 formatı, JP2 dosya formatının uzantısı olarak genel olarak kabul edildi.

## JPX Dosya Biçimi

JPX dosya formatı, [JP2](/tr/image/jp2/) dosya formatı tarafından tanımlanan işlevselliğin ötesinde veri yapılarına ihtiyaç duyan uygulamaların gereksinimlerini karşılamak üzere formüle edilmiştir. Uyumlu olmayan uzantılara sahip bir JP2 dosyası, piyasada bazı okuyucuların bazı JP2 dosyalarını yorumlayıp diğerlerini yorumlayamadığı karışıklığa yol açabilir. JPX, uygulamalarda bu tür sorunlardan kaçınmanın yanıtıdır.

### Dosya Tanımlama

JPX dosyaları, geleneksel bilgisayar dosya sisteminde saklandığında [JPF](/tr/image/jpf/) olarak saklanır. Bu nedenle JPX terimi, JPF'ye kıyasla en az yaygın olarak kullanılmaktadır. Bir JPX dosyası aşağıdaki baytlarla başlar:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Dosya Organizasyonu

JP2'ye benzer şekilde, bir JPX dosyası, bitişik bir düzende düzenlenmiş kutularla ikili yapıya sahip bir kutular koleksiyonudur. İlk kutu, ilk baytı ile dosyanın başlangıcını verir ve son kutunun son baytı, dosyanın son baytını temsil eder.
JPX dosyasındaki bir kutunun ikili yapısı, [JP2](/tr/image/jp2/) dosya biçiminde tanımlananla aynıdır.

### CodeStream'in JPX'te saklanması

JPX dosya biçimi, görüntü kod akışının parçalara bölünmesine izin verir. Bu, görüntünün tek bir döşemesini değiştirmeyi ve tüm dosyayı yeniden yazmadan değiştirilen döşemeyi dosyanın sonuna yazmayı mümkün kılar. Orijinal [JP2](/tr/image/jp2/) dosya formatı, tüm kod akışının dosyanın bitişik bir bölümünde depolanmasını kısıtlar; bu, görüntünün tek bir döşemesini değiştirmek isteyebilecek görüntü düzenleme uygulamaları için sorunlu olabilir. JPX dosya biçimine göre yukarıdaki desteklenebilirlik. Görüntü kod akışının parçalanması, JPX dosya formatını JP2 dosya formatına göre üstün kılar. Ek olarak, JPX dosya formatı, çoklu kod akışının birleştirilmesine ve işlenmiş sonuç üretilmesine izin verir. Kod akışları, birleştirme ve animasyon olarak birleştirilebilir.

## Referanslar ##

* [JPEG 2000'e Genel Bakış](https://jpeg.org/jpeg2000/)

