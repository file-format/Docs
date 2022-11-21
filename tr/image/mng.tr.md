{
  "date" : "2019-10-11",
  "keywords" :[ "mng dosyası", "mng dosya biçimi", "mng dosyası nedir", "dosya", "mng örneği", "mng dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MNG Dosya Formatı - Çoklu Görüntü Ağı Grafik Dosya Formatı",
  "description":"MNG dosya formatı ve MNG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .mng dosyası nedir?

.mng uzantılı bir dosya, [PNG](/tr/image/png/) resim formatına benzeyen ancak animasyonlu resimleri destekleyen bir Çoklu Resim Ağ Grafikleri dosya formatıdır. Ek animasyon özellikleriyle PNG biçimini aşırı yüklemekten kaçınmak için geliştirilmiştir. MNG ayrıca [GIF](/tr/image/gif/) dosyalarına benzer, ancak daha fazla sıkıştırma kullanır ve tam alfa özelliğini destekler. MNG dosyaları için resmi olmayan MIME ortam türü video/x-mng'dir. MNG dosyaları ImageMagik ve IrfanView gibi uygulamalarda açılabilir.

## MNG Dosya Biçimi

MNG dosya formatı PNG'ye benzer ve PNG spesifikasyonlarında tanımlandığı gibi aynı yığın yapısını kullanır. Bir MNG kod çözücü, kod çözme talimatları için herhangi bir özel bayrak belirtmeden PNG veri akışlarının kodunu çözebilmelidir. MNG, birden çok görüntüyü bir "çerçevede" gruplandırır ve bazı görüntüler bir konumdan diğerine hareket etmek için hareketli grafik olarak kullanılır. Mekanizma, görüntü verilerinin yeniden iletilmeden yeniden kullanılmasına izin verir. [MNG belirtimlerine](http://www.libpng.org/pub/mng/spec/) geliştiricinin referansı için başvurulabilir.

### MNG İmzası

MNG veri akışı, aşağıdakileri içeren 8 baytlık bir imzayla başlar:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Bu, PNG imzasına benzer ancak PNG yerine MNG içerir.

### MNG Çerçevesi

Bir MNG çerçevesi, daha küçük görüntülerin iki boyutlu görüntüsünden oluşur. Her bir küçük resme, satır ve sütun indeks kombinasyonu kullanılarak erişilebilir. Biçim, bir dizi iki boyutlu düzlemden oluşan üç boyutlu "voksel" verilerini saklama yeteneğine sahiptir. Her düzlem bir PNG veya Delta-PNG veri akışı ile temsil edilir. Her Delta-PNG veri akışı, bir görüntüyü üst PNG görüntüsünden farklılıklar olarak tanımlar. Bu, her biri için eksiksiz bir PNG veri akışı kullanmaktansa sonraki görüntüleri temsil etmenin çok daha kompakt bir yolunu sağlar.

## Referanslar ##

* [MNG](http://www.libpng.org/pub/mng/)
* [MNG Biçimi v 1.0](http://www.libpng.org/pub/mng/spec/)

