{
  "date" : "2019-10-11",
  "keywords" :[ "qgs dosyası", "qgs dosya biçimi", "qgs dosyası nedir", "dosya", "qgs örneği", "qgs dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - QGIS Proje Dosyası Formatı",
  "description":"QGS dosya formatı ve QGS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## QGS dosyası nedir?

.qgs uzantılı bir dosya, açık kaynaklı bir çapraz platform CBS uygulaması olan [QGIS](https://www.qgis.org/en/site/) ile oluşturulan bir proje dosyasıdır. Proje için katman özellikleri ve yardımcı veriler gibi tüm proje ayarları. Bir harita projesi diske kaydedildiğinde oluşturulur. Aslında GIS verilerine işaretçiler, katmanlar hakkında stil bilgileri ve proje başlığı gibi bilgileri tutan bir yapılandırma dosyasıdır. QGS dosyaları, ücretsiz olarak indirilebilen QGIS yazılımıyla açılabilir.

## QGS Dosya Biçimi

QGS dosyaları [XML](/tr/web/xml/) biçimindedir ve proje verilerini XML etiketleri olarak depolar. Bir QGS dosyası aşağıdakiler gibi bilgiler içerir:

* Proje Başlığı
* CRS projesi
* katman ağacı
*yakalama ayarları
* ilişkiler
* harita tuvali kapsamı
* proje modelleri
* efsane
* mapview yuvaları (2D ve 3D)
* Temel veri kümelerine (veri kaynakları) ve kapsam, SRS, birleştirmeler, stiller, oluşturucu, karışım modu, opaklık ve daha fazlası dahil olmak üzere diğer katman özelliklerine bağlantıları olan katmanlar.
* proje özellikleri

### QGS Üst Düzey XML Etiketleri

{{< figure src="../qgstoplevel.png" title="" >}}

### Genişletilmiş Üst Düzey Proje Katmanı Etiketleri

{{< figure src="../qgstoplevel.png" title="" >}}

## Referanslar

* [QGIS](https://www.qgis.org/en/site/)

