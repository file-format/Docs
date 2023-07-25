{
  "date" : "2019-10-11",
  "keywords" :[ "gml dosyası", "gml dosyası nedir", "dosya", "gml örneği", "gml dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML - Coğrafya İşaretleme Dili Dosya Biçimi",
  "description":"GML dosya formatı ve GML dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## GML dosyası nedir?

GML, Open Geospatial Consortium (OGC) tarafından geliştirilen XML spesifikasyonlarına dayanan Coğrafya İşaretleme Dili anlamına gelir. Format, farklı dosya formatları arasında değiş tokuş için coğrafi veri özelliklerini depolamak için kullanılır. Coğrafi sistemler için bir modelleme dili ve internetteki coğrafi işlemler için açık bir değiş tokuş formatı olarak hizmet eder.

## GML Dosya Biçimi ##

Çoğu XML tabanlı gramerde olduğu gibi, dilbilgisinin iki bölümü vardır - belgeyi tanımlayan şema ve gerçek verileri içeren örnek belge. Bir GML belgesi, bir GML Şeması kullanılarak tanımlanır. Bu, kullanıcıların ve geliştiricilerin noktalar, çizgiler ve çokgenler içeren genel coğrafi veri kümelerini tanımlamasına olanak tanır. Kullanıcılar, uygulama şemalarını kullanarak noktalar, çizgiler ve çokgenler yerine yollara, otoyollara ve köprülere başvurabilir.

GML'nin mekansal verilerin haritalarda temsili için yorumlanmaması gerektiğini belirtmekte fayda var. GML içeriğinin temsili, GML'nin oluşturulma amacından farklıdır. Kısacası, GML, yalnızca görüntüleme amacıyla haritalama uygulamaları tarafından kullanılabilen uzamsal içerikleri tutmak için kullanıldığı için XML'e benzer.

### GML'de İçerik Oluşturma ###

GML, özelliklerin ve geometrilerin bir listesi olan özellikleri kullanarak uzamsal verileri temsil eder. Bir Mülkün bir adı, tipi ve değer açıklaması vardır. Geometriler, aşağıdakiler gibi temel geometri yapı taşlarından oluşur:

* puan
* çizgiler
* eğriler
* alt çerçeveler ve
* çokgenler

GML'nin gelecekteki sürümleri, özellikler arasındaki topolojik ilişkilerin yanı sıra 3B geometriyi de destekleyecek şekilde planlanmıştır.

GML kodlaması zaten oldukça karmaşık özelliklere izin veriyor. Bir özellik, örneğin diğer özelliklerden oluşabilir. Dolayısıyla, bir havaalanı gibi tek bir özellik, taksi yolları, pistler, hangarlar ve hava terminalleri gibi diğer özelliklerden oluşabilir. Bir coğrafi özelliğin geometrisi, birçok geometri öğesinden de oluşabilir. Geometrik olarak karmaşık bir özellik bu nedenle noktalar, çizgi dizileri ve çokgenler dahil olmak üzere geometri türlerinin bir karışımından oluşabilir.

### Örnekler ###

GML 1.0 ve 2.0, Poligonları, Noktaları ve LineString nesnelerini şu şekilde kodlar:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## Referanslar ##

* [GML Spesifikasyonları](https://www.ogc.org/standard/gml/)
* [GML - Wikipedia Tarafından](https://en.wikipedia.org/wiki/Geography_Markup_Language)

