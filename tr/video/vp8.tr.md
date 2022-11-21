{
  "date" : "2021-03-10",
  "keywords" :[ "VP8", "Dosya", "Uzantı", "Dosya Biçimi", "Video Biçimi", "TrueMotion Video", "WebRTC", "WebM"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP8 - TrueMotion Video Dosyası",
  "description":"VP8 dosya formatı ve VP8 dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VP8",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## VP8 dosyası nedir?

VP8, Google tarafından en iyi resim kalitesi veri hızına ve kodlama hızına sahip en iyi video formatlarından biri olarak duyurulur. VP8'in en iyi avantajı, H.264'ün telifsiz yerine geçmesidir. Yüksek kaliteli videoyu dosya veya bit akışı olarak kodlamak ve kodunu çözmek için özel bir formattır. Ücretsizdir, çünkü Google tüm VP8 patentlerini telifsiz bir kamu lisansı altında yayınlamıştır. Tüm WebRTC video oturumlarının neredeyse %90'ı veya daha fazlası VP8 kullanır.

## VP8 Dosya Biçimi

VP8, 2008'de On2 Technologies tarafından geliştirildi ve daha sonra 2010'da Google'a ait oldu. Web ve mobil cihazlar için yüksek kaliteli video sağlamak üzere tasarlanmıştır. VP8 için ilk ses-video kapsayıcısı WebM idi ve bu codec, 2011'de WebRTC video codec'i olarak seçildi. Bu format, HTML5, Web Real-Time Communication ve farklı tarayıcılarda video oynatma gibi birçok endüstriyel uygulamada kabul görüyor. Bu formatı tam HD çözünürlükte desteklemek için tam bir pazar talebi var. Video konferans, video yayını, mobil cihazlardan kayıt gibi farklı amaçlar için kullanılmaktadır.

## Özellikler ##

### VP8'in Özellikleri
 



* Ücretsiz video codec'i
* En ilerici video dosyası formatı
* Çerçeve kaybına karşı geliştirilmiş direnç
* Yüksek hızlı video çözme
* Donanım platformlarında icat etmesi kolay
* Saf bir giriş modu özelliğine sahiptir, yani video düzenleme gibi uygulamalarda rasgele erişim sağlamak için sıralı tahmin olmaksızın yalnızca bireysel olarak kodlanmış kareler kullanma
* libvpx, VP8 video akışlarını kodlama konusunda yetkin olan tek yazılım kitaplığıdır
* VP8, özellikle bir kalite aralığında çalışacak şekilde tasarlanmıştır.

* Web'e bağlı, düşük güçlü mobil ve implante cihazlardan birçok işlemci çekirdeğine sahip en gelişmiş masaüstü bilgisayarlara uzanan geniş bir istemci donanımı yelpazesi vardır.
* 420 renk örnekleme, kanal başına 8 bit renk derinliği, aşamalı tarama ve en yüksek 16383x16383 piksel görüntü formatına kadar görüntü boyutları, VP8 aracılığıyla kolayca çalıştırılabilir
* Bu tasarım yerleşimlerinin altındaki sıkıştırma yeteneği ve kod çözücü basitliği dürtüsü, VP8'de kabul edilen diğer video sıkıştırma formatlarına kıyasla birkaç benzersiz teknik özelliğe yol açtı.
* VP8, diğer formatlarda görülen çok sayıda referans hareket dengeleme şemasından üç referans çerçevesi kullanır.
* VP8, kare hızı veya veri hızıyla sınırlı değildir. Hem genişlik hem de yükseklik için 14 bit kullanır, bu da en yüksek çözünürlüğü 16384x16384 piksel yapar.

### VP8'in Sınırları

Çözünürlük, veri hızı ve kare hızı açısından VP8'in sınırları aşağıdaki gibidir:

* VP8, maksimum 16384x16384 piksel çözünürlük için genişlik ve yükseklik için 14 bit uygular
* VP9, maksimum 65536x65536 piksel çözünürlük için genişlik ve yükseklik için 16 bit kullanır
* Kare hızı veya veri hızı üzerinde herhangi bir kısıtlama yoktur
 



 



## Referanslar

* [VP8 Vikipedi](https://en.wikipedia.org/wiki/VP8#:~:text=VP8%20%20first%20yayınlandı%20tarafından,%2C%20replaceing%20its%20predecessor%2C%20VP7.&text= %20May%2019%2C%20at%20its,bir%20geri alınamaz%20ücretsiz%20patent%20lisans)
* [Springer Bağlantısı](https://link.springer.com/chapter/10.1007/978-81-322-1157-0_32)

