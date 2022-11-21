{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "QGIS Projesinin Sqlite Veritabanı", "uzantı", "format", "QGIS", "Yardımcı Veritabanı", "QGD dosyası nedir"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - QGIS Projesinin Sqlite Veritabanı",
  "description":"QGIS projesinin bir sqlite veritabanı olan QGD ve QGD dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## .qgd dosyası nedir?

.QGD dosya uzantılı dosya aslında **QGIS** projesinin proje için yardımcı verileri barındıran ilişkili sqlite veritabanıdır. Proje için herhangi bir yardımcı veri olmayacaksa, QGD dosyası boş kalacaktır.

## QGD Dosya Biçimi ile ilgili ayrıntılar

Klasik modda, yardımcı veritabanı xml dosyası boyunca .qgd uzantılı bir dosya olarak kaydedilir. **Yardımcı Veritabanı** sistemi, alternatif bir yol olarak sistemdeki verilerin okunmasına ve yazılmasına olanak tanır. Sıkıştırılmış bir kapsayıcı olan QGZ'yi oluştururken, .qgd dosyası .qgz dosyasına dahil edilir.

## Yardımcı Veritabanı Nedir?
Yardımcı Veritabanı, aslında hedef veritabanının çoğaltılmasına yanıt olarak oluşturulan bir bekleme db sistemidir. Yardımcı veritabanı aslında yinelenen bir veritabanı durumudur, kopyaladığınız veritabanı olacaktır. Örneğin, yinelenen veritabanını kullanarak yedek bir veritabanı kurarsanız, kaynak veritabanı hedef olacak ve yedek veritabanı yardımcı olarak bilinecektir.


## Referanslar

* [QGZ – QGIS için yeni bir varsayılan proje dosyası formatı](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS Dosya Biçimleri](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

