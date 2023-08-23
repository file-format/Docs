{
  "date" : "2019-10-11",
  "keywords" :[ "odg dosyası", "odg dosya biçimi", "odg dosyası nedir", "dosya", "odg örneği", "odg dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODG Dosya Biçimi",
  "description":"ODG dosya formatı ve ODG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ODG dosyası nedir?

ODG dosya biçimi, çizim öğelerini bir vektör görüntüsü olarak depolamak için Apache OpenOffice'in Draw uygulaması tarafından kullanılır. Advancement of Structural Information Standards (OASIS) tarafından özetlenen XML tabanlı dosya biçimi belirtimlerini takip eder. ODG, noktaları, çizgileri ve eğrileri kullanarak çizimleri vektör görüntüleri olarak temsil eder. OpenOffice'in yanı sıra LibreOffice ve diğer uygulamalar da ODG dosya biçimiyle çalışmayı destekler. Örneğin, OpenOffice tarafından desteklenen diğer biçimler arasında [ODT](/tr/word-processing/odt/), ODF, [ODP](/tr/presentation/odp/) ve [ODS](/tr/spreadsheet/ods/) yer alır.


## ODG Dosya Biçimi Özellikleri

ODG dosya formatı, iyi tanımlanmış şema ile yapılandırılmış XML belge formatı olan OpenDocument formatına dayanmaktadır.
Bir OpenDocument biçiminin her yapısal bileşeni, ilişkilendirilmiş niteliklere sahip bir öğe tarafından temsil edilir. XML tabanlı yapı, metin belgesi, elektronik tablo veya çizim dosyası gibi tüm belge türleri için ortaktır. Bir belge farklı stiller içerebilir. Bir OpenDocument dosya yapısı aşağıdaki öğelerden oluşur.
* Doküman kaynağı
* Belge Meta Verileri
* Gövde Öğesi ve Belge türleri
* Uygulama ayarları
* Kodlar
* Yazı Yüzü Bildirimleri
* Stiller
* Sayfa Stilleri ve Düzenleri

## Belge Kökleri ##

Bir belge kök öğesi tüm belgeyi içerir ve OpenDocument biçimindeki bir dosyanın birincil öğesidir. Aynı türdeki belge kök öğeleri, metin, belgeler, elektronik tablolar ve çizim belgeleri gibi tüm belge türleri için geçerlidir.

### Kök Öğeler ###
Tek bir XML belgesi, kendi kök öğesi tarafından temsil edilir. Desteklenen beş farklı kök öğe aşağıdaki gibidir.

`<office:document>` - Office belgesini tek bir XML belgesinde tamamlayın.
`<office:document-content>` - Belge içeriği ve içerikte kullanılan otomatik stiller.
`<office:document-styles>` - Belge içeriğinde kullanılan stiller ve stillerin kendisinde kullanılan otomatik stiller.
`<office:document-meta>` - Yazar veya son kaydetme eyleminin zamanı gibi belge meta bilgileri.
`<office:document-settings>` - Pencere boyutu veya yazıcı bilgileri gibi uygulamaya özel ayarlar.

### ODG Belgesi Meta Verileri ###
OpenDocument, içindeki tüm meta veri öğelerini içerir. \<office:meta> eleman. Bir belge hakkındaki bu genel bilgiler, belgenin başında yer alır ve uygulamalar, aynı öğelerin birden çok örneğini güncelleyebilir.

### Gövde Öğesi ve Belge Türleri ###
Belge gövdesi, belge tipi öğesini kullanarak belgede bulunan içeriğin türünü gösterir. Bu belge türleri şunlardır:
* metin belgeleri
* çizim belgeleri
* sunum belgeleri
* elektronik tablo belgeleri
* grafik belgeleri
* görüntü belgeleri

### Uygulama ayarları ###
Ofis uygulamalarının ayarları, belge yapılandırması veya belgenin görsel görünümü ile ilgili farklı ayarları temsil eder. Her kategori bir ile temsil edilir. `<config:config-item-set>`. Bu tür ayar kategorilerinin örnekleri şunları içerir:
* Belge ayarları, örneğin varsayılan yazıcı
* Görünüm Ayarları, örneğin yakınlaştırma seviyesi

### Kodlar ###
Bir belgenin birkaç komut dosyası içermesi yaygın bir durumdur. Bir OpenDocument dosyasındaki her betik, bir ile temsil edilir. `<office:script>` öğesi. Bu komut dosyası öğeleri, tek bir içinde bulunur. `<office:scripts>` öğesi. Belge yüklenirken komut dosyaları belgeyi güncellemez.
### Font Yüzü Bildirimleri ###

Yazı tipi yüzü bildirimi, bir belgenin yazarı tarafından kullanılan yazı tipleri hakkında bilgi içerir. Bu bilgi, bu yazı tiplerini diğer sistemlerde bulmanıza yardımcı olur.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Stiller ###
Aşağıdaki stiller OpenDocument biçimi tarafından desteklenir.

"Ortak Stiller" - Bu tür stillerin XML gösterimlerine stiller denir.
"Otomatik Stiller" - Bir belgenin kullanıcı arabirimi görünümünde paragraf gibi bir nesneye atanan biçimlendirme özelliklerini içerir.
"Ana Stiller" - stil uygulandığında belge içeriğiyle birlikte görüntülenen biçimlendirme bilgilerini ve ek içeriği içeren ortak bir stil. Ana stile bir örnek, ana sayfalardır.

## Referanslar ##
* [Office Uygulamaları için OASIS Açık Belge Formatı](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument Biçimi - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

