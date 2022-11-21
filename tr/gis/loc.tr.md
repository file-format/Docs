{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "dosya", "uzantı", "dosya formatı", "GPS Konumu", "Ara Nokta"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - GPS Konum Dosya Biçimi",
  "description":"LOC dosya formatı ve LOC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## LOC dosyası nedir?

.loc uzantılı bir dosya, jeo-uzamsal konumları ara noktalar olarak içeren bir GPS konum dosyasıdır. Yol noktası, Coğrafi Bilgi Sistemi (GIS) uygulamaları tarafından kullanılan bir konumu ifade eden bir Enlem-Boylam değeri çiftidir. DeLorme Topo gibi GPS haritalama programları, son kullanıcılar tarafından seçilebilir katmanlar olarak bu LOC dosyalarında bulunan bilgileri okumak ve görüntülemek için LOC dosyalarını kullanır. Ek olarak, bunlar uygulamalar arasında GPS verisi alışverişi için kullanılır. LOC dosyaları, bu tür dosyaların içeriklerini ilgili coğrafi konumdaki haritada çizilen katmanlar ve veriler olarak görüntüleyen [TopoGrafix EasyGPS](https://www.easygps.com/) gibi uygulamalar kullanılarak açılabilir.

## LOC Dosya Biçimi - Daha Fazla Bilgi

LOC dosyalarının [GPX](/tr/gis/gpx/) dosyalarıyla benzerlikleri vardır ancak farklı biçimde kaydedilirler. Bunlar [XML](/tr/web/xml/) dosyaları olarak kaydedilir ve burada yol noktalarının içeriği ve ilişkili bilgiler yapılandırılmış etiketlerde bulunur. XML, farklı uygulamalar arasında veri alışverişi için genelleştirilmiş bir dil olduğundan, bu, LOC verilerinin diğer uygulamalarla alışverişini kolaylaştırır.

## LOC Dosya Biçimi - Örnek

Aşağıda, bir LOC dosyasından bir yol noktasının başlığı ve metni yer almaktadır. Görüldüğü gibi başlık bilgisi verinin konum kaynağını içermektedir. Yol noktası, "kimlik" gibi bilgileri ve yol noktasıyla ilişkili ilişkili içerik verilerini içerir. Son olarak, ara nokta, enlem ve boylam değerlerinin ve bu belirli yol noktasıyla ilişkili metnin bir koleksiyonudur.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Referanslar

* [TopGraphic EasyGPS](https://www.easygps.com/)

