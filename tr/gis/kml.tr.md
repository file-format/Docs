{
  "date" : "2019-10-11",
  "keywords" :[ "kml dosyası", "kml dosyası nedir", "dosya", "kml örneği", "kml dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Anahtar Deliği İşaretleme Dili",
  "description":"KML dosya formatı ve KML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## KML dosyası nedir?

KML, Keyhole İşaretleme Dili), XML gösteriminde jeo-uzamsal bilgileri içerir. KML olarak kaydedilen dosyalar, desteklemeleri koşuluyla Coğrafi Bilgi Sistemi (GIS) uygulamalarında açılabilir. Uluslararası standart olarak kabul edildikten sonra birçok uygulama KML dosya formatı için destek sağlamaya başlamıştır. KML, iç içe öğeler ve nitelikler içeren etiket tabanlı bir yapı kullanır. Tüm etiketler büyük/küçük harfe duyarlıdır ve [KML](https://developers.google.com/kml/documentation/kmlreference) Referansına göre bu etiketlerin sırasına uyulması önemlidir.

## Kısa Tarih ##

KML, orijinal olarak Keyhole Earth Viewer olarak bilinen Google Earth ile kullanılmak üzere geliştirilmiştir. KLM, 2008 yılında Open Geospatial Consortium tarafından 2008 yılında uluslararası standart olarak benimsenmiştir. Format, Google Earth ile kullanılmak üzere geliştirildiğinden, KML dosyalarını ilk görüntüleyen ve düzenleyen olma özelliğini taşımaktadır. Zaman geçtikçe, farklı dillerde çeşitli API'ler dahil olmak üzere KML dosya formatlarını destekleyen daha fazla proje var.

## KML Dosya Biçimi Özellikleri ##

KML Referansı, tam dosya formatı özelliklerine sahip olmak için başvurmak için eksiksiz bir kılavuzdur. Standart bir KML dosyası şunlardan oluşur:

* Yer işaretleri
* Açıklayıcı HTML Yer İşaretlerinde
* Zemin Bindirmeleri
* Yollar
* çokgenler

Bunlara ek olarak, KML dosyasının gelişmiş bir sürümü şunları içerebilir:

* Geometri Stilleri
* Vurgulanan Simgeler için Stiller
* Ekran Bindirmeleri
* Ağ Bağlantıları

KML öğesinin her biri, dosyada bulunan bilgileri coğrafi olarak konumlandıran uzunlamasına bilgilere sahiptir. Ancak yön, yükseklik ve eğim gibi ek parametreler de olabilir.

### Yer İşaretleri ###

Dünya yüzeyindeki bir konumu temsil etmek için kullanılır ve şu şekilde tanımlanır:<Point> eleman. Aşağıda, bir yer işaretinin KML dosyasında nasıl temsil edildiğine dair bir örnek verilmiştir.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### Yer İşaretlerinde Açıklayıcı HTML ###

Ek bilgiler, yer işaretinin gösterimini daha da geliştiren bir yer işaretiyle ilişkilendirilebilir. Bu tür bilgiler bağlantıları, yazı tipi boyutlarını, stilleri ve renkleri içerir. Ayrıca, yer işaretinin parçası olacak metin hizalama ve tablolar da içerir.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### Yer Paylaşımları ###

Bunlar, bir görüntünün Dünya yüzeyine katmanlanmasını temsil eder. bu<icon> element, bindirme görüntü dosyasına giden bağlantıyı içerir.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### Yollar ###

Yollar şu şekilde temsil edilir:<LineString> lat-long çiftlerinin bir koleksiyonu olan öğe. Bunları kullanarak, Google Earth'te birçok farklı türde yol oluşturulabilir.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## KML Dosyasında Mekansal Referanslama ##

Geo-Locations hakkında herhangi bir Geospatial dosyasında yer alan bilgiler, mekansal referans bilgisi olmadan farklı anlamlara sahip olabilir. Varsayılan olarak, KML dosyasının uzamsal referansı, 1984 Dünya Jeodezik Sistemi, WGS84 tarafından tanımlanır.

## Referanslar ##

* [KML Referansı](https://developers.google.com/kml/documentation/kmlreference)
* [KML için Google Geliştirici Eğitimi](https://developers.google.com/kml/documentation/kml_tut)
* [KML Dosya Biçimi](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

