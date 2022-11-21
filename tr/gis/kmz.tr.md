{
  "date" : "2019-10-11",
  "keywords" :[ "kmz dosyası", "kmz dosyası nedir", "dosya", "kmz örneği", "kmz dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - KML Sıkıştırılmış Dosya Biçimi",
  "description":"KMZ dosya formatı ve KMZ dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## KMZ dosyası nedir?

KMZ (KML Sıkıştırılmış) dosyası, Google Earth gibi GIS uygulamalarında görüntülenebilen jeo-uzamsal bilgileri içeren sıkıştırılmış [KML](/tr/gis/kml/) dosyasının bir temsilidir. Yer işaretleriyle ilgili bilgiler, dosyada özel bir adla birlikte enlem ve boylam olarak gösterilir. Tek bir paket halindeki KMZ dosyası, diğer kullanıcılarla kolaylıkla paylaşılabilir. KMZ dosyaları, modelin coğrafi temsili için 3B model verilerini de içerebilir. Bir KMZ dosyası, dosyayı çevrimiçi bir konuma kaydedip ardından URL'yi Google Haritalar Arama kutusuna yazarak Google Haritalar'da açılabilir.

## Dosya Yapısı ##

Bir MKZ dosyasının içeriği, bir ana KML dosyasından ve sıfır veya daha fazla ilişkili dosyadan oluşur. WinZIP gibi standart açma programı kullanılarak çıkarılabilir. KMZ dosya formatı da 10:1 sıkıştırma oranıyla bir arşive sıkıştırılmıştır. Verileri Google Earth benzeri uygulamalardan doğrudan KMZ dosya biçimine aktarabilirsiniz. Ana KML dosyasının adı **doc.kml**'dir. Bir KMZ dosyasını paketlerken içine birden fazla KML dosyası eklenebilir ancak Google Earth KMZ dosyasını açarken ilk KML dosyasını arayıp okuduğu için bunun bir faydası olmayacaktır. Arşivde bulunan diğer KML dosyalarını yok sayar. İstenilen KML dosyasının Google Earth tarafından okunduğundan emin olmak için KMZ dosyası içerisine yalnızca tek bir KML dosyasının yerleştirilmesi önerilir.

doc.kml dosyasında atıfta bulunulan görüntüler, modeller, dokular, ses dosyaları ve diğer kaynaklar, ana klasör içindeki başka bir alt klasöre yerleştirilir. Bu, destekleyici dosyaların sayısına bağlı olarak bazı karmaşıklıkları da içerebilir. Bu kurucu kaynaklara bağlantılar, göreceli olarak veya mutlak referans yoluyla referans olabilir.

### Göreli Başvuru ###

Kaynaklar, ana klasör içindeki bir alt klasörde ana doc.kml'nin yanına yerleştirildiğinde, aşağıdaki örnekte gösterildiği gibi (yalnızca simge için) ilgili referans bu destekleyici dosyalara işaret edebilir.

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Mutlak Referans ###

Kaynaklara mutlak olarak da başvurulabilir. Mutlak referanslar, bağlantılı dosya için tam URL'yi içerir. Dosyalar merkezi bir sunucuya gönderildiğinde, mutlak referanslama, bunların göreceli referanslamaya kıyasla net kalmasını sağlar. Dosyalar yeni bir sisteme taşındığında bu linkler bozulacağı için yerel dosyalara kesinlikle başvurulması önerilmez. Mutlak başvuruya bir örnek aşağıdaki gibidir:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Ayrıca bakınız ##

* [GeoJSON](/tr/gis/geojson/)

## Referanslar ##

* [Google Earth ve KMZ Dosyaları](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

