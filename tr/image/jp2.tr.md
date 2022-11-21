{
  "date" : "2019-10-11",
  "keywords" :[ "jp2 dosyası", "jp2 dosya biçimi", "jp2 dosyası nedir", "dosya", "jp2 örneği", "jp2 dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Görüntü Dosyası Biçimi",
  "description":"JP2 dosya formatı ve JP2 dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## JP2 dosyası nedir? ##

JPEG 2000 (**JP2**), bir görüntü kodlama sistemi ve en gelişmiş görüntü sıkıştırma standardıdır. Aynı anda herhangi bir kalitede kayıpsız içeriği kodlamak için dalgacık teknolojisini kullanır. Ayrıca, kodlama verimliliğinde herhangi bir önemli ceza olmaksızın, JPEG 2000, aynı içeriğe etkili bir şekilde çeşitli diğer çözünürlük ve niteliklere erişme ve kodunu çözme yeteneğine sahiptir. JPEG 2000'deki kod akışları, uzamsal rasgele erişim olanağı sağlayan ilgi bölgelerine sahip olarak önemli ölçüde ölçeklenebilir.

JPEG 2000, en ölçeklenebilir standartlardan biri olarak öne çıkıyor. Bir görüntünün farklı bölümleri, çeşitli nitelikler kullanılarak saklanabilir. Kod akışını çeşitli şekillerde düzenleyerek dikkate değer bir performans artışı elde edilebilir. Yine de JP2, bu esnekliğin bir sonucu olarak karmaşık ve hesaplama açısından zorlayıcı kodlayıcılar/kod çözücüler gerektirir. JPEG ile karşılaştırıldığında, JPEG 2000 yalnızca görüntünün kenarına yakın halkalar oluşturan ve bulanık olabilen çınlama yapaylıkları üretirken, JPEG hem çınlama hem de engelleme yapaylıkları olabilen 8×8 görsel yapaylık blokları kullanır. Terapixels'teki boyutları ve 38 bit/örnek kadar yüksek olabilen hassasiyeti ile 16384'e kadar farklı bileşene sahiptir.

## Tarih ##

2000 yılında, Ortak Fotoğraf Uzmanları Grubu komitesi, bu yeni dalgacık tabanlı yöntemle kendi ayrık kosinüs dönüşümü tabanlı JPEG standardını geliştirmek amacıyla JP2'yi tasarladı. JPEG komitesi, temel yöntemlerini lisans ücretlerinden muaf tutmayı amaçladı. 20 şirket arasındaki JP2 lisans kazanma yarışmasını kıl payı farkla kazandılar. JPEG 2000, bir ISO standardı olarak ilan edildi, ancak çoğu web tarayıcısı 2017'den beri JPEG 2000'e yardım etmeye hazır değil.

## JPEG 2000 görüntü kodlama sisteminin parçaları ##

Aşağıda, JPEG 2000 için tüm standartlar paketini oluşturan ana bölümler yer almaktadır.


|Parça|Başlık|Açıklama|Numara
---|---|---|---|
|Bölüm 1|Çekirdek kodlama sistemi| Kod akışının sözdizimini tanımlar. JPEG 2000 görüntülerinin kodunu çözmede yer alan farklı aşamalar. Temel dosya biçimi JP2'yi, meta verileri ve sağlanacak IP haklarını açıklar.|ISO/IEC 15444-1
|Bölüm 2|Uzantılar|Dosya biçimi kod akışı için uzantıları tanımlar ve HDR örnek gösterimlerine, renk alanı belirtimine, kırpmaya, geometrik dönüşümlere izin verir; çeşitli animasyonlar, meta veriler ve çoklu kod akışı.|ISO/IEC 15444-2
|Bölüm 3|Motion JPEG 2000 (MJ2 veya MJP2)|Görüntüleri bağımsız bir kod akışında kodlayarak hareket sekansları için bir dosya formatı tanıtın.|ISO/IEC 15444-3
|Bölüm 4|Uygunluk|Kodlama ve kod çözme için test tekniklerini belirtir ve hem çıplak kod akışları hem de JP2 dosyaları için dosyaları kontrol eder.|ISO/IEC 15444-4
|Bölüm 5|Referans yazılım|Çekirdek kodlama sistemini uygulayan ve açık kaynak lisansları altında bulunan iki kaynak kod paketinden (Java, C) oluşur.|ISO/IEC 15444-5
|Bölüm 6|Bileşik görüntü dosyası formatı|JPM dosya formatını tanımlar ve faks benzeri uygulamalar için çok sayfalı belge görüntülemeye izin verir. JBIG2 ve JPEG kullanımını destekler.|ISO/IEC 15444-6
|Bölüm 8|JPEG 2000 Güvenli (JPSEC)|İşlem, içerik ve teknolojilerin güvenliğini sağlar ve güvenli JPEG 2000 bit akışlarına izin verir.|ISO/IEC 15444-8
|Bölüm 9|JPIP|Meta verilere ve görüntülere erişim için ağ ortamındaki araçları tanımlar ve Etkileşimli ve verimli protokolleri belirtir|ISO/IEC 15444-9
|Bölüm 10|JP3D|Bölüm 1'in hacimsel uzantısı ve Z boyutunu tanıtıyor. Kutucuklar, kod blokları, bölgeler ve 3B ilgi alanı erişilebilirlik özellikleri kavramını genişletir.|ISO/IEC 15444-10
|Bölüm 11|JPWL|Hataya açık bir kablosuz ağ üzerinden iyi organize edilmiş iletimle ilgilenir. Bu uzantı, kod çözücülerle uyumludur|ISO/IEC 15444-11
|Bölüm 13|Giriş Düzeyi Kodlayıcı|Çekirdek kodlama sisteminin giriş düzeyi kodlayıcı uygulamasını tanımlar.|ISO/IEC 15444-13
|Bölüm 14|JPXML|XML'de bir gösterim ve işaretçi segmentlerini ve görüntünün dahili verilerine erişim yöntemlerini açıklar.|ISO/IEC 15444-14
|Bölüm 15|HTJ2K (Geliştirme Aşamasında)|Alternatif bir blok kodlama algoritması belirtir. Algoritma, on kat daha fazla verim ve kayıpsız kodlama/kod çözme sunar.|

## JP2 Dosya Biçimi ##

JPEG 2000, dosya formatını ve kod akışını JPEG-1 ile aynı şekilde tanımlar. Görüntü örnekleri özellikle JPEG 2000 tarafından açıklanmış olsa da, JPEG-1, görüntüyü kodlamak için gerekli olan renk alanı ve çözünürlüğü hakkında başka ek bilgiler içerir. JPEG 2000 dosyası olarak saklanan bir görüntü varsa, uzantı olarak **.jp2** kullanılır. Bu dosya formatı, animasyon mekanizmalarını ve çok sayıda kod akışının konfigürasyonunu tek bir görüntüde tanımlayan JPEG 2000 part-2 uzantısı ile daha da geliştirildi. **.jpx** uzantısı, görüntüler bu genişletilmiş dosya biçimi kullanılarak kaydedildiğinde kullanılır. Kod akışı verilerinin öncelikli olarak dosyalara kaydedildiği düşünülmediğinden, bu amaçla standart bir uzantı tanımlanmamıştır. Test amaçlı olmasına rağmen, sık sık **.jpc** veya **.j2k** uzantısını alır. JPEG-1'in aksine, JPEG 2000, meta verileri XML biçiminde kodlamak için farklı bir yol seçer. Exif etiketleri ve XML bileşenleri arasında referans olarak 12234-1.4 standardı (ISO TC42 komitesi tarafından) kullanılır. JPEG 2000, içinde bir ISO standardı olan XMP içerebilir.

### Parçalar ###
JPEG 2000 dosyaları ardışık parçalardan oluşur. Her parçanın 8 bayt başlığı vardır: 4 bayt yığın boyutu (önce big-endian, yüksek bayt) ve 4 bayt yığın türü - önceden tanımlanmış imzalardan biri: "jP" veya "jP2".

İkinci öbek "ftyp" türünde olmalı ve 8 uzaklığında bir alt türe sahip olmalıdır. JPEG 2000, şu değerlerden biri olması gereken alt tür tarafından tanımlanır: "jp2 "(dosya türü \*.JP2), "jp20" (dosya \*.JPA), "jpm" (dosya türü \*.JPM), "jpx " (dosya türü \*.JPX) yazın.

Bilinmeyen tür tespit edilene kadar yığınları yineleyerek, JPEG 2000 görüntü/video dosyası oluşturuyoruz.

### Renk dönüşümü ###

Başlangıçta, görüntülerin RGB renk uzayından başka bir renk uzayına dönüştürülmesi gerekir. Bu amaçla iki yol vardır: Tersinmez Renk Dönüşümü (ICT) ve Tersinir Renk Dönüşümü (RCT). İlki YC,,B,,C,,R, renk uzayını kullanır ve sabit/kayan nokta olarak uygulanması gerekirken, daha sonra değiştirilmiş bir YUV renk uzayı ve doğası gereği tersine çevrilebilir.// //RGB modeliyle sınırlı değil, JPEG 2000 dili, çoklu bileşen dönüşümü kullanır.

### Döşeme ###

Renk dönüşümü yapıldığında, görüntü, ayrı ayrı dönüştürülebilen ve kodlanabilen, kiremit adı verilen dikdörtgen bölgelere dönüşür. Tüm karoların boyutu aynı olacaktır veya tüm görüntü tek bir karo olarak düşünülebilir. Kod çözücü, döşeme avantajından yararlanır ve daha az bellek tüketir veya bazı döşemeleri kısmen kodlayabilir. Bu tekniğin resmin kalitesinde bozulma gibi bir dezavantajı olsa da.

### Dalgacık dönüşümü ###

Döşemeden sonraki görüntü, tersinmez veya tersinir olabilen ve evrişim veya kaldırma şeması kullanılarak uygulanan dalgacık dönüştürülür.

### Sıkıştırma oranı ###

Bir görüntünün fiziksel özelliklerine bağlı olarak, %20'lik bir sıkıştırma kazancı elde edilir. JPEG 2000'in uzamsal fazlalık tahmini, sıkıştırma işleminde hayati bir rol oynar ve yüksek çözünürlüklü görüntüler en büyük avantajı kazanma eğilimindedir.

## ## standardı tarafından sunulan uygulamalar

* Çerçeve tabanlı HD videoların kaydedilmesi, düzenlenmesi ve saklanması
* Tıbbi görüntüler ve biyometri
* uydu görüntüleri, uzaktan algılama ve hareket algılama
* İstemci/sunucu iletişimi, ağ dağıtımı ve depolama.
* Dijital sinema, Canlı HDTV besleme katkısı, Sayısallaştırılmış Görsel-işitsel öğeler

## Referanslar ##

* [JPEG 2000'e Genel Bakış](https://jpeg.org/jpeg2000)
* [JPEG 2000 resim kodlama sistemi](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

