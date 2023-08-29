{
  "date" : "2019-10-11",
  "keywords" :[ "png dosyası", "png dosya biçimi", "png dosyası nedir", "dosya", "png örneği", "png dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PNG Dosya Biçimi - Raster Görüntü Dosyası",
  "description":"PNG dosya formatı ve PNG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## PNG dosyası nedir?

**PNG** (Taşınabilir Ağ Grafikleri) dosyası, kayıpsız sıkıştırma kullanan bir raster görüntü dosyası biçimidir. Bu dosya formatı, Grafik Değişim Formatının ([GIF](/tr/image/gif/)) yerini alması için oluşturulmuştur ve telif hakkı sınırlaması yoktur. Ancak, PNG dosya formatı animasyonları desteklemez. PNG dosya biçimi, kullanıcıları arasında popüler olmasını sağlayan kayıpsız görüntü sıkıştırmayı destekler. Zaman geçtikçe PNG, yaygın olarak kullanılan resim dosyası formatlarından biri olarak gelişti.

## PNG Dosya Biçiminin Kısa Tarihi

PNG dosya formatının oluşturulmasının arkasındaki ana sebep, GIF dosya formatında kullanılan patentli sıkıştırma algoritması Lempel-Ziv-Welch idi. Bu, diğer GIF sınırlamalarıyla birlikte [**GIF**](/tr/image/gif/) dosya formatının değiştirilmesi ihtiyacını doğurdu. PNG dosya formatı için ilk teklif ve isim Ocak 1995'te geldi. PNG dosya formatlarıyla ilgili önemli olaylar aşağıda listelenmiştir:

* Ekim 1996: PNG spesifikasyonları Sürüm 1.0 yayınlandı ve daha sonra [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083 olarak yayınlandı. Aynı sürüm, Ekim 1996'da bir W3C Tavsiyesi oldu.
* Aralık 1998: Bazı küçük değişiklikler ve üç yeni parçanın eklenmesiyle Sürüm 1.1 yayınlandı.
* Ağustos 1999: Fazladan bir öbek ekleyen Sürüm 1.2 yayınlandı.
* Kasım 2003: PNG, Uluslararası Standart oldu (ISO/IEC 15948:2003). PNG'nin bu sürümü, sürüm 1.2'den yalnızca biraz farklıdır ve yeni parça eklemez.
* Mart 2004: ISO/IEC 15948:2004

## GIF ve PNG'nin İşlevsel Karşılaştırması

PNG dosya formatı basit ve taşınabilir, yasal olarak ipoteksiz, değiştirilebilir, esnek ve sağlam olacak şekilde tasarlanmıştır. Aşağıdaki tablo, yeni özelliklere ek olarak PNG dosya biçiminden devralınan GIF özelliklerini listeler.

|Özellik|GIF|PNG|
---|---|---|
|256 renge kadar dizin renkli görüntüler|Evet|Evet|
|Akış desteği|Evet|Evet|
|Şeffaflık|Evet|Evet|
|Yardımcı bilgiler|Evet|Evet|
|Donanım ve Platform Bağımsızlığı|Evet|Evet|
|Etkili|Evet|Evet|
|Piksel başına 48 bit'e kadar gerçek renkli görüntüler|Hayır|Evet|
|Piksel başına 16 bit'e kadar gri tonlamalı görüntüler|Hayır|Evet|
|Tam alfa kanalı (genel şeffaflık maskeleri)|Hayır|Evet|
|Görüntü gama bilgisi|Hayır|Evet|
|Güvenilirlik|Hayır|Evet|
|Daha hızlı ilk sunum|Hayır|Evet|

## PNG Dosya Yapısı

Hemen hemen tüm İşletim Sistemlerinde PNG dosyalarını açma desteği vardır. Örneğin, işletim sistemi varsayılan olarak kurulumun bir parçası olarak sunulan desteğe sahip olduğundan, Microsoft Windows görüntüleyici PNG dosyalarını açma yeteneğine sahiptir. Bir PNG dosyası, bir dizi //parça// tarafından takip edilen bir PNG "imzasından" oluşur.

### PNG Dosya Başlığı

Bir PNG dosyasının ilk sekiz baytı her zaman aşağıdaki (ondalık) değerleri içerir:

{{{137 80 78 71 13 10 26 10 }}}

Bu imza, dosyanın geri kalanının, bir IHDR parçasıyla başlayan ve bir IEND parçasıyla biten bir dizi parçadan oluşan tek bir PNG görüntüsü içerdiğini gösterir.

### Parçalar ###

Her öbek dört bölümden oluşur:

**Uzunluk:** Öbeğin veri alanındaki bayt sayısını veren 4 baytlık işaretsiz bir tamsayı. Uzunluk yalnızca veri alanını sayar; kendisini, öbek türü kodunu veya CRC'yi saymaz. Sıfır, geçerli bir uzunluktur. Kodlayıcıların ve kod çözücülerin uzunluğu işaretsiz olarak ele alması gerekse de, değeri 231 baytı geçmemelidir.

**Yığın Türü:** 4 baytlık yığın türü kodu. Açıklamada ve PNG dosyalarını incelemede kolaylık sağlamak için tür kodları, büyük ve küçük ASCII harflerinden (AZ ve az veya 65-90 ve 97-122 ondalık) oluşacak şekilde sınırlandırılmıştır. Bununla birlikte, kodlayıcılar ve kod çözücüler, kodları karakter dizileri olarak değil, sabit ikili değerler olarak ele almalıdır. Örneğin IDAT tip kodunu bu harflerin EBCDIC karşılıklarıyla göstermek doğru olmaz. Yığın türleri için ek adlandırma kuralları bir sonraki bölümde ele alınmıştır.

**Yığın Veri:** Varsa yığın türüne uygun veri baytları. Bu alan sıfır uzunlukta olabilir.

**CRC:** Öbek türü kodu ve yığın veri alanları dahil, ancak uzunluk alanı hariç yığındaki önceki baytlar üzerinden hesaplanan 4 baytlık bir CRC (Döngüsel Artıklık Denetimi). Veri içermeyen yığınlar için bile CRC her zaman mevcuttur.

Yığın veri uzunluğu, maksimuma kadar herhangi bir sayıda bayt olabilir; bu nedenle uygulayıcılar, yığınların baytlardan daha büyük herhangi bir sınırda hizalandığını varsayamaz.

Yığınlar, her bir yığın türüne konulan kısıtlamalara tabi olarak herhangi bir sırada görünebilir. (Önemli bir kısıtlama, IHDR'nin önce ve IEND'in en sonda görünmesi gerektiğidir; bu nedenle, IEND öbeği bir dosya sonu işaretçisi görevi görür.) Aynı türde birden çok parça görünebilir, ancak yalnızca o tür için özel olarak izin verilmişse.

#### Öbek Türleri

Yığın Türleri, Yığın Türüne atanan 4 baytlık büyük/küçük harfe duyarlı ASCII değerine göre **Kritik** ve **Yardımcı** parçalar olarak sınıflandırılır. Tüm uygulamalar, standart kritik parçaları anlamalı ve başarılı bir şekilde oluşturmalıdır. Geçerli bir PNG görüntüsü, bir IHDR parçası, bir veya daha fazla IDAT parçası ve bir IEND parçası içermelidir.

### Sıkıştırma

PNG sıkıştırma yöntemi 0 (şu anda PNG için tanımlanan tek sıkıştırma yöntemi), en fazla 32768 baytlık bir kayan pencere ile indirme/şişirme sıkıştırmasını belirtir. Deflate sıkıştırma, zip, gzip, pkzip ve ilgili programlarda kullanılan bir LZ77 türevidir. Patentsiz statüsünü destekleyen kapsamlı araştırmalar yapılmıştır. zlib veri akışı içindeki sıkıştırılmış veriler, her biri ham (sıkıştırılmamış) verileri, sabit Huffman kodlarıyla kodlanmış LZ77 ile sıkıştırılmış verileri veya özel Huffman kodlarıyla kodlanmış LZ77 ile sıkıştırılmış verileri temsil edebilen bir dizi blok olarak depolanır. Son bloktaki bir işaret biti, onu son blok olarak tanımlayarak kod çözücünün sıkıştırılmış veri akışının sonunu tanımasına olanak tanır.

#### Ön Sıkıştırma Filtreleme

Görüntü verilerini optimum sıkıştırmaya hazırlamak için ön sıkıştırma filtreleri uygulanır. PNG filtre yöntemi, aşağıdaki gibi beş temel filtre tipini tanımlar:

|Filtre Türü|Ad|Tahmini Değer|
---|---|---|
|0|Yok|Tarama çizgisi değiştirilmeden iletilir|
|1|Alt|Her bayt ile önceki pikselin karşılık gelen baytının değeri arasındaki farkı iletir.|
|2|Yukarı|Yukarı() filtresi, tahmin edici olarak geçerli pikselin solundaki yerine hemen üstündeki pikselin kullanılması dışında Sub() filtresine benzer.|
|3|Ortalama|Average() filtresi, bir pikselin değerini tahmin etmek için iki komşu pikselin (sol ve üst) ortalamasını kullanır.|
|4|Paeth|Paeth() filtresi, üç komşu pikselin (sol, üst, sol üst) basit bir doğrusal işlevini hesaplar, ardından hesaplanan değere en yakın komşu pikseli öngörücü olarak seçer.|

Filtreleme algoritmaları, görüntünün bit derinliği veya renk türü ne olursa olsun piksellere değil "baytlara" uygulanır. Filtreleme algoritmaları, bir tarama çizgisi tarafından oluşturulan bayt dizisi üzerinde çalışır. Görüntü bir alfa kanalı içeriyorsa, alfa verileri görüntü verileriyle aynı şekilde filtrelenir.

Görüntü taramalı olduğunda, taramalı desenin her geçişi, filtreleme amaçları için bağımsız bir görüntü olarak ele alınır. Filtreler, bir geçiş sırasında fiilen iletilen piksellerin oluşturduğu bayt dizileri üzerinde çalışır ve "önceki tarama çizgisi", tam görüntüde bitişik olan değil, aynı geçişte önceden iletilen çizgidir. Herhangi bir geçişte iletilen alt görüntünün her zaman dikdörtgen olduğunu, ancak tam görüntüden daha küçük genişlik ve/veya yükseklikte olduğunu unutmayın. Bu alt resim boş olduğunda filtreleme uygulanmaz.

## Referanslar ##

* [PNG - Ana Sayfa](http://www.libpng.org/pub/png/)

