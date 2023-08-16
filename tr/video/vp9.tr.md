{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "Dosya", "Uzantı", "Dosya Biçimi", "Video Biçimi", "TrueMotion Video", "VPX", "On2 Teknolojileri"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 - TrueMotion Video Dosyası",
  "description":"VP9 dosya formatı ve VP9 dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## VP9 dosyası nedir?

Google, VP8'in halefi olarak telifsiz, açık kaynaklı bir video kodlama standardı olarak VP9 codec'ini geliştirmiştir. Orijinal olarak YouTube'daki ultra HD içeriği sıkıştırmak için tasarlandı çünkü selefinin kodlama verimliliğini genişletiyor ve geliştiriyor. Orijinal VPX codec'lerinden bahsedecek olursak, bunlar 2010 yılında Google tarafından asimile edilen On2 Technologies'den geliyordu. Google daha sonra codec'i açık kaynaklı hale getirdi. VP8 ve VP9 formatlarının her ikisi de, operatörlerin kaynak kodlarını ifşa etmeden hem özel yazılımlarda hem de açık kaynaklı yazılımlarda kodlama veya kod çözme yeterliliklerini düzenlemesine izin veren ücretsiz bir BSD lisansı altında mevcuttur.

## VP9'un Teknik Özellikleri

* VP9, Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 ve sRGB ile 120 fps'ye kadar maksimum 8192x4352 çözünürlük ve çoklu renk alanları sağlar
* Düşük bit hızlı sıkıştırmadan yüksek kaliteli ultra-HD'ye kadar tüm web ve mobil kullanım durumları, ek 10/12 bit kodlama desteği ve HDR bu format tarafından tam olarak desteklenir
* Video bit hızlarını diğerlerine kıyasla %50'ye kadar azaltabilir
* Uyarlanabilir akış için desteklenmiştir ve YouTube ve diğer tanınmış web video sağlayıcıları tarafından kullanılır.
* Chrome, Opera, Edge, Firefox ve Android cihazların yanı sıra milyonlarca akıllı TV, bu codec bileşeninin kodunun çözülmesini destekler
* 1080p'den yüksek video çözünürlükleri VP9 aracılığıyla değiştirilir ve kayıpsız sıkıştırmaya izin verir
* Rec gibi farklı renk uzayları. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240 ve sRGB, VP9 tarafından desteklenir
* Hybrid Log-Gamma ve Perceptual Quantizer kullanan HDR video da VP9 tarafından desteklenebilir


## Kısa Tarihçe

* VP9 video codec geliştirmesi 2011 yılında başlamış olup, dekoderi Aralık 2012'de Chromium web tarayıcısına eklenmiştir.
* İlk Google Chrome web tarayıcısı sürümü Şubat 2013'te piyasaya sürüldü ve o sırada kod çözme yayınlandı
* Google, Ağustos 2013'te VP9 son desteğiyle Chrome 29.0.1547'yi piyasaya sürdü
* Ekim 2013'te FFmpeg'e içgüdüsel bir VP9 kod çözücü eklendi
* Mozilla, Aralık 2013'te Firefox'a 18 Mart 2014'te yayınlanan 2. sürümde VP9 desteğini ekledi.
 

## VP9'un çalışması

Genellikle 4K video, belirli pikselleri küçülterek resim kalitesini yükseltir, VP9 codec bileşeni ve HEVC, bit hızını ve dosya boyutunu küçültmek için onları büyütür. Bu çelişkili görünse de, kodlama motoru daha büyük pikselleri alır ve onları daha iyi çözünürlük verimliliğine dönüştürür. Video çerçevelerini içeren kaynak video, sıkıştırılmış bir video bit akışı oluşturmak için kodlanır veya sıkıştırılır. Her ayrı çerçeve önce piksel bloklarına bölünür. Bloklar daha sonra üç boyutlu işten çıkarmalar için incelenir ve değiştirilemeyen alanlardan yararlanmak için çerçeveler arasındaki sıralı bağlantılar değerlendirilir. Bunlar, bir sonraki karede verilen bloğun niteliklerini sağlayan hareket vektörleri aracılığıyla kodlanır. Artık bilgi, etkili bir ikili sıkıştırma kullanılarak kodlanır.

## Referanslar

* [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9)
* [MDN Web Belgeleri](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [Hindistan cevizi](https://www.coconut.co/)

