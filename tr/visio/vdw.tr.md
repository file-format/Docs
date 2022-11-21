{
  "date" : "2019-10-11",
  "keywords" :[ "vdw","vdw dosyası", "vdw dosya biçimi", "vdw dosya türü", "dosya", "tür", "vdw dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - Visio Grafik Hizmeti Dosya Biçimi",
  "description":"VDW dosya formatı ve VDW dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## VDW dosyası nedir?

VDW, bir Web çizimini işlemek için gereken akışları ve depoları belirten Visio Graphics Service dosya biçimidir. Bir web çizimi, bir vektör veya taramalı çizim olarak işlenebilen çizim sayfaları, şekiller, yazı tipleri, resimler, veri bağlantıları ve diyagram güncelleme bilgileri koleksiyonudur. VDW dosyaları Microsoft Visio'da da açılabilir, ancak öncelikle web'de kullanılmak üzere kaydedilir. Microsoft Visio, Visio dosyalarını [PNG](/tr/Image/PNG/), [BMP](/tr/Image/BMP/), [PDF](/tr/pdf/) ve diğerleri dahil olmak üzere bir dizi farklı dosya biçimine dönüştürme yeteneği sunar.

## **VDW** Dosya Biçimi

VDW dosya formatının teknik özellikleri [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) tarafından çevrimiçi olarak mevcuttur ve geliştiriciler tarafından oluşturmak için referans alınabilir. uygulamalar. Teknik belge, depoları ve akışları içeren bileşik bir dosyada yer alan verileri açıklar. Bir Web Çiziminin temsili, bir ZIP arşivi aracılığıyla VisioServerData adlı bir akış aracılığıyla mümkün olur. Arşivdeki bir ShapGraphic XML Bölümü, Web çiziminde görüntülenen ve Genişletilebilir Uygulama İşaretleme Dili (XAML) ile ifade edilen grafik öğelerini açıklar. ZIP arşivindeki XML parçalarından oluşan bir koleksiyon, Web çiziminin veri bağlantısını, şekli hakkında bilgileri ve diyagram güncelleme mantığını açıklar. Bu parçalar XML olarak ifade edilir. DataGraphic XML bölümü, Web çizimindeki veriler veri kaynağından yenilendikten sonra değerlendirilecek yeniden hesaplanmış özellikleri açıklar. ZIP arşivindeki ek öğeler, Web çiziminde kullanılan yazı tipleri ve resimler için bilgi içerir.

|![Bir Dosyanın Olası Uygulanması](/tr/web/vdw.png "Bir Dosyanın Olası Uygulanması")

## Referanslar

* [[MS-VGSFF]: Visio Grafik Hizmeti (.vdw) Dosya Biçimi](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

