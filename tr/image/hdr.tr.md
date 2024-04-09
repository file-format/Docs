{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR Dosya Biçimi - HDR görüntü dosyası nedir?",
  "description":"HDR dosya formatı ve HDR dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## HDR dosyası nedir?

HDR dosyası, dijital kamera fotoğraflarını depolamak için bir Yüksek Dinamik Aralık (HDR) raster görüntü dosyası biçimidir. Fotoğraf editörlerinin, sınırlı dinamik aralığa sahip dijital görüntülerin rengini ve parlaklığını geliştirmesine olanak tanır. Bu değişiklik, köşelerdeki parlaklığı artırarak doğala yakın bir görüntü elde edilmesini sağlayabilir. HDR dosyaları genellikle 32 bit raster görüntüler olarak kaydedilir. Adobe Photoshop, HDR dosyaları oluşturabilir ve açabilir.

HDR dosyaları, HDRI olarak da bilinir.

## HDR Dosya Biçimi - Daha Fazla Bilgi

HDR dosya biçimi, orijinal Radiance Picture (.pic) dosya biçimini temel alır. Bir HDR dosyasının piksel verileri genellikle sıkıştırılmamış olarak depolanır, ancak bazı durumlarda basit bir çalıştırma uzunluğu kodlama sistemi kullanılarak sıkıştırılır.

### HDR Dosya Yapısı

Bir HDR görüntü dosyası aşağıdaki üç bölümden oluşur:

* **Başlık:** Bir HDR dosyası, görüntü dosyasındaki ilk baytlarla tanımlanır, yani "#?RADIANCE".
* **Çözüm Dizesi:** Başlığın ardından 4 değerden oluşan tek bir çözüm satırı gelir; bir X ve Y etiketinin ardından sayısal bir tamsayı değeri gelir. X ve Y'nin sırası dönüşü belirtir. X ve Y'nin pozitif ve negatif değerlerle birleşimi olası tüm görüntü yönlendirmesini ve dönüşlerini kapsar.
* **Piksel Verileri:** Bir HDR dosyasının piksel verileri sıkıştırılmamış veya standart çalışma uzunluğu kodlaması kullanılarak sıkıştırılmıştır.

## Açık Kaynaklı HDR/HDRI API'leri

* **[imageinfo](https://github.com/xiaozhuai/imageinfo)** - Yüklemeden/kod çözmeden görüntü boyutu ve formatı almak için platformlar arası süper hızlı tek başlıklı [C++](/tr/programming/cpp/) kitaplığı.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Yüklemeden/kod çözmeden görüntü boyutu ve formatı almak için Rust kitaplığı. [.avif](/tr/image/avif/), [.bmp](/tr/image/bmp/), [.cur](/tr/image/cur/), [.dds](/tr/image/dds/), ['yi destekler. gif](/tr/image/gif/), hdr (resim), [heic (heif)](/tr/image/heic/), [.icns](/tr/image/icns/), [.ico](/tr/image/ico/), [.jp2](/tr/image/jp2/), [jpeg (jpg)](/tr/image/jpeg/), [jpx](/tr/image/jpx/), ktx, [png](/tr/image/png/), [psd](/tr/image/psd/), qoi, tga, tiff (tif) ve webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - HdrHistogram'ın Java uygulaması.

## Referanslar

* [Radiance HDR](http://paulbourke.net/dataformats/pic/)
* [görüntü bilgisi](https://github.com/xiaozhuai/imageinfo)

