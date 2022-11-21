{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKS Dosya Biçimi",
  "keywords" :[ "mks", "matroska video", "mkv biçimi", "dosya", "biçim", "video"],
  "description":"Yalnızca Matroska tarafından oluşturulan altyazılar için MKS dosya formatı ve MKS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## MKS dosyası nedir?

MKS dosyaları genellikle yalnızca altyazı içeren Matroska dosyaları olarak bilinir. Matroska genel bir dosya kabı olmasına rağmen, belirli formatlardaki bilgileri saklamaktan kaçınır. Bazı ses veya video kapsayıcılarında altyazılar kullanıldığından, Matroska bazı yaygın altyazı biçimlerini depolamaya özen gösteriyor. Matroska'nın büyüme oranıyla tutarlı olmasına yardımcı olur. Altyazıları Matroska'da saklamak için aşağıdaki noktaları izlemeniz gerekir:

- “.mks”. uzantı, Matroska dosyası tarafından kullanılacaktır (yalnızca altyazıları içerir).
- **CodecPrivate**, bir akışın tamamında genel olan codec'lerle ilgili tüm bilgileri depolamak için kullanılıyor.
- Zaman damgası yerel depolama biçiminde kullanılan Başlatma ve durdurma zaman damgalarını kaldırın. Bunun yerine, Blok zaman damgasını ve Süreyi kullanın.
- Saydam katmana sahip her şeyi kullanabilirsiniz, buna video da dahildir.

## Ortak Altyazı Formatları

Matroska'da depolanan daha yaygın altyazı biçimleri hakkında bazı kısa notlar:

### Görüntüler Altyazıları
VobSub altyazı formatı, Matroska'ya aktarılan ilk görüntü alt yazı formatıdır. Bu biçim, altyazıların bir DVD'den dışa aktarılmasıyla oluşturulur. VobSub bir dizi çoklu akıştan oluşuyorsa, Matroska'da depolanırken izler ayrılmalıdır.

### SRT Altyazıları
SRT, tüm altyazı biçimleri arasında en basit ve temel olanıdır. Aşağıda gösterildiği gibi dört bölümden oluşur:
 



1. Altyazının sırasını gösteren bir sayı.
2. Altyazının ekranda görünme ve kaybolma süresi.
3. Altyazının kendisi.
4. Bir sonraki altyazının başladığını belirtmek için boş bir satır.
 



### SSA/ASS Altyazıları
Sub Station Alpha (SSA), popüler altyazı düzenleyicisi SubStation Alpha tarafından kullanılan bir dosya biçimidir. SSA altyazıları, fansubbers tarafından yaygın olarak kullanılmaktadır. Karaoke, konumlandırma, stil verme gibi modern özellikleri görüntüleme yeteneğine sahiptir.
 



### WebVTT Altyazıları
World Wide Web Konsorsiyumu (W3C), “Web Video Metin İzleri Formatı” olarak kısaltılan WebVTT'yi geliştirdi. Bu biçim, HTML öğesiyle bağlantılı olarak harici metin izleme kaynaklarını işaretlemek için kullanılıyor.

### HDMV sunum grafikleri altyazıları
HDMV sunum grafikleri altyazı formatı (HDMV PGS) bir dizi bitmap'tir ve buna metin diyemeyiz. Başka bir deyişle, bunun yalnızca zamanlanmış bir grafik görüntüler dizisi olduğunu söyleyebilirsiniz. Bilgileri ayıklamak için PGS'yi SRT'ye dönüştürmek gerekli bir süreçtir.

### HDMV metin altyazıları
HDMV metni, Blu-ray'lerde kullanılan metinsel altyazı formatı olarak bilinir. Matroska, TextST altyazılarını sakladığında yalnızca UTF-8 karakter kümesine izin verir.

### Dijital Video Yayını (DVB) altyazıları
DVB altyazı formatı, TV sinyallerinde çeşitli dillerdeki altyazıların iletimini ve görüntülenmesini düzenlemek için tanıtıldı. Tipik bir altyazı formatı, iletim sistemlerinin üreticisi ne olursa olsun, herhangi bir izleyicinin DVB altyazılı yayınları izlemesine de izin verir.


## Referanslar ##

- [Matroska Altyazıları](https://www.matroska.org/technical/subtitles.html)

