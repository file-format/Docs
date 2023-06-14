{
  "date" : "2020-01-10",
  "keywords" :[ "otg dosyası", "otg dosya biçimi", "otg dosyası nedir", "dosya", "otg örneği", "otg dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - OpenDocument Çizim Şablonu Dosya Biçimi",
  "description":"OTG dosya formatı ve OTG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## OTG dosyası nedir?

Bir OTG dosyası, OASIS Office Uygulamalarını [1.0 spesifikasyonu](http://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0) izleyen OpenDocument standardı kullanılarak oluşturulan bir çizim şablonudur. -os.pdf). Dosyanın içeriğini daha da geliştirmek için kullanılabilecek bir vektör görüntüsü için çizim öğelerinin varsayılan organizasyonunu temsil eder. OTF dosyaları, belgenin içeriğini temsil etmek için XML biçimini temel alan diğer OpenDocument biçimi tabanlı dosyalar gibidir. OTF dosyaları, herhangi bir metin veya standart XML düzenleyicide açılarak görüntülenebilir.

## OTG Dosya Biçimi Özellikleri ##

OTG dosya formatı, köklü bir şemaya sahip OpenDocument XML formatına dayanmaktadır. Bir OpenDocument biçiminin her bir bileşeninin yapısı, ilişkili öznitelikleri olan ve metin belgesi, elektronik tablo veya çizim dosyası gibi tüm belge türleri için ortak olan bir öğeyle temsil edilir. Bir çizim şablonu olan OTG, aşağıdakileri içeren Grafik İçeriği özelliklerini kapsamlı bir şekilde kullanır:

* Grafik Uygulamalar için Gelişmiş Sayfa Özellikleri
* Çizim Şekilleri
* Çerçeveler
* 3D Şekiller
* Özel şekil
* Sunum Şekilleri
* Sunum Animasyonları
* SMIL Sunum Animasyonları
* Sunum Etkinlikleri
* Mevcut Metin Alanları
* Sunum Dokümanı İçeriği

### Grafik Uygulamalar için Gelişmiş Sayfa Özellikleri ###
#### Asıl Not Defteri ####

Asıl Din Notu öğesi, bu tür sayfaların yazdırılmasını destekleyen uygulamalar için dinleyici notu sayfalarının otomatik olarak oluşturulmasına yönelik bir şablondur.
` ile ilişkili olabilecek öznitelikler<style:handout-master> ` öğesi:

|Düzen|Özellik|Açıklama
---|---|---|
|Sunum Sayfası Düzeni|sunum:sunum-sayfası-düzeninin-adı|` bağlantısı<style:presentation-page-layout> öznitelik
|Sayfa Düzeni|`stil:sayfa düzeni-adı` | Dinleyici ana sayfasının boyutlarını, kenarlığını ve yönünü içeren bir sayfa düzenini belirtir.
|Sayfa Stili|`draw:style-name`|Bir çizim sayfası stili atayarak dinleyici notu ana sayfasına ek biçimlendirme nitelikleri atar.|
|Başlık Bildirimi| `sunum:use-header-name`| Dinleyici notu ana sayfasında görüntülenen tüm başlık alanları için kullanılan başlık alanı bildiriminin adını belirtir.
|Altbilgi Bildirimi| Presentation:use-footer-name|Kullanıcı dinleyici notu ana sayfasında görüntülenen tüm alt bilgi alanları için kullanılan alt bilgi alanı bildiriminin adını belirtir.
|Tarih ve Saat Bildirimi|kullan-tarih-saat-adı|Dil ana sayfasında görüntülenen tüm tarih-saat alanları için kullanılan tarih-saat alanı bildiriminin adını belirtir.

### Çizim Şekilleri ###
OpenDocument formatı, herhangi bir belge türü tarafından kullanılabilen çeşitli çizim şekillerini destekler.

|Şekil|İlişkili Nitelikler| elementler
---|---|---|
Dikdörtgen - `draw:rect `|Konum, Boyut, Stil, Katman, Z-Dizini, Kimlik, Başlık Kimliği, Metin bağlantısı, tablo arka planı, çizim bitiş konumu, Yuvarlak köşeler|Başlık, Uzun Açıklama, Olay Dinleyiciler, Tutkal Noktaları, Metin
Satır `<draw:line> `|Stil, Katman, Z-Dizini, Kimlik, Başlık Kimliği ve Dönüşümü, Metin bağlantısı, tablo arka planı, çizim bitiş konumu, Başlangıç noktası, Bitiş Noktası|Başlık, Uzun Açıklama, Olay Dinleyiciler, Tutkal Noktaları, Metin
Çoklu çizgi `draw:polyline | Konum, Boyut, Görünüm kutusu, Stil, Katman, Z-Dizini, Kimlik, Başlık Kimliği ve Dönüşümü, Metin bağlantısı, tablo arka planı, çizim bitiş konumu, Noktalar| Başlık, Uzun Açıklama, Olay Dinleyiciler, Tutkal Noktaları, Metin
çokgen `draw:polygon `|Konum, Boyut, Görünüm kutusu, Stil, Katman, Z-Dizini, Kimlik, Başlık Kimliği ve Dönüşümü, Metin bağlantısı, tablo arka planı, çizim bitiş konumu, Noktalar|Başlık, Uzun Açıklama, Olay Dinleyiciler, Tutkal Noktaları, Metin
|Normal Çokgen `<draw:regular-polygon> `|Konum, Boyut, Stil, Katman, Z-Dizini, Kimlik, Başlık Kimliği ve Dönüşümü, Metin bağlantısı, tablo arka planı, çizim bitiş konumu, İçbükey, Köşeler, Keskinlik|Başlık, Uzun Açıklama, Olay Dinleyiciler, Tutkal Noktaları, Metin
|Paht `<draw:path> `|Konum, Boyut, Görünüm kutusu, Stil, Katman, Z-Dizini, Kimlik, Başlık Kimliği ve Dönüşümü, Metin bağlantısı, tablo arka planı, çizim bitiş konumu, Yol verileri| Başlık, Uzun Açıklama, Olay Dinleyiciler, Tutkal Noktaları, Metin

### Çerçeveler ###
Bir teknik resim belgesindeki çerçeve, metin kutuları, resimler veya nesneler içeren dikdörtgen bir kaptır. Çerçeveler, konturlar, görüntü haritaları ve köprüler gibi ek özellikleri destekler. Bir çerçeve, bir nesnenin yanı sıra bir görüntü de içerebilir, böylece bir nesnenin birden çok yorumuna sahip olunmasına izin verilir. Uygulamalar, ilgili öğeyi en iyi desteğe dayalı olarak işler.

Çerçeveler şunları içerebilir:
* Metin kutuları
* OpenDocument biçiminde veya nesneye özgü bir ikili biçimde temsil edilen nesneler
* Görüntüler
* Uygulamalar
* Eklentiler
* Yüzer çerçeveler

Aşağıda gösterildiği gibi bir belgede bir çerçeve bulunur.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Referanslar ##
* [Office Uygulamaları için OASIS Açık Belge Formatı](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument Biçimi - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

