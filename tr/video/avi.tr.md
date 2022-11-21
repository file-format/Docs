{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Sıkıştırılmış Sesli Video", "Dosya", "Uzantı", "Dosya Biçimi", "Multimedya Kabı", "XVid", "DivX", "Kodekler", "Kaynak Değişim Dosyası Biçimi", "RIFF "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AVI Dosya Biçimi - Bir Ses Video Araya Ekleme Dosyası",
  "description":"AVI dosya formatı ve AVI dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## AVI dosyası nedir? ##

**AVI** dosya biçimi, Microsoft tarafından tanıtılan bir Audio Video multimedya kapsayıcı dosya biçimidir. **XVid** ve **DivX** gibi çeşitli codec'ler (Kodlayıcılar/Kod Çözücüler) kullanılarak oluşturulan ve sıkıştırılan ses ve video verilerini tutar. AVI içeriklerini kodlamak için farklı codec'ler kullanılabileceğinden, alma uygulamaları, yani AVI oynatıcılar, bunları ancak AVI içeriklerinin oluşturulduğu gerekli codec'ler yüklüyse açabilmelidir. Biçim, tüm **Microsoft Windows** platformlarının yanı sıra neredeyse tüm diğer büyük platformlarda varsayılan olarak desteklenir. Çeşitli uygulamalar ve API'ler, AVI oluşturma/kaydetme, okuma ve MP4, MOV, WMV, vb. gibi diğer popüler biçimlere dönüştürme yeteneği sağlar.

## AVI Dosya Biçimi ##

.avi uzantılı bir dosya bir AVI dosyasıdır. Kaynak Değişim Dosyası Formatının (RIFF) bir alt formatıdır. RIFF, verileri bir FourCC etiketiyle tanımlanan bloklar veya "parçalar" halinde düzenler. Bir AVI dosyası, RIFF biçimli bir dosyadaki yalnızca bir "yığın"dır.

İlk alt yığında, dosyanın başlığı "hdrl" etiketi ile tanımlanır; içeriği videonun genişliğini, yüksekliğini ve kare hızını içerir. İkinci alt yığında, hareket etiketi videonun kare hızını temsil eder. AVI videosu, bu yığındaki gerçek işitsel/görsel verilerden oluşur. Ayrıca, dosyaya ait ayrı ayrı veri parçalarının dosya içindeki konumunu gösteren "idx1" etiketli üçüncü bir isteğe bağlı alt yığın da vardır.

### Sınırlamalar ###

* En boy oranı bilgisi, orijinal AVI spesifikasyonunda kodlanamaz, ancak daha sonraki OpenDML spesifikasyonu (AVI 2.0) standartlaştırılmış bir yöntem sunar.
* AVI dosyaları film ve televizyon post prodüksiyonlarında yaygın olarak kullanılsa da, bunlara zaman kodu eklemeye yönelik çeşitli yaklaşımlar rekabet halindedir ve bu da biçimin kullanılabilirliğini etkiler.
* AVI'de kodlanmış bir video dosyası, kodlanan çerçevenin (B-kare) ötesinde gelecekteki çerçeve verilerini gerektiren bir sıkıştırma tekniği kullanamaz.
* Değişken bit hızlarına (VBR) sahip AVI dosyalarını kullanmak sorunludur (örneğin, 32 kHz'in altındaki örnekleme hızlarında MP3 ses)
* Standart tanımlı uzun metrajlı filmleri normalde kullanıldığı şekilde kodlayan bir AVI dosyası, dosyanın nasıl kullanıldığına bağlı olarak, muhtemelen saatte yaklaşık 5 MB ek yüke neden olur
* AVI dosyalarının yazı tipleri ve altyazılar gibi ekleri barındıramaması durumunda, altyazılar video akışına sabit kodlanmalı veya ayrı bir dosyada dağıtılmalıdır.

## Kısa Tarih ##

AVI, daha sağlam ve gelişmiş bir ses ve video dosyası formatı sağlamak amacıyla Microsoft tarafından 1992 yılında tanıtıldı. Biçim, internet kullanımıyla hızla popüler hale geldi ve bireylerin video dosyalarını bulut tabanlı medya depolama yoluyla doğrudan ve dolaylı olarak paylaşmasına olanak sağladı.

## Referanslar ##

* [AVI - Wikipedia'dan](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

