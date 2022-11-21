{
  "date" : "2021-26-08",
  "keywords" :[ "dcr dosyası", "dcr dosya biçimi", "dcr dosyası nedir", "dosya", "dcr örneği", "dcr dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCR - Dijital Kamera RAW Görüntü Dosyası",
  "description":"DCR dosya formatı ve DCR dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DCR",
  "menu" : {
    "docs" : {
      "identifier":"image-dcr",
      "parent" : "image"
}
},
  "lastmod" : "2021-26-08"
}

## .dcr dosyası nedir? ##
dcr uzantılı bir dosya, Kodak Dijital Fotoğraf Makinesi RAW (DCR) biçiminde kaydedilmiş bir dijital fotoğrafın içeriğini içerir. DCR, **Digital Camera Raw**'un kısaltmasıdır; Kodak dijital fotoğraf makinesi tarafından yakalanan görüntü verilerinin sıkıştırılmamış ve kayıpsız sürümünü içerir. Profesyonel fotoğrafçılar, görüntüleri düşük kaliteli sıkıştırılmış görüntü formatlarından daha yüksek kalitede sakladıkları için bu dosyaları kullanmayı severler.

## DCR dosya formatı
DCR, Eastman Kodak Company tarafından geliştirilen tescilli bir formattır; kısaca Kodak olarak anılır. Bir Digital Camera Raw (DCR) görüntü dosyası, bir dijital kameranın görüntü sensöründen minimum düzeyde işlenmiş veri içerir. Bu dosyalar henüz işlenmemiştir ve bu nedenle yazdırılmaya veya bir bitmap grafik düzenleyiciyle düzenlenmeye hazır değildir.
Genellikle bir ham dönüştürücü, görüntüyü, depolama, yazdırma veya daha fazla manipülasyon için TIFF veya JPEG gibi bir raster dosya biçimine dönüştürmeden önce doğruluk ve iyileştirmenin yapılabileceği geniş gamlı bir dahili renk alanında işler.
### Dosya içeriği
Ham dosyaların yapısı genellikle genel bir model izler:
- Dosyanın bayt sıralamasının bir göstergesini içeren kısa bir dosya başlığı.
- CFA'nın nitelikleri, sensörün boyutu ve renk profili dahil olmak üzere sensör görüntü verilerini yorumlamak için gereken kamera sensörü meta verileri.
- Herhangi bir CMS ortamına veya veritabanına dahil edilmek üzere yararlı olabilecek görüntü meta verileri. Bazı ham dosyalar, Exif biçimindeki verileri içeren standartlaştırılmış bir meta veri bölümü içerir.
- Bir resim küçük resmi.
- Dosyayı kameranın LCD panelinde önizlemek için kullanılan, görüntünün tam boyutlu bir JPEG dönüştürmesi.
- Sinema filmi taramalarında, dosya dizisindeki zaman kodu, anahtar kodu veya taranan bir makaradaki kare sırasını temsil eden kare numarası.
- Sensör görüntü verileri
### Sensör görüntü verileri
Ham dosya, film fotoğrafçılığında fotoğraf filminin oynadığı gibi, dijital fotoğrafçılıkta da rol oynar. Ham dosyalar, bu nedenle, kameranın görüntü sensörü piksellerinin her birinden okunan tam çözünürlük verilerini içerir. Kameranın sensörü neredeyse sürekli olarak bir CFA (Renk Filtresi Dizisi) ile kaplıdır. Ham biçim verileri mevcut olduğunda yüksek dinamik aralıklı görüntüleme dönüştürmede kullanılabilir; bu, üç ayrı görüntü yakalamayı içeren çoklu pozlamalı HDI yaklaşımına daha basit bir alternatif olarak kullanılabilir.


## Referanslar ##

* [Ham görüntü biçimi - Wikipedia'ya göre](https://en.wikipedia.org/wiki/Raw_image_format)
* [DCR Dosyası Nedir](https://expertphotography.com/dcr-file/)

