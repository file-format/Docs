{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - ESRI ArcInfo Binary Grid Formatı",
  "description":"ADF dosya formatı ve ADF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## ADF dosyası nedir?

.adf uzantılı bir dosya, ArcGIS, ArcView ve ArcInfo gibi ESRI yazılım uygulamaları tarafından kullanılan bir raster veri dosyası biçimidir. Uzamsal veriler, ESRI'ye özgü bir ikili ızgara olarak depolanır. Izgara, tamsayı ve kayan nokta olabilen hücrelerin satırlarından ve sütunlarından oluşur. Bir ADF dosyasındaki tamsayı ızgaraları ayrık verileri ve kayan noktalı ızgaralar sürekli verileri temsil eder. Diğer bir popüler ESRI dosya biçimi, Coğrafi Bilgi Sistemleri (GIS) uygulamaları tarafından kullanılacak vektör verileri biçiminde Jeo-uzamsal bilgileri temsil eden [SHP](/tr/gis/shp/) dosyasıdır.

## ADF Dosya Biçimi - Daha Fazla Bilgi

ADF dosyaları ikili ızgarada diske ikili dosyalar olarak kaydedilir. Tamsayı ızgaraları, bir değer öznitelik tablosunda (KDV) saklanan özniteliklere sahiptir. Kılavuzdaki her benzersiz değerin, kaydın benzersiz değeri sakladığı ve kılavuzdaki hücre sayısının bu değerle temsil edildiği KDV'de bir kaydı vardır.

Kayan nokta ızgaralarında KDV yoktur.

### Izgara Yapısı

ADF dosyasının içinde ızgaralar, döşenmiş bir raster veri yapısı kullanılarak uygulanır. Bu raster veri yapısının içindeki temel birim, dikdörtgen bir hücre bloğudur. Her blok diskte depolanır ve döşeme adı verilen değişken uzunlukta bir dosya yapısında sıkıştırılır. Her blok, bir değişken uzunluklu kayıt olarak saklanır.

GRID rasterleri, bir çalışma alanının bir bilgi alt dizini ve her GRID için bir alt dizin içerdiği çalışma alanlarında depolanır. Karşılık gelen ızgara için coğrafi konumu ve öznitelik verilerini içeren birkaç dosya vardır. Bilgi alt dizini, çalışma alanında GRID ve kapsamlar gibi diğer veri kümeleri hakkında belirli bilgileri tutan birkaç dosya içerir.

## Referanslar ##

* [ESRI Izgara Formatı](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)
