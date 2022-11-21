{
  "date" : "2021-03-18",
  "keywords" :[ "qgz dosyası", "qgz dosya biçimi", "qgz dosyası nedir", "dosya", "qgz örneği", "qgz dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Kuantum GIS Sıkıştırılmış Projesi",
  "description":"Yalnızca sıkıştırılmış bir QGS olan QGZ dosya formatı ve QGZ dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Bir QGZ dosyası nedir?

**QGZ** dosya biçimi, bir [QGS](https://docs.fileformat.com/gis/qgs/) dosyası ve bir QGD dosyası içeren sıkıştırılmış bir arşivdir. Oysa QGD dosyası, proje için yardımcı verilerden oluşan qgis projesinin sqlite veritabanıdır. Yardımcı veri yoksa, QGD dosyası boş kalacaktır.

## QGZ Dosya Biçimi ile ilgili ayrıntılar

QGZ, **QGIS 3 proje dosyası formatının** yeni bir çeşidi olarak tanıtıldı. Bu biçim, QGS xml dosyası için sıkıştırılmış bir kaptır. Kullanıcılar isteğe bağlı bir biçim olan QGD'yi seçerse, bu durumda kap, yardımcı depolama veritabanını depolamak için faydalıdır.

Klasik modda, yardımcı veritabanı xml dosyası boyunca .qgd uzantılı bir dosya olarak kaydedilir. Sıkıştırılmış kapsayıcıyı seçerken, .qgd dosyası .qgz'nin içine dahil edilir, Kullanıcıları herhangi bir sorun olmadan kolaylaştırır, kullanıcılar proje dosyalarını paylaşırken onu silemez veya kopyalamayı unutamaz!


## Referanslar

* [QGZ – QGIS için yeni bir varsayılan proje dosyası formatı](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS Dosya Biçimleri](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

