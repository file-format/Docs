{
  "date" : "2021-07-28",
  "keywords" :[ "ntf dosyası", "ntf dosya biçimi", "ntf dosyası nedir", "dosya", "ntf örneği", "ntf dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - Ulusal Aktarım Formatı Dosyaları",
  "description":"NTF dosya formatı ve NTF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## Bir NTF dosyası nedir?
.ntf uzantılı dosyalara **Ulusal Aktarım Formatı (NTF)** Dosyaları denir; çoğunlukla UK Ordnance Survey (OS) tarafından kullanılır; özellikle jeo-uzamsal verilerin aktarımı için. İngiliz Standartları Enstitüsü tarafından yönetilmektedir. Ordnance Survey dijital verileri için standart aktarım formatı haline geldi. Bir tür Enine Mercator olan İngiltere'nin Ulusal Izgara projeksiyonu, NTF dosyaları için tüm coğrafi referanslı bilgileri tutar.

## NTF dosya biçimi
NTF dosya formatı Birleşik Krallık'ta Ordnance Survey'e aittir; içe aktarma için GDB kitaplığı tarafından desteklenir. NTF dosya biçiminin Mevcut sürümü 2.0'dır. Bu dosya formatı, yapı başına yalnızca bir öznitelik alanına sahip olan **PCIDSK** vektör segmentinin sınırlamasını ele almak için sunulmuştur, ancak vektör verileriyle çıkarılabilecek çeşitli öznitelikler vardır. NTF dosya formatı dolaşmak için iki parçaya sahip olacak şekilde oluşturulmuştur. Her segment aynı vektörlerden oluşur, ancak farklı niteliklere sahiptir. Bir NTF vektör dosyasının ilk Segmenti, öznitelik olarak özellik kod numarasına sahip vektörleri içerir. İkinci segment, öznitelik olarak değere sahip vektörleri içerir.

### Koordinat referans sistemi
GDB kitaplığı, uygun TM projeksiyon özelliklerine sahip raster ve vektör verilerini temsil eder:

- Referans Boylam: 49.0
- Referans Enlem: 2.0
- Yanlış Doğu: 400000
- Yanlış Kuzeyleme: -100000
- Ölçek: 0,9996012717
- Elipsoid: Havadar 1830 (E009)
NTF dosyalarının güncellenmesi veya yazılması için herhangi bir destek mevcut değildir ve DTM dosyalarına bağlanılamaz.

### Ogrinfo örneği
Aşağıdaki örnek, katman numaralarını almak için bir NTF dosyasında **ogrinfo** kullanır:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Referanslar

* [Birleşik Krallık Ulusal Aktarım Formatı (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Web Haritalama - Tyler Mitchell tarafından çizilmiştir](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

